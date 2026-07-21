# Handover Instructions — Pears Challenge / Tech for Resilience Website

You don't need any technical knowledge to use this. Open **Claude Code** in this
project folder, paste the message at the bottom of this file, and Claude will do
the rest — it will ask you to do only the two things a human must do (approve a
Wix login in your browser, and confirm before publishing).

## Before you start — one prerequisite

**The Wix site itself must already be transferred to your Wix account** (this is
a separate step from this code handover — ask whoever built the site to do it via
their Wix dashboard: Site Settings → Transfer Site). If you're not sure this has
happened yet, ask Claude Code to check (see the message below) — it will tell you
if something's wrong rather than guessing.

## What to tell Claude Code

Copy and paste this into Claude Code, in this folder:

---

> I'm the new owner of this Wix site (not a developer). Please help me connect
> this project to my Wix account and confirm it's set up correctly. Steps:
>
> 1. Check that `wix.config.json` exists in this folder and read the `siteId` in it.
> 2. Run `npx @wix/cli@latest login` and tell me exactly what to do in the browser
>    (I'll need to log in with my own Wix account).
> 3. Once I've logged in, run `npx @wix/cli@latest whoami` and show me which
>    account is now connected — I need to confirm it's really me.
> 4. Check that the `siteId` in `wix.config.json` matches a site I actually own in
>    my Wix dashboard (I'll give you my dashboard URL or site name to compare).
> 5. Do NOT publish/release anything yet — just confirm the connection is correct
>    and tell me in plain language what you found.
>
> If anything looks wrong (I don't own the site yet, the login didn't work, the
> site ID doesn't match), stop and explain what's missing in simple terms — don't
> try to fix it by guessing.

---

## Later, whenever you want to publish a change

Once the connection above is confirmed working, and any time you've asked Claude
Code to make a change to the site's design or code (not the content — see below),
tell it:

> Please publish the current version of this site to my live Wix site. Show me
> the live link when it's done so I can check it.

## Everyday content changes — no code needed at all

Most changes you'll want (text, photos, FAQ questions, timeline, stats, footer
links, nav menu) do **not** need Claude Code or any of the above — they're edited
directly in your **Wix dashboard → CMS** and **Wix dashboard → Forms**, and go
live immediately, no "publish" step required. Only ask Claude Code to "publish"
when a *design or layout* change was made to the actual code.

## If something goes wrong

Tell Claude Code plainly what happened (e.g. "the login step failed" or "whoami
shows the wrong account") and ask it to explain what that means before trying
anything else. It's better to pause and ask than to guess.

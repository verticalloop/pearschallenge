# Handover Instructions — Pears Challenge / Tech for Resilience Website

Welcome — this website is now yours. This file is the only thing you need. It
walks you through everything, in order, from a completely empty computer to
being able to make changes to your site yourself, using **Claude Code** (an
AI coding assistant you'll install below) instead of writing code by hand.

You do not need any technical background. Just follow the sections in order,
top to bottom, and don't skip ahead. Each step tells you exactly what
"it worked" looks like before you move to the next one.

**What this project actually is:** this is the code for your website. It
talks to your Wix site (which holds your content, forms, and hosting) behind
the scenes. Most day-to-day changes don't need this file at all — see
[Everyday content changes](#everyday-content-changes--no-code-needed-at-all)
below. This file is for the less-common cases: changing the design/layout, or
the one-time setup to make this all yours.

**What you'll need before starting:**
- A Mac or Windows computer
- Your own **GitHub** account (the one you already use)
- Your **Wix** account (the one you already use)
- A **claude.ai** account (free to create if you don't have one)

---

## Section 1 — Get your computer ready (one-time)

Do this once. After this section, your computer is permanently set up and you
never need to repeat it.

### 1a. Install Node.js

Node.js is a program Claude Code needs in order to run.

1. Go to [nodejs.org](https://nodejs.org)
2. Click the button labeled **LTS** (it will say something like "20.x.x LTS")
3. Open the downloaded file and click "Next" through the installer, accepting
   the defaults, until it finishes.

**How you know it worked:** you'll do a check for this in step 1b, together
with Terminal.

### 1b. Open a Terminal window

A Terminal is just a plain window where you type commands instead of
clicking buttons. That's all it is — nothing to be afraid of.

- **On a Mac:** press `Cmd + Space`, type `Terminal`, press Enter.
- **On Windows:** click the Start menu, type `Command Prompt`, press Enter.

A plain window with text should open. Type this and press Enter:

```
node --version
```

**How you know it worked:** you see something like `v20.11.0` printed. If you
see an error like "command not found," go back to step 1a — Node.js didn't
install correctly.

### 1c. Install Claude Code

In the same Terminal window, type:

```
npm install -g @anthropic-ai/claude-code
```

Press Enter and wait for it to finish (this can take a minute).

**How you know it worked:** type `claude --version` and press Enter — you
should see a version number printed, not an error.

### 1d. Sign in to Claude Code

Still in the Terminal, type `claude` and press Enter. The first time you run
it, it will ask you to sign in — it opens your browser to claude.ai. Sign in
(or create a free account if you don't have one) and approve the connection.

**How you know it worked:** you're back in the Terminal and it shows a
Claude Code prompt instead of an error.

### 1e. Download your website's code onto your computer

Before this step, make sure you've completed **Section 2** below (accepting
the GitHub transfer) — you need the repository in your own account first.

In the Terminal, type this, replacing `YOUR-GITHUB-USERNAME` with your own
GitHub username:

```
git clone https://github.com/YOUR-GITHUB-USERNAME/pearschallenge.git
cd pearschallenge/tech-for-resilience
```

**How you know it worked:** the Terminal shows a "Cloning into..." message
and finishes without a red error. Typing `ls` (Mac) or `dir` (Windows)
afterward should show files like `index.html` and this `HANDOVER.md`.

---

## Section 2 — Accept the repository and site transfers

Do these in any order, but finish both before Section 3.

1. **GitHub email:** check your inbox for an email from GitHub about a
   "repository transfer" or "invitation" (sent to the GitHub account you
   gave Verticalloop) — click to accept it. This moves the `pearschallenge`
   code repository into your own GitHub account.
2. **Wix email:** check your inbox for an email from Wix about a "site
   transfer" — click to accept it. This makes the website officially yours
   inside your existing Wix account.

**How you know it worked:** you can log into github.com and see a repository
called `pearschallenge` under your own account, and you can log into your
Wix dashboard and see this site listed there.

---

## Section 3 — Connect your GitHub account to Claude Code

This is the one step that feels the most "technical" — but it's really just
one screen you click through, done once.

1. In the Terminal, inside the `pearschallenge/tech-for-resilience` folder
   (from step 1e), type `claude` and press Enter to start Claude Code.
2. The first time you ask Claude Code to do something involving GitHub (for
   example, pasting the message in Section 4 below), it will open your
   browser and ask you to **Connect GitHub** / **Authorize**.
3. This is a GitHub screen asking for permission to read and edit
   repositories on your behalf — this is expected and safe.
4. **Look carefully at the account name shown at the top of that screen.**
   It must be *your* GitHub account (the one the repository was transferred
   into in Section 2), not any other GitHub account you or someone else may
   have used on this browser before.
   Picking the wrong account here is the single most common mistake — if
   you're not sure, log out of GitHub in your browser first and log back in
   as yourself before clicking Authorize.
5. When asked which repositories to allow access to, choose "Only select
   repositories" and pick `pearschallenge` (or "All repositories" if you'd
   rather not think about this again in the future).
6. Click **Authorize**.

**How you know it worked:** back in the Terminal, Claude Code confirms it can
see your repository and continues with whatever you asked it to do. You only
do this once — every future Claude Code session in this folder just works.

---

## Section 4 — Confirm everything is connected correctly

With Claude Code running (Section 3), copy and paste this whole message:

---

> I'm the new owner of this Wix site and this GitHub repository (not a
> developer). Please help me confirm everything is set up correctly. Steps:
>
> 1. Check that `wix.config.json` exists in this folder and tell me the
>    `siteId` in it.
> 2. Check this folder's GitHub remote/origin and confirm it points to my own
>    GitHub account, not anyone else's.
> 3. Run `npx @wix/cli@latest login` and tell me exactly what to do in the
>    browser (I'll need to log in with my own Wix account).
> 4. Once I've logged in, run `npx @wix/cli@latest whoami` and show me which
>    account is now connected — I need to confirm it's really me.
> 5. Check that the `siteId` from step 1 matches a site I actually own in my
>    Wix dashboard (I'll give you my dashboard URL or site name to compare).
> 6. Tell me whether my custom domain shows as connected to this site in my
>    Wix dashboard.
> 7. Do NOT publish/release anything yet — just confirm everything above and
>    tell me in plain language what you found.
>
> If anything looks wrong (wrong GitHub account, I don't own the Wix site
> yet, the login didn't work, the site ID doesn't match, the domain isn't
> connected), stop and explain what's missing in simple terms — don't try to
> fix it by guessing.

---

Only move on once Claude Code confirms all of the above look correct.

---

## Everyday content changes — no code needed at all

Most changes you'll want — text, photos, FAQ questions, timeline, stats,
footer links, nav menu, form questions — do **not** need Claude Code or
anything in this file. Edit these directly in your **Wix dashboard → CMS**
and **Wix dashboard → Forms**. Changes there go live immediately, with no
"publish" step required.

Only come back to Claude Code when you need to change the actual **design or
layout** of the site.

---

## Section 5 — Making a design/code change

Anytime you want a design or layout change, start Claude Code in the
`pearschallenge/tech-for-resilience` folder (Terminal → `claude`) and
describe what you want in plain English, for example:

> Change the homepage headline to "Pears Challenge 2026" and update the
> date to March 14.

Claude Code will make the change and show you what it did. Once you're happy
with it, tell it:

> Please publish the current version of this site to my live Wix site. Show
> me the live link when it's done so I can check it.

---

## If something goes wrong

Tell Claude Code plainly what happened — for example:
- "The login step failed"
- "Whoami shows the wrong account"
- "GitHub access was denied"
- "My domain isn't showing as connected"
- "I think I authorized the wrong GitHub account in Section 3"

Ask it to explain what that means before trying anything else. It's always
better to pause and ask than to let it guess.

---

## A closing note

This is a one-time handover — from this point on, this project is fully
yours, and Verticalloop won't need to be involved in day-to-day changes. Keep
this file for future reference; if you ever forget how any of this works,
just come back and re-read it, or paste the relevant section into Claude
Code and ask it to walk you through it again.

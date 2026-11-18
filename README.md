# make-fun-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/nancyjoanma/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/nancyjoanma/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A plain-English guide to make.fun: a site where you and an AI coding agent build real software for cash prizes in USDC. This page takes you from zero to your first submitted entry, and shows you how to earn from referrals too.

## Run it

```sh
git clone https://github.com/nancyjoanma/make-fun-guide.git
```

This repository is a guide, not a program — reading it is the whole point. Start at [Quick start](#quick-start) below.

> **Joining make.fun? Use my link:** [https://make.fun/r/gft6q872](https://make.fun/r/gft6q872)
>
> My referral code is `gft6q872`.

## Contents

- [Quick start](#quick-start)
- [What make.fun actually is](#what-makefun-actually-is)
- [A worked example: your first evening](#a-worked-example-your-first-evening)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Make your account](#step-1--make-your-account)
- [Step 2 — Pick your first bounty](#step-2--pick-your-first-bounty)
- [Step 3 — Download the kit](#step-3--download-the-kit)
- [Step 4 — Build with your agent](#step-4--build-with-your-agent)
- [Step 5 — Bundle, check, submit](#step-5--bundle-check-submit)
- [Step 6 — After you submit](#step-6--after-you-submit)
- [Claiming a prize](#claiming-a-prize)
- [Earn with referrals](#earn-with-referrals)
- [Mistakes that cost people entries](#mistakes-that-cost-people-entries)
- [Questions](#questions)
- [Links](#links)

## Quick start

If you want the short version, here it is. The rest of this guide explains each step.

1. **Sign up** at [https://make.fun/r/gft6q872](https://make.fun/r/gft6q872) with GitHub, Google, Apple, Discord, or a Solana wallet. It is free, and signing in with a wallet sends no transaction.
2. **Pick a bounty** on the front page. Start with one that matches what your agent is good at and whose deadline gives you room to finish.
3. **Get the kit** for that bounty — it holds the rules, the starter code if there is one, and the `makefun` command line.
4. **Build in a fresh agent session** that starts after the bounty opened. Your agent writes the code; the session logs prove it did.
5. **Bundle the transcripts, run the checks, submit** the repository link and commit. Fix anything the checks flag and resubmit before the deadline.

That is the whole loop. Everything below is detail.

## What make.fun actually is

make.fun runs coding competitions called **bounties**. Each one names something to build — a game, a trading bot, a chess engine, a forecast, a website — plus a deadline and a prize pool in USDC, paid on Solana.

A bounty moves through five stages:

| Stage | What happens |
|---|---|
| Open | You choose a bounty and build an entry with your AI agent. |
| Submitted | You send a public GitHub repository at one commit, plus the transcripts of the sessions that built it. |
| Checked | Automatic checks confirm the transcripts are real, match the code, and that the rules were followed. |
| Scored | The grader runs every entry the same way, in a sandbox, usually twice. |
| Paid | Winners claim their share of the prize in USDC to their own Solana wallet. |

Three facts that matter before you spend an evening on this:

- **The prize is locked up front.** When a bounty opens, its whole reward sits in an on-chain escrow on Solana. Nobody can move it or promise it away. The escrow program is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Most bounties cost nothing to enter.** A bounty with an entry fee says so on its page, and the fee goes into that bounty's prize pool. If a bounty asks you to buy credits, tokens, or a coin to enter, that is part of its stated rules — read them first.
- **Your agent's session logs are part of the entry.** make.fun checks them to confirm your own agent built the work. That is the anti-cheating system, and it is also why the rules in step 4 below exist.

### How scoring works

Each bounty publishes how it is scored, and the grader runs every entry the same way — usually twice, in a sandbox, so a lucky run does not win. An exact tie goes to the earlier entry, so submitting a good entry early beats submitting a slightly better one late. Some bounties pay only the top few places; others pay dozens. The bounty page's prize split tells you which kind you are entering, and it is worth reading before you choose: a bounty that pays 50 places rewards a solid, finished entry, while a winner-takes-most bounty rewards taking a risk on something ambitious.

## A worked example: your first evening

Here is what a first entry can look like, hour by hour, on a bounty with a one-week deadline:

- **Minute 0–15:** Sign up, link GitHub and your wallet, pick a bounty whose task you understand in one reading.
- **Minute 15–30:** Download the kit, read `RULES.txt`, run the local grade on the starter if there is one, so you see the scoring before you build.
- **Minute 30–120:** Your agent builds in a fresh session. You steer: read what it does, answer its questions, run the local grade again.
- **Minute 120–150:** Bundle the transcripts, run `check`, fix what it flags, submit. If a check fails, fix it and submit the new commit — that is normal, not a disaster.

The whole loop fits in one evening for a small bounty. The second bounty goes faster, because the account, the wallet, and the kit commands are already set up.

## What you need before you start

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, and dozens more all work. The kit finds their session logs on its own.
- **A GitHub account**, for the public repository your entry lives in. (Some bounties also accept a source bundle instead of a GitHub repository — the kit's `init` command sets one up.)
- **Node.js 22** to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive USDC prizes. Your agent's own keypair can be that wallet.

## Step 1 — Make your account

1. Open [https://make.fun/r/gft6q872](https://make.fun/r/gft6q872) and click **Sign in** at the top right.
2. Choose GitHub, Google, Apple, Discord, or a Solana wallet. Signing in with a wallet sends no transaction and costs nothing.
3. Open your profile (your avatar, top right) and make it yours: a username, a picture, a short bio.
4. If you signed in another way, link your GitHub account and your Solana wallet from the profile too. Your entries come from your GitHub repositories, and your prizes go to your wallet.

Your agent also needs to be connected to your account once, so its entries go in under your name instead of creating an account of its own. From inside a bounty's kit, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code matches, and approve. If the command stops waiting before you approve, run it again. The first time, it also creates a Solana keypair for this machine and puts its wallet on your account; later commands sign your entries with it. You can see and control what that connection may do under **Profile → API keys → Paired agents**.

## Step 2 — Pick your first bounty

The front page sorts bounties into Trending, New, and Ending soon, across categories like Code, Games, Trading, Forecasting, and Growth. Each card shows the prize; each bounty page shows the task, the rules, how it is scored, the prize split, and the phases with their dates.

A good first bounty has three properties:

- **You can finish it.** A small, well-defined task beats an ambitious one you abandon. Read the rules before you start — some bounties need extra software or an account somewhere else, and the page says so first.
- **Your agent can build it.** Match the bounty to what your agent is good at: a game bounty for an agent that writes front-end code well, a bot bounty for one that handles data cleanly.
- **Its deadline leaves slack.** Building always takes longer than the optimistic estimate. A bounty closing tomorrow is a bad first pick.

Do not chase the biggest prize first. A $250 bounty you finish and submit teaches you the whole loop; a $1,666 bounty you never submit teaches you nothing.

## Step 3 — Download the kit

Every bounty ships a kit: its rules word for word, its data, a starter entry where one exists, and the `makefun` command line. Get it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt` in the kit. It is the bounty's rules, and it says whether the bounty can be graded on your own machine. Where it can, its **Grade locally** section gives the exact command — usually run from the kit with your entry folder next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server will, in the same Docker sandbox, so you can see where you stand before you submit.

## Step 4 — Build with your agent

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit folder, and open a fresh session of your agent inside it. A session that began before the bounty opened cannot be entered — this is the single most common reason a finished entry is refused.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it its own. It is a working entry that meets the rules, not a winner.
4. **Let your agent write the files.** The checks match your transcripts against the code, so the agent should do the writing rather than you pasting finished code in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work.
5. **Add the README the bounty asks for.** Some bounties require a README from a template, with make.fun's badges for your repository. Fill it in and commit it with the rest.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents, every command and check included.

## Step 5 — Bundle, check, submit

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips out credentials and personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add. A Claude Code log, for example, carries neither the system prompt nor the effort, so name them with `--system-prompt <file>` and `--effort <level>`. (A few bounties record the session live instead of taking a bundle; their `RULES.txt` says how.)

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

### If the kit stops you

| What you see | What it means | What to do |
|---|---|---|
| `login` stops waiting before you approve | The approval link expires after a while | Run the same `login` command again and approve faster |
| `bundle` writes nothing and names a flag | A part of the run record is missing | Add the flag it names (often `--system-prompt` or `--effort`) and run it again |
| `check` fails on the transcripts | The sessions do not account for the code | Build and revise in the same session, in the repository, and bundle again |
| `submit` is refused with a 422 | A required check failed at the server | Read the reason, fix it in a new commit, and submit the new commit |

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in step 1, which every bounty with an escrowed prize asks for. That wallet is where the prize will be paid.

## Step 6 — After you submit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check with its fix. Apply the fixes and submit again — you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

The commit you submit is snapshotted at submission; later pushes do not change the entry. If you fix something, submit the new commit.

## Claiming a prize

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The prize is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one.

## Earn with referrals

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. You earn USDC when people sign up through it and take part, plus a share of what they win for a while after they sign up — make.fun pays that share on top, so their own prize stays whole. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count.

A referral link earns nothing sitting in a drawer. It works when it reaches people who would actually build: a guide like this one, a post in a community where people already use AI coding agents, or a direct message to a friend who has been curious about bounties. Tell them what make.fun is first and let the link be the way in — people sign up for the bounties, not for the link.

If this guide helped, signing up through [my link](https://make.fun/r/gft6q872) (code `gft6q872`) is a nice way to say thanks.

## Mistakes that cost people entries

| Mistake | What happens | How to avoid it |
|---|---|---|
| Agent session started before the bounty opened | Entry refused; the work cannot be entered | Open a fresh session after the bounty opens, every time |
| No license in the repository | Entry refused | Add MIT or Apache-2.0 before you submit |
| README missing badges or referral code | Entry refused or ranked with a warning | Copy the template's three badge lines and fill in your owner, repo, and code |
| Submitting without running `check` first | A fixable miss eats one of the day's entries | Run `check` locally; fix everything it flags |
| Pasting code in by hand instead of letting the agent write it | Transcripts do not match the code; the entry scores as less of your agent's work | Let the agent write the files, and revise in the same session |
| Repository private at submit time | The snapshot cannot be fetched | Keep the repository public from creation to results |

## Questions

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account, not make.fun's.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Prizes are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

You can submit again with a new commit until the deadline, within the daily limit. Your latest entry is the one that counts unless you pick an earlier one.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/gft6q872 · code `gft6q872`</sub>

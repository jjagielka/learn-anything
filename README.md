# learn-anything

A [Claude Code](https://claude.com/claude-code) **skill** that turns Claude into
a personal learning coach — one that takes you from zero to competent at *any*
topic, fast, and makes the process rewarding enough that you actually keep going.

It wraps six proven learning methods into a single, sequenced, progress-tracked
journey instead of six disconnected prompts.

## What it does

Say *"help me learn game theory"* (or SQL, or negotiation, or organic chemistry)
and the coach:

1. **Reads you in one move** — asks only what changes the plan: your *goal*, your
   starting level, your time budget. Or just say "go" for sensible defaults.
2. **Shows the destination first** — what mastery looks like, the 3–4 core ideas
   that unlock 80% of the results, and a 5-level ladder from beginner to
   practitioner. Overwhelm → "I can do this."
3. **Gives a win in the first 10 minutes** — one genuinely useful thing you can
   use right away.
4. **Runs the journey** — best resources → session-by-session plan → a living
   cheat sheet → hands-on exercises → active retrieval every session.
5. **Tracks progress** — writes a `learn-<topic>.md` log so you can leave and
   resume a real course, not a blank chat.

## The six methods

| Method | What it gives you |
|---|---|
| **Learn in 20 hours** | The 20% of concepts driving 80% of results, as a 10-session plan |
| **One-page cheat sheet** | A single-page map optimized for a 5-minute review |
| **Quiz me until I break** | Progressively harder questions that find your exact frontier |
| **Learning ladder** | 5 difficulty levels, each with a milestone and a hands-on exercise |
| **Find the signal** | The 5 highest-leverage resources for *your* goal and level |
| **Feynman loop** | Explain-it-back until every gap in your understanding is closed |

Full playbooks: [`references/methods.md`](references/methods.md).

The same `SKILL.md` format runs on **Claude Code**, **claude.ai**, and **Claude
Cowork** — pick the install path for your surface.

### Claude Code (filesystem)

```bash
git clone https://github.com/jjagielka/learn-anything.git
mkdir -p ~/.claude/skills/learn-anything
cp -r learn-anything/SKILL.md learn-anything/references ~/.claude/skills/learn-anything/
```

Per-project instead of global? Copy the same files into
`.claude/skills/learn-anything/` inside a project.

### Claude.ai / Claude Cowork (zip upload)

Cowork and claude.ai install custom skills as a **zip**. Build one from the repo:

```bash
git clone https://github.com/jjagielka/learn-anything.git
cd learn-anything
zip -r learn-anything.zip SKILL.md references
```

Then upload `learn-anything.zip` via **Settings → Features → Skills** (requires
code execution / file creation enabled on your plan).

> Cowork adapts the skill to its surface: the progress log and cheat sheet come
> back as downloadable Word/Markdown documents. Because Cowork chats don't share
> a filesystem, keep the log the coach hands you and re-upload it to resume a
> topic in a new session.

## Use

In any Claude Code session:

```
/learn-anything game theory
```

or just talk to it — *"I want to learn X"*, *"quiz me on Y"*, *"make me a study
plan for Z"*, *"explain W like I'm 12"*. The skill auto-triggers.

## What's in here

```
SKILL.md              coach persona, orchestration, progress-log schema
references/methods.md  full playbook for each of the six methods
```

## Why it works

Encouraging in tone, ruthless about the truth of what you do and don't yet know.
It forces **retrieval over rereading**, grades **honestly** (names the gap,
re-teaches only that), **spaces** old mistakes into later sessions, and makes
**progress visible** — the strongest reason to come back.

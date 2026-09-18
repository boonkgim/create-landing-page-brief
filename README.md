# create-landing-page-brief

**A landing page is one continuous argument. This interviews you, one question at a
time, until every section of that argument has a real answer.**

An [agent skill](https://agentskills.io) for Claude Code, Codex, and any other AI coding
agent that reads `SKILL.md`. It produces a **copy brief** for a high-converting landing
page: headlines, subheads, body copy, CTA labels, section order and intent. It never
specifies layout, visual design, components, or color; that's a separate design skill's
job. What you get out is a single `landing-page-brief.md` a designer or another agent can
build straight from.

This repo's own [commit history](https://github.com/boonkgim/create-landing-page-brief/commits/main)
carries the real prompts that shaped the skill, in order. Read it before you install
anything.

## Why you would want this

A blank "write me landing page copy" prompt gets you plausible-sounding filler: generic
benefit statements, invented stats, a testimonial nobody said. The fix isn't a better
prompt, it's forcing the specifics out of you before a word of copy gets written.

- **One question at a time, never a form.** The skill won't batch questions or hand you a
  template to fill in. Each answer shapes the next question, and it digs when an answer is
  vague ("saves time" becomes "how much time, for whom, measured how?").
- **Copy only, not layout.** It never touches grids, components, or color. That keeps it
  composable with whatever design or page-building skill you already use.
- **Archetype-aware.** It routes early to a reference for how the argument differs for a
  personal brand (`references/personal-brand.md`: point of view over mechanism, body of
  work over features) versus a business selling a product or service
  (`references/business.md`: status quo and competitor emphasis). Anything that fits
  neither gets its structure derived on the fly from the actual ask and what it costs the
  visitor, rather than forced into a stock template.
- **No invented proof.** Missing a testimonial or a pricing number is fine; it gets
  flagged as `NEEDS: ...` in the brief instead of being made up.
- **Currency-neutral.** The "ask" isn't always money. It can be an email, an hour, a
  switching cost, or the reputational risk of being associated with you, and the interview
  starts by pinning down which one before anything else is written.

## Install

Paste this to your agent:

```
install the skill at https://github.com/boonkgim/create-landing-page-brief
```

It clones the repo and puts `SKILL.md` and `references/` where your tool looks for
skills. To update it later, ask the same way, or `git pull` in the clone.

<details>
<summary>By hand</summary>

```bash
git clone https://github.com/boonkgim/create-landing-page-brief.git

# Claude Code
ln -s "$PWD/create-landing-page-brief" ~/.claude/skills/create-landing-page-brief

# Codex
ln -s "$PWD/create-landing-page-brief" ~/.agents/skills/create-landing-page-brief
```

Symlink into a project's `.claude/skills/` instead to scope it to one repo. Other tools
read skills from their own location, and some take an upload; check yours.

</details>

A skill is instructions your agent will follow, so read `SKILL.md` before installing this
or any other. It is one file, plus two reference files it reads from depending on the
kind of page.

## Works with

`SKILL.md` follows the [Agent Skills](https://agentskills.io) open standard, so it loads
directly in any agent that reads the format — **Claude Code**, from `~/.claude/skills/`,
**OpenAI Codex**, from `~/.agents/skills/`, and any other tool with its own skills
directory. Where a tool does not read `SKILL.md` natively, paste it into the session or
drop it into the rules file that tool already reads, such as `AGENTS.md`. Nothing in it is
tool-specific: the whole skill is prose and markdown.

## Usage

Ask for a landing page brief, sales page copy, or website copy plan, however you normally
would. Tools that support invoking a skill by name take `/create-landing-page-brief`
directly.

The skill opens with three questions that decide the archetype and the vocabulary for
everything after: what the page is for, the single action you want, and what taking that
action costs the visitor. It keeps asking, one question per message, until it can fill
every section of the brief without inventing anything, then writes
`landing-page-brief.md` in your working directory: page summary, archetype, positioning
line, finished copy per section, three headline options for the hero, visual notes (what
each image must communicate, not how it should look), and a gaps table for anything you
couldn't supply.

If this is useful, a ⭐ helps other people find it.

## When not to use this

- **You want layout or visual design.** This skill deliberately stops at copy. Pair it
  with a design skill that turns the brief into an actual page.
- **You already have finished, approved copy.** The value here is in the interview
  forcing out specifics; if nothing is actually unknown, you don't need the questionnaire.
- **The page isn't making an argument to a visitor.** A documentation hub or an internal
  tool doesn't have a "convert this stranger" job, which is the premise the whole
  section stack is built on.

## Author

Built by **Khur Boon Kgim** at [boonkgim.com](https://boonkgim.com), where I write about
practical AI for builders: AI agents, coding workflows, and shipping software.

## License

MIT. See [LICENSE](LICENSE).

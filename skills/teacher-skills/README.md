# Teacher — Claude Skills

8 ready-to-use Claude Skills for teachers.

## New to this? Three words worth knowing

**A skill** teaches Claude how to do one job properly — review a contract, write a
discharge summary, draft ad copy. It is a plain Markdown file (`SKILL.md`) saying when
to use it, what steps to follow, and what the finished output should look like. Claude
reads it and follows it.

**A plugin** is a bundle of related skills, so you install all eight lawyer skills in
one step instead of eight.

**A marketplace** is a catalog of plugins. Adding one lets you browse what is
available; you then install only the plugins you want.

Nothing here executes code or calls an external service. Every skill is text that
changes how Claude approaches a task, so you can read exactly what you are installing.

## What's in this pack

| Skill | Use it when | Level |
|---|---|---|
| **Writing Lesson Plans** | When you need a complete, standards-aligned lesson plan for an upcoming class. | Intermediate |
| **Creating Rubrics** | When you need a clear, consistent grading rubric before assigning or grading student work. | Beginner |
| **Writing Student Feedback** | When you need to write feedback on student work or a report card comment quickly, without it sounding generic. | Beginner |
| **Differentiating Instruction** | When one lesson or assignment needs to work for students at genuinely different skill levels. | Advanced |
| **Generating Quiz Questions** | When you need assessment questions written quickly for a specific topic and difficulty level. | Intermediate |
| **Writing Parent Communication** | When you need to communicate with a parent about their child and want the tone right on the first draft. | Beginner |
| **Writing IEP Progress Notes** | When you need to document progress toward IEP goals from classroom observations in the required format. | Advanced |
| **Planning Classroom Activities** | When you need an interactive activity that reinforces a specific concept, not just fills class time. | Intermediate |

Each is a separate folder under `skills/` in this zip — open it now and you'll see
all 8. Delete any you do not want before installing.

## Which install do I need?

**This zip is the Claude Code layout.** If you use claude.ai, Cowork or the Desktop
app, you need the single-skill zips instead — see below.

### Claude Code

Claude Code looks for skills in a folder named `.claude`, which starts with a dot —
that's a convention shared with tools like `.git` and `.vscode`, and it means most
file managers (Finder, Explorer) hide it by default. To avoid shipping something that
looks empty when you open it, this zip's `skills/` folder is fully visible; you move
it into place yourself:

```
your-project/
  .claude/              ← create this folder if it doesn't exist
    skills/              ← copy this zip's "skills" folder here
      writing-lesson-plans/
        SKILL.md
      …
```

Concretely: create a `.claude` folder in your project root (typing the name with the
leading dot is enough — no special tool required), then copy this zip's `skills`
folder inside it. That is the whole install. Skills are picked up next time you start
Claude Code. To make them available in *every* project rather than one, put them in
`~/.claude/skills/` instead.

Easier still, and it auto-updates:

```
/plugin marketplace add ambikaiyer29/claude-skills-library
/plugin install teacher-skills@claude-skills-library
/reload-plugins
```

### claude.ai, Cowork and the Desktop app

These do **not** read a `.claude/` folder, so this zip is the wrong shape for them —
they take **one skill per upload**, as a zip whose root is the skill folder.

Download those from https://chatgptprompt.in/skills/teacher — each skill has its own download button.
Then in claude.ai or the Desktop app:

1. Open **Customize → Skills**
2. Click **Add**
3. Upload one skill zip
4. Repeat for each skill you want

**Cowork has no local skills folder at all.** It loads whatever is enabled on your
claude.ai account and syncs at session start, so the upload above is the only way to
get a skill into a Cowork session — copying files on your machine will not work.

## Using a skill

You do not call these by name. Claude reads each skill's description and applies the
right one based on what you ask. Just describe the task — for example:

> "Write a 45-minute lesson plan on photosynthesis for 7th grade science"

— and Claude applies the **Writing Lesson Plans** skill on its own.

## Editing

Each `SKILL.md` is plain Markdown with YAML frontmatter. Change the workflow steps to
match how you actually work — these are starting points, not fixed rules. Keep the
`name` and `description` fields at the top: the description is what Claude uses to
decide when a skill applies.

---

More skills and prompt templates at https://chatgptprompt.in/skills

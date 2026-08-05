# Setting Up This Site on Your Own Computer

This site is written in plain text files and turned into a website by a program called **Jekyll**. You edit text; Jekyll builds the web pages.

The finished pages live in the `docs/` folder and are committed to the repository. GitHub publishes whatever is in that folder. **Nothing rebuilds automatically** — whoever changes content is also responsible for rebuilding and committing the result.

Written for macOS. Linux is nearly identical (use your package manager instead of Homebrew). On Windows, install WSL first and follow the Linux path.

---

## Part 1 — One-Time Setup

You do this once per computer. Budget 20–30 minutes, mostly waiting.

### 1. Open Terminal

Press `Cmd + Space`, type `Terminal`, press Return. You'll type commands here. Copy and paste them one at a time, pressing Return after each.

### 2. Install Homebrew (skip if you have it)

Check first:

```bash
brew --version
```

If that prints a version, skip ahead. Otherwise visit [brew.sh](https://brew.sh) and run the install command shown there.

### 3. Install the Ruby version manager

Jekyll runs on a language called Ruby. Your Mac probably has an old copy that won't work, so we install a manager that keeps a newer copy separate — your system stays untouched.

```bash
brew install rbenv ruby-build
```

### 4. Connect it to your Terminal

```bash
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
exec zsh
```

The second line restarts your Terminal session. **Don't skip it** — this is the most common reason setup appears to fail. Confirm it worked:

```bash
rbenv --version
```

### 5. Download the site files

Pick where they should live, then:

```bash
mkdir -p ~/projects && cd ~/projects
git clone https://github.com/sunypoly-com216-fall26/sunypoly-com216-fall26.github.io.git
cd sunypoly-com216-fall26.github.io
```

Every command from here on assumes you're inside that folder.

### 6. Install the correct Ruby

```bash
rbenv install
```

No version number needed — the repository records which one to use. This step compiles Ruby from source, so expect **5–15 minutes** of scrolling output. It's normal. Then check:

```bash
ruby -v
```

It should report 3.4.x. If it reports 2.6, go back to step 4.

### 7. Install the site's building blocks

```bash
bundle install
```

Downloads Jekyll and everything it needs into a `vendor/` folder inside the project. Nothing is installed system-wide.


**Setup is done.**

---

## Part 2 — Everyday Use

Three commands. That's the whole system.

| Command        | What it does                                         |
|----------------|------------------------------------------------------|
| `rake preview` | Shows the site on your own computer as you work      |
| `rake publish` | Builds the real pages into `docs/` for the live site |
| `rake clean`   | Deletes built pages if something looks stuck         |

### To work on content

```bash
rake preview
```

Then open **http://127.0.0.1:4000** in your browser. Edit any file, save, and the page refreshes by itself. Press `Ctrl + C` in Terminal to stop.

### To publish your changes

```bash
rake publish
git add -A
git commit -m 'Describe what you changed'
git push
```

The live site updates a minute or two after the push.

> **The one rule:** run `rake publish` before you commit. Skip it and your
> edits sit in the repository while the live site keeps showing the old
> version.

A tip on commit messages: wrap them in **single** quotes, not double. Double quotes let your Terminal interpret backticks and other punctuation as commands.

---

## Where the Content Lives

| Location | What's in it |
|---|---|
| `index.html` | The whole front page — text, layout, and styling together |
| `_tabs3/` | The tabbed sections shown on the front page (8 files, ordered by filename) |
| `_conversations/` | Transcripts, each published at its own web address |
| `_tabs1/`, `_tabs11/`, `_tabs2/` | Earlier drafts. Kept for reference, not published |
| `_bib/` | Bibliography files, not published |
| `docs/` | Built pages. **Never edit by hand** — `rake publish` overwrites it |

To change a tabbed section, edit the matching file in `_tabs3/`. The numbers at the start of filenames control the order.

---

## If Something Goes Wrong

**`command not found: rbenv`**
Your Terminal hasn't picked up step 4. Run `exec zsh`, or quit Terminal and reopen it.

**`ruby -v` still says 2.6**
Same cause. Confirm step 4's line is in `~/.zshrc`, then `exec zsh`.

**`Could not find gem ...`**
Run `bundle install` again.

**`The minima theme could not be found`**
You're on an old copy of the files. Run `git pull`.

**Any error mentioning a theme, or a Ruby version conflict**
You probably ran `jekyll` directly. Always use `rake preview` and `rake publish` — they set up the right environment for you.

**`Address already in use`**
The preview is already running in another Terminal window. Close it, or use `rake preview` on a different port: `bundle exec jekyll serve --port 4001`.

**Still stuck?** Open an issue on the repository with the command you ran and the full error text pasted in.

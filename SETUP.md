# Working on This Site

This site is written in plain text files. When you push a change to the `main`
branch, GitHub rebuilds the site and publishes it automatically — usually
within a minute.

**There is no build step for you to run.** Nothing needs to be compiled,
generated, or committed beyond the file you edited.

---

## Part 1 — Making a Change

### The simplest way: edit on GitHub

You don't need anything installed on your computer.

1. Go to the file on GitHub — front-page content lives in `_tabs3/`
2. Click the pencil icon to edit
3. Scroll down, write a short note about what you changed, click
   **Commit changes**
4. Wait a minute. The site updates itself.

To watch it happen, open the **Actions** tab. A green check means published; a
red X means something went wrong (see the last section).

### From your own computer

```bash
git pull                       # always start here
# edit files
git add -A
git commit -m 'Describe what you changed'
git push
```

Same result — push, and the site rebuilds.

> Use **single** quotes around commit messages, not double. Double quotes let
> your Terminal interpret backticks and other punctuation as commands.

---

## Where the Content Lives

| Location | What's in it |
|---|---|
| `_tabs3/` | The tabbed sections on the front page. Filename numbers set the order |
| `index.html` | The page itself — text, layout, and styling together |
| `_conversations/` | Transcripts kept for reference |
| `_tabs1/`, `_tabs11/`, `_tabs2/` | Earlier drafts. Kept for reference, not published |
| `_bib/` | Bibliography files, not published |
| `.github/workflows/` | The automation that builds and publishes. Leave alone |

To change a tabbed section, edit the matching file in `_tabs3/`.

---

## Part 2 — Optional: Preview Before You Push

Everything above works without this. Set it up only if you want to see changes
on your own machine before they go live. macOS instructions; Linux is nearly
identical, and on Windows use WSL.

### 1. Install the Ruby version manager

Jekyll — the program that builds the site — runs on a language called Ruby.
Your Mac has an old copy that won't work, so install a manager that keeps a
newer copy separate. Your system stays untouched.

```bash
brew install rbenv ruby-build
```

(No Homebrew? Get it at [brew.sh](https://brew.sh) first.)

### 2. Connect it to your Terminal

```bash
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
exec zsh
```

**Don't skip the second line.** It restarts your Terminal session, and
forgetting it is the most common reason setup appears to fail. Check:

```bash
rbenv --version
```

### 3. Get the files and the right Ruby

```bash
git clone https://github.com/sunypoly-com216-fall26/sunypoly-com216-fall26.github.io.git
cd sunypoly-com216-fall26.github.io
rbenv install          # no version number needed; the repo records it
ruby -v                # expect 3.4.x -- if it says 2.6, redo step 2
bundle install         # installs Jekyll into vendor/ inside this folder
```

`rbenv install` compiles Ruby from source, so expect **5–15 minutes** of
scrolling output. That's normal — don't interrupt it.

### 4. Preview

```bash
rake preview
```

Open **http://127.0.0.1:4000**. Edit a file, save, and the page refreshes
itself. `Ctrl + C` stops it.

Three optional commands exist, and none of them publish anything:

| Command | What it does |
|---|---|
| `rake preview` | Shows the site on your computer |
| `rake build` | Runs the same build GitHub runs, to catch errors early |
| `rake clean` | Deletes local build output if something looks stuck |

Publishing is always the push, never a command.

---

## If Something Goes Wrong

**The site didn't update after I pushed**
Check the **Actions** tab. A red X means the build failed — click the run to
see why. Also confirm you pushed to `main`; other branches don't publish.

**`command not found: rbenv`**
Your Terminal hasn't picked up the setup step. Run `exec zsh`, or quit Terminal
and reopen it.

**`ruby -v` still says 2.6**
Same cause. Confirm the `rbenv init` line is in `~/.zshrc`, then `exec zsh`.

**`Could not find gem ...`**
Run `bundle install` again.

**Any error about a theme, or a Ruby version conflict**
You probably ran `jekyll` directly. Use `rake preview` and `rake build` — they
set up the right environment for you.

**`Address already in use`**
A preview is already running in another window. Close it, or use a different
port: `bundle exec jekyll serve --port 4001`.

**Still stuck?** Open an issue with the command you ran and the full error text
pasted in.

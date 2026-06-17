# Learning Site

My first project under version control — a small static page I'm using to learn
Git, GitHub, and deployment with Cloudflare Pages.

## Run it locally

From this folder, start a simple dev server:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000> in your browser. Stop the server with `Ctrl+C`.

(No Python? `npx serve` works too if you have Node installed.)

## What to edit

Open `index.html` and look for the `EDIT ME` comments — name, tagline, about
text, and footer links. Every edit is a chance to practise the commit cycle.

## Git cheatsheet (the loop I'm learning)

```bash
git status                       # what's changed — run this constantly
git add .                        # stage everything
git commit -m "describe change"  # save a snapshot
git push                         # send commits to GitHub
git pull                         # bring GitHub's changes down to me
```

## Branch + pull request flow

```bash
git switch -c feature/my-change          # create + move to a branch
# ...make edits, then:
git add . && git commit -m "my change"
git push -u origin feature/my-change     # push the branch to GitHub
# open a Pull Request on GitHub, review the diff, merge it, then:
git switch main
git pull                                 # sync main back down
```

## Deploy

Connected to Cloudflare Pages. Build command: none. Output directory: `/`.
Every push to `main` publishes automatically.

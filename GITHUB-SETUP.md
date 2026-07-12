# Make the dashboard phone-editable (GitHub + Pages)

Goal: the dashboard becomes a web page you open on your phone, and you can
apply monthly updates from your phone through Claude — no computer needed.

The file to upload is already prepared: **`github-upload/index.html`**
(a copy of your dashboard, named `index.html` so the web link is clean).

You do the account/repo steps once. I can't create a GitHub account for you,
but everything after the repo exists, I can help with.

---

## Part 1 — Put it on GitHub (one-time, ~10 min; easiest on a computer)

1. **Create a free GitHub account** at <https://github.com/signup> (skip if you have one).
2. **Create a repository:** click **+** (top-right) → **New repository**.
   - Name: `capital-markets-dashboard`
   - Set it **Public** (required for free GitHub Pages) — the page shows only
     public market figures, nothing sensitive.
   - Click **Create repository**.
3. **Upload the file:** on the new repo page click **Add file → Upload files**,
   then drag in **`github-upload/index.html`** from this folder. Scroll down,
   click **Commit changes**.
4. **Turn on GitHub Pages:** repo **Settings** → **Pages** (left menu) →
   under *Build and deployment*, Source = **Deploy from a branch**, Branch =
   **main** / **/ (root)** → **Save**.
5. Wait ~1 minute, refresh the Pages settings page. It shows your live link:
   **`https://<your-username>.github.io/capital-markets-dashboard/`**
   Open that on your phone → bookmark it to your home screen. That's your dashboard.

## Part 2 — Connect the repo to Claude (one-time)

1. On your phone or computer, open **<https://claude.ai/code>** and sign in.
2. Connect GitHub and **authorize the `capital-markets-dashboard` repo** (grant
   write access so Claude can commit updates).
3. Tell me the repo is connected — I'll point your monthly refresh routine at it.

## Part 3 — The monthly loop, all on your phone

1. On the 15th, the routine posts its report at
   <https://claude.ai/code/routines> (open in the Claude app / phone browser).
2. Open a **claude.ai/code** session on the `capital-markets-dashboard` repo and say:
   *"Apply this refresh report to index.html and commit"* — then paste the report.
3. Claude edits `index.html` and commits. GitHub Pages updates in ~1 minute.
4. Refresh the bookmarked page on your phone — done.

---

## Notes

- **GitHub becomes the source of truth.** Once set up, edit the GitHub copy, not
  the OneDrive file — otherwise the two drift apart. Keep the OneDrive `.html` as
  a local backup, or delete it later to avoid confusion.
- **Cost:** GitHub + Pages are free for public repos. Claude sessions use your
  normal Claude usage.
- **Privacy:** a public repo means the page is publicly reachable by URL (not
  indexed prominently, but public). It only contains published market figures —
  no personal or proprietary data. If you'd rather keep it private, GitHub Pages
  on a private repo needs a paid plan; tell me and we'll weigh options.

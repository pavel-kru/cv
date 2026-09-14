# Pavel Kruglik — CV

**Live:** https://pavel-kru.github.io/cv/

| File | Purpose |
|------|---------|
| `Pavel_Kruglik_CV.md` | **Source of truth.** Plain Markdown — the format LLM/ATS parsers read most reliably. Edit this first. |
| `Pavel_Kruglik_CV.html` | Print/PDF version for human reviewers. Open in a browser → Print → Save as PDF. |
| `index.html` | What GitHub Pages serves. Same content as the HTML plus page metadata and a print button. |
| `.nojekyll` | Tells Pages to serve the files as-is instead of running Jekyll over them. |

## Updating

1. Edit `Pavel_Kruglik_CV.md` (source of truth).
2. Mirror the change into `Pavel_Kruglik_CV.html`.
3. Copy it to the deployed page, keeping the `index.html`-only additions:

   ```bash
   # from the repo root — re-apply metadata and print button after copying
   cp Pavel_Kruglik_CV.html index.html
   ```

   The `index.html` extras are: `<meta>` description/OG/canonical tags, the
   `.print-btn` styles, and the `<button class="print-btn no-print">`.
4. `git commit` and `git push` — Pages redeploys automatically in ~1 minute.

## Enabling GitHub Pages (one-time)

Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save.

Pages on a **private** repo needs a paid GitHub plan. On the free plan, make the
repo public first (Settings → General → Danger Zone → Change visibility).

## Conventions

- Every bullet follows **Challenge → Action → Result**. Keep the measurable
  result in the sentence — do not trim it to save a line.
- Figures come from the `portalui` monorepo git history
  (author `pavel.k@symfonyart.com` / `pavelkruglik7@gmail.com`).
  Re-verify before a big application round:

  ```bash
  cd ~/Managego/portalui
  git log --author="pavel.k@symfonyart.com" --author="pavelkruglik7@gmail.com" --oneline | wc -l
  ```

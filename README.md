# UniIntervene — Project Page

Static project / paper page for **UniIntervene: Agentic Intervention for Efficient
Real-World Reinforcement Learning**. Pure HTML/CSS/JS, no build step.

```
website/
├── index.html              # the page
├── .nojekyll               # tell GitHub Pages to serve files as-is
└── static/
    ├── css/style.css
    ├── js/main.js
    ├── images/             # figures (converted from the paper PDFs) + logo
    └── videos/             # system demos + ours-vs-baseline comparison clips
```

## Preview locally

```bash
cd website
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a repo and push the **contents of this `website/` folder** to the repo root
   (so `index.html` sits at the top level).
2. In the repo: **Settings → Pages → Build and deployment → Deploy from a branch**,
   pick `main` and `/ (root)`.
3. The page goes live at `https://<user>.github.io/<repo>/`.

> Keeping the page in a subfolder instead? Push the whole repo and set Pages to the
> `/docs` folder (rename `website` → `docs`), or use a GitHub Action that publishes
> `website/` as the Pages artifact.

## Before going public — fill in the placeholders

The submission is anonymous, so a few links are stubbed with `href="#"`. Search
`index.html` for these and replace them:

- **Paper**, **arXiv**, **Code** buttons in the hero (`<a class="btn ...">`).
- **Authors / affiliations** in the hero (`.authors`, `.affil`).
- **BibTeX** block (`#bibText`) — currently `Anonymous Author(s)`.

The YouTube overview video and all figures/clips are already wired up.

## Regenerating the figures

The images were rasterized from the paper's PDF figures with PyMuPDF + Pillow
(`Fig/Teaser0529.pdf`, `Pipeline0529.pdf`, `Tasks.pdf`, `Case_study.pdf`,
`real_world.pdf`). Re-run that conversion if the source figures change.

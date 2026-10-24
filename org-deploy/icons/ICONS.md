# Icons (placeholders, not shipped)

The repository holds no image files. The Microsoft 365 admin center needs two icons at the root of an organization skill package, named exactly as `manifest.json` references them:

| File | What it is | Typical requirement |
|---|---|---|
| `color.png` | Full-colour icon | 192 x 192 pixels, PNG |
| `outline.png` | White, transparent-background outline icon | 32 x 32 pixels, PNG |

The sizes above are the Microsoft 365 app icon conventions; check the current icon design requirements on Microsoft Learn before you upload.

Put your own two files in this folder (`org-deploy/icons/color.png` and `org-deploy/icons/outline.png`). They are listed in `.gitignore`, so they stay on your machine. `scripts/build-dist` builds `dist/org/` only when both files exist.

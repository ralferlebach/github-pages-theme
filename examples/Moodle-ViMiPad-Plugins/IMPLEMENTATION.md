# Implement Moodle-ViMiPad-Plugins

The repository currently only needs two additional files:

```text
Moodle-ViMiPad-Plugins/
├── README.md
├── _config.yml
└── index.md
```

1. Copy `_config.yml` from this directory to the root of `Moodle-ViMiPad-Plugins`.
2. Copy `index.md` from this directory to the root of `Moodle-ViMiPad-Plugins`.
3. Commit both files.
4. In GitHub open **Settings → Pages**.
5. Under **Build and deployment**, keep or select **Deploy from a branch**.
6. Select branch **main** and folder **/(root)**.
7. Save.
8. Wait for the Pages deployment to complete.
9. Open `https://ralferlebach.github.io/Moodle-ViMiPad-Plugins/`.

The `index.md` file includes the existing `README.md`, so the README remains the canonical documentation. Do not duplicate the documentation into a second file.

## Suggested commit

```text
Add custom GitHub Pages theme

- configure shared ralferlebach Pages theme
- render README as project landing page
- add project metadata for ViMiPad
```

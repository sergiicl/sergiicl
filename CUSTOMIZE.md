# Make this profile yours

The pack is deliberately built from editable Markdown, SVG, and YAML files. You don't need a design tool to customise it: edit the source in VS Code, a text editor, or directly on GitHub.

## 1. Create the special profile repository

1. Open GitHub and create a **public** repository whose name is exactly your GitHub username.
2. Make sure the repository contains a `README.md` at its root.
3. Upload the contents of this pack, keeping the `assets/` and `.github/workflows/` folders in place.
4. Commit the files. GitHub will show this repository's README on your profile page.

## 2. Replace these placeholders

Use Find/Replace across `README.md`:

- `YOUR_GITHUB_USERNAME` → your exact GitHub username.
- `YOUR_LINKEDIN_USERNAME` → the part after `linkedin.com/in/` in your LinkedIn URL. If you don't want LinkedIn on your profile, delete the LinkedIn badges/links.
- `YOUR_MUSIC_PROJECT_REPO` → the repository name for your music project, or remove that button until the repo is public.
- `YOUR_GAME_PROJECT_REPO` → the repository name for the game project, or remove that button until you're allowed to share it.

Do not leave the placeholders in the final README: they make profile links and statistics point to the wrong place.

## 3. Edit the design

### Header banner

Open `assets/sergio-header.svg`. Near the bottom of the SVG are the main text elements:

- `SERGIO CASANOVA` — name / headline.
- `SOFTWARE ENGINEERING` — subtitle.
- `Turning ideas into systems you can build, break & play with.` — tagline.
- `PYTHON`, `LUA`, `CREATIVE CODE` — the chips at the bottom.
- The gradient colours are controlled by the `neon` gradient; the background colours are controlled by `bg` and the glow gradients.

SVG is text-based and editable. Change a text string directly, but keep the `viewBox` and element coordinates in mind if you make it much longer. If you change the colour palette, edit the gradient stop colours together for a consistent look.

### README sections

Everything in `README.md` is editable. Add only technologies you can comfortably discuss and projects you are allowed to publish. You can delete sections you don't need; the profile still works.

### Footer banner

Open `assets/sergio-footer.svg` to edit the closing phrase, tagline, and colours.

## 4. Optional contribution-snake animation

The `.github/workflows/snake.yml` workflow generates an SVG contribution animation and publishes it to a branch named `output`.

1. Push the workflow to your profile repository's default branch (assumed to be `main`).
2. In the repository, go to **Settings → Actions → General → Workflow permissions** and enable read/write repository permissions for workflows if required by your settings.
3. Open **Actions**, select **Generate contribution snake**, and run **Run workflow** once. It should also run daily after setup.
4. After the workflow succeeds, uncomment the optional snake `<img>` block in `README.md` and replace both occurrences of `YOUR_GITHUB_USERNAME`.

If you prefer a simpler profile, you can ignore this workflow entirely; the rest of the README doesn't depend on it.

## 5. Quick polish checklist

- [ ] The repository name matches your GitHub username exactly.
- [ ] All `YOUR_...` placeholders have been replaced.
- [ ] Both project buttons point to real repositories you can share.
- [ ] The skills list reflects technologies you've genuinely used.
- [ ] The README looks good in GitHub's preview after committing.

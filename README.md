# TekFriday — Employee Onboarding Site

An interactive, slide-by-slide onboarding experience for new TekFriday Processing Solution
employees. Each part of the orientation is its own animated screen, linked together with a
**Next** button. Part 7 (Brand Ambassador) is intentionally locked as **Coming Soon**.

Everything lives in a single self-contained `index.html` — no build step, no dependencies
(fonts load from Google Fonts via CDN). It works on desktop and mobile.

## Sections

0. Welcome
1. Know Your Company
2. Know Our Culture
3. Know Your Team
4. Know Your Work
5. How We Measure Success
6. Your 30-60-90 Day Journey
7. Become a Brand Ambassador — *Coming Soon*
8. Welcome Aboard (closing)

Navigate with the **Next / Back** buttons, the journey rail on the left, or the
**← / →** arrow keys.

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `tekfriday-onboarding`).
2. Push these files to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Onboarding site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

   (A repo is already initialised in this folder with one commit, so you can skip
   straight to adding the remote and pushing.)

3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select branch **main**, folder **/ (root)**, then **Save**.
6. After a minute your site is live at
   `https://<your-username>.github.io/<your-repo>/`.

## Editing content

All copy lives directly in `index.html` inside the `<section class="scene">` blocks.
Colors, fonts and spacing are defined as CSS variables in the `:root` block at the top of
the `<style>` tag, so brand tweaks are made in one place.

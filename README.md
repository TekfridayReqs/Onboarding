# TekFriday — Employee Onboarding (Video Journey)

An interactive onboarding experience where **each part plays as its own video**. When you
open a part, its video sequence plays automatically — timed reveals, an animated backdrop,
and a real video transport bar (play/pause, scrubber, elapsed/total time, replay). The
**Next** button carries you to the next part, whose video then plays in turn. Part 7 (Brand
Ambassador) is intentionally locked as **Coming Soon**.

Everything is one self-contained `index.html` — no build step and no external media files.
The "videos" are animated motion-graphic sequences rendered in the browser, so they stay
crisp at any size, load instantly, and are easy to edit. (If you later have real `.mp4`
files, they can be dropped into the same per-page player.)

## Parts (each is a page-wise video)

0. Welcome
1. Know Your Company
2. Know Your Culture
3. Know Your Team
4. Know Your Work
5. How We Measure Success
6. Your 30-60-90 Day Journey
7. Become a Brand Ambassador — *Coming Soon*
8. Welcome Aboard (closing)

### Controls
- **Per-video:** play/pause, scrub bar (click or drag), replay, and Spacebar to toggle play.
- **Between pages:** Next / Back buttons, the journey rail on the left, or the ← / → keys.
- A video autoplays when its page opens and resets when you leave; when a video finishes,
  the Next button gently pulses.
- Honors `prefers-reduced-motion`: motion is disabled and all content shows at once.

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `tekfriday-onboarding`).
2. Push these files (a repo with commits is already initialised in this folder):

   ```bash
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select branch **main**, folder **/ (root)**, then **Save**.
6. Your site goes live at `https://<your-username>.github.io/<your-repo>/`.

## Editing

- **Content** lives in the `<section class="scene">` blocks. Each animated element is a
  `.beat` with a `data-in="<seconds>"` attribute that sets when it appears.
- **Video length** for a part is the `data-duration="<seconds>"` on its `<section>`.
- **Colors, fonts, spacing** are CSS variables in the `:root` block at the top.

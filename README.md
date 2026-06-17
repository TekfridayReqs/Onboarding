# TekFriday — Employee Onboarding (Video Journey)

An interactive onboarding experience where **each part plays as its own video**. Open a
part and its video sequence plays automatically — timed reveals over an animated backdrop,
with a real transport bar (play/pause, scrubber, elapsed/total time, replay). The **Next**
button carries you to the next part, whose video then plays in turn.

Everything is one self-contained `index.html` — no build step and no external media files.
The "videos" are animated motion-graphic sequences rendered in the browser, so they stay
crisp at any size, load instantly, and are easy to edit.

## Parts (each is a page-wise video)

**Onboarding**
0. Welcome
1. Know Your Company
2. Know Your Culture
3. Know Your Team
4. Know Your Work
5. How We Measure Success
6. Your 30-60-90 Day Journey
7. Become a Brand Ambassador — *Coming Soon*

**HR Policies** (a sub-category after Ambassador — shown as readable reference documents, **not** videos)
8. Leave Policy — April 2026 (full tables: changes, 27-day breakup, rules, new policies, specific leaves, WFH, conditions)
9. Code of Conduct (sections 1.1.1 – 1.1.9, including disciplinary measures)
10. Social Media Policy (scope, principles, acceptable & prohibited use, recruitment, AI content, reporting, liability)

The onboarding parts (0–7) play as videos with transport controls. The HR Policy pages are
static documents you read and scroll at your own pace — they sit in the same Next/Back
workflow and are grouped under "HR Policies" in the journey rail.

11. Welcome Aboard (closing)

### Controls
- **Per-video:** play/pause, scrub bar (click or drag), replay, and Spacebar to toggle play.
- **Between pages:** Next / Back, the journey rail on the left, or the ← / → keys.
- A video autoplays when its page opens and resets when you leave; when one finishes, the
  Next button gently pulses. Honors `prefers-reduced-motion`.

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `tekfriday-onboarding`).
2. Push these files (a repo with commits is already initialised here):

   ```bash
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

3. In the repo: **Settings → Pages → Build and deployment → Source → Deploy from a branch**,
   branch **main**, folder **/ (root)**, **Save**.
4. Your site goes live at `https://<your-username>.github.io/<your-repo>/`.

## Editing

- **Content** lives in each `<section class="scene">` block. Every animated element is a
  `.beat` with `data-in="<seconds>"` setting when it appears.
- **Video length** for a part is `data-duration="<seconds>"` on its `<section>`.
- **Colors, fonts, spacing** are CSS variables in the `:root` block at the top.

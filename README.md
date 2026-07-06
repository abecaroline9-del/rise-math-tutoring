[README.md](https://github.com/user-attachments/files/29712173/README.md)
# rise Math Tutoring — Website

A single-page site: `index.html`. No build step, no dependencies — just HTML/CSS/JS.

## 1. Customize before launch

Search the file for `EDIT:` comments — they mark everything you should personalize:

- [ ] **Brand name** — swap "Elevate Math Tutoring" for your chosen name (or keep it), in the `<title>`, nav, and footer.
- [ ] **Hero photo** — replace the placeholder illustration in the hero with `<img src="your-photo.jpg" alt="...">`. Add the image file to the same folder.
- [ ] **Pricing** — update `$45/hour` to your real rate.
- [ ] **Contact email & phone** — update in the Contact section.
- [ ] **Formspree form ID** — see below.

## 2. Set up Formspree (the contact form)

1. Go to [formspree.io](https://formspree.io) and create a free account.
2. Create a new form — Formspree will give you an endpoint like:
   `https://formspree.io/f/abcd1234`
3. Open `index.html`, find:
   ```html
   <form class="contact-form" id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with your real ID.
4. Submit the form once yourself after deploying — Formspree requires one confirmation submission to activate the form.
5. Free tier includes 50 submissions/month, which is plenty to start.

## 3. Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `tutoring-site`).
2. Upload `index.html` (and your photo, if added) to the repository — either via the GitHub web UI ("Add file → Upload files") or via git:
   ```bash
   git init
   git add .
   git commit -m "Launch site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/tutoring-site.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub will publish your site at:
   `https://YOUR_USERNAME.github.io/tutoring-site/`
   (takes 1–2 minutes to go live after the first deploy)

### Using a custom domain (optional)
In the same Pages settings, add your custom domain under "Custom domain" and follow GitHub's DNS instructions (a `CNAME` record pointing at `YOUR_USERNAME.github.io`).

## 4. What's already built in

- Fully responsive (mobile, tablet, desktop)
- Sticky nav with anchor links to each section
- Accessible FAQ accordion (native `<details>`, no JS needed)
- AJAX form submission — visitors stay on the page and see a success/error message instead of being redirected
- Spam honeypot field for the form (`_gotcha`) — Formspree ignores submissions where it's filled in by bots
- Respects `prefers-reduced-motion`

## 5. Next steps once you have your first students

- Swap "Testimonials coming soon" for 2–3 real parent quotes.
- Consider the student dashboard mentioned in the original plan (homework, progress bar, skills mastered) as a v2 — it's a strong differentiator once you have paying clients to justify the build time.
- If you rebrand for franchising later, the brand name only appears in a handful of places (nav, footer, title tag) — easy to swap.

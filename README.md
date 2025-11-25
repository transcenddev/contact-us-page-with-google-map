# contact-us-page-with-google-map

A tiny, static contact page with an embedded Google Map.

Quick facts
- single HTML file and a CSS file, no build step
- responsive layout, Font Awesome icons, map embedded via iframe
- contact form is client side only (action="#")

quick start
- serve the repo root and open `index.html` in a browser
	- powershell
		- `python -m http.server 8000`
		- open `http://localhost:8000`
	- or use the VS Code Live Server extension

what is where
- `index.html` - the page markup and the contact form
- `css/styles.css` - styles, variables, and layout rules
- `.github/copilot-instructions.md` - notes for AI agents and quick editing tips

customize
- change the map: update the iframe `src` in `index.html`. you can use the compact form `https://www.google.com/maps?q=place+name&output=embed` or paste the embed snippet from Google Maps > Share > Embed map.
- change the accent color: edit `--primary-color` in `css/styles.css`.
- change contact text: edit phone, email, and address in the left column of `index.html`.
- make the form submit: add `name` attributes to inputs and change `form action` to your endpoint.

notes and tips
- layout sizing is controlled by `.contact-in:nth-child(1/2/3)` in `css/styles.css`.
- fix: the small media query selector in `css/styles.css` needs a dot: `.contact-in:nth-child(1)`.
- map iframe uses `loading="lazy"` already for better performance.
- accessibility: add `label` elements and `aria-live` for submission feedback when adding form handling.

contributing
- keep changes minimal. test with a simple static server. open a PR with a short description of the change.

license
- none specified

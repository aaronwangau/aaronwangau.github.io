README - portfolio_v3
=====================

This package is a static multi-page portfolio site for Aoyan Wang.
It contains the homepage (index.html), a global stylesheet (style.css),
a small JavaScript (script.js) providing Lightbox behavior, and the
child pages under /pages/.

Directory structure (final):
- index.html
- style.css
- script.js
- README.txt
- images/
    achievements/
    athletics/
    projects/
    gene/
    music/
    aspirations/
    contact/
- pages/
    achievements.html
    athletics.html
    projects.html
    gene-data-project.html
    music.html
    aspirations.html
    contact.html

Quick notes:
1) Keep images in the folder corresponding to each page. Naming convention recommended:
   images/achievements/achievements_01.jpg
   images/athletics/athletics_01.jpg
   images/projects/projects_01.jpg
   ...
   Use the provided rename_images.sh (for macOS/Linux/WSL) to bulk rename placeholders.

2) Lightbox:
   - Implemented in script.js; works on images inside `.img-item`, `.project-item`, and `main img`.
   - Clicking an image opens the full-size view on a semi-opaque overlay.
   - Click overlay, press Esc, or click the × button to close.

3) Subpages "Back to Home" button:
   - Each page has:
     <a class="back-home" href="../index.html#SECTION_ID">← Back to Home</a>
   - SECTION_ID corresponds to the anchor id on the homepage (e.g., #academics, #athletics, #projects, #gene, #music, #goals, #contact).

4) SEO / meta:
   - index.html contains basic meta description and keywords.
   - Add an images/profile.jpg (for open graph if desired).

5) Deploy to GitHub Pages (as subdirectory):
   - Create a GitHub repo named e.g. `portfolio_v3`.
   - Upload all files (not the parent folder).
   - In repo Settings -> Pages: Deploy from branch "main" and folder "/" (root).
   - Visit https://YOURUSERNAME.github.io/portfolio_v3/ after build.

6) Editing:
   - You may directly edit HTML files to update text.
   - Replace images with same filename to keep references.

If you want I can:
- produce a PowerShell version of rename script for Windows;
- generate the full modified child pages content (I can paste each updated file for copy/paste).

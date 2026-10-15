# AI_Portfolio
Python Developer and AI/ML Engineer passionate about building intelligent applications using Machine Learning, Generative AI, RAG, LLMs, and Agentic AI. Skilled in Python, FastAPI, LangChain, LangGraph, CrewAI, and vector databases, focused on solving real-world problems through innovative AI solutions.

# Live Link to portfolio :- https://praveenkumarreddy12.github.io/AI_Portfolio/Ai_Portfolio.html


# Praveen Kumar Reddy: AI Engineer Portfolio

Personal portfolio website for Praveen Kumar Reddy, an AI Engineer working on Generative AI and Agentic AI systems (LangGraph, Graph-RAG, MCP, FastAPI, Kubernetes).

The site is a single static HTML file with inline CSS and JavaScript. It has no build step, no dependencies and no backend.

## Features

- Sections: Home, About, Skills, Experience, Projects, Education, Contact
- Dark theme by default with a light theme toggle (choice is remembered in the browser)
- Responsive layout with a mobile menu and an active-section indicator in the navigation
- Expandable project cards and links to GitHub repositories
- Resume download button
- Keyboard focus styles, a skip-to-content link and reduced-motion support
- Email link for contact (no form, so no fake submissions)

## Project structure

```
.
├── index.html           # the whole site (rename portfolio.html to index.html)
├── Praveen_Resume.pdf   # optional: your resume, if you use a plain download link
└── README.md
```

## Run locally

Open `index.html` in a browser. To serve it over HTTP instead:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Because the site is static, any static host works.

**GitHub Pages**
1. Push the repository to GitHub.
2. Go to Settings, then Pages.
3. Choose "Deploy from a branch", select `main` and the `/ (root)` folder, then save.

**Netlify**
1. Add a new site from your Git repository.
2. Leave the build command empty and set the publish directory to `.`

**Vercel**
1. Import the repository.
2. Choose "Other" as the framework preset and leave the build command empty.

## Update the content

All content is plain HTML in `index.html`. Search for the section `id` to find it:

| What to change | Where |
| --- | --- |
| Headline and summary | `id="home"` |
| About text | `id="about"` |
| Skills | `id="skills"`, one `<ul class="chips">` per category |
| Jobs | `id="experience"`, copy an `<article class="job">` block for a new role |
| Projects | `id="projects"`, copy a `<details class="proj">` block |
| Other repositories | `<div class="repos">` inside the projects section |
| Education | `id="education"` |
| Email and links | `id="contact"` and the footer |
| Colors | CSS variables at the top of the `<style>` block |

### Placeholders to fill in

Search for `todo` in the file. These items need your input:

- LinkedIn URL (hero and contact sections)
- Repository links for RAG-Based AI Career Coach and Multi-Agent Trip Planner

Replace each `<span class="todo">...</span>` with a real link, or delete it.

### Certifications

The certifications section is not included, because the resume marks it "include only if verified". Once you confirm they are yours, add a new `<section id="certifications">` with the certification name, issuer, year and credential link (only if you have one), and add a matching link to the navigation list.

### Resume download

The current build embeds the resume PDF in the page as a base64 string (`RESUME_B64` near the bottom of the file). To update it:

```bash
base64 -w0 Praveen_Resume.pdf   # on macOS: base64 -i Praveen_Resume.pdf
```

Paste the output between the quotes of `RESUME_B64`.

A simpler option for a normal Git repository is to replace the resume button with a plain link and keep the PDF next to `index.html`:

```html
<a class="btn" href="Praveen_Resume.pdf" download>Download resume</a>
```

## Fonts

The page loads Bricolage Grotesque and Public Sans from Google Fonts, with system fonts as fallbacks.

## Testing status

Not yet verified: responsive layouts at each breakpoint, browser-console errors, a keyboard-only walkthrough, color contrast, and the resume download on the final host. Check these after deploying.

## Contact

bissaiahgaripraveenreddy.dev@gmail.com · [GitHub](https://github.com/Praveenkumarreddy12)

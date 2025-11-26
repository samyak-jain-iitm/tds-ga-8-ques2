---
marp: true
title: ProductX Documentation Presentation
author: Technical Writer – 25ds1000058@ds.study.iitm.ac.in
theme: default
paginate: true
---

<style>
/* Custom theme-ish styling (overrides default) */
section {
  background: #020617;
  color: #e5e7eb;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}
h1, h2, h3 {
  color: #38bdf8;
}
a {
  color: #22c55e;
}
code {
  font-size: 0.9em;
  padding: 0.1em 0.2em;
  border-radius: 4px;
  background: rgba(15,23,42,0.9);
}
table {
  width: 100%;
}
th, td {
  padding: 0.25em 0.5em;
}
blockquote {
  border-left: 4px solid #38bdf8;
  padding-left: 0.75em;
  color: #e5e7eb;
  font-style: italic;
}
</style>

<!-- _class: lead -->
<!-- _header: **ProductX Docs** -->
<!-- _footer: ProductX v1.0 – Internal Use Only -->

# ProductX  
# Documentation Presentation

**Technical Writer**  
25ds1000058@ds.study.iitm.ac.in  

> Maintainable, versioned, and exportable documentation for ProductX.

---

<!-- _header: **ProductX Docs** -->
<!-- _footer: Why a Marp-based deck? -->

## Objectives

- Maintain documentation as **Markdown** in version control (Git)
- Reuse content for:
  - Web (HTML GitHub Pages)
  - PDF handouts
  - PowerPoint slide decks
- Keep slides **close to the source docs** to avoid duplication
- Enable **automated builds** via CI/CD

---

<!-- _header: **ProductX Docs** -->
<!-- _footer: Repository layout -->

## Repository Structure

| Path                | Purpose                           |
| ------------------- | --------------------------------- |
| `docs/slides.md`    | Main Marp presentation            |
| `docs/images/`      | Diagrams & screenshots            |
| `docs/themes/`      | Optional custom CSS themes        |
| `package.json`      | Build scripts for Marp CLI        |
| `.github/workflows` | CI to export HTML/PDF/PPTX        |

- Single source of truth in Git
- Reviewable via pull requests
- Easy rollback by tagging releases

---

<!-- _header: **ProductX Docs** -->
<!-- _footer: Build & export with Marp -->

## Build & Export (Marp CLI)

```bash
# HTML for GitHub Pages
marp docs/slides.md -o docs/dist/slides.html

# PDF handout
marp docs/slides.md --pdf --allow-local-files

# PowerPoint deck
marp docs/slides.md --pptx

# Images for marketing or docs
marp docs/slides.md --images png

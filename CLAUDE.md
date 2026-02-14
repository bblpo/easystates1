# CLAUDE.md - AI Assistant Guide for easystates1

## Project Overview

**easystates1** is a static website for Easystates, a data analysis and visualization platform focused on U.S. states data. The site is built with the Nicepage website builder and serves as the web presence for an academic consulting firm specializing in electoral politics, redistricting, and voting rights analysis.

## Tech Stack

- **HTML5 / CSS3 / JavaScript** (no framework, no build step)
- **jQuery 3.5.1** for DOM manipulation
- **Nicepage 3.24.3** - visual website builder framework providing utility-first CSS and interactivity
- **Google Fonts** - Roboto, Open Sans

There is **no package.json, no build system, no bundler, no test framework, and no linter**. This is a pure static site served directly from HTML files.

## Directory Structure

```
/
├── index.html              # Landing page (redirects to Home.html)
├── Home.html               # Homepage with hero section
├── About.html              # Services overview page
├── Contact.html            # Contact page with founder bio
├── Ez-Database.html        # Database product feature page
├── Home.css                # Homepage-specific styles
├── About.css               # About page styles
├── Contact.css             # Contact page styles
├── Ez-Database.css         # Database page styles
├── Blog-Template.css       # Blog listing styles
├── Post-Template.css       # Blog post styles
├── nicepage.css            # Nicepage framework stylesheet (~34K lines, DO NOT edit)
├── nicepage.js             # Nicepage framework JS (bundled, DO NOT edit)
├── jquery.js               # jQuery 3.5.1 (DO NOT edit)
├── blog/
│   ├── blog.html           # Blog listing page
│   ├── post.html           # Post template
│   └── post-1..5.html      # Individual blog posts
└── images/
    ├── Ez5.jpeg            # Logo/brand image
    ├── Liu.jpeg            # Founder portrait
    └── ...                 # Additional images
```

## Key Conventions

### Files to NOT edit
- `nicepage.css` - Auto-generated framework stylesheet (34K+ lines)
- `nicepage.js` - Bundled framework JavaScript
- `jquery.js` - Third-party library

### HTML patterns
- Pages use Nicepage utility classes: `u-section-*`, `u-sheet-*`, `u-text-*`, etc.
- Data attributes configure behavior: `data-image-width`, `data-animation-name`, etc.
- All pages share a consistent header/nav and footer structure
- Structured data (JSON-LD) is embedded for SEO
- Generator meta tag: `<meta name="generator" content="Nicepage 3.24.3, nicepage.com">`

### CSS patterns
- Each page has its own CSS file (e.g., `Home.css` for `Home.html`)
- Utility-first classes from Nicepage framework
- Selectors follow `.u-section-N .u-sheet-N` scoping pattern
- Responsive breakpoints: 1199px, 991px, 767px, 575px

### Navigation structure
All pages link to: Home, About, Ez-Database, Blog, Contact

## How to Run Locally

No build step needed. Serve the files with any static HTTP server:

```sh
python3 -m http.server 8000
# or
npx http-server .
```

Then open `http://localhost:8000` in a browser. The `index.html` redirects to `Home.html`.

## Git Conventions

- Commit messages are short, lowercase descriptions (e.g., `typo`, `update states`, `bio fix`)
- Primary branch: `main` (remote) / `master` (local)

## Domain Context

The site promotes these services:
- **Redistricting Analysis** - Congressional and state-legislative district analysis
- **RPV (Racially Polarized Voting) Analysis** - EI, RxC, ER methods
- **VRA (Voting Rights Act) Analysis** - Gingles II/III analysis
- **Ez Database** - Product with 1000+ variables of longitudinal U.S. state data (hosted at easystates.com)

Founder: Baodong Liu, Ph.D., Professor of Political Science, University of Utah.

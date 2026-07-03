SmartLoans Landing & Legal Pages
===============================

Overview
--------
This project is a single-page web experience for SmartLoans, a peer-to-peer lending marketplace in Mexico.
The `index.html` file contains:

1. Main marketing landing page (home)
2. Privacy Policy page
3. Terms of Use page

All three views are implemented in the same HTML file using a simple page router in JavaScript.

Main Value Proposition
----------------------
SmartLoans connects:
- Acreditados (borrowers)
- Prestamistas (lenders)
- Licenciados en derecho (lawyers)

Key capabilities highlighted in the page:
- Biometric verification (Azure Face API)
- AI-based SmartScore risk model
- Digital contracts and promissory notes
- Legal recovery flow for non-payment cases
- Mobile app availability on iOS and Android

Page Structure
--------------
The document includes three routed sections:

- `#page-home` (active by default)
  - Navigation bar
  - Hero section
  - Trust bar
  - About section
  - 10-step process section
  - User profile cards (borrower/lender/lawyer)
  - SmartScore explanation
  - Legal protection process
  - Technology stack section
  - Download call-to-action
  - Footer with internal links

- `#page-privacy`
  - Full privacy policy (Spanish)
  - Data categories, legal basis, retention, ARCO rights, third-party sharing, security

- `#page-terms`
  - Full terms of use (Spanish)
  - Service scope, user obligations, liabilities, legal jurisdiction

Routing & Navigation
--------------------
Routing is handled with JavaScript functions:

- `showPage(name)`:
  - Hides all `.page` sections
  - Shows target section by id `page-{name}`
  - Scrolls to top
  - Updates browser history path (`/`, `/privacy`, `/terms`)

- `showSection(id)`:
  - Used when returning to home and scrolling to a target section anchor

- `popstate` listener:
  - Handles browser back/forward navigation

- Initial path check:
  - Opens `privacy` or `terms` if URL path matches

Design & Styling
----------------
- Uses custom CSS inside `<style>` tags in `index.html`
- Primary visual identity:
  - Navy/blue palette
  - Accent green/purple/gold
- Responsive behavior via media queries for:
  - 1024px
  - 768px
  - 480px
- Typography:
  - Google Font: Inter

Technology Snapshot
-------------------
- HTML5
- CSS3 (embedded)
- Vanilla JavaScript (embedded)
- No build system or external framework required

External Integrations Referenced
--------------------------------
- Google Fonts
- Apple App Store URL
- Google Play URL
- Azure-based architecture mentioned in content:
  - Azure App Service
  - Azure Face API
  - Azure SQL
  - Azure Blob Storage
  - Notification Hub

Legal & Contact Information in Content
--------------------------------------
Referenced contact emails:
- privacidad@smartloans.mx
- soporte@smartloans.mx
- legal@smartloans.mx

Location:
- Hermosillo, Sonora, México

How to Run Locally
------------------
Option 1:
- Open `index.html` directly in a browser.

Option 2 (recommended for path testing):
- Serve with a local static server, for example:
  - Python: `python3 -m http.server 8000`
  - Then open: `http://localhost:8000`

Notes
-----
- The file currently contains duplicated style blocks for document pages, which still works but could be refactored for maintainability.
- Since all content is in one file, updates to legal text, branding, and links can be done quickly without multi-file coordination.

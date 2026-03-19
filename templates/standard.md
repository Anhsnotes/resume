# Standard Resume Template

ATS-optimized, 2-page resume generated as HTML then converted to PDF via Chrome headless.

## Output Format

- Source: `output/AnhDong_Resume.html`
- Final: `output/AnhDong_Resume.pdf`
- Generation command:
  ```
  "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
    --headless --disable-gpu --no-sandbox \
    --print-to-pdf="output/AnhDong_Resume.pdf" \
    --no-margins --no-pdf-header-footer \
    "file://$(pwd)/output/AnhDong_Resume.html"
  ```

## Page Setup

- Page size: US Letter
- Margins: 0.4in top, 0.5in sides, 0.35in bottom
- Font: Arial, Helvetica, sans-serif
- Base font size: 8.5pt
- Line height: 1.3
- Target length: 2 pages (strict)

## Section Order

1. Name (centered, `<h1>`)
2. Contact line (phone | email | location | LinkedIn)
3. Summary
4. Technical Skills
5. Work Experience
6. Projects
7. Education
8. Certifications & Professional Development

## ATS Optimization Rules

These rules ensure the resume is correctly parsed by Applicant Tracking Systems.

### Headings

- Use standard ATS-recognized section names: Summary, Technical Skills, Work Experience, Education, Projects, Certifications
- Headings use real text in `<h2>` tags — CSS `letter-spacing: 3.5pt` and `text-transform: uppercase` create the spaced-caps visual look
- NEVER manually space out letters (e.g., "W O R K") — ATS reads "W O R K" as separate characters and fails to match

### Name

- Real text `Anh Dong` in `<h1>` — CSS `letter-spacing: 5pt` and `text-transform: uppercase` for visual spacing
- NEVER use `A N H  D O N G` in HTML

### Layout

- Use `<table>` for title/date alignment (job headers, education rows) — universally parsed by ATS
- NEVER use CSS flexbox or grid — many ATS parsers cannot handle them
- Use `page-break-inside: avoid` on job blocks to prevent mid-entry page breaks

### Skills Section

- Comma-separated keywords grouped by labeled category
- Include both abbreviation AND full form: "Retrieval-Augmented Generation (RAG)", "SQL Server Analysis Services (SSAS)"
- 9 categories: Data Engineering, AI & Machine Learning, Databases, Pipeline & Orchestration, Analytics & BI, Infrastructure, Programming, Web Frameworks, Platforms

### Job Entries

- Structure: `<table>` row with title (left) and dates (right), then `<p>` for company, then `<ul>` for bullets
- Dates: spelled-out months ("March 2025" not "03/2025") — more ATS parsers recognize this format
- Company line: Company name, City, State only — no employment type in parentheses
- Bullets: standard `<ul><li>` HTML — NEVER use CSS `::before` pseudo-elements for bullet characters (ATS can't read them)
- Tools/technologies mentioned inline naturally ("using SQL, Alteryx, and Tableau") — NOT in trailing parentheses ("(SQL, Alteryx, Tableau)") since some ATS ignore parenthetical text

### Bullet Writing Rules

- Start with past-tense action verb (present tense for current role)
- Include quantified metric in every bullet where possible (%, $, time saved, headcount)
- Pattern: Action + Context + Quantified Result

### Education

- Same `<table>` layout as jobs for degree/date alignment
- Include degree abbreviation AND full name: "Master of Science in Information Systems (MSIS)"

### Projects

- Include URL on the same line as project name
- Spell out key terms: "Retrieval-Augmented Generation (RAG)", "Open Policy Agent (OPA)"

## CSS Class Reference

| Class | Element | Purpose |
|---|---|---|
| `.contact` | `<p>` | Contact info line |
| `.summary` | `<p>` | Career summary paragraph |
| `.skills-block` | `<p>` | One skill category line |
| `.job` | `<div>` | Wraps entire job entry |
| `.job-line` | `<table>` | Title/date row |
| `.company` | `<p>` | Company, city, state |
| `.project` | `<div>` | Wraps project entry |
| `.project-title` | `<span>` | Bold project name |
| `.edu-line` | `<table>` | Degree/date row |
| `.school` | `<p>` | School name |
| `.note` | `<p>` | Italic note (e.g., "Additional Experience") |

## How to Regenerate

1. Edit `output/AnhDong_Resume.html`
2. Run the Chrome headless command above
3. Verify 2 pages: `mdls -name kMDItemNumberOfPages output/AnhDong_Resume.pdf`
4. If over 2 pages, reduce font-size or line-height — do NOT remove content first

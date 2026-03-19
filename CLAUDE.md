# Resume Craft

A personal knowledge base of work history, skills, and achievements. Claude uses this data to generate tailored, unique resumes for specific job postings.

## Workflow

1. User provides a job posting (URL, text, or key requirements)
2. Claude analyzes the posting for required skills, keywords, and priorities
3. Claude selects the most relevant experience from `data/` and crafts a targeted resume
4. Output follows the format and tone best suited for the role and industry

## Instructions

@.claude/CLAUDE.md

## Project Rules

Modular rules are loaded automatically from `.claude/rules/`:

- **Resume Writing** — `.claude/rules/resume-writing.md`
- **Data Integrity** — `.claude/rules/data-integrity.md`
- **Git Conventions** — `.claude/rules/git-conventions.md`

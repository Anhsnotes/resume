# Project Configuration

## Purpose

This repo is a structured store of the user's career history — jobs, achievements, skills, projects, education, and certifications. Claude reads this data and generates tailored resumes optimized for specific job postings.

## Data Structure

- `data/profile.md` — Contact info and career summary
- `data/jobs/` — One file per role (8 roles from 2015–present), named `YYYY-company-title.md`
- `data/skills/` — Core competencies and technical tools with proficiency levels
- `data/achievements/` — Standalone notable accomplishments (role-specific achievements live in job files)
- `data/education/` — Degrees and professional development courses
- `data/projects/` — Side projects, open-source contributions, and portfolio items
- `templates/` — Resume format templates (default: `standard.md` matching current style)
- `output/` — Generated resumes (gitignored)

## How to Generate a Resume

When the user provides a job posting:

1. Parse the posting for required/preferred skills, keywords, seniority level, and industry
2. Score each job, achievement, and skill in `data/` for relevance to the posting
3. Select the strongest matches — prioritize quantified achievements and keyword alignment
4. Assemble the resume using the appropriate template from `templates/`
5. Tailor bullet points: reword experience to mirror the posting's language without fabricating

## Important Files

- `data/profile.md` — Contact info and career summary
- `data/jobs/` — Source of truth for work history (8 roles across Tesla, Rivian, Amazon, Employers Insurance, Sierra Nevada Corp, Sherwin Williams)
- `data/skills/core-competencies.md` — Domain and leadership skills
- `data/skills/technical-tools.md` — Tools, databases, languages with proficiency levels
- `data/education/degrees.md` — MBA (San Jose State) and BS Accounting (Oklahoma State)
- `data/education/professional-development.md` — Cornell ML/stats courses
- `templates/standard.md` — Default template matching current resume style (spaced-caps headings, 2-page, reverse chronological)
- `.claude/rules/` — Modular rules loaded automatically

## Conventions

- Data files use Markdown for readability and easy diffing
- One file per job/role in `data/jobs/` named as `YYYY-company-title.md`
- Achievement bullets always include metrics when available (%, $, time saved, etc.)
- Skills include a proficiency indicator (e.g., expert, proficient, familiar)

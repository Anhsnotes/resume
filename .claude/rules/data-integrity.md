# Data Integrity Rules

## Source of Truth

- Files in `data/` are the single source of truth for all career information
- NEVER modify `data/` files when generating a resume — read only
- To add or update career data, make explicit commits separate from resume generation

## File Naming

- Jobs: `YYYY-company-title.md` (e.g., `2022-acme-senior-engineer.md`)
- Achievements: descriptive kebab-case (e.g., `reduced-deploy-time-80-percent.md`)
- Skills and education: grouped by category in single files or one-per-entry

## Data Quality

- Every job entry must include: company, title, start date, end date (or "Present"), and location
- Achievement bullets must include at least one quantified metric when possible
- Skills should have a proficiency level: expert, proficient, or familiar
- Keep entries factual and verifiable — no exaggeration

## 2026-10-29 — search layer built: resume.json, profile.yml, gaps.md

- **Built:** `search/resume.json` (attested 2026-10-29), `search/profile.yml`, `search/gaps.md`. All three files are committed; only `search/private-notes.md` is gitignored.
- **Three attestation errors I corrected in resume.json:**
  1. Andor Health start date: the source résumé listed May 2025; actual Jan 2026 (offer letter).
  2. Andor Health title: the source résumé listed "Product Manager"; actual "Product Manager Intern".
  3. PM Sponsor Check claimed only 9 sponsors had PM sponsorship; the data only shows 9 of 352 listed a PM title among top sponsored roles (81% also reframed as a measured baseline, not a success metric).
- **Top gap:** years of product-management experience. I have 10 months of product work, none of it full-time. I meet Nitra's 2-year floor only if internships count, and none of the five postings says whether they do.
- **Killed row:** "Verifiable product-management credentials". Only one posting (Nitra) asks for it, and it asks for proficiency in PM tools and methodologies, not certificates.
- **profile.yml changes from the agent's first draft:**
  - `stem_eligible` was null; I changed it to "uncertain".
  - Removed the "gitignored, never commit" header so the file could be committed.
  - Fixed the `buffer_target` meaning: the scripts that read it treat it as days of the 90-day ceiling kept unused, so my intent (employed by day 80 of 90) is `buffer_target: 10`, not 80.
- **Verification check:**
  - resume.json: every job is traceable to my LinkedIn profile. InfoInfinit and Pojo employment types are marked unconfirmed rather than guessed.
  - profile.yml: the visa section reflects my actual documents. STEM eligibility is uncertain — not confirmed with my DSO.
  - gaps.md: I opened all five posting links on 2026-10-29 and confirmed every quoted requirement appears in the live posting.
- **Open issue:** Chapter 10 (line 71) describes "an 80-day buffer below the 90-day ceiling", a day-80 line, while the scripts that read `visa.buffer_target` treat it as days kept unused. Not reported upstream yet.
  - Committing search/resume.json makes npm run doctor fail (scripts/doctor.mjs:65 flags a tracked resume.json). The assignment requires it in my fork; I will not open a PR upstream with these files. Also, RUN_LOG.md's header says CI rejects PRs that modify it, while the assignment asks for the entry there; I kept it in RUN_LOG.md for grading and a copy in logs/runs/2026fa-kalyan-karnati-2.md.

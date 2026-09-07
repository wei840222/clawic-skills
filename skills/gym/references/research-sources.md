# Gym Research Sources

Verified during the 2026-09-07 `gym` refactor. Use these when citing activity guidelines, progressive overload, protein targets, or recovery defaults.

## Physical activity guidelines

- **WHO Physical activity fact sheet** — Adults should do at least 150–300 minutes of moderate-intensity aerobic activity per week, or 75–150 minutes of vigorous-intensity activity, plus muscle-strengthening on 2 or more days. https://www.who.int/news-room/fact-sheets/detail/physical-activity
- **U.S. Physical Activity Guidelines current guidelines hub** — Federal overview of the current Physical Activity Guidelines for Americans and supporting materials. https://odphp.health.gov/our-work/nutrition-physical-activity/physical-activity-guidelines/current-guidelines
- **CDC Adult physical activity guidelines** — Practical adult guidance aligning with 150 minutes moderate / 75 minutes vigorous weekly activity plus twice-weekly strength work. https://www.cdc.gov/physical-activity-basics/guidelines/adults.html
- **ACSM physical activity guidelines resources** — Professional summary of physical-activity recommendations used by exercise practitioners. https://acsm.org/education-resources/trending-topics-resources/physical-activity-guidelines/

## Progressive overload, volume, and recovery

- **Schoenfeld et al., 2017 (PubMed 28698222)** — Dose-response evidence supporting weekly set volume as a driver of hypertrophy; used to keep beginner/intermediate weekly-set landmarks concrete. https://pubmed.ncbi.nlm.nih.gov/28698222/
- **Schoenfeld et al., 2019 (PubMed 30334597)** — Resistance-training frequency evidence used to keep same-muscle recovery warnings practical rather than absolute. https://pubmed.ncbi.nlm.nih.gov/30334597/
- **BJSM consensus / resistance training overview (57/18/1180)** — Contemporary resistance-training practice framing for load management and progression quality. https://bjsm.bmj.com/content/57/18/1180

## Safety and clinical boundaries

- **NCBI Bookshelf NBK482180** — Clinical context for musculoskeletal assessment and when remote coaching should stop and refer out. https://www.ncbi.nlm.nih.gov/books/NBK482180/
- **MedlinePlus exercise patient instructions index** — Consumer-facing recovery and activity caveats used to keep post-procedure / flare language conservative. https://medlineplus.gov/ency/patientinstructions/000235.htm

## Knowledge updates applied

- Replaced legacy hard-coded home-directory data paths with portable `<state_root>` resolution.
- Kept progressive-overload defaults (+2.5kg / +1-2 reps, ≤10% week-over-week) and 4–6 week deload cadence, grounded in volume/frequency literature rather than brand copy.
- Reframed injury sections from bare prohibitions into higher-risk choices plus concrete substitutes and a safety route.
- Clarified scope against `fitness` (program design), `dietitian`/`nutrition` (meal-level nutrition), and `habits` (attendance streaks).

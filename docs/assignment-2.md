# Assignment 2 - ICU prediction project

Assignment 2 is a separate applied project that builds on the evidence-first
workflow used in the modules. The repository provides the briefing deck and
recording, while the windowed datasets remain in the private distribution
channel approved for the course.

## Assignment package

- [Assignment guide and briefing deck (PDF)](../assignments/assignment-2/ICU_Prediction_Assignment_Briefing.pdf)
- [Editable briefing deck (PPTX)](../assignments/assignment-2/ICU_Prediction_Assignment_Briefing.pptx)
- [Play the assignment briefing online](https://waziz786.github.io/MedML-toolbox/#assignment-2)

Use the briefing deck as the authoritative source for the exact deliverable
wording and submission requirements.

## Recommended workflow

1. Read the briefing deck once before opening the data.
2. Select the prediction window required for the project stage.
3. Define the cohort, prediction time, outcome, and unit of observation.
4. Audit data quality, missingness, class balance, and feature availability
   within that window.
5. Build a reproducible baseline and document preprocessing decisions.
6. Evaluate predictions using more than one metric and explain the operating
   threshold.
7. Record limitations, possible leakage, fairness concerns, and the difference
   between an educational model and a clinical tool.
8. Submit the deliverables listed in the briefing deck.

## Prediction windows

The private assignment package contains one table for each prediction window:

| Window | Private file |
| --- | --- |
| 1 week | `icu24_w1.csv` |
| 6 hours | `icu24_w6.csv` |
| 12 hours | `icu24_w12.csv` |
| 24 hours | `icu24_w24.csv` |

These files contain row-level clinical data and are intentionally not
committed to this public repository. Do not upload them to GitHub issues,
releases, notebooks, or shared links. Keep them in the course-approved private
location and record only the path through local configuration.

## Before submission

- Confirm that the prediction timestamp is earlier than the outcome window.
- Check that every feature would be available at prediction time.
- Keep preprocessing and evaluation inside the training workflow.
- Report the cohort definition, split strategy, metrics, and uncertainty.
- Include a short limitations and clinical-interpretation section.

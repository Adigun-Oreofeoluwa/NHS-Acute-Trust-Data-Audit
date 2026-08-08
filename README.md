# NHS Acute Trust Performance Data Audit

Analysis of performance data across 134 NHS acute trusts, with a focus on
data quality issues affecting reliability of published figures.

## The question
[An independent data quality audit of NHS acute trust performance data across 134 trusts. The goal was to establish whether the dataset was reliable enough to draw meaningful conclusions from before conducting any analysis. Key findings included specialist trusts reporting N/R for metrics that did not apply to them, high variation in Diagnostics over 6 weeks flagged as a likely data collection inconsistency rather than a genuine performance difference, and four trusts consistently below average across six of seven metrics. Documented in a 22-entry audit log and visualised in a four-page Power BI dashboard.]

## Data
Source: [https://www.england.nhs.uk/statistics/statistical-work-areas/ae-waiting-times-and-activity/ae-attendances-and-emergency-admissions-2026-27/], covering [01/2026-02/2026]. [134 rows]
Key Fields:
Trust Code
Trust Name
Region (added via INDEX/MATCH enrichment)
Trust Type (General Acute or Specialist — added during cleaning)
Percentage waiting within 18 weeks for elective treatment (January 2026)
Percentage waiting more than 52 weeks for elective treatment (January 2026)
Cancer Faster Diagnosis Standard (January 2026)
Cancer 62-day Combined Performance (January 2026)
Diagnostics proportion waiting over 6 weeks (January 2026)
A&E 4-hour performance (February 2026)
A&E 12-hour performance — Provisional (February 2026)
Below Average Count (calculated field added during analysis)

## Approach
Cleaned and profiled in Excel, modelled and visualised in Power BI.
Full audit log of issues found: [audit-log.md](audit-log.md)

## Data quality findings
22 issues identified, including [two or three of the most interesting ones]

## Dashboard
![Overview](screenshots/overview.png)
[One line on what this page shows]

## What I'd do differently
[One honest paragraph]

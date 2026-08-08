# Data Quality Audit Log

22 issues found while auditing NHS acute provider performance data
across 134 trusts.

| ID | Issue | Records | Root cause | Action |
|---|---|---|---|---|
ID	Metric / Column	Trust affected	Issue description	Severity	Action taken
AQ-001	All metrics	All trusts	Dataset contains 144 rows but the interactive NHS source table displayed only 118 to 119 trusts. Difference likely due to inclusion of specialist and children's trusts filtered out of the web view. Requires confirmation.	Medium	Noted: no rows removed pending investigation
AQ-002	All metric columns	All trusts	Data covers two different time periods: elective and cancer metrics are January 2026, A&E metrics are February 2026. Time period inconsistency across columns affects direct comparison.	High	Flagged: noted in all analysis as a limitation
AQ-003	A&E 12-hour performance	All trusts	Column is marked "Provisional" in the source file. Figures may be subject to revision and should not be treated as final.	High	Flagged: noted as provisional in analysis
AQ-004	Cancer Faster Diagnosis	Alder Hey Children's NHS Foundation Trust	Trust records 100% for Cancer Faster Diagnosis Standard, a statistical outlier. May reflect small patient volume at a specialist children's hospital rather than a data error. Requires investigation.	Medium	Flagged: to be investigated in analysis phase
AQ-005	Region	All trusts	Regional classification was not available in source files or reference files. The etr.csv reference file contained town-level geography rather than NHS England regional groupings. Region data was manually assigned using secondary knowledge.	Medium	Resolved: manual region mapping applied and verified
AQ-006	Metric counts	Multiple trusts	Provider counts differ across metrics. Some columns show "Rank out of 118" while others show "Rank out of 119." Indicates at least one trust has missing data for certain metrics.	High	Under investigation: blanks check in progress
AQ-007	All percentage columns	All trusts	Percentage sense check completed across all 144 rows and 7 metric columns. No values found outside the 0 to 100% range. Data passes basic boundary validation.	Low	Closed: no action required
AQ-008	Multiple metrics	9 trusts	Nine trusts have 2 missing metric values each. Pattern suggests specialist trusts not operating standard cancer or A&E pathways. Full list to be documented.	Medium	Under investigation
AQ-009	Single metric	4 trusts	Four trusts each have 1 missing metric value. To be investigated whether the same metric is absent across all four or different metrics per trust.	Low	Under investigation
AQ-010	Multiple metrics	Great Ormond Street Hospital For Children NHS Foundation Trust	Three missing metric values. Trust is a specialist paediatric hospital and does not operate standard acute pathways for cancer and emergency care. Missing data is consistent with trust type rather than a reporting failure.	Medium	Flagged: recommend excluding from cross-trust comparisons or treating separately in analysis
AQ-011	A&E 4-hour and 12-hour performance	10 to 11 trusts	A&E metrics have the highest missing data rate in the dataset, significantly higher than elective and cancer metrics. Likely reflects specialist trusts without conventional A&E departments rather than reporting failures. This structural difference means A&E metrics are not comparable across all trusts and should be analysed as a subset.	High	Flagged: A&E analysis to be scoped to reporting trusts only
AQ-012	All metrics	14 trusts	25 blank cells replaced with N/R (Not Reported) to distinguish intentional non-reporting from accidental data gaps. Concentrated in A&E metrics (21 of 25 blanks) consistent with specialist trust profiles.	Medium	Resolved: N/R applied

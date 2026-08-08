# Data Quality Audit Log

22 issues found while auditing NHS acute provider performance data
across 134 trusts.

| ID | Issue | Records | Root cause | Action |
|---|---|---|---|---|
| AQ-001 | Blank cells shown as dashes | 47 | Excel display formatting in source file | Replaced with zeros in Power Query |
| AQ-002 | Provisional figures unlabelled | 12 | Source published before validation | Excluded from trend comparison |

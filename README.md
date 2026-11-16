# Empty Trailer Repositioning in a Shared Trailer Pool

MGSC 404 (McGill, Desautels) – Project 2, Group 4
Micah Green, Henry Huang, Michael Raposo, Sabina Frankova, Elena Hanusova

A carrier shares 96 empty trailers across 24 facilities and 168 shipments over 10 days.
We built a mixed-integer program in Gurobi that decides which empties to move, when,
and with which tractor, at the lowest total cost.

**Result (main file):** $165,705 vs $277,779 for a nearest-empty baseline (40% lower),
mostly by avoiding excess-empty charges at over-full yards. Solved to optimality
(gap 0) over 138,930 candidate tours in under 5 seconds.

## Files
- `MGSC_404_Group_4_Model.ipynb` – data, tour generation, Gurobi model, penalty analysis, baseline
- `MGSC_404_Group_4_Checker.ipynb` – independent feasibility checker and tests
- `MGSC_404_Group_4_Report.pdf` – formulation and results
- `MGSC_404_Group_4_Presentation.pdf` – slides
- `data/` – input workbooks
- `results/` – plans written by the notebooks

## How to run
Requires Python with pandas, numpy, openpyxl and gurobipy, plus a Gurobi licence
(the model is too large for the free pip licence; an academic licence works).
Run `MGSC_404_Group_4_Model.ipynb` first, then `MGSC_404_Group_4_Checker.ipynb`.

# Optimal Office Hours

## Description

Find the optimal walk-in office hours given every student's availability.

- Poll every student's availability using the free online scheduling tool [doodle.com](URL). Export the result as an excel spreadsheet.
- Use `optimal-office-hours.ipynb` to rank every possible combination of office hours based on how many students can attend them.

**Ranking algorithm**: Office hours schedules are first ranked based on the number of students who can attend at least one office hour. In case of tie, the number of students who can attend at least two slots is used. In case of tie, the number of students who can attend at least three slots is used. And so on.

**Caveat 1**: The ranking algorithm only works well if students share every time slot they can in principle attend. If a student only shares their favorite slot, the schedule ends up being built around it.

**Caveat 2**: The computation time grows very quickly with the number of time slots. For example, the algorithm check about 200,000 options to find the best 6 out of 25 potential slots, but about 16,000,000 to find the best 6 out of 50.

## Author

Yaouen Fily

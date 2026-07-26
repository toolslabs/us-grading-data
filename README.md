# US Grading Data

Open, structured data about how grades are calculated in US schools — letter
grade scales, district grading policies, and the standard formulas behind
weighted grades, semester grades, and "what do I need on my final" math.

Maintained by the team behind
**[Final Grade Calculator](https://final-gradecalculator.net/)**, where this
data powers a set of free, private, browser-based grade calculators.

## What's here

| File | Contents |
| --- | --- |
| [`data/letter-grades.json`](data/letter-grades.json) | The standard US letter grade scale: percentage cutoffs and 4.0-scale GPA points for A+ through F |
| [`data/district-policies.json`](data/district-policies.json) | Verified district grading policies (semester weights, final exam weights, category caps), each with a link to the official published source |
| [`formulas.md`](formulas.md) | The grade formulas implemented by our calculators, with worked examples |

## Ground rules for this data

1. **Every district entry cites its official source** — a published policy
   page or student handbook, with the date we accessed it. No folklore.
2. **Cutoffs vary.** The letter scale here is the most common US 4.0 mapping;
   individual schools and instructors set their own cutoffs and rounding
   rules. The syllabus always wins.
3. **Corrections welcome.** If your district's published policy differs from
   an entry here, open an issue with a link to the official source and we'll
   fix it.

## Use this data

Free to use under [CC BY 4.0](LICENSE) — use it in your app, your research,
or your classroom, with attribution to
[final-gradecalculator.net](https://final-gradecalculator.net/).

See the live tools built on this data:

- [Final Grade Calculator](https://final-gradecalculator.net/) — the score you need on your final
- [Grade Calculator](https://final-gradecalculator.net/grade-calculator/) — class grade from categories or points
- [Final Exam Calculator](https://final-gradecalculator.net/final-exam-calculator/) — every final, one plan
- [Weighted Grade Calculator](https://final-gradecalculator.net/weighted-grade-calculator/) — weighted averages done right
- [Semester Grade Calculator](https://final-gradecalculator.net/semester-grade-calculator/) — two terms plus a final

## Roadmap

- University GPA policies (registrar-published grading scales, Latin honors
  thresholds, repeat/replacement rules)
- AP exam score-band estimates with a documented methodology
- More district semester-weight policies

Data is versioned by school year; see releases.

# US grade formulas, with worked examples

The formulas implemented by the calculators at
[final-gradecalculator.net](https://final-gradecalculator.net/). All
percentages are 0–100; weights are the share of the course grade, written as
a decimal (25% = 0.25) unless noted.

## 1. Score needed on a final exam

What you need on the final to end the course at your target grade.

```
Needed = (Target − Current × (1 − W)) ÷ W
```

- `Current` — your grade going into the final
- `W` — the final exam's weight as a decimal
- `Target` — the course grade you want

**Example:** current 87.4%, final worth 25%, target 90%:
`(90 − 87.4 × 0.75) ÷ 0.25 = 97.8` → you need a **97.8%** on the exam.

Edge cases: a result above 100 means the target is out of reach from the
exam alone; a result at or below 0 means the target is already locked in.
Your floor (scoring 0 on the final) is `Current × (1 − W)`.

→ Live tool: [Final Grade Calculator](https://final-gradecalculator.net/)

## 2. Class grade from weighted categories

```
Grade = Σ(category score × category weight) ÷ Σ(graded weight)
```

Only graded categories count: ungraded work is excluded from both sums,
which is how most instructors (and, by default, portals like Canvas) compute
a current grade.

**Example:** homework 92 at 20%, quizzes 84 at 20%, midterm 78 at 30%, final
(30%) not yet taken:
`(92×20 + 84×20 + 78×30) ÷ (20+20+30) = 83.7%` with 30% of the grade still open.

→ Live tool: [Grade Calculator](https://final-gradecalculator.net/grade-calculator/)

## 3. Points-based class grade

```
Grade = Σ(points earned) ÷ Σ(points possible) × 100
```

Points-based syllabi encode their own weights: a 200-point exam simply
outweighs a 40-point quiz five to one.

## 4. Weighted average (general form)

```
Weighted average = Σ(score × weight) ÷ Σ(weight)
```

Weights need not total 100 — only their proportions matter, so credit hours
(3-2-1) work exactly like percentages (50/33/17).

**Example:** scores 92, 84, 78 at weights 20, 30, 50:
`(92×20 + 84×30 + 78×50) ÷ 100 = 82.6%`.

→ Live tool: [Weighted Grade Calculator](https://final-gradecalculator.net/weighted-grade-calculator/)

## 5. Semester grade (two terms + final exam)

```
Semester = T1×W1 + T2×W2 + Exam×W3
```

Under the common 40/40/20 pattern, W1 = W2 = 0.4 and W3 = 0.2. Districts
vary — see [`data/district-policies.json`](data/district-policies.json) for
verified examples.

**Example (40/40/20):** quarters 88 and 91, exam 85:
`0.4×88 + 0.4×91 + 0.2×85 = 88.6%`.

Solved backwards for a target semester grade:

```
Exam needed = (Target − T1×W1 − T2×W2) ÷ W3
```

**Example:** quarters 88 and 91, target 90: `(90 − 35.2 − 36.4) ÷ 0.2 = 92`.

→ Live tool: [Semester Grade Calculator](https://final-gradecalculator.net/semester-grade-calculator/)

---

Letter-grade mapping for all results: [`data/letter-grades.json`](data/letter-grades.json).
License: [CC BY 4.0](LICENSE) — attribution to final-gradecalculator.net.

# Beautiful Dead Ends

A research journal in Jupyter notebooks, exploring mathematical problems that
are easy to state, impossible to solve, and endlessly interesting to think about.

The goal is not to solve these problems. The goal is to understand *why* they
resist solution — what kind of hardness each one has, what the walls look like
up close, and what that tells us about the limits of mathematical reasoning.

---

## The problems

### Collatz Conjecture

Take any positive integer. If it's even, halve it. If it's odd, multiply by 3
and add 1. Repeat. The conjecture says you will always eventually reach 1.

Nobody has proved it. Nobody has found a counterexample. The difficulty turns
out to be about pseudo-randomness and a fundamental gap between what measure
theory can see (almost all integers) and what the conjecture requires (every
integer). There may not be a proof, in the formal sense — the neighbourhood of
this problem contains provably undecidable questions.

| Notebook | Contents |
|---|---|
| `01_collatz_the_problem.ipynb` | The problem stated precisely, sequences visualised |
| `02_collatz_stopping_times.ipynb` | Stopping times, their distribution, the tree structure |
| `03_collatz_known_results.ipynb` | Published results — Terras (1976), the density/universality gap |
| `04_collatz_record_breakers.ipynb` | Delay records, binary structure, visit frequency |
| `05_collatz_synthesis.ipynb` | The three walls: why this problem resists proof |

---

### Hadwiger's Conjecture

Every graph that needs k colours to colour its vertices properly contains a
complete graph K_k as a minor (a structure obtainable by contracting edges).

Stated in 1943. Proved for k ≤ 4 by Hadwiger himself. Proved for k = 5 and
k = 6, but both proofs require the Four Colour Theorem. For k ≥ 7: completely
open. The difficulty is that the proof strategy for k = 5 and k = 6 has no
known analogue beyond k = 6 — the tools ran out.

| Notebook | Contents |
|---|---|
| `hadwiger_01_the_problem.ipynb` | Graph colouring, chromatic number, graph minors defined and implemented |
| `hadwiger_02_minors_in_depth.ipynb` | Branch sets, the Hadwiger number, structure vs minor content |
| `hadwiger_03_proven_cases.ipynb` | Why k=5 and k=6 are equivalent to the Four Colour Theorem |
| `hadwiger_04_computational.ipynb` | Random graph trials, adversarial cases, the Grötzsch graph |
| `hadwiger_05_the_wall.ipynb` | Three walls — and how this hardness differs from Collatz |

---

### Kaprekar's Constant

Take any four-digit number where not all digits are the same. Arrange its
digits in descending order and ascending order. Subtract. Repeat.

You will always reach 6174. Always. In at most seven steps.

This one is included for contrast. The mystery looks real — until you understand
it. Then it dissolves completely: elementary modular arithmetic, a small image,
a unique fixed point. No open problems. The explanation is total.

| Notebook | Contents |
|---|---|
| `kaprekar_01.ipynb` | The phenomenon, the proof, the functional graph, the contrast |

---

## What these problems have in common

They are all easy to state. A child can understand what any of them is asking.

They are all computationally accessible — you can explore them, generate data,
visualise structure, test cases. None of them require advanced machinery to
begin investigating.

And they all eventually run into a wall. The walls are completely different:

- **Collatz:** pseudo-randomness at the individual level; possible undecidability
- **Hadwiger:** proof tools that work up to k=6 and then simply stop
- **Kaprekar:** no wall (included to show what a complete explanation looks like)

The point of this series is to understand the shape of each wall. Not to get
through it.

---

## Running the notebooks

```bash
git clone git@github.com:stetho/beautiful-dead-ends.git
cd beautiful-dead-ends
pip install -r requirements.txt
jupyter notebook
```

Each notebook is standalone — no shared state between them. Run them in any
order, though the numbered sequence within each problem series builds
understanding progressively.

---

## Author

Steve Thompson — [stetho.me](https://stetho.me) | [GitHub](https://github.com/stetho)


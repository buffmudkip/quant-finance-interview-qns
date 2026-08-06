# Quant Finance Interview Questions

Worked solutions to problems from **Xinfeng Zhou — _A Practical Guide to
Quantitative Finance Interviews_** ("the Green Book"), coded up as I read through
the book.

## Notebook

[`quant_finance_interviews.ipynb`](quant_finance_interviews.ipynb) — each problem
comes with a markdown explanation of the reasoning and **one general-purpose
function** that solves every instance (all `n`, arbitrary parameters), not just
the specific numbers in the book.

### Coverage

| § | Theme | Problems |
|---|-------|----------|
| **2.1** | Problem Simplification | Screwy pirates · Tiger and sheep |
| **2.2** | Logic Reasoning | River crossing · Birthday problem · Card game · Burning ropes · Defective ball · Trailing zeros · Horse race · Infinite power tower |
| **2.3** | Thinking Out of the Box | Box packing · Calendar cubes · Door to offer · Message delivery · Last ball · Light switches · Quant salary |
| **2.4** | Application of Symmetry | Coin piles · Mislabeled bags · Wise men |
| **2.5** | Series Summation | Clock pieces · Missing integers · Counterfeit coins · Glass balls |
| **2.6** | The Pigeon Hole Principle | Matching socks · Handshakes · Have we met before? · Ants on a square · Counterfeit coins II |
| **2.7** | Modular Arithmetic | Prisoner problem · Division by 9 · Chameleon colors |
| **2.8** | Math Induction | Coin split · Chocolate bar · Race track |
| **2.9** | Proof by Contradiction | Rainbow hats |
| **3.1** | Differentiation | Reference notes: rules · standard derivatives · applications |
| **3.2** | Integration | Reference notes: FTC · antiderivatives · techniques · applications |
| **3.3** | Partial Derivatives & Multiple Integrals | Reference notes: partial & mixed derivatives · general chain rule · Cartesian→polar · worked Gaussian integral |

§2.3 leans on insight over computation, so its pure *aha* puzzles (Calendar
cubes, Door to offer, Message delivery, Light switches) are written up as prose;
only the problems with real algorithmic content carry code. §2.4 continues that
mix: Coin piles and Wise men carry code, while Mislabeled bags is a one-draw
deduction written up as prose. Every §2.5 problem carries code; each is
generalised to `n` except Clock pieces, whose numbers 1–12 are fixed in place.
§2.6 is entirely prose: it explains the pigeon hole principle (basic and
generalised forms) and applies it to each problem — these are proofs of
inevitability, not algorithms. §2.7 opens with a detailed primer on congruences
and then gives full derivations: Prisoner problem and Chameleon colors carry
solve-for-`n` code, while Division by 9 is a markdown-only proof. §2.8 works the
induction step by step for each problem: Coin split and Race track carry
solve-for-`n` code (and Race track also gives the `O(n)` greedy shortcut), while
Chocolate bar is a markdown-only proof paired with its piece-count shortcut.
§2.9 gives the Rainbow hats problem a plain, step-by-step walkthrough (each
prisoner covers one residue of the colour sum mod `n`, so exactly one is always
right) with a solve-for-`n` function.

Chapter 3 switches from puzzles to a **calculus reference**: §3.1 (differentiation)
and §3.2 (integration) are comprehensive markdown notes — rules, standard tables,
and applications (Taylor expansions, optimisation, expectations of continuous
random variables) — with no code, since the material is formula-centric. §3.3
adds partial derivatives, the general chain rule, and the Cartesian→polar change
of variables, then works the Gaussian integral `∫₀^∞ e^{-x²/2} dx = √(π/2)`.

More sections will be added as I read further.

## Running

```bash
pip install notebook
jupyter notebook quant_finance_interviews.ipynb
```

The notebook uses only the Python standard library.

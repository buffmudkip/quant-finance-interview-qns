# Quant Finance Interview Questions

Worked solutions to problems from **Xinfeng Zhou — _A Practical Guide to
Quantitative Finance Interviews_** ("the Green Book"), coded up as I read through
the book.

## Notebooks

- [`quant_finance_interviews.ipynb`](quant_finance_interviews.ipynb) — **Chapter 2
  brain teasers.** Each problem gets a markdown explanation of the reasoning and,
  where there is algorithmic content, **one general-purpose function** that solves
  every instance (all `n`, arbitrary parameters), not just the book's numbers.
- [`quant_finance_calculus.ipynb`](quant_finance_calculus.ipynb) — **Chapter 3
  calculus.** Comprehensive, formula-centric reference notes (no code): rules,
  standard tables, worked examples, and **use cases** for each method.
- [`quant_finance_probability.ipynb`](quant_finance_probability.ipynb) — **Chapter 4
  probability theory.** Each problem gets an explanation plus a solve-for-`n`
  function, with a Monte-Carlo check where the closed form is subtle.

### Coverage — Chapter 2 · brain teasers (`quant_finance_interviews.ipynb`)

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

### Coverage — Chapter 3 · calculus (`quant_finance_calculus.ipynb`)

Formula-centric reference notes (no code); every method carries some **use cases**.

| § | Topic | Contents |
|---|-------|----------|
| **3.1** | Differentiation | rules · standard-derivatives table · applications — extrema, Rolle, MVT, L'Hôpital, Taylor, Newton, related rates |
| **3.2** | Integration | FTC · antiderivatives table · techniques (u-sub, by parts, partial fractions, trig sub, improper) · applications (geometry, expectations, Gaussian & Gamma, discounting) |
| **3.3** | Partial Derivatives & Multiple Integrals | partial & mixed derivatives (Clairaut, Hessian) · general chain rule · Cartesian→polar · worked Gaussian integral `∫₀^∞ e^{-x²/2} dx = √(π/2)` |
| **3.4** | Important Calculus Methods | Taylor's series (`i^i`, Bernoulli) · Newton's method (`√37`, bisection & secant) · Lagrange multipliers (distance to a plane) |
| **3.5** | Ordinary Differential Equations | separable · first-order linear (integrating factor) · homogeneous 2nd-order (characteristic equation) · non-homogeneous (undetermined coefficients) — worked examples throughout |
| **3.6** | Linear Algebra | correlation as vector angle · eigenvalues/eigenvectors · positive semidefinite / correlation matrices · linear least squares (normal equations + OLS assumptions) · Cholesky & SVD for correlated normals |

### Coverage — Chapter 4 · probability theory (`quant_finance_probability.ipynb`)

Each problem carries a solve-for-`n` function (plus a Monte-Carlo check where useful).

| § | Topic | Problems |
|---|-------|----------|
| **4.1** | Basic Probability Definitions & Set Operations | Coin toss game (→ `1/2`) · Card game (→ `8/17`) · Drunk passenger (→ `1/2`) · N points on a circle (→ `N/2^{N-1}`) |
| **4.2** | Combinatorial Analysis | Poker hands (four-of-a-kind / full house / two pairs) · Hopping rabbit (→ Fibonacci) · Screwy pirates 2 (→ `C(11,5)` locks, `C(10,5)` keys) · Chess tournament (→ `2^{n-1}/(2^n-1)`) · Application letters (derangement → `11/30`) · Birthday problem (→ 23) · 100th digit of `(1+√2)^3000` (→ 9) · Cubic of integer (→ `1/100`) |
| **4.3** | Conditional Probability & Bayes' Formula | Boys and girls (`1/3` vs `1/2`) · All-girl world? (`50%`) · Unfair coin (Bayes → `1024/2023`) · Fair bit from an unfair coin (von Neumann) · Dart game (→ `n/(n+1)`) · Russian roulette series (½ · go 2nd `5/11` · spin · don't spin) |

More sections will be added as I read further.

## Running

```bash
pip install notebook
jupyter notebook quant_finance_interviews.ipynb   # or _calculus / _probability
```

The brain-teaser and probability notebooks use only the Python standard library;
the calculus notebook is all markdown (no execution needed).

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

§2.3 leans on insight over computation, so its pure *aha* puzzles (Calendar
cubes, Door to offer, Message delivery, Light switches) are written up as prose;
only the problems with real algorithmic content carry code. §2.4 continues that
mix: Coin piles and Wise men carry code, while Mislabeled bags is a one-draw
deduction written up as prose. Every §2.5 problem carries code; each is
generalised to `n` except Clock pieces, whose numbers 1–12 are fixed in place.
§2.6 is entirely prose: it explains the pigeon hole principle (basic and
generalised forms) and applies it to each problem — these are proofs of
inevitability, not algorithms.

More sections will be added as I read further.

## Running

```bash
pip install notebook
jupyter notebook quant_finance_interviews.ipynb
```

The notebook uses only the Python standard library.

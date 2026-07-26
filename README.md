# Algebra Calculator

A multi-line algebra and logic calculator that runs entirely in the browser.

**Live:** https://algebra-calculator-tomsekord.vercel.app

Type math the way you'd write it and every line solves as you go. Values you solve for are
remembered, so later lines can build on earlier ones — and earlier lines can even reference
values defined further down, like a spreadsheet.

## Two tabs

**Algebra** — arithmetic, equations, calculus and number theory.

- Exact answers by default: `1/2 + 1/3` gives `5/6`, `√12` gives `2√3`, `25!` gives all 26 digits
- Equations: linear, quadratic, cubic, absolute value, trig (`sin(x)=0.5` → `π/6`),
  exponential and logarithmic (`e^x=10` → `ln(10)`, `ln(x)=1` → `e`)
- Systems of equations across lines, of any size — including cases where one variable is
  already known, redundant equations, and contradictory ones (which are reported as such)
- Calculus: derivatives, definite and indefinite integrals, limits, sums, products, Taylor series
- Number theory: gcd, lcm, mod, floor, ceil, round, sign, nPr, nCr, factorial
- Your own functions (`f(x) = x²`, then `f(3)` or `f'(x)`) and sequences (`a_n = 3+2n`, then `a_5`)
- Domain-restricted questions: `sin(x)=0.5, 0≤x≤2π` answers whether a solution exists in that range

**Logic** — statements that evaluate to True or False.

- Propositions: `A=True`, then use `A` in later lines
- Connectives `∧ ∨ ¬ ⊕ ⊼ ⊽ → ↔` — typing the words `and`, `or`, `not`, `xor`, `implies`, `iff`
  converts them to symbols automatically
- Quantifiers `∃` and `∀` over ℕ, ℤ, ℝ, ℂ or your own set (`L={1,2,3}`)
- Membership tests (`5∈ℕ`) and comparisons (`2(3+4)=14`)

## Modes

- **Exact / Decimal** — keep `√3` as `√3`, or show `1.732050808`
- **Real / Complex** — in Real mode `i` is an ordinary variable; in Complex mode it's the
  imaginary unit, so `√(−1)` is `i` and `e^(iπ)` is `−1`

## Also

On-screen keyboard with a tooltip on every key, a guided tour behind the **?** button,
undo/redo (Ctrl+Z / Ctrl+Y), drag to reorder lines, and a layout that works on phones.

## Running it locally

There's no build step — it's a single HTML file. Open `index.html` in a browser, or serve
the folder:

```bash
python -m http.server 5501
```

then visit http://localhost:5501.

## Deployment

Pushing to `main` deploys to Vercel automatically. The site is also reachable at
`algebra-calculator-zeta.vercel.app`, which is the same deployment under a different alias.

Built with [MathQuill](http://mathquill.com/) for math input, [KaTeX](https://katex.org/) for
rendering, and [math.js](https://mathjs.org/) + [nerdamer](https://nerdamer.com/) for evaluation.

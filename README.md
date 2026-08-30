# Busy Hydra

Busy Hydra, denoted BH(n), is a googological function based on ZFC-definable natural numbers and iterative maximization.

## Author

This definition was created and first published by the author of this repository.  
Contact: [@trirpy](https://t.me/trirpy)

## Definition

Fix a finite alphabet Σ sufficient to encode formulas in the first-order language of set theory.

For each n ∈ ℕ, consider all strings of length n over Σ.

Fix an effective decoding rule that maps strings to first-order formulas. Invalid strings are treated as inadmissible.

An expression E ∈ Σⁿ defines a natural number m if it determines a formula Φ_E(m) such that ZFC proves

∃! m ∈ ℕ : Φ_E(m).

Let

Eₙ = { E ∈ Σⁿ : E defines a natural number }.

Define

M(n) = max { m ∈ ℕ : ∃ E ∈ Eₙ, E defines m }.

If Eₙ = ∅, define

M(n) = 0.

Also set

M(0) = 0.

Because Σ is finite, Σⁿ is finite for every fixed n. Therefore, whenever Eₙ is nonempty, the maximum M(n) exists and is finite.

## Iteration

Define a sequence

L₀ = n,

Lₖ₊₁ = M(Lₖ).

Thus

L₀ = n,
L₁ = M(n),
L₂ = M(M(n)),

and in general

Lₖ = Mᵏ(n).

The construction performs n iterations of M.

## Busy Hydra

The initial number of branches is n.

At level k, each active head produces M(Lₖ) new heads.

The total number of heads, including the initial n heads, is defined by

BH(n) = n + n ∑ (k = 0 to n−1) ∏ (i = 0 to k) M(Lᵢ),

where

L₀ = n,
Lₖ₊₁ = M(Lₖ).

This defines the Busy Hydra function.

## Finiteness

For every fixed n, only finitely many iterations of M are performed.

Since M(n) is finite for every n, the resulting value is finite:

BH(n) < ∞.

## Growth

The main source of growth is the iteration

n → M(n) → M²(n) → ⋯ → Mⁿ(n).

The exact asymptotic growth class of Busy Hydra has not been established.

## Computability

The definition of M depends on provability in the chosen formalization of ZFC.

Questions concerning the computability of M and BH require a separate formal analysis.

No unconditional claim of non-computability is made here without such an analysis.

## Comparison with Busy Beaver

Busy Beaver is a natural function for comparison because both constructions involve maximization over finite sets of descriptions.

However, M(n) and Busy Beaver are defined by different rules.

No exact asymptotic equivalence between BH and Busy Beaver is claimed here.

The conjecture

BH ≍ BB

is only a conjecture and is not presented as a proved theorem.

## Status

Busy Hydra is an original googological function defined by the author of this repository.

The repository serves as a primary public record of the definition and its subsequent revisions.

The mathematical properties stated above are intended to distinguish definitions, proved consequences, and conjectures.

In particular, the comparison

BH ≍ BB

is explicitly a conjecture rather than a theorem.

## Contact

Telegram: [@trirpy](https://t.me/trirpy)

## Revision history

The Git history of this repository records subsequent changes to the definition and documentation

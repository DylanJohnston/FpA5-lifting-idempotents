# Lifting Idempotents from $`\mathbb{F}_pA_5`$ to $`\mathbb{Z}_{(p)}A_5`$

Supplementary code for the paper "[On a question by Roggenkamp about group algebras](https://arxiv.org/abs/2507.21316)", which was joint work with Dmitriy Rumynin.

Let $`\mathbb{F}_p`$ be the prime field of characteristic $`p`$, and let $`\mathbb{Z}_{(p)}`$ denote the localisation of the integers at the prime $`p`$. Let $`A_5`$ be the alternating group on $`5`$ letters. We have $`|A_5| = 60 = 2^2\cdot3\cdot5`$.

Lifting an idempotent $`\overline{e} \in \mathbb{F}_pA_5`$ to $`\mathbb{Z}_{(p)}A_5`$ amounts to finding an element $`e \in \mathbb{Z}_{(p)}A_5`$ such that:
- $`e \equiv \overline{e} \pmod{p}`$
- $`e^2 = e`$

In this repository, primitive idempotents (equivalently, indecomposable projective modules) are lifted from $`\mathbb{F}_pA_5`$ to $`\mathbb{Z}_{(p)}A_5`$ for the "modular primes" $`p = 2`$, $`3`$, and $`5`$.

For each of these primes, there are three indecomposable projective modules to lift. The process of lifting them is as follows:
- Identify primitive idempotents in $`\mathbb{F}_pA_5`$,
- Lift these primitive idempotents to the group ring over the $`p`$-adic integers $`\widehat{\mathbb{Z}_p}A_5`$.
- Check that all coefficients in the lift to $`\widehat{\mathbb{Z}_p}A_5`$ have $`p`$-adic expansions with repeating digits, i.e., the coefficients lie in $`\mathbb{Z}_{(p)} \subset \mathbb{Q}`$.

Details can be found in the following notebooks:
- [idempotent-lift-F_2A_5.ipynb](https://github.com/DylanJohnston/FpA5-lifting-idempotents/blob/main/idempotent-lift-F_2A_5.ipynb)
- [idempotent-lift-F_3A_5.ipynb](https://github.com/DylanJohnston/FpA5-lifting-idempotents/blob/main/idempotent-lift-F_3A_5.ipynb)
- [idempotent-lift-F_5A_5.ipynb](https://github.com/DylanJohnston/FpA5-lifting-idempotents/blob/main/idempotent-lift-F_5A_5.ipynb)

All three notebooks follow a similar structure. In fact, the $`p = 3`$ case was completed first, and the others are copies of it with the relevant modifications. This approach results in heavy code repetition, but in return, each notebook is fully self-contained. This was deemed to be worth it.

# EM Algorithm Lab

An interactive study guide for §8.7 of Kevin P. Murphy, *Probabilistic Machine Learning: An Introduction*
(bound optimization and the EM algorithm; §8.7.3.4 MAP estimation and §8.7.3.5 nonconvexity omitted).

**Live:** https://isaackrallison.github.io/em-algorithm/

Every section has an **Explain it** box at four levels (Kid, High school, Undergrad, Grad / MLE), switchable globally from the top bar.

- **8.7.1 Bound optimization (MM):** climb a quadratic minorizer on a bumpy objective, step by step. Push the bound's curvature below the safe value to watch it poke through and break the guarantee, and compare it with Newton's method overshooting or going downhill (Figures 8.23–8.24).
- **8.7.2 The EM algorithm:** Figure 8.23 for real. A 1-D mixture where θ = μ₁, with separate E and M buttons. The E step draws a bound that touches ℓ, and the M step climbs it and opens a KL gap. The objective has two peaks, so you can see EM stop at a local maximum.
- **8.7.2.1 Lower bound:** Jensen's inequality on the log curve, and how it yields the ELBO.
- **8.7.2.2 E step:** one data point, a guess q, and ELBO(q) = log p(y|θ) − KL. The gap closes exactly at the posterior.
- **8.7.2.3 M step:** draggable 1-D data with responsibility bars. The M step objective peaks at the weighted mean, with a table of expected sufficient statistics.
- **8.7.3 EM for a GMM:** Old Faithful with the book's initialization. Separate E and M steps, jump-to-iteration (Figure 8.25), per-point E step arithmetic on hover, draggable initial means, and an "inject a bug" toggle that breaks monotonicity.
- Step-by-step math breakdowns, a 30-question quiz tagged by level, and a cheat sheet.

Single self-contained `index.html`, no build step. Loads Google Fonts and MathJax from cdnjs.

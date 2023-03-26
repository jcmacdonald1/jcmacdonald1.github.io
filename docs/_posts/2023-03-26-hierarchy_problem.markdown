---
layout: post
title:  "The hierarchy problem, and what to do about it - Part I"
date:   2023-03-26
categories:
---
According to the Wikipedia [article][wiki-unsolved-problems] that lists the unsolved problems in physics, the hierarchy problem can be posed as the question <em>"What prevents quantities at the electroweak scale, such as the Higgs boson mass, from getting quantum corrections on the order of the Planck scale?"</em>[^1]. So what does this mean, and is it really correct to consider this a "problem" at all?

[^1]: The hierarchy problem is sometimes posed as the related question <em>"Why is gravity such a weak force?"</em>. The more technical formulation above is what I believe most particle physicists mean when they talk of the hierarchy problem, and so will be the focus of this article.

I would like to present the hierarchy problem in a couple of ways, starting in this post with the usual (confusing) textbook formulation. This will be followed in a future post with a more careful treatment that really gets to the heart of the issue. In both cases I will consider real scalar fields for simplicity, but the same arguments apply to the Higgs doublet in the Standard Model.

<h1>Confusing textbook argument</h1>
The usual argument goes something like this. Consider a massive scalar field theory with Lagrangian

$$\mathcal{L} = \frac{1}{2}(\partial\phi)^2 - \frac{1}{2}m\phi^2 - \frac{\lambda}{4!}\phi^4.$$

The measured mass parameter $$m^2_{\mathrm{phys}}$$ is given by the pole of the propagator, which at leading order is simply $$m^2$$. So far so good. What happens if we compute $$\mathcal{O}(\lambda)$$ quantum corrections? The propagator changes to

$$\frac{1}{p^2 - m^2} \rightarrow \frac{1}{p^2 - m^2 + \Pi(p^2)},$$

where $$\Pi(p^2)$$ contains the $$\mathcal{O}(\lambda)$$ quantum corrections. The new pole position is then at $$m^2_{\mathrm{phys}} = m^2 - \Pi(m^2_{\mathrm{phys}})$$. The two 1PI diagrams that contribute at leading order are shown in Fig. X. In momentum space, the second diagram gives a correction

$$-\frac{\lambda}{2}\int_{|p|\leq\Lambda_0}\frac{d^4p}{(2\pi)^4}\frac{1}{p^2+m^2} \approx -\frac{\lambda}{32\pi^2}\Lambda_0^2,$$

where we have chosen to integrate up to some high-energy cutoff $$\Lambda_0\gg m$$, and have neglected the subdominant logarithmic term. We can then write

$$m^2_{\mathrm{phys}} = m^2 + \frac{\lambda}{32\pi^2}\Lambda^2_0.$$ 

So then, we computed the quantum corrections, and find that they are quadratic in $$\Lambda_0$$. This is presumably some large scale on the order of the Planck scale. But we observe that $$m_{\mathrm{phys}} \sim 125\,\mathrm{GeV}$$, so that means there must be some very delicate cancellation happening between $$m^2$$ and the quantum corrections to make the measured value come out so small. This is the hierarchy problem!

At least this is how the story usually goes. But I don't find it very convincing. For a start, what is $$m^2$$ anyway? Surely this is just an <em>unobservable</em> parameter in the Lagrangian, whose value is essentially arbitrary. In fact, we often treat $$m^2$$ as being infinite, and use it to absorb divergences, such as those that would arise in the $$\Lambda_0 \rightarrow \infty$$ limit. Usually this is done by introducting counterterms $$m^2 \rightarrow m^2 + \delta m^2$$, where by a careful choice of $$\delta m^2$$ it is even possible to make $$m^2 = m^2_{\mathrm{phys}}$$. At this point it is really not clear what the actual "problem" is.

Furthermore, it should be noted that we used a cutoff in the above treatment, but of course other renormalisation schemes exist. What happens in dimensional regularisation? In the $$\overline{\mathrm{MS}}$$ scheme we find

$$m^2_{\mathrm{phys}} = m^2 - m^2\frac{\lambda}{32\pi^2}\left[\ln\left(\frac{\mu^2}{m^2}\right)+1\right],$$

where now $$m^2 = m^2(\mu^2)$$ becomes a function of the arbitrary scale $$\mu$$. There are no remaining divergences in this expression, and no quadratic dependence on a large energy scale. It seems like the hierarchy problem has disappeared simply by changing renormalisation scheme.

So what is going on here? To properly understand the hierarchy problem, we should consider what would happen if there were additional heavy degrees of freedom in our theory, and apply the tools of effective field theory. This will be the subject of the next part in this series.

[wiki-unsolved-problems]: https://en.wikipedia.org/wiki/List_of_unsolved_problems_in_physics
[aqft-notes]: https://www.damtp.cam.ac.uk/user/dbs26/AQFT/chap5.pdf
[eft-matching-notes]: https://indico.in2p3.fr/event/22195/contributions/86017/attachments/59873/81148/eftlectures.pdf

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
# nzmodes
Latex description of the method used to sample over the n(z) coefficients.

The general situation is: you wish to run Markov chains to sample some Bayesian probability $p(q,s | D) \propto \mathcal{L}(D | q,s) p(q) p(s)$ where $D$ are some data, $q$ are some parameters of interest, and $s$ holds a fairly large number of nuisance parameters.  The prior $p(s)$ on the nuisance parameters is not known explicitly, however, it is only realized as samples from the distribution, i.e.\ from a previous Markov chain.  How can one do this?

The method described here is to use the samples to create a linear compression of the long nuisance-parameter vector $s$ into some smaller vector $u$, by ignoring directions that do not alter the likelihood of the data.  Standard density estimators can then be used to create $p(u).$

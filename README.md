# Approximating-optimal-SMC-proposal-distributions-in-individual-based-epidemic-models
Many epidemic models are naturally defined as individual-based models: where we track the state of each individual within a susceptible population. Inference for individual-based models is challenging due to the high-dimensional state-space of such models, which increases exponentially with population size. We consider sequential Monte Carlo algorithms for inference for individual-based epidemic models where we make direct observations of the state of a sample of individuals. Standard implementations, such as the bootstrap filter or the auxiliary particle filter are inefficient due to mismatch between the proposal distribution of the state and future observations. We develop new efficient proposal distributions that take account of future observations, leveraging the properties that (i) we can analytically calculate the optimal proposal distribution for a single individual given future observations and the future infection rate of that individual; and (ii) the dynamics of individuals are independent if we condition on their infection rates. Thus we construct estimates of the future infection rate for each individual, and then use an independent proposal for the state of each individual given this estimate. Empirical results show order of magnitude improvement in efficiency of the sequential Monte Carlo sampler for both SIS and SEIR models. 
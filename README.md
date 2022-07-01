# CoauthorshipsLPM

__Data__ and __latent position modelling results__ for a coauthorship network on the topic _latent position modelling_.

The raw data was downloaded from __Scopus__ on 22nd January 2022. It consists of all the Scopus entries that cite Hoff, P. D., Raftery, A. E., & Handcock, M. S. (2002). _Latent space approaches to social network analysis._ __Journal of the American Statistical Association__, 97(460), 1090-1098.

We cleaned these data to correct for duplicate names appearing due to middle names.

Then, we constructed a __network of coauthorships__ between all those individuals with _at least two publications_.

Thus, any two individuals are connected with an edge if and only if:

- they appear in at least one bibliographic entry together;

- they appear independently in at least two bibliographic entries.

The resulting network is _binary_ and _undirected_, and it is stored in the file __data_coauthorships_lpm.RData__.


After this, we used the __R__ package __latentnet__ to fit a basic _latent position model_, a _latent position clustering model_, and a _latent position clustering model with random effects_. Model choice for the number of dimensions and for the number of clusters was performed using the BIC criterion implemented in __latentnet__. The fitting algorithm was run with default parameter values.

The results for each model fitting are available from the folder '/results'. The results are provided as an __RData__ file, in __pdf__, and in __html__ format.


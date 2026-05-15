Abstract—Named Entity Recognition (NER) for low-resource
languages remains challenging because modern neural architec-
tures require large annotated corpora that are unavailable for
most languages. Bengali, the seventh most spoken language with
over 230 million native speakers, is still severely under-resourced
for NER tasks. This paper investigates whether structured
probabilistic models, particularly Conditional Random Fields
(CRFs), can remain competitive with deep neural approaches
under extreme data scarcity. We propose a Latent Morphology
CRF that models morphological segmentation as a latent variable
and jointly learns Bengali suffix distributions with NER through
Expectation-Maximization (EM), without requiring explicit mor-
phological annotations. We evaluate four model families—Basic
CRF, Latent Morph CRF, BiLSTM, and multilingual BERT
(mBERT)—across six training subsets ranging from 1% to 100%
of the WikiANN Bengali corpus. Experimental results show that
CRF-based models outperform neural baselines in extremely
low-resource settings. At 1% training data, the BiLSTM model
collapses entirely (F1 = 0.000), whereas the Latent Morph CRF
achieves an F1-score of 0.509. A performance crossover occurs
at approximately 10% training data, beyond which mBERT
becomes dominant, achieving an F1-score of 0.947 using the full
dataset. An ablation study further reveals that contextual features
contribute most significantly to performance (F1 drop = 0.032),
while morphological features provide modest but consistent
improvements. These findings establish practical data-threshold
guidelines for developing Bengali NER systems under resource-
constrained conditions.

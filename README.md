# Age of Exposure 2.0: Estimating word complexity using Iterative Models of Word Embeddings
This repository contains the training and inference code for the "Age of Exposure - Word Learning using Iterative Models of Word Embeddings" paper.

Not included:
- The "Touchstone Applied Science Associates, Inc." corpus
- The "Corpus of Contemporary American English" corpus
- The Childes Child-Directed Speech corpora (https://childes.talkbank.org/)

Included:
- *train_models.py*: trains incremental Word2Vec models
- *compute_indices.py*: computes word indices used for predicting AoE scores
- *evaluate_aoa.py*: evaluates models using a set of indices
- *generate_aoe_v2_predictions.py*: trains using AoA norms and runs inference on the entire corpus vocabulary
- **run_experiment.sh**: calls all scripts in order, given a quantiles file and an experiment name

## Environment set-up
Install Anaconda: https://www.anaconda.com/products/individual
And load the environment from the yml file:

```bash
conda env create -f environment.yml
```

Then you can activate the environment:
```bash
conda activate age_of_exposure_v2
```

And download other necessary resources:
```bash
python -m spacy download en_core_web_lg
```

## License

Apache 2.0. Please review the "LICENSE" file in the root of this directory.

## Contact
Please contact us through the emails listed on the papers in the references section.

## Resources
- resources/AoEv1.csv: the indices from the AoE 1.0
- resources/predicted_AoE2_vocab_sorted_linear_rf_tasa_coca_cds.csv: predicted AoA scores for the best performing model in AoE 2.0

## References
Dascalu, M., McNamara, D., Crossley, S., & Trausan-Matu, S. (2016, March). Age of exposure: a model of word learning. In Proceedings of the AAAI Conference on Artificial Intelligence (Vol. 30, No. 1).

Botarleanu, R. M., Dascalu, M., Watanabe, M., McNamara, D. S., & Crossley, S. A. (2021, June). Multilingual Age of Exposure. In International Conference on Artificial Intelligence in Education (pp. 77-87). Springer, Cham.

To be added: AoE 2.0
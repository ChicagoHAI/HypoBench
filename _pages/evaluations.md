---
layout: page
permalink: /evaluations/
title: Evaluation Methods
---

### Utility-driven Evaluation
We evaluate the generated hypotheses by assessing how well they help language models make predictions on various classification tasks. The hypotheses are used to guide the models in making predictions, and the performance (accuracy) of the models is measured to determine the utility of the hypotheses.

- **Classification Tasks**: We use the hypotheses to help language models make predictions on test examples. After seeing all the generated hypotheses, The models first identify the most relevant hypotheses for each example and then use those hypotheses to make a prediction.
- **Data Splits**: We test on both in-distribution (IND) datasets and out-of-distribution (OOD) datasets. This helps us understand how well the hypotheses generalize to new scenarios.

The focus of our evaluation is on how well the hypotheses perform in unfamiliar or new contexts, as this reflects their ability to generalize beyond the data they were generated from.

### Ground Truth Hypothesis Discovery 
For the synthetic datasets, we evaluate the generated hypotheses by comparing them to the ground truth hypotheses. We measure the similarity between the generated hypotheses and the ground truth hypotheses to determine how well the hypothesis generation methods can discover the true underlying patterns in the data.
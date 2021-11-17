# Algorithm Evaluation

We evaluated the rule generation algorithm from two aspects:

(1) we test whether the generated rules performs consistently in terms of **completeness**(coverage) and **parsimony**(complexity) with the change of user-defined parameters and whether the algorithm has a good time performance to be used in an interactive system.

(2) we compare the proposed surrogate rule set generation method with the widely used surrogate decision tree method in terms of the complexity of the rules and the completeness of the data the rules can cover when we fix the threshold of fidelity and number of features in a rule.

For all the experiments, we first train a black-box classification model as the model to be explained (to be approximated). Then we run experiments as described above.

You can find all the model training code in the folder `black_box_model_training/` where we also include the datasets used for model training. The description of datasets and model we trained is below:

| Data              | num_instance     | num_feature    | num_class    | Model | Accuracy |
| ----------------- | ---------------- | -------------- | ------------ | ----- | -------- |
| crime             | 1595             | 100            | 2            | MLP   | 83.5%    |
| diabetes          | 1000             | 7              | 2            | MLP   | 75.5%    |
| dry bean          | 10888            | 15             | **<u>7</u>** | SVM   | 93.1%    |
| income            | <u>**12545**</u> | 5              | 2            | SVM   | 76.5%    |
| loan              | 6317             | 21             | 2            | SVM   | 73.6%    |
| penn music origin | 874              | **<u>117</u>** | 2            | MLP   | 80.7%    |
| obesity level     | 1688             | 15             | **<u>7</u>** | MLP   | 83.0%    |
| penn cpu          | 6553             | 20             | 2            | MLP   | 81.9%    |
| penn satelitte    | 5148             | 35             | 2            | MLP   | 85.6%    |
| penn wind         | 5259             | 13             | 2            | MLP   | 83.2%    |


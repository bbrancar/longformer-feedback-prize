# Longformers for Argument Classification

In this repo, our team employed transformer-based architectures to classify argumentative elements of students’ writing is analysed. This task is originally based on the [Feedback Prize Kaggle](https://www.kaggle.com/c/feedback-prize-2021/) competition. The task involves segmenting writing into argumentative and rhetorical elements and classifying a test set based on classes determined by professional annotators.

The project involves employing transformers capable of classifying long strings of text. We employed Allen AI's Longformer, a transformer whose dialated attention mechanism can perform classification on longer strings.

For more information about Longformers, check out this awesome [paper](https://arxiv.org/abs/2004.05150) by [Iz Beltagy](https://arxiv.org/search/cs?searchtype=author&query=Beltagy%2C+I), [Matthew E. Peters](https://arxiv.org/search/cs?searchtype=author&query=Peters%2C+M+E), [Arman Cohan](https://arxiv.org/search/cs?searchtype=author&query=Cohan%2C+A).

## How to run the model

The dataset, downloaded from the Kaggle [site](https://www.kaggle.com/competitions/feedback-prize-2021/data), consists of a csv with labeled training data along with a folder of original essays. Given that the user has the `train.csv` file and the folder containing the accompanying essays, the following line will be enough to train and run the model with the default configuration.

    python main.py

The user can freely experiment with the parameters under the experiment group of `default.json` file. These hyperparameters include batch size, learning rate, gradient norm, maximum tokenization length etc.

Alternatively, the users can create their own .json file, following a similar architecture to `default.json`. In that case, the user should run the following command:

    python main.py your_own_json_file.json

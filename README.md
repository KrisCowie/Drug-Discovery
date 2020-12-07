# Drug-Discovery
## Using Neural Networks to help with idenfying mechanisms of action in chemicals.
With this project, I wanted to take a look at the drug discovery pipeline, and see if neural networks could be used to make initial discovery and development more efficient
There was a concurrently running competition at Kaggle here : https://www.kaggle.com/c/lish-moa
There are four notebooks:
  1) Exploratory Data Analysis
  2) Feature Engineering
  3) Preprocessing
  4) Running the Neural Network

I wanted to use a neural network architecture I hadn't before, and after much reading, came across TabNet, a new type of DL architecture from Google researchers.

Their initial paper is here: https://arxiv.org/abs/1908.07442

The problem we're trying to solve is how to label novel drugs by what they do.

So most drugs are either some type of agonist, or antagonist, i.e. an inhibitor, or an activator.

When discovering new drugs, typically companies will take batches of human cells, and subject them to the novel chemicals, and record the genes and cell viability through genetic and cell assays.

The dataset linked above in the Kaggle competition is novel in that it a) combines these steps into one - where they test for the activation of genetic pathways at the same time as testing for cell viability, and 2) Tests batches of 100 different human cells at a time

This solves two major problems - trying to identify what human cells the chemical will work on prior to actually knowing what it will do, and checking the activation and toxicity of the drugs across a wide range of potential interactions. Something like 60% of drugs are ejected from the pipeline when they're discovered to have side effects which make them unusable. This use of genetic and cell assays should alleviate that.

So the actual dataset is 100 different cell viability features, along with 772 different genetic expression assay features.

Which makes the dataset highly tabular, and a perfect candidate for using this new Tabnet architecture on.

Check out the presentation if you'd like to learn more, and the notebooks should also be enlightening.

The TabNet architecture, and some serious feature engineering and preprocessing turned out to be an excellent approach to solving this problem

In the future, it would be good to expand the dataset on which this network was trained, as several classes of drugs had limited numbers of records

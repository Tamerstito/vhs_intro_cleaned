Intro to Deep Learning — Exercise Series

Project Overview
This folder gathers the four practical notebooks I completed for Kaggle’s Intro to Deep Learning micro‑course. Each notebook built on the last to move from a single neuron to multi‑layer neural networks and optimisation techniques:
exercise‑a‑single‑neuron.ipynb – Implemented a 1‑layer dense model to learn a simple linear relationship.
exercise‑stochastic‑gradient‑descent.ipynb – Explored how batch size and learning rate affect convergence using SGD.
exercise‑overfitting‑and‑underfitting.ipynb – Demonstrated regularisation (dropout, weight decay) and early stopping.
exercise‑deep‑neural‑networks.ipynb – Constructed a deep feed‑forward network and improved accuracy on the Fashion‑MNIST dataset.

Technologies Used
Core deep‑learning API: TensorFlow 2 / Keras
Data manipulation: pandas, numpy
Model evaluation: scikit‑learn (train‑test split, metrics)
Visualisation: matplotlib

How I Ran the Notebooks
Opened each exercise notebook in Kaggle.
Executed cells sequentially, filling in code for TODO sections, then submitted for auto‑grading.

Challenges Faced & What I Learned
Vanishing gradients – Early deep models with relu activations stalled; switching to he_normal weight initialisation improved training speed.
Overfitting – Small datasets quickly over‑fit; I applied dropout (0.2–0.3) and monitored validation loss with EarlyStopping patience = 3.
Hyper‑parameter intuition – Hands‑on plots of learning curves clarified how batch size and learning rate trade‑off training stability and speed.

Future Improvements
Try Batch Normalisation between dense layers to stabilise activations.
Port the workflow to PyTorch for comparison and practice.
Experiment with Cyclical Learning Rates to potentially reach better minima.
Extend to CNN layers for image data and explore transfer learning from pre‑trained models.
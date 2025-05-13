Handwritten Digit Recognition — Dense NN & CNN Comparison
========================================================

Project Overview  
This notebook revisits the MNIST dataset. I first retrained the fully connected network used in the earlier hand‑written‑digit exercise and saved its weights. I then built a compact two‑layer convolutional network that keeps the 28 × 28 image grid intact. Both models are trained for ten epochs in Google Colab, evaluated on the official test set, and the weight files are saved for future inference.

Files in this folder  
mnist_digit_recognition_cnn_<your_last_name>.ipynb – the Colab notebook with code, comments, and results  
mnist_nn.weights.h5 – weights for the dense network trained with Adam  
mnist_cnn.weights.h5 – weights for the convolutional network  
(Optionally) mnist_nn_sgd.weights.h5 – weights for the dense network trained with plain SGD  

Technologies Used  
TensorFlow / Keras for modelling and training  
NumPy for array manipulation  
Matplotlib for quick image checks  
Colab GPU (T4) for hardware acceleration  

How to run the notebook  
Open the .ipynb file in Colab, turn on a GPU runtime, and run all cells from top to bottom. The notebook will write the two .h5 files in the same folder. To reload a model later, recreate the matching architecture and call model.load_weights(<file_name>).

Main results and observations  
Dense network with Adam finishes around 98 % test accuracy and carries roughly 243 k trainable parameters.  
The same dense architecture with SGD ends a little lower, about 97 % accuracy, reflecting slower convergence in the same epoch budget.  
The CNN needs only 34 k parameters but reaches about 99 % accuracy on both validation and test splits. Training each epoch takes longer than the dense runs, yet the final loss is much lower and the validation–test gap is minimal, suggesting better generalisation.

Future work  
Add early‑stopping to cut unnecessary CNN epochs.  
Try simple data augmentation (random shifts or small rotations) to see if the dense model can improve.  
Convert the CNN to a TensorFlow Lite model for lightweight deployment.
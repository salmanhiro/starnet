Required packages:
- numpy
- h5py
- random
- Keras (1 or 2)
- Tensorflow or Theano (backend for Keras)
- Matplotlib 
- Seaborn
- sklearn
- vos
- jupyter

command line:

```
pip install numpy
pip install h5py
pip install matplotlib 
pip install seaborn
pip install sklearn
pip install keras
pip install tensorflow
pip install vos
pip install jupyter
```

Create a CADC account here [url]

```
git clone [above github link]
cd starnet
getCert
```

enter your CADC account information

```
jupyter notebook
```
A new browser tab should pop up, if not, copy and paste the given link into your in your browser.

Before starting any of the other notebooks, be sure to read through 1_Download_Data.ipynb to find out what data you need for which notebooks. Not all of the available data is completely necessary depending on where you would like to begin, but reading through the notebooks will provide a more complete understanding of the necessary steps taken when creating a neural network model.

Below is a description of the available notebooks:

1_Download_Data.ipynb
- provides descriptions of all of the available data, where the data is necessary, and the scripts needed to download the data
- files available for download in this notebook: apStar_visits_main.h5, apStar_combined_main.h5, high_snr_test_apids.npy, training_set.h5, mean_and_std.npy, high_snr_test_data.h5, low_snr_test_data.h5

2_Preprocessing_of_Training_Data.ipynb
- step by step preproceprocessing of the training data to create a training set
- required files to run this notebook: apStar_visits_main.h5
- files created in this notebooks: high_snr_test_apids.npy and training_set.h5

3_Preprocessing_of_Test_Data.ipynb
- step by step preproceprocessing of test data to create two test sets
- required files to run this notebook: apStar_combined_main.h5 and high_snr_test_apids.npy
- files created in this notebooks: mean_and_std.npy, high_snr_test_data.h5 and low_snr_test_data.h5

4_Train_Model_Keras_1.ipynb
- building model architecture, setting hyper-parameters, and training model using Keras 1
- required files to run this notebook: mean_and_std.npy and training_set.h5
- files created in this notebooks: Model_0.h5

4_Train_Model_Keras_2.ipynb
- building model architecture, setting hyper-parameters, and training model using Keras 2
- required files to run this notebook: mean_and_std.npy and training_set.h5
- files created in this notebooks: Model_0.h5

4_Train_Model_Keras_1_Simple.ipynb
- IMPORTANT: if you are limited to simple computing resources, use this notebook instead of 4_Train_Model_Keras_1.ipynb
- this notebook is identical to 4_Train_Model_Keras_1.ipynb but uses fewer training examples and more iterations
- required files to run this notebook: mean_and_std.npy and training_set.h5
- files created in this notebooks: Model_0.h5

4_Train_Model_Keras_2_Simple.ipynb
- IMPORTANT: if you are limited to simple computing resources, use this notebook instead of 4_Train_Model_Keras_2.ipynb
- this notebook is identical to 4_Train_Model_Keras_2.ipynb but uses fewer training examples and more iterations
- required files to run this notebook: mean_and_std.npy and training_set.h5
- files created in this notebooks: Model_0.h5

5_Test_Model.ipynb
- obtain model predictions for the test sets and plot the results against ASPCAP DR12 labels
- required files to run this notebook: mean_and_std.npy, high_snr_test_data.h5, and low_snr_test_data.h5

6_Error_Propogation.ipynb
- obtain model statistical errors for a test set predictions
- required files to run this notebook: mean_and_std.npy, a test set of your choice, apStar_combined_main.h5

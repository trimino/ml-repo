# Description of UCI Datasets

The files in the UCI datasets directory contain training files and test files for three datasets. Both the training file and the test file are text files, containing data in tabular format. Values are separated by white space. With the EXCEPTION of the last column, the i-th row and j-th column contain a number, which is the value for the j-th dimension of the i-th object. The LAST column stores a string, which is the class label for each object. **Make sure you do not use data from the last column (i.e., the class labels) as parts of the input vector.**

The datasets are copied from the UCI repository of machine learning datasets. Note that some datasets may have a "numerical label" version and a "string label" version. The only difference between the two versions is that class labels are represented by numbers in the "numerical" version and by non-numerical strings in the "string" version. Here are some details on each dataset:

- The pendigits dataset. This dataset contains data for pen-based recognition of handwritten digits.
  - 7494 training objects, stored at pendigits_training.txt.
  - 3498 test objets, stored at pendigits_test.txt
  - 16 dimensions.
  - 10 classes.
  - There is also a "string label" version of this dataset, stored at pendigits_string_training.txt and pendigits_string_test.txt.

- The satellite dataset. The full name of this dataset is Statlog (Landsat Satellite) Data Set, and it contains data for classification of pixels in satellite images.
  - 4435 training objects, stored at satellite_training.txt.
  - 2000 test objets, stored at satellite_test.txt.
  - 36 dimensions.
  - 6 classes.
  - There is also a "string label" version of this dataset, stored at satellite_string_training.txt and satellite_string_test.txt.

- The yeast dataset. This dataset contains some biological data whose purpose I do not understand myself.
  - 1000 training objects, stored at yeast_training.txt.
  - 484 test objets, stored at yeast_test.txt.
  - 8 dimensions.
  - 10 classes.
  - There is also a "string label" version of this dataset, stored at yeast_string_training.txt and yeast_string_test.txt.

For each dataset, a training file and a test file are provided. The name of each file indicates what dataset the file belongs to, and whether the file contains training or test data.

Note that, for the purposes of your assignments, it does not matter at all where the data come from. The methods that you are asked to implement should work on all three datasets, as well as ANY other datasets following the same format.

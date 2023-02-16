# Gaussian Distribution
This is a Python class for creating and visualizing Gaussian distributions. The class can calculate the mean and standard deviation of a set of data, read in data from a text file, plot a histogram of the data, and plot a probability density function of the data.

### Dependencies
The class requires the following libraries to be installed:

math, matplotlib

### Usage
To use the Gaussian class, follow these steps:
1. Create an instance of the class: `my_distribution = Gaussian()`.
2. If desired, set the mean and standard deviation when creating the instance: `my_distribution = Gaussian(mu=10, sigma=2)`.
3. If you have data in a text file, read in the data using the `read_data_file()` method: `my_distribution.read_data_file('mydata.txt')`.
4. Calculate the mean and standard deviation using the `calculate_mean()` and `calculate_stdev()` methods:

```python
mean = my_distribution.calculate_mean()
stdev = my_distribution.calculate_stdev()
```

5. Plot a histogram of the data using the `plot_histogram()` method: `my_distribution.plot_histogram()`.
6. Plot a probability density function of the data using the `plot_histogram_pdf()` method: `my_distribution.plot_histogram_pdf()`.
7. If desired, add two Gaussian distributions using the `__add__()` method: `result = my_distribution1 + my_distribution2`.
8. To output the mean and standard deviation of the Gaussian distribution, call the `__repr__()` method: `print(my_distribution)`

###Methods
The Gaussian class has the following methods:

* `__init__(self, mu=0, sigma=1)`: creates a new Gaussian distribution with an optional mean (mu) and standard deviation (sigma)
* `calculate_mean(self)`: calculates the mean of the data set
* `calculate_stdev(self, sample=True)`: calculates the standard deviation of the data set, taking into account whether the data is a sample or the population
* `read_data_file(self, file_name, sample=True)`: reads in data from a text file and calculates the mean and standard deviation
* `plot_histogram(self)`: plots a histogram of the data set
* `pdf(self, x)`: calculates the probability density function of the Gaussian distribution at a given x value
* `plot_histogram_pdf(self, n_spaces=50)`: plots a histogram of the data set and the probability density function of the Gaussian distribution
* `__add__(self, other)`: adds two Gaussian distributions together
* `__repr__(self)`: outputs the mean and standard deviation of the Gaussian distribution

### Attributes
The Gaussian class has the following attributes:

* `mean`: the mean of the Gaussian distribution
* `stdev`: the standard deviation of the Gaussian distribution
* `data`: the data used to create the Gaussian distribution

### Example
Here is an example of how to use the Gaussian class:

```python
from gaussian import Gaussian

# create an instance of the class
my_distribution = Gaussian()

# read in data from a file and calculate mean and standard deviation
my_distribution.read_data_file('mydata.txt')
mean = my_distribution.calculate_mean()
stdev = my_distribution.calculate_stdev()

# plot a histogram of the data
my_distribution.plot_histogram()

# plot a probability density function of the data
my_distribution.plot_histogram_pdf()

# add two Gaussian distributions together
my_distribution2 = Gaussian(mu=5, sigma=3)
result = my_distribution + my_distribution2

# output the mean and standard deviation of the Gaussian distribution
print(my_distribution)
```

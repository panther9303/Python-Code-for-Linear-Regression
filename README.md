# Python-Code-for-Linear-Regression
This Code helps us in finding relation between multiple dependent variables which concludes to a Linear equation

import numpy as np
from scipy.optimize import curve_fit

# Define the model function
def model(x, k, m):
    b, c = x
    return k * (b + c) ** (-m)

# Given data points
b = np.array([74, 72, 73])
c = np.array([95, 94, 94.5])
a = np.array([250, 300, 275])

# Fit the model to the data
popt, pcov = curve_fit(model, (b, c), a)

# Extract the best-fit parameters
k_opt, m_opt = popt
k_opt, m_opt

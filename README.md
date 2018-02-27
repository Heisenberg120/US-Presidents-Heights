# US-Presidents-Heights
Fundamentals of exploratory data analysis on a basic dataset

#to find avg hieght of the US President

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
#import seaborn; seaborn.set()  #set plot style

import os
os.getcwd()
os.chdir('C:/Users/Rohit/Documents/datasets')
os.getcwd()

data = pd.read_csv('president_heights.csv')
heights = np.array(data['height(cm)'])
print(heights)

#now we can print a variety of summary statistics

print(" Mean Height = ", np.mean(heights))
print(" Std Deviation = ", np.std(heights))
print(" Minimum Height = ", np.min(heights))
print(" Maximum height = ", np.max(heights))


# we can also compute the percentiles and median
print(" 25th Percentile of Heights = ", np.percentile(heights, 25))
print(" Median Height = ", np.median(heights))
print(" 75th Percentile Heights = ", np.percentile(heights, 75))


#visual representation of data

%matplotlib inline                   

plt.hist(heights)
plt.title('Height Distribution of US Presidents')
plt.ylabel('Number')
plt.xlabel('Heights(cm)')


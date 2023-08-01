# Business Process (BPMN) for Booking a Room Online

Here is a BPMN diagram that describes how a customer visits a website to book a room online. 

![BPMN Diagram](https://i.imgur.com/5zvJZ8y.png)

The data involved in the above process steps are:
- Customer data (name, email, phone number)
- Room data (room type, room number, room availability)
- Payment data (credit card number, billing address)

## Pre-processing Phase

Here is the Python code for pre-processing phase:

```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Check Non-Null and NaN values
df = pd.read_csv('data.csv')
print(df.isnull().sum())

# Calculate the distribution and dimension
print(df.describe())

# Visualize with Seaborn and Matplotlib libraries
sns.set(style="ticks", color_codes=True)
g = sns.pairplot(df)
plt.show()


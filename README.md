###  Development by Thiyagarajan A 
###  Register no: 212222240110 
###  Date: 
# Ex.No: 01A PLOT A TIME SERIES DATA


# AIM:
To Develop a python program to Plot a time series data ( stock market price ).
# ALGORITHM:
Import the dataset from a CSV file using pandas and load it into a DataFrame.

Display the first few rows of the dataset to understand its structure.

Convert the 'Date' column to a datetime format and set it as the DataFrame index.

Create a time series plot of the 'Open' stock prices using matplotlib.

Add titles, labels, gridlines, and a legend, then display the plot.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt

# Load the data from the CSV file
file_path = 'Google_Stock_Price_Train.csv'
data = pd.read_csv(file_path)

# Display the first few rows of the dataset to understand its structure
print(data.head())

# Convert the 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'])

# Set the 'Date' column as the index
data.set_index('Date', inplace=True)

# Plot the time series data for 'Open' stock prices
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Open'], label='Open Price')
plt.title('Google Stock Price (Open)')
plt.xlabel('Date')
plt.ylabel('Price')
plt.grid(True)
plt.legend()
plt.show()
```

# OUTPUT:

![exp1](https://github.com/user-attachments/assets/bf6287c5-ccf0-4b82-af78-284af61da6fd)


# RESULT:
Thus we have created the python code for plotting the time series of given data.

---
title: Matplotlib
draft: false
tags:
---
## Introduction 
- Matplotlib is [[Python]]'s plotting library built on [[NumPy]] that can integrate directly with [[Pandas]]
- Workflow:
```mermaid 
flowchart LR 
id1(data) --> id2(plot)
id2 --> id3(axis on figure)
id3 --> id4(customize)
id4 --> id5(save & share plot)
```
> [!tip]
>Figure and plot are used interchangably
## Importing and getting started 
```python
%matplotlib inline # makes the notebook directly render the graphs 
import matplotlib.pyplot as plt
```
- `plt.plot;` creates a blank plot or figure (the ; gets rid of the array)
	- if the `;` is annoying, you can just type `plt.show()` after `plt.plot` to get the same effect 
### Pyplot vs object-oriented 
- According to the documentation, we should always use object-oriented when possible
### Methods of getting started 
```python 
# Method 1 
fig = plt.figure()
ax = fig.add_subplot()
plt.show()

# Method 2
fig = plt.figure()
ax = fig.add_axes([1,1,1,1])
ax.plot(x,y)
plt.show()

# Method 3 (recommended)
fig, ax = plt.subplots()
ax.plot(x,y)
```
## Example workflow 
```python
# 0. Import matplotlib and get it ready for plotting in Jupyter 
%matplotlib inline 
import matplotlib.pyplot as plt

# 1. Prepare data 
x = [1, 2, 3, 4]
y = [11, 22, 33, 44]

# 2. Setup plot 
fig, ax = plt.subplots(figsize=(5,10)) # (width, height)

# 3. Plot data 
ax.plot(x, y)

# 4. Customize plot 
ax.set(title="Simple Plot", 
	  xlabel="x-axis",
	  ylabel="y-axis")

# 5. Save your image 
fig.savefig("path/filename.png")
```
## Different types of plots  
- `ax.scatter(data)`: creates a scatterplot 
- `ax.bar(data, data)`: creates a bar plot 
- `ax.barh(list(data), list(data))`: creates a horizontal bar plot 
- `ax.hist(data)`: creates a histogram
## Combining plots
```python 
# Option 1 
fig, ((ax1, ax2), (ax3, ax4)) = plt.subplots(nrows=2
											ncols=2
											figsize=(10,5))
ax1.plot(data)
ax2.scatter(data)
a3.bar(data)
a4.hist(data)

# Option 2 
fig, ax = plt.subplots(nrows=2
					  ncols=2
					  figsize=(10,5))
ax[0,0].plot(data)
ax[0,1].scatter(data)
ax[1,0].bar(data)
ax[1,1].hist(data)
```
## Plotting from pandas DataFrames 
- `car_sales.plot(x="column name", y="column name")`: this is the [[Pandas]] version of matplotlib 
- `car_sales.plot.hist()`
### Pyplot vs matplotlib object-oriented method 
- When trying to get a quick visualization, pylot is fine but the object-oriented method is better for all other instances 
## Object oriented method 
```python
# create the plot 
fig, ax = plt.subplots(figsize=(10,6))
# plot the data 
scatter = ax.scatter(x=over_50["age"], 
					 y=over_50["chol"], 
					 c=over_50["target"])
# customize the plot 
ax.set(title="Heart Disease and Chlestrol Levels", 
	   xlabel="Age", 
	   ylabel="Cholestrol")
# Add legend 
ax.legend(*scatter.legend_elements(), title="Target")

# Add a horizontal line 
ax.axhline(over_50["chol"].mean(),
		  linestyle='--');
```
## Object oriented subplots 
```python 
# subplot of chol, age, thalach
fig, (ax0, ax1) = plt.subplot(nrows=2,
							  ncols=2, 
							  figsize=(10,10),
							  sharex=True)

# add data to a0
scatter = ax0.scatter(x=over_50["age"], 
					 y=over_50["chol"], 
					 c=over_50["target"])

# customize ax0
ax0.set(title="Heart Disease and Chlestrol Levels",  
	   ylabel="Cholestrol")

# add legend to ax0
ax0.legend(*scatter.legend_elements(), title="Target")

# Add a horizontal line to ax0
ax0.axhline(over_50["chol"].mean(),
		  linestyle='--');

# add data to ax1
scatter = ax1.scatter(x=over_50["age"], 
					 y=over_50["thalach"], 
					 c=over_50["target"],
					 cmap="winter")

# customize ax1
ax1.set(title="Heart Disease and Max Heart Rate", 
	   xlabel="Age", 
	   ylabel="Max Heart Rate")

# add legend to ax1
ax0.legend(*scatter.legend_elements(), title="Target")

# Add a horizontal line to ax1
ax0.axhline(over_50["thalach"].mean(),
		  linestyle='--')

# add title to the figure 
fit.suptitle("Heart Disease Analysis", fontsize=16, fontweight="bold");
```
## Customizing plots 
- `plt.style.available`: shows you what you have available to you 
- `plt.style.use('seaborn-whitegrid')`
- `plt.style.use('seaborn')`
- `plt.style.use('ggplot')`
- `ax.set(title="", xlabel="", ylabel="")`
- `ax.legend().set_visible(True)`
- `cmap='winter'` -- you can google different color maps 
- `ax.set_xlim([])`
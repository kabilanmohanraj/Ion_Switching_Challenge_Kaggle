# Ion_Switching_Challenge_Kaggle
My submission to the ion switching challenge hosted on kaggle which scored a LB score of 0.91640. You can find the competition details here! https://www.kaggle.com/c/liverpool-ion-switching

### About the competition:
Many diseases, including cancer, are believed to have a contributing factor in common, **ion channels**. Ion channels are pore-forming proteins present in animals and plants. They encode learning and memory, help fight infections, enable pain signals, and stimulate muscle contraction. When ion channels open, they pass electric current. The critical first step in the analysis of this current is event detection, so called **“idealisation”**. Existing methods of detecting these state changes are slow and laborious. Humans must supervise the analysis, which imparts considerable bias, in addition to being tedious. These difficulties limit the volume of ion channel current analysis that can be used in research. Therefore, bringing this analysis into the domain of artificial intelligence could enable rapid automatic detection of ion channel current events in raw data.

### About the data
The training data has 3 columns
1. Time at which the signal was captured
2. The signal value
3. Number of open channels

While the test data has 2 columns
1. Time
2. The signal value

What we had to predict is the number of open channels at a given time point. Basically this is a **classification problem** where the target column is a  discreet set of integers from 0-10.

### My solution
This solution is a **general approach** anyone would adapt to solve this problem.
1. Clean the data - remove baseline drift and such
2. Apply suitable machine learning algorithms to perform the classification
The respective steps are included in separate notebooks. The algorithms that I tested were the random forest and a hybrid recurrent neural network - an existing implementation (https://doi.org/10.1038/s42003-019-0729-3).

The intuitions for the methodologies applied here come from this research paper above.

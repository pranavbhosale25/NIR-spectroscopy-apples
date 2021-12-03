## Project Goal : Predicting origin of apples based on spectral data 

### About this notebook

- The dataset consists of NIR spectroscopy data of 300 apples
- The apples belong to 3 categories - Fuji apples, Red Star apples and Gala apples
- There are 100 samples of each type 
- The apples come from two provinces - Shaanxi and Shandong - 50 from each (50 * 2 * 3 = 300 samples)
- The intention is to use this data and build a classifier that can identify the source of the apples based on its spectral signature


### Process followed:
- After importing the data we do some initial preprocessing on it
- To adjust for the noise present in the data, we perform Savitzky-Golay smoothing 
- After that, we do Multiplicative Scatter Correction - a normalization technique for spectral data
- Post this, by PCA the best 6 components are picked 
- On this data, we use Support Vector Machines as the classifier of choice
- After training the SVM separately on each apple category, we predict the category for the test data

### Reference for the dataset and procedure:
Li, C., Li, L., Wu, Y., Lu, M., Yang, Y., &; Li, L. (2018). Apple variety identification using near-infrared spectroscopy. Journal of Spectroscopy, 2018, 1–7. https://doi.org/10.1155/2018/6935197

### For helping me understand MSC and the implementation too:
https://nirpyresearch.com/two-scatter-correction-techniques-nir-spectroscopy-python/

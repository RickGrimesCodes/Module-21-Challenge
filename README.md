# Module 19 Supervised Machie Learning Challenge for UNCC Data Analytics Bootcamp
This project was a great introduction to deep learning! It was cool to get a hang of what different
neural networks can do

## Directory Layout

#### ModelExport - A directory containing the two models made
* `CharityDeepLearningModel.h5` Unoptimized Model
* `CharityDeepLearningModelOptimized.h5` Optimized model
#### `Starter_code.ipynb` - The Jupyter Notebook containing the code for the unoptimized model
#### `Model_Optimizer.ipynb` - The Jupyter Notebook containing the code for the optimized model

## Deep Learning report

### Intro
&emsp;We've trained two models to help evaluate whether a charity should be funded or not funded,
using deep learning aka neural networks.\
The first model leaves a lot of data that could create necessary noise, so the second model gets
rid of that information so that the training occurs more efficiently, and is more accurate.

### First Model (unoptimized model)
&emsp;The first model has basic optimization techniques done, we've taking 'APPLICATION_TYPE',
and renamed the types with a count below 500 to 'Other'. We did a similar thing with 'CLASSIFICATION',
except those below 1000 were renamed to 'Other'. \
&emsp;After that we split the data, 'one hot encoded' it,
and ran it through two layer nodes being 100 and 30 respectively, then proceeded to train it on 200 epochs. The resulting accuracy
was ~73%\
(placeholder for relevant image)

### Second Model (optimized model)
&emsp;Similar to the first model, but instead we removed other data the may have clouded the training.
This includes dropping these three columns: 'STATUS','SPECIAL_CONSIDERATION', and 'EIN'.
We also re-named rows with a name occuring less than five times to 'Other'.\
&emsp;We've also added a third layer (not including the output layer) and upped the node counts for
the first and second layer. These being 100, 30 and 10 respectively. Trained at 100 epochs\
&emsp;All of this made the resulting model ~6% more accurate. With the optimized model being 79%
more efficient.

### Other Solutions?
&emsp;While another solution such as Random Forest Classifier might seem a probable,
it is predicted to be less accurate than Standard Scaler. With predicted accuracy being around ~77%

### To summarize
&emsp; To summarize, we've seen that Standard Scaler is probably the best solution for this dataset
and after removing data that can't really be categorized by a neural network, and outliers, we can
get a really awesome Standard Scaler model that is 79% accurate with this dataset. I've learned allot
with this challenge, thanks for taking the time to read my report!


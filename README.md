# CS-F425-Project-CIMON

## Files Included


```CIMON.ipynb``` : This file contains all the code that was written as a part of the project


```CIMON_Visualization.ipynb``` : This notebook contains code for the PCA visualization of the hash codes


```CIMON_Pseudo Graph Viz.ipynb```: This notebook contains the code for visualizing the pseudo graph post spectral clustering.

```CIMON_paper.pdf``` : PDF of the paper CIMON : Towards higher quality hash codes

```Project Report.pdf``` : Project Report

```Requirements.txt``` : Contains all the dependencies for running the ```CIMON.ipynb```


## Instructions to run CIMON.ipynb
1. DL_CIMON folder has been shared. If not, you can access it with the following [link](https://drive.google.com/drive/folders/1x5ZSlugRMdtQKs9jvDJvC6W34iA0fdM-?usp=sharing)

2. Add a shortcut of this folder to the "MyDrive" folder in your drive.

3. Now you are good to go to run the notebook.


## Contributions
- We present the first network that uses learned deep hash codes for
classification purposes.

- We first train the CIMON network in a (modified manner as mentioned
above) to learn a network that can learn good hash codes for images.
We train a small MLP (as shown in Figure 1) using the training set of the
STL10 dataset. This is done as follows:

- The image is passed through the trained network to obtain the hash
code for the image.

- Using the hash code as the input to the MLP, we train the MLP to
classify the image given the hash code.

- Just like any other network, using the cross entropy loss, we train
the MLP

- We have also added visualizations of the hash codes that the network has
learnt. The visualizations support our hypothesis that classification can be
performed from the hash code space because for the classes of images
taken, the network was able to produce hash codes that form visibly
separate clusters in low dimensional space. (Figure 2)
There are only 5000 training examples in the STL10 dataset, and we were
able to achieve a good accuracy by first training an unsupervised learning
model to learn hash codes, and then training a supervised learning model
on just 5000 images. These are results that we obtained on the STL10
dataset:
- Best test accuracy : 86.56 %
- Best train accuracy : 84.9 %

Training Plot on STL10 Dataset

![Screenshot from 2022-05-16 19-11-22](https://user-images.githubusercontent.com/57453637/168659870-9702e97a-dbb5-4166-9056-5480441e1c96.png)

For a more detailed report, have a look at [Project Report.pdf](/Project%20Report.pdf)

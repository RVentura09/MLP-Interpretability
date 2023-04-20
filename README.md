# MLP Interpretability
 Locally interpretable Pneumonia classifier

This model generates a local interpretation for the model prediction based on feature weights.This interpretation is obtained by implementing 
Aletheia unwrapper (1) ,such interpretation can also be obtained by implementing Alejandro Kuratomi's unwrapper (2) which used Aletheia paper as reference.

In the notebook we can generate global or local interpretations. To generate a global interpretation we feed aletheia unwrapper with the entire test set of interest. If we need a single interpretation we must pass a dataset containing only the instance of interest.

#### Recommended version for libraries

aletheia-dnn
Python 3.9 
matplotlib>=3.7.1
numpy>=1.23.5
pandas>= 1.5.3
seaborn>=0.12.2
scikit-learn>=1.2.2
statsmodels>=0.13.5

#### Data 

The pneumonia dataset is published by Kermany et al. on Mendeley Data <https://data.mendeley.com/datasets/rscbjbr9sj/2>.

#### Preprocess 

1) Manually remove images that contain sensors or other objects that are external to the natural human biology
2) Use any available method to remove the "R" marker from the images , we used the notebook called Letter_remover an adaptation from (4).
3) Review images and delete any inconsistencies generated by the letter remover.
4) Crop the images to remove sections that are not relevant for the task such as neck,side walls and shoulders ,we used the python noteboke Image_cropper adaptation done from (5).
5) Store the data set in a folder named Data_Cropped containing the images organized by their corresponding label Normal-Pneumonia 

#### Usage

1) Before running the MLP_Pneumonia notebook extract a couple of images to a separate location in order to test the interpretability of the model.
2) Run MLP_Pneumonia notebook.


References
1. Agus Sudjianto, William Knauth, Rahul Singh, Zebin Yang and Aijun Zhang. 2020. Unwrapping The Black Box of Deep ReLU Networks: Interpretability, Diagnostics, and Simplification. arXiv:2011.04041 

2. Alejandro Kuratomi Hernandez ,Ph.D. Machine Learning Interpretability.  https://alku.blogs.dsv.su.se/

3. Kermany, Daniel; Zhang, Kang; Goldbaum, Michael (2018), “Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification”, Mendeley Data, V2, doi: 10.17632/rscbjbr9sj.2

4. Dr. Sreenivas Bhattiprolu ,https://raw.githubusercontent.com/bnsreenu/python_for_microscopists/master/Tips_Tricks_42_How%20to%20remove%20text%20from%20images.py

5. Sergio Canu ,https://pysource.com/2021/03/04/how-crop-images-with-opencv-and-python/






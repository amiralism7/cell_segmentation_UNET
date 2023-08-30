# cell_segmentation_UNET

In a microscopic image with numerous visible cells, segmentation of individual cells enables the measurement of particular cellular properties, giving extensive insight into cellular heterogeneity. The process of cell segmentation involves dividing a microscopic picture domain into segments that each represent a single instance of a cell. 

U-Net with Cross Entropy Loss is a model widely used for semantic segmentation. However, it fails to prevent the over-merging of neighboring cells. Here, we aimed to investigate whether improving the loss function could enhance the performance of the image segmentation deep learning model. 
Therefore, we hypothesized that adding a dynamic weighted loss function would improve the model accuracy rather than merely applying a Cross Entropy Loss. We used a modified U-Net consisting of convolutional, max pooling, and upsampling layers with batch normalization and ReLu activation functions.

Additionally, we further deployed a weighted map to Cross Entropy Loss as a penalty factor to more tightly penalize merging the neighboring cells by the model. 
We found that our model could more efficiently segment neighboring cells. 

Overall, we concluded that using a weighted loss, in which the background labels separate neighboring cells and receive a significant weight in the loss function, would enhance the model performance. 
Although our dataset contained errors in ground truth labels, we could increase the model's accuracy. The main limitation of our model was that we had to use the cell's nuclei as an input channel in addition to the cytoplasm. 
Future research may concentrate on enhancing our model's ability to segment 3D and sequential data, as well as employing transfer learning techniques to improve model performance.

## Members of our Team:
- Amirali Soltanmohammadi
- Reza Saboori
- Mahdi Mirbazel
- Mahdi Nouraie
- Mostafa Mortezapour
- Mina Naseh
- Mehran Ilaghi
- Saba Panah
- Sina Maghsoudlou

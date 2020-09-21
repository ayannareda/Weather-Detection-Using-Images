# Weather-Detection-Using-Images

Weather detection using images. Used CNN deep learning approach to classify weather images into five classes :- <br />

1. Rainy <br />
2. Cloudy <br />
3. Sunny <br />
4. Snowy <br />
5. Foggy<br /><br />

Dataset used in this project is available on IEEEDataPort website.<br />
You can download the sataset from https://ieee-dataport.org/documents/five-class-weather-image-dataset-1<br /><br />

Dataset includes five types of weather conditions (cloudy, sunny, foggy, rainy and snowy).<br />
This dataset, called FWID, includes 4000 images for each weather category, leading to a total of 20000 images.<br /><br />

Steps :-<br />
1. Run Data_Slicing.ipyn<br />
2. Run Preparing_data.ipyn<br />
3. Run Training.ipynb<br />
4. Run Testing.ipynb<br /><br />

Methedology :-<br /><br />

First we sliced our Original dataset and took only particaular number of images of every class for further processing.<br /><br />

Then we detected edges on every image. and cropped the part of image with higher number of edges and kept only the part with less no. of edges (Sky_part).<br /><br />

Then converted the images into matrices using image_utils from Keras.preprocessing library.<br />
then saved those matrices in (.npy) file.<br />
Also saved the labels in (.npy) file.<br /><br />

Now, we will load the prepared data file (.npy) and prepared label file (.npy) in our Training file.<br />
Convert the label in One-hot vector.<br /><br />

The we build a CNN based deep neural network using Keras library.<br />
Then we compiled our model with loss function "categorical_crossentropy" and optimizer as "Adam".<br /><br />

After training, we achieved <br /><br />
Training accuracy = 98.77%<br />
<img src="https://github.com/gearhead0909/Weather-Detection/blob/master/Accuracy.png" alt="alt text" width="500" height="300"><br /><br />

Loss = 0.04<br />
<img src="https://github.com/gearhead0909/Weather-Detection/blob/master/Loss.png" alt="alt text" width="500" height="300"><br /><br />

After training, save the trained model.<br />
Then in testing we we used seperated and prepared data (.npy) to run our trained model.<br />
Acheived testing accuracy = 74.28%

# CNN_forImage

Convolutional Neural Network (CNN) is a type of neural network that is commonly used for image data. CNN uses Feature Extraction in it.<br><br>
CNN is a technique where we apply filters to produce more meaningful features.<br>

<h2>-- architecture --</h2>
The architecture at CNN has two phases, namely Feature Extractor and Fully Connected<br>
The following CNN architecture is used here:<br>

- **Feature Extractor**<br>
*Input 3x64x64*<br>
#Convolution use ReLu, MaxPool<br>
*conv_block(3, 8), #8 x 32 x 32<br>
conv_block(8, 16), #16 x 16 x 16<br>
conv_block(16, 32), #32 x 8 x 8<br>
conv_block(32, 64), #64 x 4 x 4<br>
nn.Flatten() #get 1024 pixel*<br>

- **Fully Connected**<br>
*linear_block(64 * 4 * 4, 256, dropout=0.1), #by default activation ReLu<br>
linear_block(256, 2, activation="lsoftmax")*<br>

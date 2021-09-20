# Video Classification
**Extract video Features::**  Video -> SequenceImages -> (InceptionResNetV2) -> SequenceImageFeatures -> (TransformerArchitecture) -> VideoFeatures -> Classifiers(Dense, Softmax)

Dataset :: [Action Recognition Data Set](https://www.crcv.ucf.edu/data/UCF101.php "UCF101") 

* Dataset :: 
  * This dataset contains videos and there corresponding labels (We have taken a small subset of dataset).

* Inspiration::
  * We have to train a model for video action recognition.
  * We will use pretrained DenseNet121 model for image features extractions.

Tools :: Tensorflow, Numpy, Pandas, PIL, Keras \
Architecture :: DenseNet121 (Pretrained), Transformer

### Steps::
  1. Load dataset zip from zip Files.

  2. Convert videos to sequece of images with the help of OpenCV.
  
  3. Get features of images and create our sequence dataset (DenseNet121).

  4. SequenceFeatures -> PositionalEncoding -> TransformerLayer -> Contextualized Features Of Video.
  
  5. Contextualized Sequence Features -> Dense Layers -> Softmax -> Get Class

Credit:: [Keras Examples](https://keras.io/examples/ "Video Classification")

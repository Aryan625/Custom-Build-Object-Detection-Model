# Custom-Build-Object-Detection-Model using SSD ResNet50 V1 FPN 640x640 (RetinaNet50)

In this project, I used the Object Detection API and retrained custom build model using RetinaNet50 to detect Cars using just 10 training images downloaded from Open Images. To build this custom model, I used the Tensorflow framework. I had set up the model to restore pre-trained weights from the checkpoint and fine-tuned the classification and box prediction layers. The custom build training loop just took about 14 min to train the model through 200 steps giving significantly very low total loss of about 0.0051. The model was then inferred on test images to detect multiple cars.

To train this custom build Object Detection model, I took the following steps:

  -	Installed the TensorFlow Object Detection API and imported necessary Object Detection API packages
  -	Downloaded the data from Open Images
  -	Prepared the data for training
  -	Downloaded checkpoints containing the pre-trained weights
  -	Located and read from the configuration file and modified the model configuration
  -	Build the custom model
  -	Restored weights from the checkpoint
    -	Defined Checkpoints for the box predictor
    -	Defined the temporary model checkpoint
    -	Restored the checkpoint
    -	Ran a dummy image to generate the model variables
  -	Configured the training loop
    -	Set training hyperparameters
    -	Selected the prediction layer variables that is to be fine tuned
    -	Defined the training step
  - Loaded test images and ran inference with new model.

The inference that was done on test images (which was extracted from video as still frames) was converted into gif which can be seen below.

![Drone shot of a car](car-anim_1.gif)
![Cars on Highway](car-anim_2.gif)

The colab notebook for this project can be found [here](https://github.com/Aryan625/Custom-Build-Object-Detection-Model/blob/main/Custom_Build_Object_Detection_Model_(SSD_ResNet50_V1_FPN_640x640_(RetinaNet50)).ipynb) or in this [google drive link](https://colab.research.google.com/drive/1378t5oBxpbUdMr4acA12AtMUoBxIra-C?usp=sharing)

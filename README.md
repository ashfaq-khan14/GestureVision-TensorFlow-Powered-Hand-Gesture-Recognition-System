# TensorFlow-Object-Detection-for-Hands-Sign-Recognition
This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API.
![IMG-20240118-WA0019](https://github.com/ashfaq-khan14/TensorFlow-Object-Detection-for-Hands-Sign-Recognition/assets/120010803/3368375e-f764-48b3-bf87-ae585c1cb1df)![WhatsApp Image 2024-01-19 at 03 49 40_e3a6eb8c](https://github.com/ashfaq-khan14/TensorFlow-Object-Detection-for-Hands-Sign-Recognition/assets/120010803/1f555c6e-5c9c-4201-be11-28f97b968935)

Steps

Step 1. Clone this repository: https://github.com/nicknochnack/TFODCourse

Step 2. Create a new virtual environment
python -m venv tfod

Step 3. Activate your virtual environment
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 

Step 4. Install dependencies and add virtual environment to the Python Kernel
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj

Step 5. Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment as shown below



Step 6. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFODCourse\Tensorflow\workspace\images\train
\TFODCourse\Tensorflow\workspace\images\test

Step 7. Begin training process by opening 2. Training and Detection.ipynb, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model.

Step 8. During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.


If not, resolve installation errors by referring to the Error Guide.md in this folder.

Step 9. Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics.



Step 10. You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g.
 cd Tensorlfow/workspace/models/my_ssd_mobnet/eval
and open Tensorboard with the following command
tensorboard --logdir=. 
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.

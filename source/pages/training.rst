Custom training
===============


Overview
********

On our Github repo `depthai-ml-training <https://github.com/luxonis/depthai-ml-training>`__ we provide several ML training notebooks trained
on various data sets. You can run these notebooks on `Google Colab <https://colab.research.google.com/notebooks/intro.ipynb>`__ - they provide
free CPU/GPU instances, so great for prototyping and even simple production models.

We currently have these ML training tutorials:

- `Tutorial - SSD MobileNetv2 training <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Easy_Object_Detection_Demo_Training.ipynb>`__
- `Tutorial - SSD MobileNetv2 training with custom data <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Easy_Object_Detection_With_Custom_Data_Demo_Training.ipynb>`__
- `Tutorial - YOLOv4-tiny based Mask Detector <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Easy_TinyYOLOv4_Object_Detector_Training_on_Custom_Data.ipynb>`__
- `Tutorial - YOLOv3-tiny based Mask Detector <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Easy_TinyYolov3_Object_Detector_Training_on_Custom_Data.ipynb>`__
- `Tutorial - DeepLabV3+ MNV2 semantic segmetnation <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/DeepLabV3plus_MNV2.ipynb>`__
- `Tool - Google Drive image batch resizer <https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/GDrive-Resize.ipynb>`__

The Tutorials
*************

.. raw:: html

   <h3>Easy Object Detector Training <a href="https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Easy_Object_Detection_With_Custom_Data_Demo_Training.ipynb" target="_blank"><img alt="Open In Colab" src="https://colab.research.google.com/assets/colab-badge.svg"/></a></h2>

The tutorial notebook
*Easy_Object_Detection_With_Custom_Data_Demo_Training.ipynb* shows how to quickly train an object detector based on the MobileNet SSDv2 network.

Optionally, see our documentation around this module (`here <https://docs.luxonis.com/tutorials/object_det_mnssv2_training/>`__)
for of a guide/walk-through on how to use this notebook.  Also, feel free to jump right into the Notebook, with some experimentation it's relatively straightforward to get a model trained.

After training is complete, it also converts the model to a .blob file that runs on our DepthAI platform and modules.
First the model is converted to a format usable by OpenVINO called Intermediate Representation, or IR. The IR model is then
compiled to a .blob file using a server we set up for that purpose. (The IR model can also be `converted locally to a blob <https://github.com/luxonis/depthai#conversion-of-existing-trained-models-into-intel-movidius-binary-format>`__.)

And that's it, in less than a couple of hours a fairly advanced proof of concept object detector can run on DepthAI to
detect objects of your choice and their associated spatial information (i.e. X, Y, Z coordinates). For example this notebook was used to train DepthAI to locate strawberries in 3D space, see below:

.. image:: https://i.imgur.com/Cz7eZUo.jpg
  :alt: Real-time 3D Strawberry Detector
  :target: https://www.youtube.com/watch?v=Okjh2OCP-o8&

.. raw:: html

   <h3>COVID-19 Mask/No-Mask Training <a href="https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/Medical_Mask_Detection_Demo_Training.ipynb" target="_blank"><img alt="Open In Colab" src="https://colab.research.google.com/assets/colab-badge.svg"/></a></h2>

The *Medical Mask Detection Demo Training.ipynb* training notebook shows another example of a more complex object detector.
The training data set consists of people wearing or not wearing masks for viral protection. There are almost 700 pictures
with approximately 3600 bounding box annotations. The images are complex: they vary quite a lot in scale and composition.
Nonetheless, the object detector does quite a good job with this relatively small data set for such a task. Again, training takes around 2 hours.
Depending on which GPU the Colab lottery assigns to the notebook instance, training 10k steps can take 2.5 hours or 1.5 hours.
Either way, a short period for such a good quality proof of concept for such a difficult task.
We then performed the steps above for converting to blob and then running it on our DepthAI module.

Below is a quick test of the model produced with this notebook on OAK device:

.. image:: http://img.youtube.com/vi/d_oUxDzWHd0/0.jpg
  :alt: COVID19 Mask Detector
  :target: https://www.youtube.com/watch?v=d_oUxDzWHd0

Supporting Notebooks
********************

.. raw:: html

   <h3>Image Resize in Google Drive <a href="https://colab.research.google.com/github/luxonis/depthai-ml-training/blob/master/colab-notebooks/GDrive-Resize.ipynb" target="_blank"><img alt="Open In Colab" src="https://colab.research.google.com/assets/colab-badge.svg"/></a></h2>

This notebook operates on your set of images in Google Drive to resize them to the format needed by the training notebooks.

.. include::  /pages/includes/footer-short.rst

# 2 - Leveraging Pre-Trained Models

__1. What is the use of `.transpose` and `.reshape` in the pre-processing ?__

`reshape` is more intuitive to explain, simply put when you try to have a different matrix/array/tensor shape from the one you originally have, say 4 by 4, and you would want to reshape it into 2 by 8, then you will need to use .reshape. On the other hand, `transpose` is inherently a matrix operation. It is an operation to interchange each row with the corresponding column. But in both cases the dimensionalities before and after the so-called "transformation" has to conform to some conservation rule like the number of elements contained in the case of .reshape. Here it's an [article](https://lihan.me/2018/01/numpy-reshape-and-transpose/) that compare both methods

__2.  All this models are pretrained, but how long does it take to train a model if you have all the data? Hours, days, weeks of processing? And if the data changes a little or some data is corrected, do you have to do all the training process again? If you are developing a new model, how do the testing if you have to wait a lot of time? __

* If for example, you can't afford a good GPU for intensive processing stuff (like training big models), you can use Google Collaboratory which offers you 16GB RAM, GPU and 50 GB ROM.
* Models can take a lot of time and also very little time. It all depends were you begin. For example there is a field called transfer learning where you grab existant NN (neural network) architectures and you only retrain the outermost layers. With the result being very effective & with little improvements, it is one of the most pragmatic pardaigms in dealing with Computer Vision.
* If the data change is in the limits of the previous data, you don't have to. If the data is out of that range, you have to.
Look, suppose you trained your model on input data in the range 1 to 10. Now, if your new data contains data that has an 11 or 20 in it, you need to retrain the model. This is because the models, while learning, approach the local minima (or simply, try to form an approximate look-up table), and once you've provided it with something completely random, it will not infer it correctly
*  resources for further research
    * https://medium.com/@prasad.pai/data-augmentation-techniques-in-cnn-using-tensorflow-371ae43d5be9
    * https://medium.com/nanonets/how-to-use-deep-learning-when-you-have-limited-data-part-2-data-augmentation-c26971dc8ced
    * https://medium.com/@erikhallstrm/hello-world-tensorflow-649b15aed18c
    * https://medium.com/@abinesh.mba13/why-gpus-are-important-in-deep-learning-4d20df9c0cb6
    * https://towardsdatascience.com/a-comprehensive-hands-on-guide-to-transfer-learning-with-real-world-applications-in-deep-learning-212bf3b2f27a
    * https://medium.com/@14prakash/transfer-learning-using-keras-d804b2e04ef8 
    
__3. Can you test more image without installing the whole system on my computer?__
* All you need for making inferences using open vino quantized model is a light weight inference engine. You will learn more about it in the upcoming lessons. It's easy to do this you will need to get an inference engine to do this. The course will also guide you with deploying an app so check that out in l4 and l5.
* Also, in the udacity workspace you can do it.. just upload your images in the images folder in the workspace and test them.

__4. Where can I download OpenVINO and non-OpenVINO pre trained models? For example, where can I download pre trained model for face expression detection?__
* https://www.analyticsvidhya.com/blog/2018/07/top-10-pretrained-models-get-started-deep-learning-part-1-computer-vision/
* TF : https://github.com/tensorflow/models
* Caffe : https://github.com/BVLC/caffe/wiki/Model-Zoo
* Onnx : https://github.com/onnx/models
* Pytorch : https://pytorch.org/docs/stable/torchvision/models.html

__5.  Locating the model downloader in the Loading Pre-Trained Models section__
The tool downloader.py is in `/opt/intel/openvino/deployment_tools/open_model_zoo/tools/downloader` path.

__6. 











# 3 - The Model Optimizer
__1. Tensorflow Model detection zoo has its own per-processing pipeline to process its input shape and size, But while converting tf model using openvino it ignores pre-proccessing step. In this case, how to know required shape and size of the tf model ? For example, downloading some model from the link https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md__

There is a utilities called `import_pb_to_tensorboard.py` under tf tools that can convert pb file into format that tensorboard can visualize. Then launch tensorboard to inspect the model layers

__2. What is segmentation fault(core dumped)? and why it is happening in the last exercise of lesson 3. and what is its cause ?__

Segmentation fault is a fault raised by memory protection hardware and it is caused by code trying to access a protected memory area.
It can be caused by a deep recursion, if you run out of process memory.
This blog post can help you debug the problem:https://blog.richard.do/2018/03/18/how-to-debug-segmentation-fault-in-python/
A segmentation fault occurs when a program attempts to access a memory location that it is not allowed to access, or attempts to access a memory location in a way that is not allowed. Please take care while modifying the two .cpp files mentioned in the Guide.

__3. If I want to make a web app using one or more pretrained models, where should I save my model or deploy it so as to achieve this ?__

There are mainly two ways to deploy model to web app:
1. Expose your model to a http endpoint and create a webapp that will interact with it.. for this you need Amazon sagemaker to deploy a model. https://github.com/Escanor1996/Depoyment_of_sentiment_analysis_model_Sagemaker
2. Create a flask based webapp where the inference of model will be done in backend..
After creating webapp you can use heroku to host your app free online. I am providing you two repos of mine which deploy model in both ways.. https://github.com/Escanor1996/Food101-Classification

__4. While training your TF models, has anyone used the freezing technique ? If yes, can you please share the code and shed some more light on this topic ?__ 

if you want to learn about reason to freeze layers of a model while optimization, you can have a look at the deeplearning.ai course by Andrew Ng, chapter about transfer learning.
Although you can freeze layers for other reasons. You can freeze a custom layer performing definite operations which don't need to be optimized. For instance you apply a definite filter to a picture as a first conv layer

__5. Can anyone share good study material for cutting parts of the model?__

follow this link : https://docs.openvinotoolkit.org/latest/_docs_MO_DG_prepare_model_convert_model_Cutting_Model.html

__6. Completed the execution of Tensorflow model, Caffe model and ONNX model. Here are the execution times for each of them. The execution time significantly reduced by each model. Is this due to the fact of absence of freezing/unfreezing steps in Caffe model and ONNX model? https://inteledgeaichallenge.slack.com/files/UREAL7J3D/FSBNSBE30/image.png)__

well to some point it is correct but in Caffe and ONNX there is no concept of freezing
ONNX was done easily because there was no ```deploy.prototxt``` like as in Caffe


# 1 - Introduction to AI at the Edge

* Example: Most voice assistants send your query to the cloud for processing, while most self-driving cars need to be able to perform their computations at the edge. Additionally, while gathering insights from millions of sales transactions probably is fine to use the higher compute available in the cloud, a remote nature camera may not be able to always send its data over a connection.

* Reasons for development of the Edge
  * The proliferation of IoT devices is leading to more edge applications.
  * Edge applications often arise from a need for low latency in processing data.
  * Edge applications often arise from a need for devices to still be able to use algorithms when disconnected from a network or the cloud.

* Aspect of the Intel® Distribution of OpenVINO™ Toolkit: Open Model Zoo is available with plenty of Pre-Trained Models. If you have your own model, you can convert it with the Model Optimizer, and then perform inference on it with the Inference Engine.

* Local Set-up
  * Make sure to make note of the [hardware requirements](https://software.intel.com/en-us/openvino-toolkit/hardware) for the Intel® Distribution of OpenVINO™ Toolkit if you want to work locally.
  * If you do want to do the exercises on your local machine (or perhaps even on a set-up like a Raspberry Pi with an [Intel® Neural Compute Stick 2](https://software.intel.com/en-us/articles/intel-neural-compute-stick-2-and-open-source-openvino-toolkit)), you can follow the instructions [here](https://docs.openvinotoolkit.org/latest/index.html) for your operating system.
  
* Intel® DevCloud - Edge
There is also the new [Intel® DevCloud platform](https://software.intel.com/en-us/devcloud/edge) for testing out edge environments. This allows you to have access to a range of Intel® hardware such as CPUs, GPUs, FPGAs, Neural Compute Stick, and more. Later courses will get more into the hardware side of things, but this another option for working with an edge environment.

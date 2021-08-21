# Optimization-TensorRT

- Converted FP32 model to FP16/INT8 - compared performance

- Usually we train the models in FP32, since we get wide range for floating point numbers, as needed for model convergence.

- But when running inference we don't specifically need FP32 since we are not going to accumlate the gradients(backprop).Forward pass is alone done for inference and to do so, FP16/INT8 wieghed model would suffice.

- This notebook containes a detailed overview of using TensorRT, model conversion and performance comparison.

NOTE: If u r working on smaller GPUs , then there won't be any drastic diff in the model performance between FP32 and FP16 (although there will be a neglible difference).
In case of powerful machine where the hardware has Naive CUDA cores , we can observe the difference in the latency and throughput.

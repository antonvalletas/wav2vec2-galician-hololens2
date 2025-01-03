# Wav2Vec 2.0 Galician HoloLens 2 ASR Models

This repository contains the fine-tuned, quantized, and optimized models used to develop the first Galician ASR system designed specifically for Industrial Metaverse applications. The models leverage the Wav2Vec 2.0 architecture optimized for on-device inference on ARM64 architectures (Microsoft HoloLens 2).

## Model Variations

### Base Model

1. **wav2vec2-base-gl.onnx**: The base model without any optimizations or quantization.

### Optimized Models

1. **wav2vec2-base-gl-onnx-optimizer.onnx**: The base model with graph optimizations using onnx-optimizer.
2. **wav2vec2-base-gl-onnx-simplifier.onnx**: The base model with graph optimizations using onnx-simplifier.
3. **wav2vec2-base-gl-ort-basic.onnx**: The base model with graph optimizations using ONNX Runtime ENABLE_BASIC optimizations.
4. **wav2vec2-base-gl-pytorch-qint8.onnx**: The base model quantized using PyTorch's QInt8 quantization.
5. **wav2vec2-base-gl-optimumDynamic-noConvInt-arm64.onnx**: The base model quantized dynamically using Optimum QInt8 datatype without convolutional integer nodes for ARM64.
6. **wav2vec2-base-gl-optimumDynamic-noConvInt-arm64-symAct.onnx**: Same as the above but with symmetric activations.
7. **wav2vec2-base-gl-optimumDynamic-noConvInt-arm64-perChannel-symAct.onnx**: Same as the above but with per-channel quantization.

### Distilled Models

1. **wav2vec2-distilled.onnx**: A distilled version of the base model for reduced size and faster inference.
2. **wav2vec2-distilled-gl-optimumDynamic-noConvInt-arm64-perChannel-symAct.onnx**: Same as the above but with dynamic per-channel quantization with symmetric activations and no convolutional integer nodes for ARM64.

### Large Models

1. **wav2vec2-large-gl-optimumDynamic-noConvInt-arm64-perChannel-symAct.onnx**: The large model quantized dynamically using Optimum QInt8 datatype without convolutional integer nodes for ARM64 with per-channel quantization and symmetric activations.
2. **wav2vec2-large-gl-pytorch-qint8.onnx**: The large model quantized using PyTorch's QInt8 datatype.

## Funding

This work has been supported by Centro Mixto de Investigación UDC-NAVANTIA (IN853C 2022/01), funded by GAIN (Xunta de Galicia) and ERDF Galicia 2021-2027.

## License

These models are released under the GPLv3 License. See the [LICENSE](LICENSE) file for more information.

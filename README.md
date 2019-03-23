<p align="center">
<img src="Resource/awesome-ml-demos-with-ios-logo.png" width="187" height="174"/>
</p>


[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/motlabs/awesome-ml-demos-with-ios) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GIF PRs More Welcome](https://img.shields.io/badge/GIF--PRs-WELCOME!-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

# Awesome Machine Learning DEMOs with iOS

We tackle the challenge of using machine learning models on iOS via Core ML and ML Kit (TensorFlow Lite).

[한국어 README](https://github.com/motlabs/iOS-Proejcts-with-ML-Models/blob/master/README_kr.md)

## Contents
- [Machine Learning Framework for iOS](#machine-learning-framework-for-ios)
  - [Flow of Model When Using Core ML](#Flow-of-Model-When-Using-Core-ML)
  - [Flow of Model When Using Create ML](#Flow-of-Model-When-Using-Create-ML)
- [Example Projects Using Various Machine Learning Models](#Example-Projects-Using-Various-Machine-Learning-Models)
  - [MobileNet](#MobileNet)
  - [Pose Estimation](#Pose-Estimation)
    - [Body Pose Estimation](#Body-Pose-Estimation)
    - [Fingertip Estimation](#Fingertip-Estimation)
  - [Object Detection](#Object-Detection)
  - [Text Detection & Recognition](#text-detection--recognition)
  - [A Simple Classification Using Create ML and Core ML](#A-Simple-Classification-Using-Create-ML-and-Core-ML)
- [Performance](#Performance)
  - [📏Measure module](#measure-module)
  - [Test](#test)
    - [Unit Test](#Unit-Test)
    - [Bunch Test (planning...)](#bunch-test-planning)
  - [Implements](#Implements)
- [Author](#Author)
- [See also](#See-also)

## Machine Learning Framework for iOS

- [Core ML](https://developer.apple.com/documentation/coreml)
- [ML Kit](https://developers.google.com/ml-kit/)
- etc. ([Tensorflow Lite](https://www.tensorflow.org/mobile/tflite/), [Tensorflow Mobile](https://www.tensorflow.org/mobile/))

### Flow of Model When Using Core ML

[![Flow of Model When Using Core ML](Resource/flow_of_model_when_using_coreml.png?raw=true)](https://docs.google.com/presentation/d/1wA_PAjllpLLcFPuZcERYbQlPe1Ipb-bzIZinZg3zXkg/edit?usp=sharing)

The overall flow is very similar for most ML frameworks. Each framework has its own compatible model format. We need to take the model created in TensorFlow and **convert it into the appropriate format, for each mobile ML framework**.

Once the compatible model is prepared, you can run the inference using the ML framework. Note that you must perform **pre/postprocessing** manually.

> If you want more explanation, check [this slide(Korean)](https://docs.google.com/presentation/d/1wA_PAjllpLLcFPuZcERYbQlPe1Ipb-bzIZinZg3zXkg/edit?usp=sharing).

### Flow of Model When Using Create ML

![playground-createml-validation-001](Resource/flow_of_model_when_using_createml.png)

## Baseline Projects

#### DONE

- Using built-in model with Core ML

- Using built-in on-device model with ML Kit
- Using custom model for Vision with Core ML and ML Kit

#### TODO

- Object Detection with Core ML and ML Kit
- Using built-in cloud model on ML Kit
  - Landmark recognition
- Using custom model for NLP with Core ML and ML Kit
- Using custom model for Audio with Core ML and ML Kit
  - Audio recognition
  - Speech recognition
  - TTS



### Image Classification

| Core ML | ML Kit |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Object<br>Classification** | |
| <p align="center">[MobileNet-CoreML](https://github.com/tucan9389/MobileNetApp-CoreML)<img src="Resource/MobileNet-CoreML-DEMO.gif" width="200"/></p> | <p align="center">[MobileNet-MLKit](https://github.com/tucan9389/MobileNetApp-MLKit)<img src="Resource/MobileNet-MLKit-DEMO.gif" width="200"/></p> |
| **Pose Estimation** | |
| <p align="center">[PoseEstimation-CoreML](https://github.com/tucan9389/PoseEstimation-CoreML)<img src="Resource/180801-poseestimation-demo.gif" width="200"/></p> | <p align="center">[PoseEstimation-MLKit](https://github.com/tucan9389/PoseEstimation-MLKit)<img src="Resource/PoseEstimation-MLKit-hourglass.gif" width="200"/></p> |
| <p align="center">[FingertipEstimation-CoreML](https://github.com/tucan9389/FingertipEstimation-CoreML)<img src="Resource/fingertip_estimation_demo003.gif" width="200"/></p> | |
| **Object Detection** | |
| <p align="center">[SSDMobileNet-CoreML](https://github.com/tucan9389/SSDMobileNet-CoreML)<img src="Resource/SSDMobileNetV2-DEMO.gif" width="200"/></p> | |
| **Text Detection &**<br>**Recognition** | |


- [KeypointAnnotation](https://github.com/tucan9389/KeypointAnnotation)<br>
  : Annotation tool for own custom estimation dataset


### Object Detection

1. [SSDMobileNet-CoreML](https://github.com/tucan9389/SSDMobileNet-CoreML)<br>: Detect 90 objects(find the object box of position and size and identify the category).

| [SSDMobileNet-CoreML](https://github.com/tucan9389/SSDMobileNet-CoreML) |
| ------------------------------------------------------------ |
| ![SSDMobileNetV2-DEMO](Resource/SSDMobileNetV2-DEMO.gif) |

### Text Detection & Recognition

1. [TextDetection-CoreML](https://github.com/tucan9389/TextDetection-CoreML)<br>
   : Detect character using Vision built-in model.
2. [TextRecognition-MLKit](https://github.com/tucan9389/TextRecognition-MLKit)<br>: Recognize text using Firebase built-in model.


| [TextDetection-CoreML](https://github.com/tucan9389/TextDetection-CoreML) | [TextRecognition-MLKit](https://github.com/tucan9389/TextRecognition-MLKit) |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| ![TextDetection-CoreML_DEMO001](Resource/TextDetection-CoreML_DEMO001.gif) | ![TextRecognition-MLKit_DEMO002](Resource/TextRecognition-MLKit_DEMO002.gif) |

### A Simple Classification Using Create ML and Core ML

1. [SimpleClassification-CreateML-CoreML](https://github.com/tucan9389/SimpleClassification-CreateML-CoreML)

| Create ML                                                    | Core ML                            |
| ------------------------------------------------------------ | ---------------------------------- |
| ![IMG_0436](Resource/playground-createml-validation-001.png) | ![IMG_0436](Resource/IMG_0436.PNG) |

## Application Projects

| Name | DEMO | Note |
| ---- | ---- | ---- |
| [dont-be-turtle-ios](https://github.com/motlabs/dont-be-turtle-ios) | <p align="center"><img src="Resource/dont-be-turtle_demo_004.gif" width="200"/></p> | - |
| [WordRecognition-CoreML-MLKit](https://github.com/tucan9389/WordRecognition-CoreML-MLKit)(preparing...) | <p align="center"><img src="Resource/TextDetection-CoreML_DEMO001.gif" width="200"/></p> | Detect character, find a word what I point and then recognize the word using Core ML and ML Kit. |


## Performance

> Execution Time: Inference Time + Postprocessing Time
>
> WordRecognition-CoreML-MLKit: Text Detection(Core ML built-in model) + Text Recognition(ML Kit built-in model)

|                              | Inference Time(ms) | Execution Time(ms) |   FPS   |
| ---------------------------: | :----------------: | :----------------: | :-----: |
|             MobileNet-CoreML |         40         |         40         |   23    |
|              MobileNet-MLKit |        120         |        130         |    6    |
|        PoseEstimation-CoreML |         51         |         65         |   14    |
|         PoseEstimation-MLKit |        200         |        217         |    3    |
|          SSDMobileNet-CoreML |  100 ~ 120         |   110 ~ 130       |    5    |
|         TextDetection-CoreML |         12         |         13         | 30(max) |
|        TextRecognition-MLKit |       35~200       |       40~200       |  5~20   |
| WordRecognition-CoreML-MLKit |         23         |         30         |   14    |

### 📏Measure module

You can see the measured latency time for inference or execution and FPS on the top of the screen.

![measure_ui](Resource/measure_ui.jpeg)

### Test

#### Unit Test

> Show output for each input?
> Drawing detail of result?
> Test for debugging?
>
> - Pose Estimation: draw dot each point and joint, print confidence each point.
> - ...

#### Bunch Test (planning...)

> Analyze outputs from a bunch of inputs
>
> - average of inference time and fps
> - accumulate execution time, fps...?
> - rendering time
> - total execution time
> - ...

### Implements

|                       | Measure📏 | Unit Test | Bunch Test |
| --------------------: | :------: | :-------: | :--------: |
|      MobileNet-CoreML |    O     |     X     |     X      |
|       MobileNet-MLKit |    O     |     X     |     X      |
| PoseEstimation-CoreML |    O     |     O     |     X      |
|  PoseEstimation-MLKit |    O     |     X     |     X      |
|   SSDMobileNet-CoreML |    O     |     O     |     X      |
|  TextDetection-CoreML |    O     |     X     |     X      |
| TextRecognition-MLKit |    O     |     X     |     X      |



## Author

- [tucan9389](https://github.com/tucan9389)

## See also

- [Core ML | Apple Developer Documentation](https://developer.apple.com/documentation/coreml)
- [Machine Learning - Apple Developer](https://developer.apple.com/machine-learning/)
- WWDC17 - Core ML 발표자료
  - [WWDC17 703 Session - Introducing Core ML](https://developer.apple.com/videos/play/wwdc2017/703/)
  - [WWDC17 710 Session - Core ML in depth](https://developer.apple.com/videos/play/wwdc2017/710/)
  - [WWDC17 506 Session - Vision Framework: Building on Core ML](https://developer.apple.com/videos/play/wwdc2017/506)
- WWDC18 - Core ML 2 발표자료
  - [WWDC18 708 Session - What’s New in Core ML, Part 1](https://developer.apple.com/videos/play/wwdc2018/708/)
  - [WWDC18 709 Session - What’s New in Core ML, Part 2](https://developer.apple.com/videos/play/wwdc2018/709/)
  - [WWDC18 717 Session - Vision with Core ML](https://developer.apple.com/videos/play/wwdc2018/717/)
- [ML Kit - Firebase](https://developers.google.com/ml-kit/)
- [Apple's Core ML 2 vs. Google's ML Kit: What's the difference?](https://venturebeat.com/2018/06/05/apples-core-ml-2-vs-googles-ml-kit-whats-the-difference/)
- [iOS에서 머신러닝 슬라이드 자료](https://docs.google.com/presentation/d/1wA_PAjllpLLcFPuZcERYbQlPe1Ipb-bzIZinZg3zXkg/edit?usp=sharing)
- [MoTLabs Blog](https://motlabs.github.io/)

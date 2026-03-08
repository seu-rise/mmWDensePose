# mmWDensePose: A High-Quality mmWave Point Cloud Benchmark for 3D Human Pose Estimation

<!-- [![Project Page](https://img.shields.io/badge/Project-Page-green.svg)](https://your-project-page) -->
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)

Official repository for **mmWDensePose: A High-Quality mmWave Point Cloud Benchmark for 3D Human Pose Estimation**.

## Abstract

Millimeter-wave (mmWave) radar enables privacy-preserving 3D human pose estimation and remains reliable under challenging lighting conditions. However, existing radar-based pose datasets are often constrained by sparse point clouds due to limited antenna configurations on commercial platforms. We present a dense mmWave radar point cloud benchmark dataset for 3D human pose estimation by using a customized 4D mmWave radar system with multi-chip cascading and optimized antenna array design. Synchronized ground-truth skeletons are provided by a Kinect V2 sensor. Using standard point-based baselines for validation, the proposed dataset yields substantially lower localization error than existing datasets. In particular, our best result achieves a 75.51\% lower mean localization error (MLE) than the best-reported result on MiliPoint. The results highlight the importance and advantages of our proposed dataset, called mmWDensePose, for accurate and robust 3D human pose estimation.

## Introduction

This repository is created for our paper on **mmWDensePose: A High-Quality mmWave Point Cloud Benchmark for 3D Human Pose Estimation**.  
Our work studies how to regress 3D skeletal keypoints directly from **mmWave radar point clouds**, and evaluates multiple baseline settings under a unified framework. In particular, we consider both:

- **25-keypoint setting**, following the Kinect V2 skeleton definition
- **19-keypoint setting**, derived for fair comparison with prior work

The repository is intended to provide resources related to the paper, including dataset descriptions, preprocessing pipelines, training and evaluation code, and benchmark implementations.

The human pose estimation dataset acquisition system is shown in Fig 1.

<div align="center">
  <img src="assets\compressed_dataset acquisition system 1.png" width="100%">
  <p><em>Fig 1: The human pose estimation dataset acquisition system</em></p>
</div>

A few representative samples are illustrated in Fig 2.

<div align="center">
  <img src="assets\samples.png" width="100%">
  <p><em>Fig 2: Sample data from the collected dataset</em></p>
</div>

Several typical test examples are shown in Fig 3.

<div align="center">
  <img src="assets\test.png" width="100%">
  <p><em>Fig 3: Several typical test examples</em></p>
</div>

**Table.** Comparison of MLE (m) on our dataset and MiliPoint (lower is better).
| Model            | Ours (mmWDensePose) 19-keypoint | Ours (mmWDensePose) 25-keypoint | MiliPoint 9-keypoint | MiliPoint 18-keypoint |
|------------------|----------------------------------|----------------------------------|----------------------|-----------------------|
| PointTransformer | 0.0372                           | 0.0439                           | 0.1496               | 0.1690                |
| PointNet++       | **0.0314**                       | **0.0386**                       | 0.1352               | 0.1491                |
| PointMLP         | 0.0359                           | 0.0434                           | 0.1282               | 0.1389                |
| DGCNN            | 0.0557                           | 0.0659                           | 0.1642               | 0.1848                |
| MLP              | 0.4866                           | 0.5689                           | --                   | --                    |

## Status

🚧 **Coming Soon**

The codebase and dataset are currently being organized and will be released after cleanup and documentation are completed.

Planned releases include:

- Dataset description and access instructions
- Data preprocessing scripts
- Training and evaluation code
- Baseline implementations
- Checkpoints and usage examples

## Dataset

The dataset used in this work will be released in this repository after further organization.

More details will be provided soon, including:

- Data format
- Train/validation/test split

## Code

The training and evaluation code is being prepared and will be released soon.

It will include:

- Data loading
- Model training
- Inference
- Evaluation scripts
- Reproducibility instructions

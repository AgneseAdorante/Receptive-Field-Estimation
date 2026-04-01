# Receptive-Field-Estimation
# Neural Data Science Project 02: Working with Calcium Data

## Overview
This repository contains the code and analysis for Project 02 of the Neural Data Science course. The project investigates whether there is a spatial structure to the location of receptive fields in the visual cortex of mice. The analysis is based on in vivo 2-photon calcium imaging data recorded while mice were performing a visual change detection task.

## Authors
* Agnese Adorante
* Hwajin Shin
* Lucia Gonzalez Anton

## Dataset
The dataset comprises recordings from 189 neurons in the primary visual cortex over 105,968 frames at a 30 Hz sampling rate. The analysis primarily focuses on the locally sparse noise stimulus. 
Data components include:
* Preprocessed calcium activity traces (dF/F)
* Stimulus metadata and 16x28 stimulus frames
* ROI masks for each cell and maximum activity projection
* Running speed and stimulus epoch tables

## Project Pipeline
The analysis is structured around the following processing steps:
* **Pre-processing**: Processing and exploring the raw calcium traces and ROI masks.
* **Spike Inference**: Extracting spike events from the calcium traces using Simple Spike Thresholding, OOPSI, and OASIS methods.
* **Receptive Field (RF) Estimation**: Reconstructing spatial and temporal receptive fields using the Spike-Triggered Average (STA) and Linear-Nonlinear Poisson (LNP) models. Spatial and temporal kernels are extracted using Singular Value Decomposition (SVD).
* **Statistical Testing & Clustering**: Evaluating the spatial structure of receptive fields through dimensionality reduction (PCA, t-SNE) and clustering algorithms like Gaussian Mixture Models (GMM). 

## Bibliography
* OOPSI spikes: [https://github.com/liubenyuan/py-oopsi](https://github.com/liubenyuan/py-oopsi)
* OASIS spikes: [https://github.com/j-friedrich/OASIS](https://github.com/j-friedrich/OASIS)
* RFEst: [https://github.com/berenslab/RFEst](https://github.com/berenslab/RFEst) and [https://github.com/huangziwei/notebooks_RFEst](https://github.com/huangziwei/notebooks_RFEst)
* Allen Institute's Stimulus Set and Response Analysis: [https://community.brain-map.org/t/documentation-brain-observatory/3026](https://community.brain-map.org/t/documentation-brain-observatory/3026)

# GeoAI Hackathon - Top 3 Solution

## Overview

This repository documents my approach and solution for the GeoAI Hackathon, where I secured a Top 3 position on the leaderboard. The objective of the competition was to detect locust breeding grounds using satellite imagery, leveraging geospatial data and deep learning techniques.

## Approach

### Phase 1 - Prithvi 1.0 + InstaGeo Model

Used Prithvi 1.0 as the backbone model combined with the InstaGeo Model.

Replaced Cross Entropy Loss with Focal Loss to better handle class imbalances and hard cases.

Trained for 7 epochs.



#### Why this worked?

Prithvi 1.0 is a proven model for geospatial tasks.

Focal Loss helps in better segmentation by focusing more on hard-to-classify pixels.


### Phase 2 - Fine-tuning Prithvi 2.0 (300M TL)

Switched to Prithvi 2.0 (300M TL) as the backbone.

Fine-tuned the model on our dataset.

Extensively experimented with hyperparameters, adjusting learning rates, batch sizes, and weight decay to optimize performance.



#### Why Prithvi 2.0 (300M TL) was relevant?

Temporal-Spatial Pattern Recognition: Prithvi 2.0 is pre-trained on extensive Earth Observation (EO) data, making it highly effective at capturing temporal and spatial patterns critical for locust habitat prediction.

Transfer Learning Benefits: The model has been trained on diverse remote sensing data, allowing it to generalize well to unseen conditions and different ecological zones.

Multi-Scale Feature Learning: It enhances detection accuracy by analyzing both fine-grained and large-scale patterns in satellite imagery.

Hyperparameter Optimization: By tuning learning rates, batch sizes, and loss functions, we optimized the model’s ability to distinguish between breeding and non-breeding zones.

Better Handling of Temporal Variations: Since locust breeding grounds shift over time, leveraging Prithvi 2.0’s ability to recognize temporal trends improved segmentation robustness.


## Dataset 

The dataset was provided by the organizers and consisted of satellite imagery of Africa. The dataset was divided into training and test sets, with annotations for locust breeding grounds. It can be created and downloaded using the InstaGeo tool provided by InstaDeep.

https://www.kaggle.com/competitions/geo-ai-hack/overview

## Acknowledgment

A huge thanks to the GeoAI Hackathon organizers -InstaDeep, Datacraft and AFD- for providing this opportunity and a challenging dataset. Special thanks to InstaDeep for their contributions in geospatial AI.


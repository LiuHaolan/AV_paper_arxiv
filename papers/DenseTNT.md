# Goal-conditioned trajectory prediction work

## [TNT: Target-driveN Trajectory Prediction](https://arxiv.org/abs/2008.08294)

tl;dr: Model the trajectory prediction uncertainty with intent uncertainty and control uncertainty: intent uncertainty is given by classifying goal anchors and 
regressing the offsets. The control uncertainty is considered unimodal given intents.

## [DenseTNT: End to end Trajectory Prediction from Dense Goal Sets](https://arxiv.org/abs/2108.09640)

tl;dr: Replace the predefined goal sets (sparse goal) in TNT with dense sampled goal to support more refined prediction.

#### Overall impression
The two-sequence goal-conditioned prediction work achieves great performance on Waymo Datasets. However, I have some doubts about the accuracy of the pseudo labels.
Is it diverse enough to capture the real-world goal distribution? 

#### Key ideas
- To model the intent uncertainty, previous work explores intent (requires additional annotation, and also too coarse-grained), anchor trajectories (preclustered from datasets).
Goals are low dimensional (x,y) compared with anchor trajectories, and it's easier to discretized based on expert knowledge (HD Map and navigation)



#### Technical details
- Using VectorNet as feature extractor.
- Unlike object detection, trajectory prediction datasets only have one groundtruth future trajectory. To cope with that, DenseTNT uses an offline optimization procedure to provide pseudo-labels

#### Notes

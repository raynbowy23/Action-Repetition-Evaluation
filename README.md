# Action-Repetition-Evaluation

This is a part of project with Chulalongkorn University in Thailand for action repetition.
Our original goal is counting archery repetition movements.
In this repo, each file are mostly written about analysis and evaluation of repetition.

## Descriptions of each file

At first, please prepare start frame, end frame, and pivot frame, which is the critical point of movement (e.g. the time when person shoot bows) manually.

- difference_images.ipynb
This file is for analysis of video characteristics and frame differences.
Mostly I tried AKAZE feature and BFMatcher, template matching, and heatmap.

- FrechetInceptionDistance.ipynb
In this file, I evaluated frame differences in terms of differences of frame quality (actually the distribution of two frames) since the input video was recorded by a fixed camera.
Thus, I used Frechet Inception Distance (GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium. https://arxiv.org/abs/1706.08500), which is mostly used at evaluation of generated image  by Generative Adversarial Networks (https://arxiv.org/abs/1406.2661).

- dtw_with_manydistances.ipynb
In this file, I used Dynamic Time Warping to compute distances of two frames.

- evaluate_openpose.ipynb
In this file, I used OpenPose and compare human joints of each frames with time dependencies.

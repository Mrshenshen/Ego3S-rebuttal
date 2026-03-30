## R1-W2 (Fig.1)

![Intro](fig\intro1.png)

## R1-W2 (Fig.1)

![Intro](fig\introduction.png)

## Reviewer TNRo
### R1-(W1&W2&Q3) (Tab.1)

| Method | Accuracy on Prior-Aligned Subset |
| :--- | :---: |
| Qwen2.5-VL-7b-GRPO (Full data) | 68.2% |
| Qwen2.5-VL-7b-CSM| 68.2% |
| Qwen2.5-VL-7b-IRL | 69.1% |
Tab.1: Accuracy on the prior-aligned subset, where the ground-truth objects belong to the top 10% most frequent objects shared by COCO and Ego4D.

### R2-W3 (Tab.2)

| Method | Acc. | Mean IoU | R@IoU=0.7 |
| :--- | :---: | :---: | :---: |
| Random Crop | 14.0% | 0.12 | 2.0% |
| Center Crop (Heuristic) | 41.0% | 0.35 | 15.0% |
| **CLIP Sliding Window (Ours)** | **86.0%** | **0.68** | **52.0%** |
Tab.2: Comparison of interaction-region selection methods on 100 manually annotated samples.
.
### R3-Q1 (Tab.3)

| Method | Clean | 10% Mask | 20% Mask | Drop (20% vs. Clean) |
|---|---:|---:|---:|---:|
| GRPO |  |  |  |  |
| **Ego3S** |  |  |  |  |
Tab. 3: Performance under partial occlusion of the interaction region.

## Reviewer oZZ4
### R4-Q3 (Tab.4)

| Training Stage | Method | Proportion of CAWR Instances (%) ↓ |
| :--- | :--- | :---: |
| Initial (Step 0) | Pre-trained Base Model | 14.6% |
| Mid-Training (Step 300) | GRPO Baseline | 18.2% |
| Mid-Training (Step 300) | **Ego3S (IRL with (r_p))** | **8.4%** |
| Final (Step 600) | GRPO Baseline | 21.5% |
| Final (Step 600) | **Ego3S (IRL with (r_p))** | **4.2%** |
Tab.4: Proportion of “Correct Answer, Wrong Reason” (CAWR) cases across training stages, evaluated by GPT-4o on a random subset of 3,000 training samples. Lower is better.


### R5-Q4 (Tab.5)

| Backbone    | Method    | Data Usage | Performance |
| ----------- | --------- | ---------: | ----------: |
| Qwen3-VL-8B | Full      |       100% |             |
| Qwen3-VL-8B | **Ego3S** |  **26.5%** |  \*\*  \*\* |
Tab.5: Performance comparison on the larger backbone Qwen3-VL-8B.


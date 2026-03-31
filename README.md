## <span style="color:blue;">Reviewer XrfR</span>
### R2-W2 (Fig.1)

![time](fig\time.png)



## <span style="color:blue;">Reviewer TNRo</span>
### R1-(W1&W2&Q3) (Tab.1)

| Method | Accuracy (%) |
| :--- | :---: |
| Qwen2.5-VL-7b-Full data | 30.5 |
| **Qwen2.5-VL-7b-CSM**| **32.7** |
| Qwen2.5-VL-7b-GRPO | 30.5 |
| **Qwen2.5-VL-7b-IRL** | **35.4** |
#### Tab.1: Accuracy on the prior-aligned subset of Egoplan2, where the ground-truth objects belong to the top 10% most frequent objects shared by COCO and Ego4D.



### R2-W3 (Tab.2)

| Method | Accuracy (%) | Mean IoU |
| :--- | :---: | :---: |
| Random Crop | 18.0 | 0.07 |
| Center Crop | 27.0 | 0.15 |
| **CLIP-based (Ours)** | **82.0** | **0.58** |
#### Tab.2: Comparison of interaction-region selection methods on 100 manually annotated samples. Accuracy denotes the percentage of samples for which the selected region correctly localizes the interaction region, while Mean IoU measures the average overlap between the selected region and the ground-truth annotation.
.
### R3-Q1 (Tab.3)

| Method | Normal | 10% Masked |
|---|---:|---:|
| Qwen2.5-VL-7b-GRPO | 30.43 | 29.69 |
| **Qwen2.5-VL-7b-Ego3S** | **36.83** | **36.07** |
#### Tab. 3: Performance on Egoplan2 under partial occlusion of the interaction region.



### R3-Q1 (Fig.2)
![reward](fig\reward_normal_noise.png)

## <span style="color:blue;">Reviewer oZZ4</span>
### R4-Q3 (Tab.4)

| Training Stage | Method | Proportion of CAWR Instances (%) ↓ |
| :--- | :--- | :---: |
| Initial (Step 0) | Qwen2.5-VL-7b | 27.1% |
| Mid-Training (Step 300) | Ego3S (IRL without ($r_p$)) | 18.9% |
| Mid-Training (Step 300) | **Ego3S (IRL with ($r_p$))** | **17.4%** |
| Final (Step 600) | GRPO | 20.5% |
| Final (Step 600) | **Ego3S (IRL with (r_p))** | **13.2%** |
#### Tab.4: Proportion of “Correct Answer, Wrong Reason” (CAWR) cases across training stages, evaluated by GPT-5.4 on a random subset of 3,000 training samples. Lower is better.




### R5-Q4 (Tab.5)

| Backbone    | Method    | Data Usage | Performance (%) |
| ----------- | --------- | ---------: | --------------: |
| Qwen3-VL-8B | Full      |       100% |            67.6 |
| Qwen3-VL-8B | **Ego3S** |  **28.3%** |      **69.8** |
#### Tab.5: Performance comparison on QAEgo4D using the larger backbone Qwen3-VL-8B.


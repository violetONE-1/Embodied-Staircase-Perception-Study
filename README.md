# Embodied-Staircase-Perception-Study

Motivation and Objective:
Inspired by the ASCENT framework presented in the paper 'Stairway to Success: An Online Floor-Aware Zero-Shot Object-Goal Navigation Framework via LLM-Driven Coarse-to-Fine Exploration', this project serves as a hands-on exploration, aiming to understand the limitations of 2D semantic models in embodied AI navigation tasks, which is a critical bottleneck in multi-floor autonomous navigation.



Phase1:Baseline (BLIP-Base)
Using the BLIP-Base model as a baseline, I uploaded diverse single-frame inputs and varied prompts. However, the model failed to deliver stable or consistent predictions, highlighting a lack of spatial robustness in zero-shot staircase detection. So after the initial setbacks in Phase 1, I pursued two distinct pathways to enhance the model's predictive accuracy and robustness.


Phase 2:Exploration

PathA:Temporal Consistency
Inspired by the active exploration logic in the ASCENT paper, I implemented Sequential Imagery Experiments (Lab 1 & Lab 3). By moving closer to the stairs step-by-step, I tried to provide the model with movement information to help it distinguish 'up' from 'down'.

PathB:Model Scaling
Upgrading from BLIP-Base to BLIP-Large to get better feature extraction.


Analysis:
However, even after these improvements, the prediction accuracy did not increase as expected. After analyzing the failure, I supposed there are 3 possible reasons:
1.The staircase images accepted by the model during its pre-training are mostly from an upward perspective.
2.2D pixels cannot provide enough spatial information.
3.The model fails to understand the motion between images.

<img width="436" height="132" alt="871b524211118cf36475067dd595513c" src="https://github.com/user-attachments/assets/540e4b56-71d1-48e9-8364-5d2bf29e970a" />


Conclusion:
While the experiment did not achieve high accuracy, it successfully proved the necessity of the ASCENT framework. As a Software Engineering student, this process has deepened my understanding of robust perception and the gap between 2D recognition and 3D spatial navigation in the field of embodied AI.

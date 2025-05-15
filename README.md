# Cluster-Analysis-on-Affect
Using latent profile analysis to examine the associations between different clusters of affect and self-injury.

**Conference Project Title**: Associations Between Latent Profiles of Momentary Affect and Self-Injurious Behaviors
**Authors**: Madeline M. Navea, Jannah R. Moussaoui, April R. Smith, Elizabeth A. Velkoff  
**Conference Presented Work At**: Society for Affective Science 2024  

---

## 🔍 Overview

This project applies cluster analysis techniques to investigate how **momentary affective states** cluster into **latent profiles** and their associations after engaging in **self-injurious behaviors (SIBs)**. Using **Ecological Momentary Assessment (EMA)** data collected over 14 days (N = 124 participants, N ≈ 6600 observations), we aim to identify affective states associated with higher risk for SIBs.

---

## 🧪 Methods

- **Data Type**: EMA with time-indexed affect + SIB reports
- **Participants**: Individuals reporting ≥3 SIBs (non-suicidal self-injury or eating disorder behaviors) in the past month
- **Analysis**:
  - **Latent Profile Analysis (LPA)** performed using `tidyLPA` and `mclust` in R
  - Model convergence issues with covariance structures led to the use of **Model 1 (equal, zero covariance)**
  - Class enumeration guided by the **K+1 rule** and **Analytic Hierarchy Process (AHP)** — profiles must contain ≥10% of sample

---

## 📈 Results

Five latent affective profiles were identified:

| Profile | Description             | Obs Points | Total SIBs |
|---------|--------------------------|------------|------------|
| P1      | Moderate Positive Affect | 2037       | 114        |
| P2      | Moderate Affect          | 865        | 97         |
| P3      | Low Overall Affect       | 2609       | 165        |
| P4      | High Negative Affect     | 463        | 62         |
| P5      | High Positive Affect     | 626        | 34         |

### Key Results:
- As expected, results indicate that SIBs may be habitual in nature, such that many are used to **relieve** affect (i.e., their overall affect goes down to baseline after engaging in a SIB). However, it is interesting to note that P1 (moderate positive affect) reported the second most SIBs for fasting and restricting.
- **P3 (Low Overall Affect)** exhibited the **highest frequency of SIBs**, despite low arousal.
- **P5 (High PA)** reported the **lowest SIB engagement**, suggesting PA may be a protective state.
- Surprisingly, **P1 (Moderate PA)** had the **second-highest SIBs**, implying that moderate PA alone is insufficient to mitigate SIB risk.
- Real-world issues in model convergence happen! This project displays solutions and restraints against using more complex models (sometimes, the more simple, the better!)

---

## 💡 Future Directions

- Next steps I will be taking: running the same model on **pre-SIB affect profiles**, rather than post-SIB.
- Integrate physiological signals or passive data for multimodal modeling.
- Apply **sequence modeling (e.g., HMM, RNNs)** to capture transitions between states over time.

---

## Citation

If you use or adapt this repository, please cite the original authors and conference submission: Navea M.M., Moussaoui J.R., Smith A.R., Velkoff E.A. (Under review). Associations between Latent Profiles of Momentary Affect and Self-Injurious Behaviors. Abstract submitted to the Society for Affective Science, Portland, Oregon. 

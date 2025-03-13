<div align="center">
<h2>Understanding Driver Intention: Enhancing IL Planning with Navigation Path Fusion</h2>

 **Leichen Wang**<sup>1</sup>, **Ziming Liu**<sup>1</sup>, **Ge Yang**<sup>1</sup>, **Yuheng Zhou**<sup>2</sup>, **Xinrun Li**<sup>1</sup>, **Xingtao Hu**<sup>1</sup>, **Dashan Guo**<sup>2</sup>, **Cong Wang**<sup>2</sup>, **Hao Sun**<sup>1</sup>, **Lei La**<sup>2</sup>, **Kevin Sun**<sup>2</sup>, **Lijuan Zhu**<sup>1</sup>, **Jian Zhou**<sup>2</sup> <br>

<sup>1</sup>Bosch Research & Technology Center Asia Pacific, Shanghai, China, <sup>2</sup>Bosch Automotive Products (Suzhou) Co., Ltd.

 **Submitted to IROS 2025** 

[![📄 Paper](https://img.shields.io/badge/Paper-Coming_Soon-blue?logo=arxiv)](https://arxiv.org/) &nbsp;[![🗂️ Navigation Path Dataset](https://img.shields.io/badge/Google%20Drive-Navigation%20Path-green?logo=google-drive)](https://drive.google.com/drive/folders/164XTPvvhoBRIj6E0HfIunPu3KAXj80ZR?usp=sharing) &nbsp;[![🚀 Demo](https://img.shields.io/badge/Demo-Coming_Soon-orange?logo=github)](https://github.com/) &nbsp;

</div>


---

## Overview

Despite impressive progress in imitation-learning (IL)-based planning for autonomous driving, existing frameworks often struggle with:
- **Mode collapse**  
- **Directional deviations**  
These issues result in trajectories that fail to align with **human driving intentions**.
<p align="center">
  <img src="assets/figs/main.png" alt="IL Planners Comparison" width="80%">
</p>

<!-- We identify the **missing link**:  
> 🔎 **Explicit modeling of navigation paths.**  
Navigation paths provide **high-level causal guidance** in human driving, but are often ignored in current planning frameworks.

--- -->


###  What's Missing?

A **key missing link** in current IL planning frameworks is the **explicit modeling of navigation paths**.  
Navigation paths provide **high-level causal guidance**, which humans naturally follow when driving. Without incorporating this crucial information, IL planners are prone to **causal misidentification** and **shortcut learning**.
<p align="center">
  <img src="assets/figs/causal_misidentification.jpg" alt="Causal Misidentification" width="80%">
</p>

---

## ✨ Our Contributions

✅ **Navigation Path Integration in IL Planners**  
- Two simple yet effective frameworks for **anchor-based** and **non-anchor-based** planners.  
- **Navigation paths** are fused as **causal priors**, eliminating mode collapse and directional deviation issues.

✅ **Toolchain for Navigation Path Generation**  
- Automatic extraction of navigation paths from **any dataset**, via our **HMM-based recovery algorithm**.

✅ **Extended NAVSIM Dataset with Navigation Annotations**  
- Released to the community to benchmark navigation-path-enhanced planning.

✅ **Comprehensive Experiments**  
- Multi-baseline comparison  
- Cross-dataset validation  
- Multi-metric assessments (planning accuracy & safety)

---

### Navigation Path Recovery Process  
An overview of our **navigation path generation and recovery pipeline**, from trajectory points to a full navigation path.

<p align="center">
  <img src="assets/figs/data_preparation.jpg" width="100%">
</p>


---
### Method  
We design two frameworks to integrate **navigation paths** into both **anchor-based** and **non-anchor-based** planners.

<p align="center">
  <img src="assets/figs/framework.png" width="100%">
</p>

---
### Comparison of NAVSIM Trajectory and Recovered Navigation Path

The table below presents a comparative visualization of `NAVSIM` trajectories and our recovered navigation path.


| **Scenario**                   | **Visualization (NAVSIM vs. Navigation Path)**                         |
|---------------------------------|-----------------------------------------------------------------------------|
| **Go Straight** | <img src="assets/gifs/straight_sample.gif" alt="Straight Movement Scenario" width="600"> |
| **Left Turn**          | <img src="assets/gifs/left_turn_sample.gif" alt="Left Turn Scenario" width="600"> |
| **Right Turn** | <img src="assets/gifs/right_turn_sample.gif" alt="Right Turn Scenario" width="600"> |
| **Sharp Turn** | <img src="assets/gifs/loop_sample.gif" alt="Loop Scenario" width="600"> |

---

## 📦 Dataset Release

We release our extended datasets for **NavSim** to support the community in research on navigation-path-enhanced planning.

### 🔗 Download Links

  Navigation path annotations for **trainval** and **test** (NavSim benchmark).

[![🗂️ Navigation Path Dataset](https://img.shields.io/badge/Google%20Drive-Navigation%20Path-green?logo=google-drive)](https://drive.google.com/drive/folders/164XTPvvhoBRIj6E0HfIunPu3KAXj80ZR?usp=sharing) &nbsp;

### 📁 Dataset Structure


After extraction, each archive contains four subfolders corresponding to different cities:
```
nav_path_trainval/
├── sg-one-north/
├── us-ma-boston/
├── us-nv-las-vegas-strip/
└── us-pa-pittsburgh-hazelwood/

nav_path_test/
├── sg-one-north/
├── us-ma-boston/
├── us-nv-las-vegas-strip/
└── us-pa-pittsburgh-hazelwood/
```
---
### Qualitative Results 

The figure below compares the original **Diffusion Drive** and our **navigation-path-enhanced Diffusion Drive** on challenging scenes from the **NAVSIM navtest split**. It demonstrates how navigation paths influence anchor trajectories across different driving scenarios.




<p align="center">
    <img src="assets/figs/qualitative_result.jpg" alt="Impact of Navigation Path on Anchor Trajectories" width="100%">
</p>

---
## 📖 Citation
If you find our **paper** or **dataset** helpful, please consider giving us a ⭐ and citing our work:

```bibtex
@misc{wang2025understanding,
    title        = {Understanding Driver Intention: Enhancing IL Planning with Navigation Path Fusion},
    author       = {Leichen Wang and Ziming Liu and Ge Yang and Yuheng Zhou and Xinrun Li and Xingtao Hu and Dashan Guo and Cong Wang and Hao Sun and Lei La and Kevin Sun and Lijuan Zhu and Jian Zhou},
    year         = {2025},
    publisher    = {GitHub},
    howpublished = {\url{https://github.com/LaoWangBosch/Understanding-Driver-Intention-by-Navigation-Path-guided-AI-planning}},
    note         = {Dataset and Code available at GitHub}
}
```
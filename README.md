<div align="center">
<h2>Understanding Driver Intention by Navigation Path guided AI planning</h2>

 **Leichen Wang**<sup>1</sup> ·**Ziming Liu**<sup>1</sup> · **Ge Yang**<sup>1</sup> · **Xingtao Hu**<sup>1</sup> · **Xinrun Li**<sup>1</sup> <br>

<sup>1</sup>Bosch Corporate Research <br>

<!-- > **submitted to IROS 2025** -->

</div>

<!-- >
[\[Arxiv\]](https://arxiv.org/abs/2401.06614) [\[Paper\]](https://arxiv.org/pdf/2401.06614.pdf) [\[Project Page\]](https://[vveicao.github.io/projects/Motion2VecSets/](https://github.com/xiaowang12345/OMG_SD_map_prior_distribution))
-->


<p>
Recent advancements in learning-based planning for autonomous driving have demonstrated promising scalability, yet they often suffer from mode collapse or directional deviations, failing to align with human driving intentions.  We identify a critical gap in existing frameworks: the lack of explicit modeling of navigation paths, leading to causal misidentification in planning tasks.  Inspired by human driving behavior, where navigation paths provide high-level guidance, we propose a novel approach that integrates navigation paths as a guide for trajectory planning.  We introduce two versatile frameworks tailored for anchor-based and non-anchor-based methods, addressing the limitations of current systems.  Additionally, we develop a toolchain for automatic navigation path generation and release an extended dataset with navigation annotations.  Extensive evaluations on the extended NavSim benchmark \textit{ and a newly collected driving dataset} demonstrate significant improvements in planning accuracy and safety, showcasing the robustness and transferability of our approach.
</p>

<p>
We argue that this omission is fundamentally unreasonable. Navigation paths are not only readily available in real-world autonomous driving systems, but they also provide a direct and interpretable way to guide the planning process. Incorporating navigation paths into E2E frameworks offers a straightforward yet powerful solution to the problem of directional deviations in trajectory planning.


To address these challenges and limitations, we propose a new planning methodology titled \textbf{Make E2E Driving Easy Again} A Simple Yet Effective Navigation Path Enhanced Planning Framework. This work builds on the strengths of existing E2E frameworks while addressing their shortcomings by explicitly incorporating navigation paths as a guiding prior for planning.
</p>

---

### Comparison of NAVSIM Trajectory and Recovered Navigation Path

The table below presents a comparative visualization of `NAVSIM` trajectories and our recovered navigation path, computed using the HMM algorithm. 
Each GIF provides a side-by-side comparison, illustrating the differences between the two trajectories across various driving scenarios.


| **Scenario**                   | **Visualization (NAVSIM vs. Navigation Path)**                         |
|---------------------------------|-----------------------------------------------------------------------------|
| **Straight Movement Scenario** | <img src="./gifs/straight_sample1.gif" alt="Straight Movement Scenario" width="600"> |
| **Left Turn Scenario**          | <img src="./gifs/left_turn_sample1.gif" alt="Left Turn Scenario" width="600"> |
| **Right Turn Scenario** | <img src="./gifs/right_turn_sample1.gif" alt="Right Turn Scenario" width="600"> |
| **Loop Scenario** | <img src="./gifs/loop_sample1.gif" alt="Loop Scenario" width="600"> |

---

---

### Impact of Navigation Path on Anchor Trajectories

The figure below illustrates the impact of navigation paths on anchors across different driving scenarios.  
It compares planning results **with and without navigation guidance**, demonstrating how the presence of a navigation path influences trajectory generation.

<p align="center">
    <img src="./figs/traj_gt_match_w_nav_path.png" alt="Impact of Navigation Path on Anchor Trajectories" width="90%">
</p>

---

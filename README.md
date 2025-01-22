<div align="center">
<h2>Make-E2E-Driving-Easy-Again-a-simple-yet-effective-navigation-path-enhanced-planning-methodology</h2>

 **Leichen Wang**<sup>1</sup> ·**Ziming Liu**<sup>1</sup> · **Ge Yang**<sup>1</sup> · **Xingtao Hu**<sup>1</sup> · **Xinrun Li**<sup>1</sup> <br>

<sup>1</sup>Bosch Corporate Research <br>

<!-- > **submitted to IROS 2025** -->

</div>

<!-- >
[\[Arxiv\]](https://arxiv.org/abs/2401.06614) [\[Paper\]](https://arxiv.org/pdf/2401.06614.pdf) [\[Project Page\]](https://[vveicao.github.io/projects/Motion2VecSets/](https://github.com/xiaowang12345/OMG_SD_map_prior_distribution))
-->


<p>
End-to-end (E2E) autonomous driving frameworks have gained significant traction as a unified paradigm for integrating perception, prediction, and planning tasks. Despite their advancements, existing frameworks often suffer from directional deviations in trajectory planning, resulting in unsafe or suboptimal behaviors, particularly in complex scenarios. This paper identifies a critical gap in current E2E approaches: the underutilization of navigation paths, a readily available and interpretable source of driving intent in real-world autonomous systems. To address this limitation, we propose Make E2E Driving Easy Again, a simple yet effective navigation-path-enhanced planning methodology. Our contributions include: (1) introducing navigation paths as explicit priors for trajectory generation, (2) designing a novel planning-navigation interaction mechanism, (3) developing and releasing a toolchain that enriches datasets with navigation path annotations, and (4) demonstrating state-of-the-art performance on multiple benchmarks. Experimental results show that our approach significantly improves trajectory alignment, planning accuracy, and safety in dynamic environments, paving the way for more robust and interpretable E2E driving frameworks.
</p>

<p>
We argue that this omission is fundamentally unreasonable. Navigation paths are not only readily available in real-world autonomous driving systems, but they also provide a direct and interpretable way to guide the planning process. Incorporating navigation paths into E2E frameworks offers a straightforward yet powerful solution to the problem of directional deviations in trajectory planning.


To address these challenges and limitations, we propose a new planning methodology titled \textbf{Make E2E Driving Easy Again} A Simple Yet Effective Navigation Path Enhanced Planning Framework. This work builds on the strengths of existing E2E frameworks while addressing their shortcomings by explicitly incorporating navigation paths as a guiding prior for planning.
</p>

---

### Comparison of NAVSIM Trajectory with our recovered Navigation Path
The following images illustrate a comparison of the visualization of trajectories from NAVSIM with our recovered navigation path based on HMM-algorithm:

---

#### Scenario 1:
<div align="center">
    <img src="./figs/comparison_navsim_with_navigation_path.jpg" alt="Comparison of Navigation with Navigation Path" width="600">
</div>

---

#### Animated Comparison:


- **Left GIF**: NAVSIM Trajectory
- **Right GIF**: Navigation Path

<table>
  <tr>
    <td><img src="./gifs/navsim_sample1.gif" alt="Original SDMap Scenario 4" width="400"></td>
    <td><img src="./gifs/nav_path_sample1.gif" alt="Modified SDMap Scenario 4" width="400"></td>
  </tr>
</table>

---
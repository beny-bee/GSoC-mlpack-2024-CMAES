<h2 align="center">
  <a href="http://ensmallen.org/"><img src="http://ensmallen.org/img/ensmallen_text.svg" style="background-color:rgba(0,0,0,0);" height=230 alt="ensmallen: a C++ header-only library for numerical optimization"></a>
</h2>

**Organisation: [mlpack](https://github.com/mlpack)**

**Project: [Integrating Advanced CMA-ES Strategies into mlpack](https://summerofcode.withgoogle.com/programs/2024/projects/Ktk40cAi)**

**Mentors: [Marcus Edel](https://github.com/zoq)**

## Abstract
mlpack is a fast, open-source, flexible C++ machine learning library aiming to provide fast, extensible implementations of cutting-edge machine learning algorithms.
This project focused on enhancing the Covariance Matrix Adaptation Evolution Strategy (CMA-ES) algorithm within mlpack (specifically the ensmallen library) by implementing advanced variants and improving its robustness.


## Goal

1. **[Implement the Increasing Population size CMA-ES (IPOP-CMA-ES) variant](http://www.cmap.polytechnique.fr/~nikolaus.hansen/cec2005ipopcmaes.pdf)**: Create a new function for the IPOP-CMA-ES.
  
2. **[Implement the Bi-population CMA-ES (BIPOP-CMA-ES) variant](https://dl.acm.org/doi/pdf/10.1145/1570256.1570333)**: Even though not initially planned, implementing BIPOP-CMA-ES was relatively easy after setting up IPOP. This variant introduces an interlaced strategy with two mechanisms to change the population size. One similar to IPOP and another that uses a smaller, varying population size.

3. **Enhance the termination criteria for CMA-ES**: Also not originally planned, but after some literature review ([A Restart CMA Evolution Strategy With Increasing Population Size](http://www.cmap.polytechnique.fr/~nikolaus.hansen/cec2005ipopcmaes.pdf) and [The CMA Evolution Strategy: A Tutorial](https://arxiv.org/pdf/1604.00772)), it became apparent to ensure the robustness and correctness the CMA-ES and its variants.

4. **[Implement the Self-Adaptive Surrogate-Assisted CMA-ES (saACM-ES) variant](https://arxiv.org/abs/1204.2356)**: Create a new function for saACM-ES. While this was part of the original plan, it has been left for future work due to the need for several prerequisite components.

## Contributions 

Here is the list of PRs (both open & closed) that I created during GSoC.

| PULL REQUESTS                                             | COMMITS                                                                                                                                                                                                                                                                                                                    | DESCRIPTION                                                                                                                                                                                                                                                                                        | STATUS         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| [#401](https://github.com/mlpack/ensmallen/pull/401) | - [3e96c67](https://github.com/mlpack/ensmallen/commit/3e96c67f16a77df95ad70c36fdc46d21abb57be4) <br> - [c5f103b](https://github.com/mlpack/ensmallen/commit/c5f103b129a3251687b24ae34ed38e7e4e5f7cbe) <br> - [718d1c1](https://github.com/mlpack/ensmallen/commit/718d1c1f40db24c62430e624f2303761745f8f13) <br> - [baf07d9](https://github.com/mlpack/ensmallen/commit/baf07d93f94ef2c546f70452953aea883a7043a7) <br> - [e8f21e7](https://github.com/mlpack/ensmallen/commit/e8f21e719fa997bf11fb2345895161ae6482e687) <br> - [ac8adca](https://github.com/mlpack/ensmallen/commit/ac8adcaaefb0c03129112405d9b8252105e575bf) <br> - [5950e89](https://github.com/mlpack/ensmallen/commit/5950e89fe6a4ea68d45dba6f495de5603bcaf6ec) | Implementation of various stopping conditions for the CMA-ES algorithm, such as stopping based on maximum iterations, target objective value, function evaluation limits, tolerance on function value, fitness stagnation, and several other criteria to ensure robust and reliable convergence. | ![status](https://via.placeholder.com/15/00FF00/000000?text=+) Open |
| [#403](https://github.com/mlpack/ensmallen/pull/403) | - [0a5d061](https://github.com/mlpack/ensmallen/commit/0a5d0611332a029bd69d490b99048f4e9a55f3bc) <br> - [2e3f7db](https://github.com/mlpack/ensmallen/commit/2e3f7db7b8cc2a45b1fce7a51ad4fd98c58e7bfc) <br> - [4abc15d](https://github.com/mlpack/ensmallen/commit/4abc15d68d5cc886f8cdd5c720105e6251d5e3de) <br> - [723b623](https://github.com/mlpack/ensmallen/commit/723b62338f98bddbc48409a7a10b998aa3b33353) <br> - [8f5ce22](https://github.com/mlpack/ensmallen/commit/8f5ce2239b64d523d44efe50b7404650b7630ade) <br> - [a6fd0ff](https://github.com/mlpack/ensmallen/commit/a6fd0ff5479f68343c79bb8292bc46b9493fcaef) <br> - [16b0be1](https://github.com/mlpack/ensmallen/commit/16b0be12dde945e287ae8e498f635e4030d5090c) <br> - [3dfe373](https://github.com/mlpack/ensmallen/commit/3dfe37327e232af3156ae46a588511fbbed8e491) <br> - [6d369f3](https://github.com/mlpack/ensmallen/commit/6d369f3b2d01003dc653bcfdc6f27bd4b3c2ee93) <br> - [4622470](https://github.com/mlpack/ensmallen/commit/4622470d8a9ea876844ba1a6f1c3fc7ecfea5fc1) <br> - [1d2dd1e](https://github.com/mlpack/ensmallen/commit/1d2dd1ed039290fb3e8352346b38f47f2e2c9121) <br> - [541c6be](https://github.com/mlpack/ensmallen/commit/541c6be986099b0b1431ab4653f741f82a1a1c9b) <br> - [2c14b7d](https://github.com/mlpack/ensmallen/commit/2c14b7de3a68bb8c77069e76d5057d7009620c78) <br> - [6d58cfd](https://github.com/mlpack/ensmallen/commit/6d58cfd91d47cba67a7d8f5b4e23de82674fd2a6) <br> - [66d9f19](https://github.com/mlpack/ensmallen/commit/66d9f190044fd53a6b35866ec5d10ab0f3b930a1) <br> - [3316077](https://github.com/mlpack/ensmallen/commit/33160772e98284ae27041e972bbe5039629fe48c) <br> - [1103561](https://github.com/mlpack/ensmallen/commit/1103561c731524fdc0710f9a506c20f7f40ece35) <br> - [aba89da](https://github.com/mlpack/ensmallen/commit/aba89da4a36960df1cc74113728c654a4bfff33f) <br> - [2508bb1](https://github.com/mlpack/ensmallen/commit/2508bb145a0381a0a52478755a70fed9b00c2fa4) <br> - [762fab9](https://github.com/mlpack/ensmallen/commit/762fab94c597eefc9cfb1e0b08b99fb30496d5eb) <br> - [942bc37](https://github.com/mlpack/ensmallen/commit/942bc371001cf45fc19377e5cb07a8fa4363243e) <br> - [8a257b5](https://github.com/mlpack/ensmallen/commit/8a257b5067889e59119601a87a5e707418596170) <br> - [4d880bb](https://github.com/mlpack/ensmallen/commit/4d880bb53be0345482f17d7642e2b2e52dc8bd92) <br> - [6bb6af4](https://github.com/mlpack/ensmallen/commit/6bb6af403949bf945a0e69853a1409d79321a666) <br> - [bdbdc01](https://github.com/mlpack/ensmallen/commit/6bb6af403949bf945a0e69853a1409d79321a666) <br> - [bdbdc01](https://github.com/mlpack/ensmallen/commit/bdbdc01cbb19503646eeddf58dde878671aa7284) | IPOP introduces a strategy of increasing population size after each optimizer restart to enhance global search. BIPOP combines this with a dual strategy of varying population sizes, optimizing performance across different types of objective functions.                                                                         | ![status](https://via.placeholder.com/15/00FF00/000000?text=+) Open |



## Evaluation metrics

In the context of evolutionary algorithms and its variants, evaluating performance across different optimization tasks is crucial. The following images illustrate the effectiveness of the mlpack's implementation on two benchmark functions: Rastrigin and Rosenbrock.

### CMA-ES
<div style="display: flex; justify-content: center; align-items: center; gap: 10px; padding: 10px; border: 2px solid #ddd; margin-bottom: 20px;">
    <img src="src/Rastrigin_CMAES.png" alt="Rastrigin CMA-ES" width="300">
    <div style="border-left: 2px solid #ccc; height: 300px;"></div>
    <img src="src/Rosenbrock_CMAES.png" alt="Rosenbrock CMA-ES" width="300">
</div>

### Active CMA-ES
<div style="display: flex; justify-content: center; align-items: center; gap: 10px; padding: 10px; border: 2px solid #ddd; margin-bottom: 20px;">
    <img src="src/Rastrigin_ActiveCMAES.png" alt="Rastrigin Active CMA-ES" width="300">
    <div style="border-left: 2px solid #ccc; height: 300px;"></div>
    <img src="src/Rosenbrock_ActiveCMAES.png" alt="Rosenbrock Active CMA-ES" width="300">
</div>

### IPOP-CMA-ES
<div style="display: flex; justify-content: center; align-items: center; gap: 10px; padding: 10px; border: 2px solid #ddd; margin-bottom: 20px;">
    <img src="src/Rastrigin_IPOP_CMAES.png" alt="Rastrigin IPOP-CMA-ES" width="300">
    <div style="border-left: 2px solid #ccc; height: 300px;"></div>
    <img src="src/Rosenbrock_IPOP_CMAES.png" alt="Rosenbrock IPOP-CMA-ES" width="300">
</div>

### BIPOP-CMA-ES
<div style="display: flex; justify-content: center; align-items: center; gap: 10px; padding: 10px; border: 2px solid #ddd;">
    <img src="src/Rastrigin_BIPOP_CMAES.png" alt="Rastrigin BIPOP-CMA-ES" width="300">
    <div style="border-left: 2px solid #ccc; height: 300px;"></div>
    <img src="src/Rosenbrock_BIPOP_CMAES.png" alt="Rosenbrock BIPOP-CMA-ES" width="300">
</div>

## Future plans 

0. **Merge the ongoing PRs**: [#403](https://github.com/mlpack/ensmallen/pull/403) and [#401](https://github.com/mlpack/ensmallen/pull/401). There are some complications for 403 that need to be addressed or simplified prior to pushing, but 401 is ready.
1. **saACM-ES Implementation**: The implementation of Self-Adaptive Surrogate-Assisted CMA-ES (saACM-ES) has been postponed for future work. This is due to the need for several prerequisite components:
   - Kernelized SVM implementation
   - Modified kernelized SVM for ranking
2. **Ongoing Maintenance**: Continued work on addressing any issues that arise in the CMA-ES implementation.

## Acknowledgement 
I want to express my gratitude to my mentor, Marcus Edel and the entire mlpack community for their constant support and guidance throughout this project. Their patience and suggestions were invaluable in overcoming challenges and pushing the project forward.

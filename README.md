# Intra-sensitivity (To be completed) 


**From regional sensitivity to intra-sensitivity for parametric analysis of free-form shapes: Application to a ship design**

[Shahroz Khan](https://www.shahrozkhan.info/)\*, [Panagiotis Kaklis](https://www.strath.ac.uk/staff/kaklispanagiotisprof/)

[[Paper]](-) [[Presentation]](-) [[Video]](-)


## Overview

This repository contains Matlab and C++ implementation of the algorithm framework of the proposed intra-sensitivity approach. 

### Extended Abstract
Parametric Sensitivity Analysis (PSA) investigates the sensitivity of parameters, defining the design space of a shape-optimisation problem, for tackling the challenges of the curse of dimensionality or decreasing the uncertainty in design’s performance. This is critical for complex engineering problems, especially those involving free-form shapes. Among the difficulties a robust PSA has to handle is related to the fact that a parameter can be sensitive within a certain local region of the design space but become insensitive in some other regions. Therefore, setting an applicable design space becomes a difficult and unnerving task for robust and desired results. As sensitivity analysis within a non-viable design space can be futile; either resulting in the elimination of an important parameter during dimension reduction or wastage of computational resources if uncertainty reduction is carried out with inaccurately classified sensitive parameters.

In this paper, we introduce the concept of intra-sensitivity to identify parameters whose perturbation in the range generates the largest inconsistency in the sensitivity of other parameters. For this purpose, we firstly develop and perform an ASM-based (Active Subspace Method [1]) regional sensitivity analysis, which investigates parametric sensitivity in local regions of the overall design space.  The results of regional analysis are then used to conduce parameters’ intra-sensitivity as they provide adequate information on how perturbing a parameter's range affects the sensitivity of itself and the remaining parameters. Once identified, intra-sensitive parameters can be tuned further to construct a viable design space, thereby avoiding uncertainty in the sensitivity results. The regional analysis has been applied in conjunction with a Dynamic Propagation Sampling approach, for tackling the computational complexity arising when high-dimensional problems are concerned. After identifying sensitive and intra-sensitive parameters, their impact on design geometry is assessed with the aid of a feature saliency map build with a Hausdorff distance-based approach aiming to identify the sensitive and intra-sensitive geometrical features or regions of geometry. This feature identification can also assist designers to compare different types of free-form parametrisations. 

The above contributions yielded a complete pipeline for studying and analysing the regional behaviour of parametric sensitivity of free-form shape. The performance of this pipeline is validated with an application in the area of computer-aided ship design using two parametric modellers (PM): a PD-based (Procedural Deformation) PM structured with T-splines [2, 3] and an FFD-based (Free-Form Deformation [4]) PM involving 24 and 104 geometrical parameters, respectively. The corresponding design spaces have been generated using as parent hull the KCS containership [5], which is extensively used for CAD and CFD experimentation in the Naval Architecture community. The volume displacement (∇) and the total resistance (R_T) of the model are taken as QoI’s (Quantities of Interest). Finally, the robustness and convergence performance of the component of this pipeline is compared with the state-of-the-art techniques.

[1] Constantine, P. G. (2015). Active subspaces: Emerging ideas for dimension reduction in parameter studies. Society for Industrial and Applied Mathematics.

[2] Kostas, K. V., Ginnis, A. I., Politis, C. G., & Kaklis, P. D. (2015). Ship-hull shape optimization with a T-spline based BEM–isogeometric solver. Computer Methods in Applied Mechanics and Engineering, 284, 611-622.

[3] Katsoulis, T., Wang, X., & Kaklis, P. D. (2019). A T-splines-based parametric modeller for computer-aided ship design. Ocean Engineering, 191, 106433.

[4] Sederberg, T. W., & Parry, S. R. (1986, August). Free-form deformation of solid geometric models. In Proceedings of the 13th annual conference on Computer graphics and interactive techniques (pp. 151-160).

[5] http://www.simman2008.dk/KCS/container.html

## Acknowledgement 
**This work received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant "[GRAPES](http://grapes-network.eu/): learninG, pRocessing And oPtimising shapES" (agreement No. 860843).**

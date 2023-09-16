# 453VulkanStarter

This repository contains starter code that you can use for homework assignments in CPSC 453 (Introduction to Computer Graphics) at the University of Calgary.

It is based on the [VulkanLaunchpadStarter](https://github.com/cg-tuwien/VulkanLaunchpadStarter) repository from TU Wien, which in turn is based on [VulkanLaunchpad](https://github.com/cg-tuwien/VulkanLaunchpad). `VulkanLaunchpad` is a framework by TU Wien targeted at Vulkan beginners. It abstracts some of the hard and overly verbose parts of the Vulkan C API.

## Setup

1. Clone this repository and switch to this branch.
2. `VulkanLaunchpadStarter` and its dependencies are added to this repository as submodules. Please update submodules by issuing the following command:
    ```bash
    git submodule update --init --recursive
    ```  
3. The code in this repository is tested with the following commit hash for `VulkanLaunchpadStarter`:
    - `63d91d5855e5ceaed3babee7bec4fe28f5c968d1`
   
   If needed, roll back the submodule to the above commit by issuing the following command in the `VulkanLaunchpadStarter` directory:
   ```bash
    git checkout <commit hash>
   ```
4. Prior to compiling, please change the primitive topology in the basic graphics pipeline provided by VulkanLaunchpad to line strips. Please see the comments in `HW1/src/LineGeometry.cpp` for details.    

3. Compile via CMake. Please review the [Setup Instructions](https://github.com/cg-tuwien/VulkanLaunchpad#setup-instructions) for `VulkanLaunchpadStarter` to setup your IDE and build environment.

## Available Examples and Skeletons

This repository branch consists of the following:
- `/HW1`:

  A fully functioning example that renders the polar plot $r = 0.8\,\cos(2\theta)$ in 2D in the 
  canonical Vulkan coordinate system where $-1 \le x \le 1$ and $-1 \le y \le 1$. For rendering, the plot is sampled at equally-spaced $\theta$ intervals and the resulting points (in Cartesian coordinates) are connected via line strips.
  In this example, all point geometry is created and managed on the CPU. Transformations are also handled on the CPU. The point geometry is sent over to the GPU for drawing as line strips.

  Transformations consist of simple translations in the $x$ and $y$ directions that are controlled
  by the cursor keys. The drawing wraps around when the center of the plot reaches the edge of the window.


  This example serves as the starter code for HW1 in CPSC 453 (Introduction to Computer Graphics) at the University of Calgary.
  
  
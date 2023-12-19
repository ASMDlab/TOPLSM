## TOPLSM
![Github Star](https://img.shields.io/github/stars/xwpken/Test)
![Github Fork](https://img.shields.io/github/forks/xwpken/Test)

MATLAB codes for topology optimization design using the paramterized level-set method.

<p align="middle">
  <img src="imag/opt_Hex8.gif" width="360" />
  <img src="imag/opt_Tet4.gif" width="360" />
</p>


## Overview
This project contains the codes for 3D topology optimization design using the parameterized level-set method, which is developed by the *Advanced Strcuture and Material Design ([ASMD Lab](https://www.x-mol.com/groups/wei_peng?lang=en))* at the *South China University of Technology ([SCUT](https://www.scut.edu.cn/en/))*.

The current codes only consider the minimum compliance design under linear elastic assumptions. However, it is easy to extend them to design problems of other disciplines, such as the compliant mechanisms and metamaterials. The basic codes for 2D minimum compliance design can be found from the appendix of this [educational paper](https://link.springer.com/article/10.1007/s00158-018-1904-8).

For more information about the basic theory and latest development of the parameterized level-set method, we recommend users to visit [our website](https://www.x-mol.com/groups/wei_peng?lang=en). If you have any questions related to these codes, please feel free to contact us through this GitHub account or directly communicate with Prof. Peng Wei (ctpwei@scut.edu.cn), the leader of this project.


### Update
The latest version is updated on **Dec 19, 2023**

## How to start

There are two folders in `src/`, which are `Hex8` and `Tet4`, respectively. The former contains the codes for optimization design problem with hexahedral elements (8 nodes) and the latter is for tetrahedral elements (4 nodes).

Each folder contains three MATLAB files `(.m)`:
* `Topo_PLSM_3D.m`: the main program; 
* `Topo_FEA.m`: the function for finite element analysis;
* `Topo_Post.m`: the function to output the optimization results;

Two MATLAB data files `(.mat)` are also necessary to define the mesh data and the boundary conditions:

* `xxxx_Mesh.mat`: the mesh data file that stores node coordinates and nodes of each element;
* `xxxx_BCs.mat`: the boundary condition data file that stores the nodes with displacement constraints and applied loads.

Just open the `Topo_PLSM_3D.m`, set the parameters, and run it. The results will be saved in automatically genertaed folder `results/`, including the optimization results `(.jpg & .vtk)` for each step, as well as the files `(.txt)` for the objective function and the material volume fraction.



## Citations

If you find these codes helpful, we would appreciate it if you could cite the following articles:

```bibtex

@article{wei201888,
  title={An 88-line MATLAB code for the parameterized level set method based topology optimization using radial basis functions},
  author={Wei, Peng and Li, Zuyu and Li, Xueping and Wang, Michael Yu},
  journal={Structural and Multidisciplinary Optimization},
  volume={58},
  pages={831--849},
  year={2018},
  publisher={Springer}
}

@article{wei2020parameterized,
  title={A parameterized level set method combined with polygonal finite elements in topology optimization},
  author={Wei, Peng and Paulino, Glaucio H},
  journal={Structural and Multidisciplinary Optimization},
  volume={61},
  number={5},
  pages={1913--1928},
  year={2020},
  publisher={Springer}
}
```

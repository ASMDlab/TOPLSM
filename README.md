## TOPLSM
![Github Star](https://img.shields.io/github/stars/ASMDlab/TOPLSM)
![Github Fork](https://img.shields.io/github/forks/ASMDlab/TOPLSM)

MATLAB codes for topology optimization design using the paramterized level-set method.

<p align="middle">
  <img src="imag/opt_Quad4.gif" width="360" />
  <img src="imag/opt_Tri3.gif" width="360" />
</p>
<p align="middle">
  <em>2D examples</em>em>
</p>

<p align="middle">
  <img src="imag/opt_Hex8.gif" width="360" />
  <img src="imag/opt_Tet4.gif" width="360" />
</p>
<p align="middle">
  <em>3D examples</em>em>
</p>

## Overview
This project contains the codes for 2D and 3D topology optimization design using the parameterized level-set method, which is developed by the *Advanced Strcuture and Material Design ([ASMD Lab](https://www.x-mol.com/groups/wei_peng?lang=en))* at the *South China University of Technology ([SCUT](https://www.scut.edu.cn/en/))*.

The current codes only consider the minimum compliance design under linear elastic assumptions. However, it is easy to extend them to design problems of other disciplines, such as the compliant mechanisms and metamaterials. The basic theories of the parameterized level set method and the instructions for the 2D codes can be found from this [educational paper](https://link.springer.com/article/10.1007/s00158-018-1904-8).

For more information about the latest development of the parameterized level-set method, we recommend users to visit [our website](https://www.x-mol.com/groups/wei_peng?lang=en). If you have any questions related to these codes, please feel free to contact us through this GitHub account or directly communicate with Prof. Peng Wei (ctpwei@scut.edu.cn), the leader of this project.


### Update
The latest version is updated on **Dec 19, 2023**

## How to start

There are two folders in `src/`, which are `2D/` and `3D/`, respectively. `2D/` contains the codes for optimization design problem with 4 nodes quadriliteral elements (`Quad4/`), and `3D/` contains the codes with 8 nodes hexahedral elements (`Hex8/`)  and 4 nodes tetrahedral elements (`Tet4/`).

For the use of codes in `2D/`, you can check this [educational paper](https://link.springer.com/article/10.1007/s00158-018-1904-8).

Each folder in `3D/` contains three MATLAB files `(.m)`:
* `Topo_PLSM_3D.m`: the main program; 
* `Topo_FEA.m`: the function for finite element analysis;
* `Topo_Post.m`: the function to output the optimization results;

Two MATLAB data files `(.mat)` are also necessary to define the mesh data and the boundary conditions:

* `xxxx_Mesh.mat`: the mesh data file that stores node coordinates and nodes of each element;
* `xxxx_BCs.mat`: the boundary condition data file that stores the nodes with displacement constraints and applied loads.

Just open the `Topo_PLSM_3D.m`, set the parameters, and run it. The results will be saved in automatically genertaed folder `results/`, including the optimization results `(.jpg & .vtk)` for each step, as well as the files `(.txt)` for the objective function and the material volume fraction.



## Citations

If you use these codes for research purposes, please cite the following articles:

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

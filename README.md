[![Operations Research Journal Logo](https://orjournal.github.io/OperationsReseachHeader.jpg)](https://pubsonline.informs.org/journal/opre)

# Learning in Inverse Optimization: Incenter Cost, Augmented Suboptimality Loss, and Algorithms

This archive is distributed in association with the journal [Operations Research](https://pubsonline.informs.org/journal/opre) under the [MIT License](LICENSE).

The software and data in this repository are a snapshot of the software and data that were used in the research reported in the paper [Learning in Inverse Optimization: Incenter Cost, Augmented Suboptimality Loss, and Algorithms](https://doi.org/10.1287/opre.2023.0254) by Pedro Zattoni Scroccaro, Bilge Atasoy, and Peyman Mohajerin Esfahani.

## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/10.1287/opre.2023.0254

https://doi.org/10.1287/opre.2023.0254.cd

Below is the BibTex for citing this snapshot of the repository.

```
@misc{zattoniscroccaro2023learning,
  author =        {Zattoni Scroccaro, Pedro and Atasoy, Bilge and Mohajerin Esfahani, Peyman},
  publisher =     {Operations Research},
  title =         {{Learning in Inverse Optimization: Incenter Cost, Augmented Suboptimality Loss, and Algorithms}},
  year =          {2024},
  doi =           {10.1287/opre.2023.0254.cd},
  note =           {Available for download at https://github.com/ORJournal/2023.0254},
}  
```

## Description

The goal of this repository is to replicate the numerical experiments in the paper "Learning in Inverse Optimization: Incenter Cost, Augmented Suboptimality Loss, and Algorithms" by Pedro Zattoni Scroccaro, Bilge Atasoy, and Peyman Mohajerin Esfahani.

## Dependencies

The code in this repository requires the following dependencies. The dependency version number corresponds to the version of the package with which the code was tested.

- [Python](https://www.python.org/) - 3.10.11
- [NumPy](https://numpy.org/) - 1.26.4
- [gurobipy](https://www.gurobi.com/) - 11.0.1. **Note**: to use Gurobi, you need a valid license. You can get a free academic license [here](https://www.gurobi.com/academia/academic-program-and-licenses/).
- [matplotlib](https://matplotlib.org/) - 3.8.4
- [polytope](https://tulip-control.github.io/polytope/) - 0.2.5
- [CVXPY](https://www.cvxpy.org/) - 1.4.3
- [scikit-learn](https://scikit-learn.org/stable/) - 1.4.2

## Installation

1. Install [Python](https://www.python.org/) 3.10.11 or current stable v3.10
2. Create a [virtual environment](https://docs.python.org/3.10/library/venv.html) and activate it
3. Upgrade pip: `python -m pip install --upgrade pip`
4. Install dependencies: `python -m pip install -r requirements.txt`

## Replicating results

The scripts are located in the `scripts` folder, the source code for the algorithms and methods developed in the paper is located in the `src` folder, and the data is located in the `data` folder. The plots with the results from the scripts are saved in the `results` folder.

- To replicate the results in Section 6.1, as well as their respective results in Appendix D.2, run the script `experiments_6_1_consistent_data.py`.
- To replicate the results in Section 6.2, as well as their respective results in Appendix D.2, run the script `experiments_6_2_inconsistent_data.py`.
- To replicate the results in Section 6.3, as well as their respective results in Appendix D.2, run the script `experiments_6_3_mixed_integer.py`.
- To replicate the results of Figure 6a  in Section 6.4, as well as the results in Appendix D.3, run the script `experiments_6_4_SAMD.py`.
- To replicate the results of Figure 6b  in Section 6.4, run the script `experiments_6_4_SAMD_batches.py`. 
- To replicate the results of Appendix D.1, run the script `experiments_AD_1_BCWP.py`. **Note**: to generate the rusults in the paper, we used `cvxpy` with MOSEK as the solver. You can get a free MOSEK academic license [here](https://www.mosek.com/products/academic-licenses/). In case you do not have a MOSEK license, `cvxpy` will use an open-source solver, e.g., [SCS](https://www.cvxgrp.org/scs/).

**Note**: the exact results from `experiments_6_4_SAMD.py` and `experiments_6_4_SAMD_batches.py` depend on the runtime of each iteration of the SAMD algorithm, thus, they will change for different hardware specifications. The results shown in the paper were computed using 1 thread of an Intel Xeon Gold 5218 CPU with a 2.30GHz clock speed and 32GB of RAM.

**Warning 1**: the scripts in the `scripts` folder use a relative path to import from the `src` and `data` folders. 

**Warning 2**: it may take hours to replicate some of the results in the paper. Tables 1, 2, and 3 in the paper show an estimate of the time required to replicate the results of Sections 6.1, 6.2, and 6.3. To quickly test the scripts in simpler examples, change the simulation parameters in the scripts to reduce the number of tested approaches, decrease the size of the datasets, the dimensions of the problem, the resolution of the plots, and/or the number of runs (i.e., the number of times the experiment is repeated).  

## Ongoing Development

This code is being developed on an ongoing basis at the author-maintained [InvOpt](https://github.com/pedroszattoni/InvOpt) Python package. In particular, the source code in the `src` folder corresponds to `invopt 0.0.7`.

## Support

For support in using this software, submit an issue [here](https://github.com/pedroszattoni/InvOpt/issues/new).
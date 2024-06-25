# Contribute to this repository

In order to contribute to this repository: 

1. **Retrive this repository**: Clone the repository as follows.

```bash
git clone -b solutions https://github.com/Talan-TechForData/datascience-solutions.git && cd datascience-solutions
```

**Note:** This will place you within the corresponding branch that contains all solutions. 

**Start within this branch and in this repositroy! (solutions), the final part of this procedure will tell you how to migrate your file into the problems repository for public access**

The procedure of developpment is as follows:
    - First you will start conceiving a notebook containing the problem formulation as well as the solutions (`solution.ipynb`).
    - Once the solutions notebook is executable you can create the notebook problem called (`problem.ipynb`)
    - Both problems will be commited within the solutions branch, once ready only the `problem.ipynb` will be moved to the main branch

2. **Setup environment** You can create a setup environment if you will in order to provide a set of packages. (Ensure a poetry installation)

```
poetry install
```

**Note** In case your package is already installed See dependencies in this [file](../pyproject.toml). Project dependencies are handled via a `poetry` so please add the new packages via `poetry add <package_name>` respecting the convention naming for versioning as [here](https://python-poetry.org/docs/dependency-specification/).

**Note**: Web environments created on Google Colab or MyBinder do not have the dependency setup that is shown here so please ***remind the candidate installations that are required***

3. Once your installation has been finished please `COPY` the notebook `sample_solution.ipynb` in this folder to the corresponding destination folder.

**Note**: Create a destination folder for your particular problem (For example `2_classical_machine_learning/<my_problem_name>`, for a problem dedicated to ML, please change `<my_problem_name>` to a short phrase that can be used as a reference). Within the repository and for each problem the folder `data` inside `<my_problem_name>` denotes the place where data is living. Place here all files required to execute and run your problem.

4. **Poupulate data** Populate your folder `data`. Current formats included in LFS (json/csv/parquet/parquet.gz), for other formats add your data via LFS. See here for more details [Install and Use LFS](https://git-lfs.com)

5. **Rename your notebook** Change the name of the notebook ``<sample_solution.ipynb>` to `<solution.ipynb>` and start writting your problem jointly with the solution. The main recommendation is to guide the user so that they can look for the information coherently. Propose a context and a motivation for your problem and the ideas of the challenge within the solution of this problem. The objective is also to keep candidates motivated at the moment of test.

6. **Clean you notebook** Please ensure that your notebook is executed completely and that you provide an objective way to qualify the answer this can be using markdown notes or explicitly mentioning the expected answer is. (See [solutions.ipynb](sample_solution.ipynb) for details)

7. **Create your problem**: Copy your `solutions.ipynb` file into a new file called `problem.ipynb`. This file will be edited to be the one read by the candidate so, the main objective will be to clear out expected answers that can be directly embedded into the files.

8. **Edit metadata for online execution** Once your `problem.ipynb` notebook is created edit the header of the notebook (See [problem.ipynb](sample_problem.ipynb) for details). In this case the main modification concerns the possibility to execute the pyhton instance from web services provided by third parties. Two proposals are given for the candidates to run their notebooks in case they do not dispose from local environments. 1. Use [Google Colab](colab.research.google.com/) 2. Use [Binder](http://mybinder.org). For this to work modify the snippet of code as follow: 

```
# Will run the notebook problem located at 1_exploratory_data_analysis/taxinyc_analysis/problem.ipynb on mybinder.org
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Talan-TechForData/datascience-questions/HEAD?labpath=1_exploratory_data_analysis/taxinyc_analysis/problem.ipynb) 
# Run the same notebook but instead in Google Colab
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aladinoster/datascience-questions/blob/main/1_exploratory_data_analysis/taxinyc_analysis/problem.ipynb) # Will run the notebook 1_exploratory_data_analysis/taxinyc_analysis/problem.ipynb
```
```

For more information on how to use [Google Colab with GitHub](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb).

9. Once you have edited this 
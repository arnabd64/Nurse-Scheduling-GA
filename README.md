# Nurse Scheduler using Genetic Algorithm

# Project Objective

Solve the **Nurse Shift Scheduling** or **Rostering** problem using genetic algorithm. In a Hospital, each nurse, for each day of the week, is assigned a predefined shift or multiple shifts by the Hosiptal Admin department. 

We have to consider **Hard constraints** that are needed to be met all costs like a nurse cannot take back to back shifts, which means a nurse cannot be assigned two consecutive shifts in a single day or the last shift of a day and the first shift of the next day.

We also have to consider **Soft Constraints** like personal shift preferences of nurses. Every nurse has the option choose one or multiple shifts per day. If a nurse chooses multiple shifts per day, it does not necessarily mean they are willing to work multiple shifts a day but rather conveys flexibility of work. In our case, a nurse has to choose atleast a single shift per day. 

# Nurse Shift Preference constraint

As a reader, the benefit of using my algorithm is that I am taking into account the nurse preferences as a soft constraint. I am not setting it as a hard constraint because I think when scaling up to hospitals with many nurses (10 - 15+) it becomes very difficult to satisfy each of the nurses' preference and we have to sacrifice nurse satisfaction in order to generate an optimal schedule. 

Adding nurse preference as **Soft Constraint** enables a balance between nurse satisfaction and an optimal schedule.

# Minimum external packages

Although there exists python frameworks for genetic algorithms like `deap` and `PyGAD`. I would like to take the difficult road and build the algorithm entire from scratch using the basic libraries like `numpy` and `PyYAML`.

Using minimum number of packages can help this project to be executed in various different platforms with negligible risks of dependency conflict.

* `numpy==1.26` will be needed for faster vectorized computations
* `PyYAML` for loading configuration files written in YAML.

# Project Setup on local machine

## Using `uv`

> *This is the recommended method*

```bash
# clone repo
$ git clone https://github.com/arnabd64/Nurse-Scheduling-GA.git workshift

# cd into project directory
$ cd workshift

# install environment
$ uv sync --no-cache
```

## Using `conda` or `pip`

> For `conda` users, Create `conda` environment

```bash
$ conda create -n ga python=3.13
$ conda activate ga
```

> For `pip` users, create a `virtualenv` environment

```bash
$ python3 -m venv venv
$ source venv/bin/acivate
```

> install dependencies

```bash
$ pip install -e .
```
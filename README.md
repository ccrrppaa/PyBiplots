# PyBiplots 
[![Anaconda-Server Badge](https://anaconda.org/carlos_t22/pybiplots/badges/installer/pypi.svg)](https://pypi.anaconda.org/carlos_t22)
[![Anaconda-Server Badge](https://anaconda.org/carlos_t22/pybiplots/badges/version.svg)](https://anaconda.org/carlos_t22/pybiplots)

## Overview
PyBiplots is a python package that performs the classic biplots methods. This methods are GH-Biplot, JK-Biplot and HJ-Biplot. 

## Instalation
* Install *PyBiplots* from **Anaconda Cloud**:
```python
pip install -i https://pypi.anaconda.org/carlos_t22/simple pybiplots
```

* Install *PyBiplots* from **GitHub**:
```python
git clone https://github.com/carlostorrescubila/PyBiplots
cd PyBiplots
pip install .
```

## Dependences 
PyBiplots supports Python 3.6+ and no longer supports Python 2.

Installation requires [numpy](https://numpy.org/), [scipy](https://www.scipy.org/), [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/), [seaborn](https://seaborn.pydata.org/), [sklearn](https://scikit-learn.org/stable/) and [adjustText](https://github.com/Phlya/adjustText)

## Example
```python
## 1. Packages needed
import pybiplots.HJ_Biplot as hj
import statsmodels.api as sm
import matplotlib

## 2. Load mtcars data
mtcars = sm.datasets.get_rdataset('mtcars').data

## 3. Fit Biplot
HJ = hj.fit(mtcars, Transform='Standardize columns')

## 4. Draw Biplot
matplotlib.style.use("seaborn")
HJ.plot(adjust_ind_name=True)
```

<img src="https://github.com/carlostorrescubila/PyBiplots/blob/master/plots/HJ_example.png" width="600">

This is a simple example. For detailed examples visit https://github.com/carlostorrescubila/PyBiplots/tree/master/examples

## References 
* [Gabriel, K. R. (1971). The biplot graphic display of matrices with application to principal component analysis. *Biometrika*, 58(3), 453-467.](http://ggebiplot.com/Gabriel1971.pdf)
* [Galindo, M. P. (1986). Una Alternativa de Representación Simultanea: HJ-Biplot. *Qüestiió*, 10:13-23.](http://diarium.usal.es/pgalindo/files/2012/07/0article-HJ-1986.pdf)

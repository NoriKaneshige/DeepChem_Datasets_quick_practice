# DeepChem_Datasets_quick_practice

## Start with some simple imports
>>> import deepchem as dc
>>> import numpy as np

## construct some simple NumPy arrays
>>> x = np.random.random((4,5))
>>> y = np.random.random((4,1))

>>> x
array([[0.55402708, 0.50016622, 0.52094697, 0.63937578, 0.83654021],
       [0.4613981 , 0.55841587, 0.46477849, 0.2483082 , 0.60661361],
       [0.99205372, 0.2913965 , 0.31229226, 0.64483285, 0.52184047],
       [0.92413698, 0.3483203 , 0.38528173, 0.17079636, 0.5426561 ]])

>>> y
array([[0.58474858],
       [0.38040572],
       [0.59258405],
       [0.79761309]])

## Wrap these arrays in a NumpyDataset object

>>> dataset = dc.data.NumpyDataset(x,y)


>>> print(dataset.X)
[[0.55402708 0.50016622 0.52094697 0.63937578 0.83654021]
 [0.4613981  0.55841587 0.46477849 0.2483082  0.60661361]
 [0.99205372 0.2913965  0.31229226 0.64483285 0.52184047]
 [0.92413698 0.3483203  0.38528173 0.17079636 0.5426561 ]]
 
>>> print(dataset.y)
[[0.58474858]
 [0.38040572]
 [0.59258405]
 [0.79761309]]

## Check if these arrays are the same as the original arrays x and y

>>> np.array_equal(x, dataset.X)
True
>>> np.array_equal(y, dataset.y)
True

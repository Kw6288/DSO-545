```python
# Code_1 Reading a text ﬁle

file = 'text.txt'

file_open = open(file, 'r')
file_read = file_open.read()

file_open.close()
```

``` python
# Code_2 Printing a text ﬁle

file = 'text.txt'

file_open = open(file, 'r')
file_read = file_open.read()

file_open.close()

print(file_read)
```

```python
# Code_3 Writing to a ﬁle

file_open = open(file, mode='w')
file_open.close()
```

```python
# Code_4 Context manager with
with open('mnist.txt',mode='r') as text:
    print(text.read())
```

```python
# Code_5 Importing ﬂat ﬁles using NumPy
import numpy as np

file = 'mnist.txt'

data = np.loadtxt(file, delimiter=',')
```

```python
# Code_6 Customizing your NumPy import-1

file = 'mnist.txt'

text = np.loadtxt(file,
                  delimiter = ',',
                 skiprows =1)
```

```python
# Code_7 Customizing your NumPy import-2

file = 'mnist.txt'

text = np.loadtxt(file,
                  delimiter = ',',
                 skiprows =1,
                 usecols = [0,2])
```

```python
# Code_8 Customizing your NumPy import-3

## import a csv file, dtype = string
import numpy as np
 
file = 'titanic_sub.csv'

text = np.loadtxt(file,delimiter = ',', dtype=str)

print(text)

## import a txt file, dtype = string
file_2 = 'seaslug.txt'

text = np.loadtxt(file,delimiter = ',',dtype =str)

print(text)
```

```python
# Code_9 Importing using pandas
import pandas as pd

data= pd.read_csv('titanic_sub.csv')

data.head()
```


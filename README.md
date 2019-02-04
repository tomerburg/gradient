# gradient
Creates a color gradient mapped to a range of numerical values.

## Installation

```
git clone https://github.com/tb1516/gradient
cd gradient
python setup.py install
```

## Usage

First, create an instance of the gradient class that stores the data used to create the color map. Input parameters are as many ranges as desired, which work as follows:

```python
obj = gradient([['#00FFFF',25.0],['#0000FF',29.0]],
               [['#0000FF',29.0],['#0000AA',32.0]],
               [['#0000AA',32.0],['#FF00FF',38.0]])
               
#[['#00FFFF',25.0],['#0000FF',29.0]] is the first range: start with #00FFFF at a value of 25 and end at #0000FF at a value of 29.
```

Create a range of levels going from 25 to 39 with an increment of 0.5:
```python
clevs = np.arange(25.0,39.0,0.5)
```

#To retrieve the gradient colormap matching to the range of levels, use the get_cmap function:
```python
cmap = obj.get_cmap(clevs) #Retrieve colormap
colors = obj.colors #Retrieve list of hex color values
```

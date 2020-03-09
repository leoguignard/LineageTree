# LineageTree

This library allows to import and work with cell (but not limited to cells) lineage trees.
With LineageTree you can read from:
	- TGMM algorithm outputs described in [Fernando et al. 2014](https://www.nature.com/articles/nmeth.3036)
	- TrackMate files described in [Tivenez et al. 2017](https://doi.org/10.1016/j.ymeth.2016.09.016)
	- MaMuT files described in [Wolff et al. 2018](https://doi.org/10.7554/eLife.34410)
	- SVF algorithm outputs described in [McDole, Guignard et al. 2018](https://doi.org/10.1016/j.cell.2018.09.031)
	- ASTEC algorithm outputs described in [Guignard, Fiuza et al. 2020](https://doi.org/10.1126/science.aar5663)
	- and few others

## Description of the repository
  - src: folder containing the package
  - setup.py: Installation script
  - README.md: This file
  - LICENCE: The licence describing file

## Basic usage
Once installed the library can be called the following way (as an example):
```python
from LineageTree import lineageTree
```
and one can then load lineage trees the following way:

For ASTEC data:
```python
lT = lineageTree('path/to/ASTEC.pkl', ASTEC=True)
```
or
```python
lT = lineageTree('path/to/ASTEC.xml', ASTEC=True)
```

For SVF:
```python
lT = lineageTree('path/to/SVF.bin')
```

For MaMuT:
```python
lT = lineageTree('path/to/MaMuT.xml', MaMuT=True)
```

For TrackMate:
```python
lT = lineageTree('path/to/MaMuT.xml', TrackMate=True)
```

For TGMM:
```python
lT = lineageTree('path/to/single_time_file{t:04d}.xml', tb=0, te=500)
```

## Dependencies
Some dependecies are requiered:
  - general python dependecies:
    - numpy, scipy
    
## Quick install
To quickly install the script so it can be call from the terminal and install too the common dependecies one can run
```shell
pip install .
```
or
```shell
python setup.py install [--user]
```

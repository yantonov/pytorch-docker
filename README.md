These scripts help to use python machine learning libraries through docker images.

Docker file provides:
1. [anaconda](https://anaconda.org/anaconda/python)
2. [pytorch](https://pytorch.org)
3. [catboost](https://github.com/catboost/catboost)
4. [jupiter](http://jupyter.org/)
5. [jupiterlab](https://jupyterlab.readthedocs.io/en/stable/)

Usage:  

Add repository to PATH variable.

Run jupiter notebook:
```bash
pytorch.sh notebook
```
Run jupiter lab:
```bash
pytorch.sh
```

After that you can connect to notebook at localhost:8888, current working directory will be mounted also.

Links:
1. [Anaconda docker files](https://github.com/ContinuumIO/docker-images)
2. [pytorch image at docker hub](https://hub.docker.com/r/yantonov/pytorch/)

These scripts help to use python machine learning libraries through docker images.

Docker file provides:
1. [anaconda](https://anaconda.org/anaconda/python)
2. [pytorch](https://pytorch.org)
3. [catboost](https://catboost.ai)
4. [jupiter](http://jupyter.org/)
5. [jupiterlab](https://jupyterlab.readthedocs.io/en/stable/)

See [requirements.txt](https://github.com/yantonov/pytorch-docker/blob/master/docker/files/requirements.txt) to check package versions.

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
1. [pytorch.org](https://pytorch.org/)
2. [image at docker hub](https://hub.docker.com/r/yantonov/pytorch/)

# NequIP

NequIP is an open-source deep learning package for learning interatomic potentials using E(3)-equivariant convolutions.

### Requirements

* Python, v3.8
* PyTorch, v1.8
* Numpy, v1.19.5
* Scipy, v1.6.0
* ASE, v3.20.1

In particular, please be sure to install Python 3.8 and Pytorch 1.8. 

### Installation

* Install [PyTorch Geometric](https://github.com/rusty1s/pytorch_geometric), make sure to install this with your correct version of CUDA/CPU. 
* Install [e3nn](https://github.com/e3nn/e3nn) - it is important to install the ```main``` branch and not the ```master```

```
pip install git+https://github.com/e3nn/e3nn.git 
```

* We use [Weights&Biases](https://wandb.ai) to keep track of experiments. This is not a strict requirement, you can use our software without this, but it may make your life easier. If you want to use it, create an account [here](https://wandb.ai) and install it: 

```
pip install wandb
```

* Install NequIP

```
pip install git+https://github.com/mir-group/nequip.git
```

### Installation Issues

We recommend running the tests using ```pytest```: 

```
pip install pytest
pytest ./tests
```

One some platforms, the installation may complain about the scikit learn installation. If that's the case, specifically install the following scikit-learn version:

```
pip install -U scikit-learn==0.23.0
```

That should fix it.

### Tutorial 

The best way to learn how to use NequIP is through the tutorial notebook in ```tutorials```. 

### Training a network

To train a network, all you need to is run train.py with a config file that describes your data set and network, for example: 

```
python scripts/train.py configs/example.yaml
```

### References

The theory behind NequIP is described in our preprint [1]. NequIP's backend builds on e3nn, a general framework for building E(3)-equivariant neural networks [2]. 

    [1] https://arxiv.org/abs/2101.03164
    [2] https://github.com/e3nn/e3nn

### Authors

NequIP is being developed by:

    - Simon Batzner
    - Anders Johansson
    - Albert Musaelian
    - Lixin Sun
    - Mario Geiger
    - Tess Smidt

under the guidance of Boris Kozinsky at Harvard.


### Citing

If you use this repository in your work, plase consider citing us with the following pre-print: 

    [1] https://arxiv.org/abs/2101.03164

# SparseConvNet
## A Spatially-sparse convolutional network
### [Benjamin Graham](http://www2.warwick.ac.uk/fac/sci/statistics/staff/academic-research/graham/), University of Warwick](http://www2.warwick.ac.uk/fac/sci/statistics/), 2013-2015, GPLv3

SparseConvNet is a convolutional neural network for processing sparse data on a variety of lattices, i.e.
(i) the square lattice,
(ii) the triagular lattice,
(iii) the cubic lattice,
(iv) the tetrahedral lattice
(and of course the hyper-cubic and hyper-tetrahedral 4D lattices as well).
![lattice](/figures/lattices.png)

Data is sparse if most sites take the value zero. For example, if a loop of string has a knot in it, and you trace the shape of the string in a 3D lattice, most sites will not form part of the knot. Applying convolution, sparsity will also hold in the large initial layers:
![lattice](/figures/trefoil.png)

This can be used to analyse 3D models, or space-time paths.
Here are some examples from a [3D object dataset](http://www.itl.nist.gov/iad/vug/sharp/contest/2014/Generic3D/index.html) The insides are hollow, so the data is fairly sparse.

![lattice](/figures/shrec.png)
Top row: four exemplars of snakes. Bottom row: an ant, an elephant, a robot and a tortoise.

### To test the CNN:
1. Put the [CIFAR-10 data files](http://www.cs.toronto.edu/~kriz/cifar-10-binary.tar.gz) in the Data/CIFAR10/ folder
2. Execute "make cifar10 && cifar10"

### Dependencies:
1. An Nvidia CUDA sm_20 capable graphics card
2. The [CUDA SDK](https://developer.nvidia.com/cuda-downloads)
3. [Google sparsehash library](https://code.google.com/p/sparsehash/downloads/list)
4. [The Armadillo library](http://arma.sourceforge.net/)

i.e.

sudo apt-get install libarmadillo-dev

wget https://sparsehash.googlecode.com/files/sparsehash_2.0.2-1_amd64.deb

sudo dpkg -i sparsehash_2.0.2-1_amd64.deb

### References
1. [Spatially-sparse convolutional neural networks](http://arxiv.org/abs/1409.6070)
2. [Sparse 3D convolutional neural networks](http://arxiv.org/abs/1505.02890)

**************************************************************************
SparseConvNet is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

SparseConvNet is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
[GNU General Public License](http://www.gnu.org/licenses/) for more details.
**************************************************************************

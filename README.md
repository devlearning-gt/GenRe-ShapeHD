# Training Generalizable Reconstruction (GenRe) on 13 ShapeNet Classes and Testing on 42 Unseen Classes

This is a repository with some minimal extensions of the original [GenRe Repository](https://github.com/xiumingzhang/GenRe-ShapeHD) to allow for training on different ShapeNet splits. Please refer to the [original paper](http://genre.csail.mit.edu/papers/genre_nips.pdf) as well. The main focus of this repository is generating ground truth data for training. For setup please follow the instructions in the original repository.

## Training Data Download

Download the training data for the 13/42 split on ShapeNet using the following command

```
wget 'link to be added'
```

## Training the Model

In the directory where the repository is cloned, make a symlink to where the data was extracted

```
ln -s path/to/data ./downloads/data/shapenet
```

Then as described in the original repository, follow these steps to train the GenRe model.
1. Train the depth estimator with `scripts/train_marrnet1.sh`
1. Train the spherical inpainting network with `scripts/train_inpaint.sh`
1. Train the full model with `scripts/train_full_genre.sh`

## Training Data Generation 

The pages below contain information to generate ground truth data for GenRe.
1. [Image Rendering](md/rendering.md)
2. [Full Spherical Images](md/spherical.md)
3. [TDF Voxel Grids](md/voxel.md)

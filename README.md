# GAN-mol-generator
Generation of molecules with a GAN (Generative Adversarial Network)

## Description
A GAN with Wasserstein Gradient policy loss (WGAN-GP) https://arxiv.org/abs/1704.00028v3 is used for generation of molecules. An encoder/decoder NN can provide the ability to translate between molecules and their real vector representations.  **cddd** by the Bayer group https://github.com/jrwnter/cddd was used for that purpose as we did in the bayesian optimization example https://github.com/Arhs99/bayesian-opt-gen-design. An example dataset is provided, obtained from ChEMBL. This set is used to train the GAN and also a ML predictive model that can be used to filter the set of generated molecules. Additional chemical filters are necessary to remove molecules that are not drug-like or synthetically infeasible but no such filtering was applied here. A diverse selection of generated molecules (using DataWarrior) is shown in the png image in the ```data/``` folder.

## Usage
The GAN pytorch implementation is based on the code provided in: https://github.com/eriklindernoren/PyTorch-GAN/blob/master/implementations/wgan_gp/wgan_gp.py
The following main packages are required:

       rdkit: 2018.03.3
       scipy:     1.1.0
       numpy:    1.13.3
      pandas:    0.24.2
     sklearn:    0.20.1
       torch:     1.1.0

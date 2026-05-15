
# Minecraft Variational Autoencoder

My Research Project explores the applicability of machine learning to Minecraft. By
using 3D snippets of player-made builds as a dataset, I trained a ‘Variational
Autoencoder’ (VAE) to compress and reconstruct these builds.

My work primarily focused on building upon the work of [Text2MC](https://github.com/shauncomino/text2mc-dataprocessor) by processing more of their [dataset](https://www.kaggle.com/datasets/shauncomino/minecraft-builds-dataset), and adding augmentation functions for geometric transformations, and weighted-random ROI sampling. After making these improvements, I retrained their 3D VAE Pytorch model with the data improvements, recording the F1 and Cosine Similarity metrics for comparison. While more training runs are needed to evaluate the improvements made, initial training showed to improve both metrics.

For those interested in using my dataset improvements, the newly processed dataset of ~31K schematics will be posted on kaggle, and the weights to newly trained models posted on HuggingFace. Analysis of the dataset and visualizations are included in data_analysis/analysis.ipynb. Training results' metrics have been pushed the submodule fork of Text2MC, under train_results/.

Additionally, weight-random ROI sampling and geometric transformations can be used on the dataset by using or modifying the Palette and MinecraftVAEDataset class in training/, also within the submodule repo.

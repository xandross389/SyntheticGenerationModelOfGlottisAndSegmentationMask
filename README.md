# Synthetic Generation Model Of Glottis And Segmentation Mask
DCGAN and Pix2Pix models for generate synthetic  glotis and segmentation masks from Vovalfolds dataset (Available in https://github.com/imesluh/vocalfolds)

In this project, we focus on the generation of synthetic glottis images via Deep Convolutional Generative Adversarial Newtworks (DCGAN); then the resulting images are segmented by another Generative Adversarial Network (GAN), peculiarly a Pix2Pix model, with the aim to obtain the corresponding synthetic labels. 

Starting with the training of the DCGAN model [dcgan_vocalfolds_256x256.ipynb] to generate artificial glottis and then with the same original dataset, training the Pix2Pix model [pix2pix_vocalfolds_intubation_segmentation.ipynb] capable of segmenting a specific class of the training dataset to produce its corresponding segmentation mask. Finally, by concatenating both models [dcgan_pix2pix_vocalfolds_intubation_hybrid_model.ipynb] to be able to use the generative capacity of the DCGAN model in conjunction with the image-to-image translation capacity of the Pix2Pix model to obtain the desired result: completely synthetic pairs of glotis and correspondent segmentation mask.


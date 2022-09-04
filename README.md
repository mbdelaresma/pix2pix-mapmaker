# MapMaker: Pix2Pix on Satellite Images

Deep Learning Course Submission

See full report [HERE](https://github.com/mbdelaresma/pix2pix-mapmaker/blob/main/FinalReport.ipynb)

![image](https://user-images.githubusercontent.com/71246479/188299984-173288d6-a416-47a0-804a-da9ceb2409d9.png)

# Summary

The pix2pix model is a generative adversarial network (GAN) that serves as an image-to-image translation done by training a deep convolutional network. Its generation of the output is conditional on the source image. [1] The GAN architecture is composed of a generator model (which creates fake images) and discriminator model (which identifies fake images). These two models are trained concurrently in an oppositional process wherein the generator’s goal is to trick the discriminator and the discriminator wants to improve on its ability to identify fake generated images. Several applications have been done for this type of model which includes labels to façade translation, edges to photo, day to night, black and white and aerial photos to maps.[1]

A model was trained based on local satellite and map images instead. The images used as training data were scraped from the Google Static Maps API wherein pairs of satellite and road map images are concatenated side by side into a single image. [2] There were 6 metropolitan areas used for the scraping namely Metro Manila, Naga, Iloilo, Cebu, Davao, and Cagayan de Oro. See the supplementary [notebook](https://github.com/mbdelaresma/pix2pix-mapmaker/blob/main/Scraper.ipynb) on image scraping for the code reference. A total of 1000 images were downloaded, taking 800 images as the training set and 200 as the test dataset.

Two models were trained with reverse functionalities. The first model tries to recreate map images from satellite images and the second model does the reverse (map to satellite).

# Sat2Map

![image](https://user-images.githubusercontent.com/71246479/188299980-9c60f77e-2053-4a82-b0bc-aebd3cc631ae.png)

# Map2Sat

![image](https://user-images.githubusercontent.com/71246479/188299964-f8346cdd-3f5a-45a2-80ef-c346d9e772a6.png)

# References

[1] https://machinelearningmastery.com/how-to-develop-a-pix2pix-gan-for-image-to-image-translation/

[2] https://github.com/taesungp/larger-google-sat2maps-dataset

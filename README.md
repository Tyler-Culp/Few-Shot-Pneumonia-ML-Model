# Overview
This was our project from UC Daivs ECS271 ML class where we created a novel few-shot training model to predict whether a patient has pneumonia based off of a chest x-ray image.
Read through our full report [here](./Few_Shot_Learning_in_Medical_Image_Training.pdf).

A standard model woud train on a huge amount of classified images (somewhere in the 1000s). The issue with this is that it is notoriously difficult to get large amounts of well documented medical images.
It also requires medical professionals to spend large amounts of their time classifying images, rather than helping patients.

To this end we made a model which would train of ~50 images yet produced similar accuracy results to the standard model (90% vs 87%).
At a high level this was done using something similar to k-nearest neighbor. By creating a "prototype" of both the normal and pnemonia case using 50 images. Test images would then be converted to a similar
object which we would check to see whether it more closely aligned with or normal or pneumonia prototype to make a prediction.

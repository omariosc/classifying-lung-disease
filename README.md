# Training Your Own AI Model

**_See this tutorial on the website [here](https://omariosc.github.io/classifying-lung-disease/)._**

In this guide, we will walk you through the process of training your own AI model using [Teachable Machine](https://teachablemachine.withgoogle.com/). This is a user-friendly platform that allows you to create machine learning models without any coding experience. We will cover the following steps:

1. **Collecting Data**: Gather the data you need for training your model.
2. **Training the Model**: Use Teachable Machine to train your model with the collected data.
3. **Testing the Model**: Evaluate the performance of your trained model.

## Step 1: Download This Repository

To get started, download this repository. You can do this by clicking on the green `"Code"` button and selecting `"Download ZIP"`.

![Download Repo](tutorial/0.%20Download%20Repo.png)

Once downloaded, extract the contents of the ZIP file to a folder on your computer. You should see the following folder structure if you explore each folder:

```sh
|-- Exported Model
│   ├── keras_model.h5
│   ├── labels.txt
├── README.md
├── TEST
│   ├── healthy
│   │   ├── ...
│   ├── disease
│   │   ├── ...
├── TRAIN
│   ├── healthy
│   │   ├── ...
│   ├── disease
│   │   ├── ...
├── tutorial
│   ├── ...
```

- The `"README.md"` file contains this tutorial (but it will be easier to follow along on the GitHub page).
- The `"tutorial"` folder contains images that will help you follow along with this tutorial.
- The `"Train"` folder contains the training data, which consists of images of healthy and diseased lungs. The `"Test"` folder contains test images that you can use to evaluate your model.
- The `"Exported Model"` folder contains a sample exported model trained on all images.

## Step 2: Get Started with Teachable Machine

Go to the [Teachable Machine website](https://teachablemachine.withgoogle.com/) and click on `"Get Started"`.

![Get Started](tutorial/1.%20Get%20Started.png)

You will be presented with three options: `Image`, `Audio`, and `Pose`. Choose `"Image Project"`.

![New Project](tutorial/2.%20New%20Project.png)

Select `"Standard Image Model"` to create a model that can classify images.

![Model](tutorial/3.%20Model.png)

## Step 3: Add Your Data

Rename the classes to `"Healthy"` and `"Diseased"` by clicking on the text and typing the new name.

![Rename Classes](tutorial/4.%20Rename%20Classes.png)

Now you can upload all the images from this repository (look at the `healthy` and `disease` folders in the `"Train"` folder in this repository) by clicking on the "Upload" button. **Note: It may take a long time if you use lots of images, but just be patient - the website will load all the images in the background.**

![Add Images](tutorial/5.%20Add%20Images.png)

*(Optional)* Now you can edit the training paramaters (by selecting `"Advanced"`).

![Training Parameters](tutorial/6.%20Training%20Parameters.png)

Once you have uploaded all the images, you can start training your model. Click on the `"Train Model"` button. It may take some time to train all the images. **Note: Make sure you do not switch tabs!**.

## Step 4: Test Your Model

After training, you can decline using the camera, and change the `"Input"` mode to `"File"`, and upload a test image, from the `"Test"` folder in this repository.

![Test Your Model](tutorial/7.%20Test%20Your%20Model.png)

*(Optional)* If you are interested in going into more detail, or making another model and testing it with some code instead of through the browser, you can export the model by clicking on `"Export Model"`. You can find a sample exported model trained on all images in the `"Exported Model"` folder in this repository. Teachable Machine provides more instructions into how you can use this.

![Exporting Your Model](tutorial/8.%20Exporting%20Your%20Model.png)

## Step 5: Stretch Exercises

1. Try and test your model with the images in the `"Extension"` folder. You have sample images for `"bronchitis"`, `"cancer"`, `"cartoon"`, `"child"`, and `"inverted"` lungs. You can also try and test your model with images from the internet. You can use [Google Images](https://www.google.com/imghp) to search for images of `"healthy lungs"` and `"disease lungs"`. What about other scans of different organs?

2. Could you try and use the exported model in either JavaScript or Python to validate all the images in the `"test"` folder from the full dataset [here](https://www.kaggle.com/datasets/obulisainaren/multi-cancer)? Look into what a [confuion matrix](https://en.wikipedia.org/wiki/Confusion_matrix) is and how we can interpet it.

## Conclusion

Congratulations! You have successfully trained your own AI model, to classify pneumonia in x-ray images of lungs using Teachable Machine.

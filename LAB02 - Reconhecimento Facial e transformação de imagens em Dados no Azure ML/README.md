Detect faces in Vision Studio
=============================

Vision solutions often require AI to be able to detect human faces. Suppose the fictitious retail company Northwind Traders wants to locate where customers are standing in a store to best assist them. One way to accomplish this is to determine if there are any faces in the images, and if so, to return the bounding box coordinates that show their location.

To test the face detection capabilities of the Azure AI Face service, you will use [Azure Vision Studio](https://portal.vision.cognitive.azure.com/). This is a UI-based platform that lets you explore Azure AI Vision features without needing to write any code.

Create an *Azure AI services* resource
--------------------------------------

You can use Azure AI Face service with an Azure AI services multi-service resource. If you haven't already done so, create an Azure AI services resource in your Azure subscription.

1.  In another browser tab, open the Azure portal at [https://portal.azure.com](https://portal.azure.com/?azure-portal=true), signing in with the Microsoft account associated with your Azure subscription.

2.  Click the ＋Create a resource button and search for *Azure AI services*. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
    -   Subscription: *Your Azure subscription*.
    -   Resource group: *Select or create a resource group with a unique name*.
    -   Region: East US.
    -   Name: *Enter a unique name*.
    -   Pricing tier: *Standard S0.*
    -   By checking this box I acknowledge that I have read and understood all the terms below: *Selected*.
3.  Select Review + create then Create and wait for deployment to complete.

Connect your Azure AI service resource to Vision Studio
-------------------------------------------------------

Next, connect the Azure AI services resource you provisioned above to Vision Studio.

1.  In another browser tab, navigate to Vision Studio at [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  Sign in with your account and making sure you are using the same directory as the one where you have created your Azure AI services resource.

3.  On the Vision Studio home page, select View all resources under the Getting started with Vision heading.

    [![The View all resource link is highlighted under Getting started with Vision in Vision Studio.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)

4.  On the Select a resource to work with page, hover your mouse cursor over the resource you created above in the list and then check the box to the left of the resource name, then select Select as default resource.

    > Note : If your resource is not listed, you may need to Refresh the page.

    [![The Select a resource to work with dialog is displayed with the cog-ms-learn-vision-SUFFIX Cognitive Services resource highlighted and checked. The Select as default resource button is highlighted.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)

5.  Close the settings page by selecting the "x" at the top right of the screen.

Detect faces in the Vision Studio
---------------------------------

1.  In a web browser, navigate to Vision Studio at [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  On the Getting started with Vision landing page, select the Face tab and then select the Detect Faces in an image tile.

3.  Under the Try It Out subheading, acknowledge the resource usage policy by reading and checking the box.

4.  Select each of the sample images and observe the face detection data that is returned.

5.  Now let's try with some of our own images. Select <https://aka.ms/mslearn-detect-faces> to download detect-faces.zip. Then open the folder on your computer.

6.  Locate the file named store-camera-1.jpg; which contains the following image:

    [![An image of people in a store.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-1.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-1.jpg)

7.  Upload store-camera-1.jpg and review the face detection details that are returned.

8.  Locate the file named store-camera-2.jpg; which contains the following image:

    [![An image of more people in a store.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-2.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-2.jpg)

9.  Upload store-camera-2.jpg and review the face detection details that are returned.

10. Locate the file named store-camera-3.jpg; which contains the following image:

    [![An image of people in a store with a plant obscuring a face.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-3.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-face-solutions/store-camera-3.jpg)

11. Upload store-camera-3.jpg and review the face detection details that are returned. Notice how Azure AI Face did not detect the face that is obscured.

In this exercise you have explored how Azure AI services can detect faces in images. If you have time, feel free to try the sample images or some of your own images.

Clean up
--------

If you don't intend to do more exercises, delete any resources that you no longer need. This avoids accruing any unnecessary costs.

1.  Open the Azure portal at [https://portal.azure.com](https://portal.azure.com/?azure-portal=true) and select the resource group that contains the resource you created.
2.  Select the resource and select Delete and then Yes to confirm. The resource is then deleted.

Learn more
----------  

To learn more about what you can do with this service, see the [Azure AI Face service page](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity).

---
---  

Read text in Vision Studio
==========================

In this exercise you'll use Azure AI service to explore the optical character recognition capabilities of Azure AI Vision. You'll use Vision Studio to experiment with extracting text from images, without having to write any code.

A common computer vision challenge is to detect and interpret text embedded within an image. This is known as optical character recognition (OCR). In this exercise you'll use an Azure AI services resource, which includes Azure AI Vision services. You'll then use Vision Studio to try out OCR with different types of images.

Create an *Azure AI services* resource
--------------------------------------

You can use Azure AI Vision's OCR capabilities with an Azure AI services multi-service resource. If you haven't already done so, create an Azure AI services resource in your Azure subscription.

1.  In another browser tab, open the Azure portal at [https://portal.azure.com](https://portal.azure.com/?azure-portal=true), signing in with the Microsoft account associated with your Azure subscription.

2.  Click the ＋Create a resource button and search for *Azure AI services*. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
    -   Subscription: *Your Azure subscription*.
    -   Resource group: *Select or create a resource group with a unique name*.
    -   Region: East US.
    -   Name: *Enter a unique name*.
    -   Pricing tier: *Standard S0.*
    -   By checking this box I acknowledge that I have read and understood all the terms below: *Selected*.
3.  Select Review + create then Create and wait for deployment to complete.

Connect your Azure AI service resource to Vision Studio
-------------------------------------------------------

Next, connect the Azure AI services resource you provisioned above to Vision Studio.

1.  In another browser tab, navigate to Vision Studio at [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  Sign in with your account and making sure you are using the same directory as the one where you have created your Azure AI services resource.

3.  On the Vision Studio home page, select View all resources under the Getting started with Vision heading.

    [![The View all resource link is highlighted under Getting started with Vision in Vision Studio.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)

4.  On the Select a resource to work with page, hover your mouse cursor over the resource you created above in the list and then check the box to the left of the resource name, then select Select as default resource.

    > Note : If your resource is not listed, you may need to Refresh the page.

    [![The Select a resource to work with dialog is displayed with the cog-ms-learn-vision-SUFFIX Cognitive Services resource highlighted and checked. The Select as default resource button is highlighted.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)

5.  Close the settings page by selecting the "x" at the top right of the screen.

Extract text from images in the Vision Studio
---------------------------------------------

1.  In a web browser, navigate to Vision Studio at [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  On the Getting started with Vision landing page, select Optical character recognition, and then the Extract text from images tile.

3.  Under the Try It Out subheading, acknowledge the resource usage policy by reading and checking the box.

4.  Select <https://aka.ms/mslearn-ocr-images> to download ocr-images.zip. Then open the folder.

5.  On the portal, select Browse for a file and navigate to the folder on your computer where you downloaded ocr-images.zip. Select advert.jpg and select Open.

6.  Now review what is returned:
    -   In Detected attributes, any text found in the image is organized into a hierarchical structure of regions, lines, and words.
    -   On the image, the location of text is indicated by a bounding box, as shown here:

    [![An image of the text in the image outlined.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/read-text-computer-vision/advert-bounding-boxes.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/read-text-computer-vision/advert-bounding-boxes.jpg)

7.  You can now try another image. Select Browse for a file and navigate to the folder where you saved the files from GitHub. Select letter.jpg.

    [![An image of a typed letter.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/read-text-computer-vision/letter.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/read-text-computer-vision/letter.jpg)

8.  Review the results of the second image. It should return the text and bounding boxes of the text. If you have time, try note.jpg and receipt.jpg.

Clean up
--------

If you don't intend to do more exercises, delete any resources that you no longer need. This avoids accruing any unnecessary costs.

1.  Open the Azure portal at [https://portal.azure.com](https://portal.azure.com/?azure-portal=true) and select the resource group that contains the resource you created.
2.  Select the resource and select Delete and then Yes to confirm. The resource is then deleted.

Learn more
----------

To learn more about what you can do with this service, see Azure AI Vision's documentation on [optical character recognition](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr).  

---  
---    

Analyze images in Vision Studio
===============================

Azure AI Vision includes numerous capabilities for understanding image content and context and extracting information from images. Azure AI Vision Studio allows you to try out many of the capabilities of image analysis.

In this exercise, you will use Vision Studio to analyze images using the built-in try-it-out experiences. Suppose the fictitious retailer *Northwind Traders* has decided to implement a "smart store", in which AI services monitor the store to identify customers requiring assistance, and direct employees to help them. By using Azure AI Vision, images taken by cameras throughout the store can be analyzed to provide meaningful descriptions of what they depict.

Create an *Azure AI services* resource
--------------------------------------

You can use Azure AI Vision's image analysis capabilities with an Azure AI services multi-service resource. If you haven't already done so, create an Azure AI services resource in your Azure subscription.

1.  In another browser tab, open the Azure portal at [https://portal.azure.com](https://portal.azure.com/?azure-portal=true), signing in with the Microsoft account associated with your Azure subscription.

2.  Click the ＋Create a resource button and search for *Azure AI services*. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
    -   Subscription: *Your Azure subscription*.
    -   Resource group: *Select or create a resource group with a unique name*.
    -   Region: East US.
    -   Name: *Enter a unique name*.
    -   Pricing tier: *Standard S0.*
    -   By checking this box I acknowledge that I have read and understood all the terms below: *Selected*.
3.  Select Review + create then Create and wait for deployment to complete.

Connect your Azure AI service resource to Vision Studio
-------------------------------------------------------

Next, connect the Azure AI service resource you provisioned above to Vision Studio.

1.  In another browser tab, navigate to [Vision Studio](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  Sign in with your account and making sure you are using the same directory as the one where you have created your Azure AI services resource.

3.  On the Vision Studio home page, select View all resources under the Getting started with Vision heading.

    [![The View all resource link is highlighted under Getting started with Vision in Vision Studio.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/vision-resources.png)

4.  On the Select a resource to work with page, hover your mouse cursor over the resource you created above in the list and then check the box to the left of the resource name, then select Select as default resource.

    > Note : If your resource is not listed, you may need to Refresh the page.

    [![The Select a resource to work with dialog is displayed with the cog-ms-learn-vision-SUFFIX Cognitive Services resource highlighted and checked. The Select as default resource button is highlighted.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/default-resource.png)

5.  Close the settings page by selecting the "x" at the top right of the screen.

Generate captions for an image
------------------------------

Now you are ready to use Vision Studio to analyze images taken by a camera in the *Northwind Traders* store.

Let's look at the image captioning functionality of Azure AI Vision. Image captions are available through the Caption and Dense Captions features.

1.  In a web browser, navigate to [Vision Studio](https://portal.vision.cognitive.azure.com/?azure-portal=true).

2.  On the Getting started with Vision landing page, select the Image analysis tab and then select the Add captions to images tile.

    [![On the Vision Studio home page, the Image analysis tab is selected and highlighted. The Add captions to images tile is highlighted.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/add-captions.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/add-captions.png)

3.  Under the Try It Out subheading, acknowledge the resource usage policy by reading and checking the box.

4.  Select <https://aka.ms/mslearn-images-for-analysis> to download image-analysis.zip. Open the folder on your computer and locate the file named store-camera-1.jpg; which contains the following image:

    [![An image of a parent using a cellphone camera to take a picture of a child in in a store](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-1.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-1.jpg)

5.  Upload the store-camera-1.jpg image by dragging it to the Drag and drop files here box, or by browsing to it on your file system.

6.  Observe the generated caption text, visible in the Detected attributes panel to the right of the image.

    The Caption functionality provides a single, human-readable English sentence describing the image's content.

7.  Next, use the same image to perform Dense captioning. Return to the Vision Studio home page, and as you did before, select the Image analysis tab, then select the Dense captioning tile.

    The Dense Captions feature differs from the Caption capability in that it provides multiple human-readable captions for an image, one describing the image's content and others, each covering the essential objects detected in the picture. Each detected object includes a bounding box, which defines the pixel coordinates within the image associated with the object.

8.  Hover over one of the captions in the Detected attributes list and observe what happens within the image.

    [![The image and its captions are displayed.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/dense-captioning.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/dense-captioning.png)

    Move your mouse cursor over the other captions in the list, and notice how the bounding box shifts in the image to highlight the portion of the image used to generate the caption.

Tagging images
--------------

The next feature you will try is the Extract Tags functionality. Extract tags is based on thousands of recognizable objects, including living beings, scenery, and actions.

1.  Return to the home page of Vision Studio, then select the Extract common tags from images tile under the Image analysis tab.

2.  In the Choose the model you want to try out, leave Prebuilt product vs. gap model selected. In the Choose your language, select English or a language of your preference.

3.  Open the folder containing the images you downloaded and locate the file named store-image-2.jpg, which looks like this:

    [![An image of person with a shopping basket in a supermarket](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-2.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-2.jpg)

4.  Upload the store-camera-2.jpg file.

5.  Review the list of tags extracted from the image and the confidence score for each in the detected attributes panel. Here the confidence score is the likelihood that the text for the detected attribute describes what is actually in the image. Notice in the list of tags that it includes not only objects, but actions, such as *shopping*, *selling*, and *standing*.

    [![A screenshot of the detect attributes panel in the Vision Studio with text and confidence scores displayed next to the original image.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/detect-attributes.png)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/detect-attributes.png)

Object detection
----------------

In this task, you use the Object detection feature of Image Analysis. Object detection detects and extracts bounding boxes based on thousands of recognizable objects and living beings.

1.  Return to the home page of Vision Studio, then select the Detect common objects in images tile under the Image analysis tab.

2.  In the Choose the model you want to try out, leave Prebuilt product vs. gap model selected.

3.  Open the folder containing the images you downloaded and locate the file named store-camera-3.jpg, which looks like this:

    [![An image of person with a shopping cart](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-3.jpg)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/analyze-images-vision/store-camera-3.jpg)

4.  Upload the store-camera-3.jpg file.

5.  In the Detected attributes box, observe the list of detected objects and their confidence scores.

6.  Hover your mouse cursor over the objects in the Detected attributes list to highlight the object's bounding box in the image.

7.  Move the Threshold value slider until a value of 70 is displayed to the right of the slider. Observe what happens to the objects in the list. The threshold slider specifies that only objects identified with a confidence score or probability greater than the threshold should be displayed.

Clean up
--------

If you don't intend to do more exercises, delete any resources that you no longer need. This avoids accruing any unnecessary costs.

1.  Open the [Azure portal](https://portal.azure.com/) and select the resource group that contains the resource you created.
2.  Select the resource and select Delete and then Yes to confirm. The resource is then deleted.

Learn more
----------

To learn more about what you can do with this service, see the [Azure AI Vision page](https://learn.microsoft.com/azure/ai-services/computer-vision/overview).
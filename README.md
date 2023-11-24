# OC_Projet_6

# "Place de marché" company wishes to launch an e-commerce marketplace.
On this marketplace, sellers offer items to buyers by posting a photo and a description.

Currently, the categorization of an item is done manually by the sellers, making it unreliable. Moreover, the volume of items is currently very small.

To make the user experience for sellers (ease of posting new items) and buyers (ease of product search) as smooth as possible, and with the view of scaling up, it becomes necessary to automate this task.

The mission is to conduct, in a first iteration, a feasibility study of an article classification engine, based on an image and a description, to automate the categorization of the item.
You need to analyze the textual descriptions and images of the products, through the following steps:

Preprocessing of text or image data as appropriate;
Feature extraction;
Dimension reduction to 2D, to project the products onto a 2D graph as points whose color corresponds to the actual category;
Analysis of the graph to deduce, with the help of descriptions or images, the feasibility of automatically grouping products of the same category;
Implementation of a measure to confirm your visual analysis, by calculating the similarity between the actual categories and the categories resulting from a segmentation into clusters.
Could you demonstrate, with this approach, the feasibility of automatically grouping products of the same category?

## Here are the constraints:

To extract text features, it will be necessary to implement:
Two "bag-of-words" type approaches, simple word counting and Tf-idf;
A classic word/sentence embedding approach with Word2Vec (or Glove or FastText);
A word/sentence embedding approach with BERT;
A word/sentence embedding approach with USE (Universal Sentence Encoder).
Attached, you will find an example of implementing these text feature extraction approaches on another dataset. I invite you to use it as a starting point, it will save you a lot of time!

To extract image features, it will be necessary to implement:
An algorithm of the type SIFT / ORB / SURF;
A CNN Transfer Learning type algorithm.
Regarding the SIFT approach, I invite you to look at the webinar we have realized, available in the resources.

## The second iteration: carry out supervised classification from images, implement data augmentation to optimize the model.
## To expand our product range, especially in fine groceries, it is necessary to test the collection of products based on "champagne" via the API available here https://rapidapi.com/edamam/api/edamam-food-and-grocery-database and provide us with an extraction of the first 10 products in a ".csv" file, containing for each product the following data: foodId, label, category, foodContentsLabel, image.

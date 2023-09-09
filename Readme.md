# Detect Similar Images Python Project- Business Objective

The objective of the similar images python project is to develop a computer vision system that can effectively and precisely identify products based on their images at the individual stock-keeping-unit (SKU) level, in response to the growing trend of online shopping and e-commerce. By implementing this computer vision project, we aim to address the market demand for automated and accurate product recognition. The primary focus of this python find similar images project is to enable users to search and discover images of products that closely resemble a given input image.

For example, imagine a user has a photo of a pair of shoes they like and want to find similar products online. The project aims to create a solution that can analyze the image, understand its key features, and provide a list of other products with similar visual characteristics, such as design, color, and style. This way, users can effortlessly explore and find alternative options that match their preferences based on the visual similarity of products.

## How to setup this project :

1. Create virtualenv & activate the virtualenv
   virtualenv venv
   source ./venv/bin/activate

2. Install requirements as pip install -r requirements.txt

## Stages

1. Download images from label_id:
   We are using Imaterialist Dataset, where given label_id , we are traversing the json file given by Imaterialist,
   and downloading those in a certain specified data path.
2. Index it in Elasticseach ,index name as label id:
   Using Feature Extraction ,we are extracting feature from MobileNetV2 with the weights of imagenet ,
   and then flatenning that array, and then we make a index named label_id as given and then we index that image vector
   with the image name so that we can cross reference it later!!
3. Query from the input image (Image2Image Query):
   In this section,we pull out the feature using Feature Extraction using above mentioned way and then use K nearest neighour
   in Elastic search to find K nearest vectors which are having maxium similarity for the queried image.

## Subtopics:

    1) Business Understanding of Use-Case
    2) Modelling -KNN Overview
    3) Higher Dimensional Database - Overview
    4) ANN BenchMarks and libraries of HDDB
    5) Imaterialist Data
    6) Downloading Imaterialist using Python Script
    7) Understanding MobileNet Arch
    8) Understanding Feature Extraction
    9) Setting up ElasticSearch with a plugin for KNN
    10) Quick Overview of ElasticSearch(Knn) from AWS Documentation
    11) How to connect to ElasticSearch using Python
    12) Indexing Using ElasticSearch   with Python
    13) Querying ElasticDb over Knn    with Python
    14) ElasticSearch API in action and understanding ImageSearch Response
    15) Understanding Django Framework and Modularity

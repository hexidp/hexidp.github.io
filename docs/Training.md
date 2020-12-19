---
layout: default
title: Concepts
nav_order: 2
---

# **Concepts**

## Training
In order to accurately predict information in an AI/ML based system, it first requires to go through a training phase. In IDP, to accurately extract out the information from a document, it requires to be first trained with documents of similar structure and format. IDP supports supervised learning by which it requires minimum 5 similar documents to train a "Model". Once the model is trained, you can upload a document which it has not seen before. It will use the trained model to predict and extract the information. Although the system requires at least 5 documents to train a model, you can train a model with more documents to increase accuracy.

### Tagging/Labelling
As part of training process, you would require to label fields that require to be extracted from the document. For example, from your invoice, you might want to extract "invoice number", "customer name", "total amount" etc. You first require creating "tags" for these fields. Subsequently, for each of the documents in the training set, you would require to label the information against these tags. In IDP, to ease the labelling process, the tool first performs the OCR on the document and identifies all the readable information. You can select the information just by clicking the information on the document and associate that information with the tag.

## Prediction
Prediction is a process of uploading a document against a trained model and extracting the information. 

## Category
For training a model for a given document type/template, you would first require to create a category. Once the category is created, you can upload documents against the category for training. Trained Model would be associated with the category.

At the time of prediction, you can upload a document against the category. System would use a model which is trained against this category for extracting out the information.

## Categoryset

Categoryset is a collection of related categories. For example, if you have 5 different variations of invoice then you can create 5 different categories for each of this invoice variation.You can group each of these categories under one Categoryset. In addition to having a trained model at each category level, the system would keep "All-in-one composed model" at a Categoryset level.

At the time of prediction, you can upload a document against the Categoryset instead of category. When you upload a document for prediction, you have to specify Categoryset, but it is not mandatory to select a category. When the category is not specified, the system will automatically determine the category, information would be extracted based on the model present at the determined category. System will also show you the confidence at which the category is determined. 

## Prebuilt Invoice
IDP supports uploading standard invoice. No training is required to be done for such documents. System automatically identifies standard fields from such documents.

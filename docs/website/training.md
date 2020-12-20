---
layout: default
title: Training
nav_order: 3
has_children: false
parent: Website
---

# Training
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---



## Training Dashboard
From this interface, you can
- View all the categorysets and categories present in the system
- View number of documents used for training and number of documents predicted using a given category.
- Edit/delete a category.
- Add new category/categoryset.
- Upload more training documents against a category
- View training status of a given category.

![](/assets/trainingDashboard.PNG)

## Creating a new Categoryset/Category
You can upload documents against existing category, new category or under  new Categoryset and new category. Just follow below simple steps
- First click on "Add your file".
- **For creating new categoryset & category**: Instead of selecting existing Categoryset and Category, just type the name of categoryset and category that you wish to create. When you upload documents, system will automatically create new categoryset and category.
- **For creating new category under existing categoryset**: Select existing Categoryset and then just type the name of the category that you wish to create. When you upload documents, system will automatically create new category.
- **For uploading more documents against existing category**: If you want to add more files to existing category then Choose Categoryset and category under it from the dropdowns. Dropdowns will dispay all the categorysets and categories present in the system. Subsequently, select the files and upload.

- System currently supports uploading tiff, jpeg/jpg, png and pdf.

![](/assets/trainingUploadFiles.gif)

## Deleting a Category
From the training dashboard,
 - You can click on ![](/assets/TrainingDeleteCategory.png) button  available against each category to delete a category.
  - Delete action deletes all the training files.
 - All the files which are **predicted** using this category **are not** affected. You can continue to see those files in prediction dashboard.

## Train a category
From the training dashboard,
- You can click on ![](/assets/TrainingEditCategory.png) button available against a given category. This will open training interface for that categorty.
- Training interface is divided into three parts
    - On the left side, you would see all the files uploaded to train this category.
    - In the middle, system will open a document.
    - On the right side, you will see all the tags which have been created for training this category.

![](/assets/TrainingCategory.PNG)

### Creating a tag
You would require to create tags to label content from the training document. Tags are nothing but form fields that you would like extract from a document. [Refer this link to know what is tagging.](/docs/Training#tagginglabelling).

From the training interface,
 - Click on ![](/assets/trainingAddTag.png). You can see this button on right side at the top in the tagging section.
 - Provide "name" to the tag and press enter.

 ![](/assets/trainingTagging.gif)


### Labelling the information 
After the tags are created, you have to label this tag by 
- First going into each document, selecting a value from the document.
- Value will be highlighted into the document.
- You can then click on the desired tag on right side to label the highlighted content.
- You will have to repeat this for all the documents in the training set. 

![](/assets/trainingTagging.gif)

### Renaming, Deleting, Ordering, Resetting a tag
- Click on a ![](/assets/TrainingTagContextMenuIcon.PNG) available against each tag.
- It will open a context menu. You can see options for renaming, deleting, ordering and resetting tags.
- Resetting a tag would de-associate values previously labelled to this tag from a current document.

![](/assets/TrainingTagContextMenu.PNG)

### Adding a Post processing rule
If you would like to clean up data everytime after each prediction then IDP supports adding simple "regular expression" against each tag. This regular expression would be executed after every prediction operation. First value matched by this regular expression would be used as a processed value.

You can add regular expression by
 - Opening context menu of a tag by clicking ![](/assets/TrainingTagContextMenuIcon.PNG).
 - Select "edit" option will show following popup where you can specify regular expression.
 - You can also check validity of regular expression by clicking validate button.
 - This regular expression will be executed each time document is sent for prediction against this category.

 ![](/assets/TrainingTagRegularExpression.PNG)

## Rest API Endpoint
After the document is uploaded for prediction, once the information is extracted and the document is "Approved", if you want to send the extracted information to any other system then you can make use of this feature. You can configure "Rest Endpoint" in this category. Currently, IDP just supports "Rest Endpoints" secured with "Basic" authentication.

To configure Rest end point for the category, follow below steps from Training Dashboard
 - Click on ![](/assets/TrainingCategorySettings.png) available against each category.
 - System will open following screen for configuring rest endpoint.
 - You can also disable the "Rest Endpoint" if you no longer want to submit the data to the endpoint.

 ![](/assets/TrainingCategorySettingsPage.PNG)
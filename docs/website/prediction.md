---
layout: default
title: Prediction
nav_order: 2
has_children: false
parent: Website
---
# Prediction

Document can be uploaded for peforming prediction from this interface. 

![](/assets/prediction1.gif)

All the documents which have been submitted for prediction can be viewed from this screen. Approved documents, Rejected documents and documents pending for review are shown in their respective tabs.  

## Predicting a file

- Use "Add Your File" button to upload one or more documents. Selecting Categoryset is mandatory, whereas selecting Category is optional. 

- When category is not specified, system would try to determine category automatically from one of the categories available in selected Categoryset . 

- Currently, system supports uploading jpeg/jpg, png and pdf.

- Once the document is uploaded, it will be listed in the table. System will first try to determine the category of that document(if category is not specified). Once the category is determined, it will extract the information based on the "trained model".
    

![](/assets/predictionUpload.gif)

## Reclassify/View extracted result

Once the document is successfully processed, "reclassify" button present in "Action" column will be enabled for that document. From reclassify screen, you can:
- Reclassify the document. Document will be analyzed again using model present in new category.
- View original data extracted from that document.
- View processed data from that document.
- View table data extracted from that document.
- Update processed data
- Send document for approval(Only for Operator Role)
- Approve/Reject document (Only for Approver/Admin Role)

![](/assets/predictionReclassify.gif)
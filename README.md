# Machine Defect Classification
Classifies whether an machine image is Healthy or Defective.

Models Used are Inception V3 and MobileNet 
 # Approach for Detecting Further Defects :-
1. Make a dataset containing all the defective images.
2. Label all the defects manually using LabelImg and hence generating the annotations.
3. Write an XML Parser that will convert the generated annotations to the required CSV Format.
4. Generating TFRecords for train and test dataset.
5. Writing a LabelMap for predicting classes. 
6. Using SSD Inception V2 Model from Tensorflow Model Zoo to train our model and get the bounding boxes for defects in each image.
NOTE:-  If we want to add another kind of defect, we can add the training images to our dataset, add it's class entry in LabelMap. After re-running the pipeline, the model will be able to identify the new kind of defect with ease.

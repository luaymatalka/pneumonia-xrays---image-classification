# Final Project for module 4
----------------
# Pneumonia Image Classification with Deep Learning

Chest x-ray image analysis is the common medical imaging exam needed to assess different pathologies. Having an automated solution for the analysis can contribute to minimizing the workloads, improve efficiency and reduce the potential of reading errors. Many methods have been proposed to address chest x-ray image classification and detection.  Thus, we propose an approach to classify chest x-ray images into either one of two categories, pathological or normal based on CNN model. By applying this model, we can potentially achieve our key goal, high confidence in the classification. The results show the applied model achieved higher accuracy. 

<pre>
Contributors:
<a href=https://github.com/luaymatalka/>Luay Matalka</a>
<a href=https://github.com/Galdina>Maria Galdina</a>
</pre>
 
### Research Goal

Build and train a CNN model that can classify patients with pneumonia using a chest x-ray image.

### Dataset:

https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.
  
Set | Normal | Pneumonia |
--- | :---: | :---: | 
Train | 1341 |3875 |
Test | 234 | 390 |
Val | 8 | 8 | 

![](/img/conf.png)

**For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans.** The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert.


### Methodology:

1. Download the dataset 
2. Reshape x-rays to 224x224 and create a baseline model with dense layers (fully connected)
3. Train the data on different models and compare recall scores
    - Use regularization for model parameters
    - Check different optimizer 
    - Сhoose the optimal number of layers and neurons
4. Test the data on the best model (highest recall score)


### Results:

___ | Precision | **Recall** | F1 | 
--- | :---: | :---: | :---: | 
0 | 0.62 | 1.00 | 0.76 | 
1 | 1.00 | 0.38| 0.55 | 
accuracy | - | - | 0.69 | 

![](confusion_matrix.png)

### Conclusion

In addition, when we deal with medical diagnosis, a false positive (i.e. prediciting illness when the patient is healthy) is less critical than a false negative (predicting healthiness when the patient is sick). The number of false negatives obtained with the CNN presented here is extremely low, which positions the machine developed here as a reliable ancillary tool for pneumonia detection.

### Future Work
- We worked are very traditional CNN architecture, no pre-trained model was used here, and their employment could be taken as a suggestion for further improvements;
 - The model was trained several times with a variety of hyperparameter combinations. Better to transfer all work with parameters to Grid Search.
 
 
<pre>
Items in Repository:
- [/data] - folder
- [/code]() - Jupyter Notebooks with all models
- [/images]() - all images
- [/py]() - additional user function
- [/presentation]() - pdf files of the final presentation
- README.md - a summary of the repository content
</pre>

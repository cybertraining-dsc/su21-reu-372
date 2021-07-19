---
date: 2021-06-16
title: "Project: Analysing Hashimoto disease causes and spontaneous cured cases using Topic Modeling"
linkTitle: "Hashimoto disease, causes, and cured"
tags: ["project", "reu"]
description: "Analizing immune systems and diet factors than can lead to hashimoto disease"
author: Sheimy Paz
github_url: https://github.com/cybertraining-dsc/su21-reu-372/edit/main/project/index.md
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

[![Check Report](https://github.com/cybertraining-dsc/su21-reu-372/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-372/actions)
[![Status](https://github.com/cybertraining-dsc/su21-reu-372/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-372/actions)
Status: draft, Type: Project


Sheimy Paz, [su21-reu-372](https://github.com/cybertraining-dsc/su21-reu-372), [Edit](https://github.com/cybertraining-dsc/su21-reu-372/blob/main/project/index.md)

{{% pageinfo %}}

## Abstract
This project proposes a new view of the Hashimoto disorder and its relationship with other diseases. The objective is to explore the association of the Hashimoto disorder with disease like h pylori bacteria, inappropriate diet, and its relationship with patients with foreign objects inserted on their body like breast implants etc. We use topic modeling which is a machine learning technic that uses a text-mining tool that help to correlate words with topics making the research process easy and organized. Accordingly, the idea is to get a better understanding of the disorder and the relationship that this has with other health issues hoping to find clear information about the causes and effect that can have on the human body.

We collect the data from silo breaker software, which contains data about news, reports, tweets, and blogs. This program will organize our findings highlighting key words related to symptoms, causes, cures, anything that can apport clarification to the disorder.

In addition, we used a segmentation method to diagnose findings on ultrasound images of patients with Hashimoto disorder. The images used in this project are strictly from a patient with Hashimoto disorder. The images were provided to us for the research since it was very difficult to find images related to this disorder either due to patient privacy rules or because the proper unfamiliarity of the disorder.

Methods information: 
Topic modeling is a text mining tool, it is extremely useful to dig into large collections of text bodies to easily organize and find the specifically information being research.

Segmentations is a process used in image to partitioning digital images into multiple segments. this method is typically used to locate objects and boundaries like lines and curves.

this will be implemented if I decide to add supervector machine to the projects afterwards.
-- [^5] Based on the extracted image features, they used Support Vector Machines (SVMs) to classify input images into several categories such as nodule versus non-nodule and follicles versus fibrosis. Sudarshan et al. used wavelet transform to analyze the input ultrasound thyroid images for the thyroid nodule classification problem. A similar approach, Raghavendra et al. used the segmentation-based fractal texture analysis technique to analyze ultrasound thyroid images under different threshold values for the classification problem. Ouyang et al. found that linear and non-linear classifiers yield similar classification results for the thyroid nodule classification based on handcrafted image features. Since the handcrafted image feature extractors were designed and selected by expert knowledge of authors, they only reflect some limited aspects of the problem. As a result, the classification performance is limited.--- (this organized and rewrited) 


**Keywords:** Thyroid disease, Hashimoto, H Pylori, Implants, Food Sensitivity, Diary sencitivity, Healthy Diets, Exercise, topic modeling, text mining, image_analisys, segmentation. 

## 1. Introduction

Hashimoto thyroiditis is an organ-specific autoimmune disorder.its symptoms were first described 1912 but the disease was not recognized until 1957, before that year it was considered to be the early symptoms of Reidel's Thyroiditis. In 1957 Hashimoto was recognized as an autoimmune disorder that destroys thyroid cells and is antibody-mediated. Pathologically speaking, Hashimoto stimulates the formation of antithyroid antibodies that attack the thyroid tissue, causing progressive fibrosis. Hashimoto is believe to be the concequence of a combination of mutated genes and eviromental factors. The disorder is difficult to diagnose since in the early course of the disease the patients may or may not exhibit symptoms and/or laboratory findings of hyperthyroidism or normal values because the destruction of the gland cells may be intermittent. [^6]Clinical and epidemiological studies suggest worldwide that the most common cause of hypothyroidism is an inadequate dietary intake of iodine and is the most common cause of hypothyroidism in developed countries.

[^4]In a female-to-men radio at least 10:1 women are more often affected than men, and the diagnostics are called between the ages of 30 to 50 years. Studies suggest that an association between high levels of thyroid autoantibodies affect the increased frequencies of mood disorders and there was found a relation between thyroid autoimmunity disease, celiac disease and panic disorder and major depressive disorder.

Due to the arduous labor to identify this disorder a Machine Learning algorithm based on prediction from the early symptoms would be help Doctors to identify Hashimoto in early stages as well as any other health issues related to it like H pylori or inadequate diets this will be helpful for patients that would be able to get the correct treatment in an early stage of the illness avoiding future complications. Also a data research algorithm dedicated to find patient testimonies of improvements or even completed healed and how were these improvements obtained. 

Hashimoto autoimmune diseases have been linked to the infection caused by H pylori bacteria. H pylori is until the date the most common chronic bacterial infection, Affecting half of the world's population and is known for the presence of Caga antigens which are virulents strains that have been found in organ and non organ specific autoimmune diseases. Another important trigger of hashimoto disorder is the inadequate modern diet patterns and the environmental factors that are closely related to it. For instance certain food consumption are an essential factor that trigs the disorder since The majority food being consumed is highly preserved and the consumption of artificial flavorings and sugars have dramatically increase in the past years, adding to it the use of chemicals and insecticides in the fruits and vegetables and the massive introduction of hormones for the meat production, all this can be the cause of the rise of autoimmune diseases.


## 3. Using Images

**Table 1:** "Differences Between Hashimoto's Thyroiditis and Grave's Disease." [^4].

![Table 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/hertoghe-table-2.jpg)


## 5. Datasets

Silobreaker software was used to obtain scientific information related to the hashimoto disease coming from different sources such as journals, procedings, tweets and news. Our date consist in the fallowing feature: ID, cluster Id, Description, publication date, SourceURL, publisher. To analyse the preform of the propose aproach to discover the hiding semantic structures related with hashimoto and thyroiditis the description from the gather data is used to study the fraquency of hashimoti and thyroiditis appears in the documents and detecting words and phrases patterns within them to automaticaly clustering work groups.  

This data was preprocessed droping the columns 'Id', 'ClusterId', 'Language', 'LastUpdated','CreatedDate','FirstReported'. Also, stop words and puntuaction were removed, we convert to lower case all the titles.

The fallowing figure represent the difference words found in our dataset and the size of the words means the frequency of the given words in the document. The size of the words is proportional to the frequency of its used.  

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/wordCloudObject.png)

The dataset is available at [Online resoure]
<https://drive.google.com/drive/u/0/folders/1Omtnn5e-yH3bbhW0-5fIbLgi8SEyfYBP>


## 6. Benchmark 
 
 what kind of benchmark can i used?

Your project must include a benchmark. The easiest is to use cloudmesh-common [^2]
 
## 6. Conclusion

A convincing but not fake conclusion should summarize what the conclusion of the project is.

## 8. Acknowledgments

Please add acknowledgments to all that contributed or helped on this project.

## 9. References

[^1]: Helicobacter pylori infection in women with Hashimoto thyroiditis, [Online resource]
      
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5265752/>

[^2]: I. Voloshyna, V.I Krivenko, V.G Deynega, M.A Voloshyn, Autoimmune thyrod disease related to helicobacterer pylori contamination, [Online resource]
      
      <https://www.endocrine-abstracts.org/ea/0041/eposters/ea0041gp213_eposter.pdf>

[^3]: How your diet can trigger Hashimoto's, [Online resource]
      
      <https://www.boostthyroid.com/blog/2019/4/5/how-your-diet-can-trigger-hashimotos>
   
[^4]: Hashimoto’s Thyroiditis, A Common Disorder in Women: How to Treat It, [Online resource]
      
      <https://www.townsendletter.com/article/441-hashimotos-thyroiditis-common-disorder-in-women/>
      
[^5]: Ultrasound Image-Based Diagnosis of Malignant Thyroid Nodule Using Artificial Intelligence, [Online resource]
      
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7180806//>
      
[^6]: Hypothyroidism in Context: Where We’ve Been and Where We’re Going, [Online resource]
      
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6822815/>
      
[^7]: Gensim Tutorial – A Complete Beginners Guide, [Onile resource]

      <https://www.machinelearningplus.com/nlp/gensim-tutorial/>

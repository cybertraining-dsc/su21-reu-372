---
date: 2021-06-16
title: "Project: Analyzing Hashimoto disease causes, symptoms and cases improvements using Topic Modeling"
linkTitle: "Hashimoto disorder, causes, symptoms and cured"
tags: ["project", "reu"]
description: "Analyzing factors as immune systems, genetics and diets than can lead to Hashimoto disease"
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

This project proposes a new view of the Hashimoto disorder and its relationship with other diseases. The objective is to explore the association of the Hashimoto disorder with disease like h pylori bacteria, inappropriate diet, patients with foreign objects inserted on their body like breast implants etc. We use topic modeling which is an extremely useful technic to dig into large collections of text bodies to easily organize and find information on specific topic. The idea is to use a text-mining tool that help to correlate words with topics making the research process easy and organized. With the purpose to get a better understanding of the disorder and the relationship that this has with other health issues hoping to find clear information about the causes and effect that can have on the human body.
The dataset was collected from silo breaker software, which contains information about news, reports, tweets, and blogs. The program will organize our findings highlighting key words related to symptoms, causes, cures, anything that can apport clarification to the disorder. 

**Keywords:** Thyroid disease, Hashimoto, H Pylori, Implants, Food Sensitivity, Diary sensitivity, Healthy Diets, Exercise, topic modeling, text mining. 

## 1. Introduction

Hashimoto thyroiditis is an organ-specific autoimmune disorder. its symptoms were first described 1912 but the disease was not recognized until 1957, before that year it was considered to be the early symptoms of Reidel's Thyroiditis. In 1957 Hashimoto was recognized as an autoimmune disorder that destroys thyroid cells and is antibody-mediated [6]. Pathologically speaking, Hashimoto stimulates the formation of antithyroid antibodies that attack the thyroid tissue, causing progressive fibrosis. Hashimoto is believe to be the concequence of a combination of mutated genes and eviromental factors[2]. The disorder is difficult to diagnose since in the early course of the disease the patients may or may not exhibit symptoms and/or laboratory findings of hyperthyroidism it may show normal values because the destruction of the gland cells may be intermittent. [6] Clinical and epidemiological studies suggest worldwide that the most common cause of hypothyroidism is an inadequate dietary intake of iodine.

In a female-to-men radio at least 10:4 women are more often affected than men, and the diagnostics are called between the ages of 30 to 50 years.[1] Studies suggest that an association between high levels of thyroid autoantibodies affect the increased frequencies of mood disorders and there was found a relation between thyroid autoimmunity disease, celiac disease and panic disorder and major depressive disorder [4].

Due to the arduous labor to identify this disorder a Machine Learning algorithm based on prediction would help Doctors to identify Hashimoto in early stages as well as any other health issues related to it like H pylori or an inadequate diets [3]. This will be helpful for patients that would be able to get the correct treatment in an early stage of the illness avoiding future complications. This research algorithm was mainly intended to find patient testimonies of improvements, completed healed cases, early symptoms, trigger factors or any useful information about the disorder.  

Hashimoto autoimmune diseases have been linked to the infection caused by H pylori bacteria. H pylori is until the date the most common chronic bacterial infection, Affecting half of the world's population and is known for the presence of Caga antigens which are virulent strains that have been found in organ and non-organ specific autoimmune diseases [1,2]. Another important trigger of Hashimoto disorder is the inadequate modern diet patterns and the environmental factors that are closely related to it [3]. For instance certain food consumption are an essential factor that trigs the disorder since The majority food being consumed is highly preserved and the consumption of artificial flavorings and sugars have dramatically increase in the past years, adding to it the use of chemicals and insecticides in the fruits and vegetables and the massive introduction of hormones for the meat production, all this can be the cause of the rise of autoimmune diseases [5].

We utilize deep learning BERT model to train our dataset. BERT is a superior performer Bidirectional Encoder, which superimposes 12 or 24 layers of multiheaded attention in a Transformer [6]. By the trained model Parameter learning we obtains the word embeddings of the input sentence or input sentence pair in the unsupervised learning framework proceeds by solving the following two tasks: Masked Language Model and Next Sentence Prediction. We try to use Bert model in the small dataset Hashimoto without any success because the BERT model was overfitting the data points. We use LDA model to train the Hashimoto dataset which allow us to find topic probabilities that we compare with the thyroiditis dataset that was trained with the BERT model-framework. 

We used NLTK which is a module that uses the process of splitting sentences from paragraph, split words, recognizing the meaning of those words, to highlighting the main subjects, with the purpose to help to understand the meaning of the document [10]. For instance, in our NLTK model we used two data sets [Hashimoto & Thyroiditis] (https://drive.google.com/drive/u/0/folders/1Omtnn5e-yH3bbhW0-5fIbLgi8SEyfYBP) and we were able to identify the top 30 topics connected to these disorders. From the information collected we were able to identify general information like the association of this disorder with other health issues. The impact of Hashimoto patient with covid19, long term consequences of untreated Hashimoto, recommendation for advance cases, and diet suggestion for improvement. The used of Natural Language tool kit made a precise and less time consuming research process.    

write about gensim

## 3. Images

**Table 1:** "Differences Between Hashimoto's Thyroiditis and Grave's Disease." [^4].

![Table 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/hertoghe-table-2.jpg)

We can observe in this table the differences between this two similar disorders that are frequently misunderstood.

## 5. Datasets

Silobreaker software was used to obtain scientific information related to the Hashimoto disease coming from different sources such as journals, proceedings, tweets, and news. Our date consists in the fallowing feature: ID, cluster Id, Description, publication date, Source URL, publisher. And the purpose is to analyze the preform of the proposed approach to discover the hiding semantic structures related with Hashimoto and thyroiditis the description from the gather data is used to study the frequency of Hashimoto and thyroiditis appears in the documents and detecting words and phrases patterns within them to automatically clustering work groups.  

This data was preprocessed dropping the columns 'Id', 'ClusterId', 'Language', 'LastUpdated','CreatedDate','FirstReported'. Also, stop words and punctuation were removed, we convert to lower case all the titles.

The fallowing figure is an example of a word cloud object and represent the difference words found in our dataset and the size of the words means the frequency of the given words in the document. Meaning that the size of the words is proportional to the frequency of its used.  

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/wordCloudObject.png)

The dataset can be download [Here](https://drive.google.com/drive/u/0/folders/1Omtnn5e-yH3bbhW0-5fIbLgi8SEyfYBP)

## 6. Results

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/IntertopicDistanceMap.png)

Figure 1. The following Intertopic Distance Map is a two-dimensional space filled with circles representing the proportional number of words that belongs to each topic making the distance to each other represent the relation between the topics, meaning that topics that are closer together have more words in common. For instance, in topic 1 we observed word like hypothyroidism, Morgan, symptoms after a small search we were able to find that Morgan is a well-known writer that presented thyroiditis symptoms after giving birth which is something that happen to some women’s and then recover after a couple of months, however this increments the risk of developing the syndrome later in their lives [11]. On topic 4 we see words like food, levothyroxine, liothyronine, selenium and dietary. the relationship between these words is symptom control, symptoms relive, some natural remedies and supplements. [12,8]

![Figure 2](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/topic%20modeling%20picture.PNG)

Figure 2. Provide a bar chart that shows 30 major terms. The bars indicate the total frequency of the term across the entire corpus. The size of the bubble measures the importance of the topics, relative to the data. for example, for visualization purposes we used the first topic that include Hashimoto, thyroiditis, and selenium. Saliency is a measure of how much the term talks about the topic. And in terms of findings is important to mentions the relationship between Hashimoto thyroiditis and selenium. Selenium is a suplement recomended for patients with this disorder that have shown a reduction on antibody levels [8]. 

![Figure 3](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/HierarchicalClustering.png)

Figure 3. In this figure, we can see that the dendrograms have been created joining points 4 with 9, 0 with 2, 1 with 6, and 12 with 13. The vertical height of the dendrogram shows the Euclidean distances between points. It is easy to see that Euclidean distance between points 12 and 13 is greater than the distance between point 4 and 9. This is because the algorithm is clustering by similarity, differences, and frequency of words. We observed in the dark green dendrogram topic 7,3,4,9 which are all related to an advance stage of the disorder. we can find the information about certain treatments, causes of the disorder, level of damage at certain stages. On the reds dendrograms we observe topics 0,2,1,6 which are closely related to diagnosis, early symptoms and procedures used for the diagnosis of the disorder.  

![Figure 4](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/SimilarityMatrix.png)

In figure 4 we observed a similarity matrix chart, the graph is build based on similarity reached from the volume of topic and association by document, therefore the graph show groups of documents that are cluster together based on similarities. in this case the blue square is an indication of a strong similarity, and the green and light green is an indication of different topics. for instance, we are able to derive as a conclusion that carcinoma cancer, carcinoma therapy, lymph papillary metastasis and hypothyroidism are closely related. in facts they are advance stages of the disorder. E.g. Carcinoma therapy is a type of treatment that can be used for this disorder [13].

![Figure 5](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/TermScoreDeclinePerTopic.png)

In figure 5, TF-IDF is an interesting technic used on machine learning that have the ability to give weight to those words that are not frequent in the document but can carry important information. In this example we can see how topic 12, covid19 pandemic patients is the at the top of the chart and then start declining when the rank term increase. The science behind this behave is explain by the TF-IDF which is term frequency - Inverse document frequency. Therefore, covid 19 was a relative new disease, and we do not expect to have a high frequency used in the document. In this case we were able to find information about Hashimoto patients and covid19 which it seems not to causes any extreme symptoms for patient with this disorder others than the ones expected from a healthy person in other words Hashimoto patients have the same risk of a healthy person [14].

![Figure 6](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/TopicProbability.png)

In figure 6, we show a probability distribution chart based on each topic frequency and its relationship with the main topic: Hashimoto thyroiditis causes or cure. We can see that topic 12 is the least frequent or least related since most of its content is about covid19. Then we have topic 11 zebrafish which is related to the investigation of the disorder but most of its content is about the research made on zebrafish and how had help researchers to understand thyroid diseases in other no mammals animals, but is not closely related to the major point of this project, however is an interesting research which have provide useful information about thyroiditis [15].

![Figure 7](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/topicwordscore.png)

In figure 7, We have Topic Word Scores chart that provides a deep understanding of large corpus of texts trough topic extraction. for instance, the data used in this project provide 5 fundamental topics from 0 to 4. In topic number 4 we have a specific word "eye" which it does not seem to have a close relationship with Hashimoto thyroiditis but in facts is related to one of the first symptoms that the human body experiment most likely when is still undiagnosed. this will further justify on the conclusion.

## 7. Benchmark 

 ```
| Name                                                            | Status | Time |
| ----------------------------------------------------------------|----------------
| parallel     Topic  Count                                       |   
| 0      -1    164       -1_cancer_follicular_carcinoma_autoimmune    ok     3.53
| 0      -1    190       -1_cancer_follicular_carcinoma_autoimmune    ok     0.002
```
find the difference gpu/tpu.

Your project must include a benchmark. The easiest is to use cloudmesh-common [^2]
 
## 8. Conclusion

**Question**
Does this look like an appropriate conclusion (is not finish yet) or may this paragraph above have a better used for the graph description in particular???

As expected, we were able to derive helpful information of the Hashimoto disorder. In fact, topic modeling helps us to build models that optimize our research process. for instance, figure 8 Topic Word Score chart provide key word that later help us to minimize the research process, and example was the word eye that may seem no essential but in fact with some research we were able to find out that was related to an early symptom of the disorder which is dry eyes. 
Another symptom reported by some patients was ablation which was found on topic 3, some patient described as an acceleration of the heart rhythm.  

**Question** or does this look like a better idea

Causes:
Food that can trig Hashimoto disease [] I will be providing a resource with explanations of the findings
Enviromental causes ---> (figure  ..)  [] I will be providing a resource with explanations of the findings
genetic causes ---> (figure ...)

Early symptoms: I will type our findings


Type of damage cause to body due to the disorder:
Tissue damage, Abnormal look of the thyroid gland (derive from figure 2(30 more salient terms)) [] i will be providing a resource with explanations of the findings
Nodule development (provided by figure 4 Similarity Matrix topic 3) [] i will be providing a resource with explanations of the findings
High antibody level (figure ) [] I will be providing a resource with explanations of the findings
.....---> i will add more this is just an example 

Ways to improve the symptoms:
food and diet (figure) [] i will be providing a resources with explanations of the findings
Selenium suplementation [8] i will explain more about the this suplement 

## 9. Acknowledgments

Please add acknowledgments to all that contributed or helped on this project.

## 10. References

[^1]: Helicobacter pylori infection in women with Hashimoto thyroiditis, [Online resource]
      
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5265752/>

[^2]: I. Voloshyna, V.I Krivenko, V.G Deynega, M.A Voloshyn, Autoimmune thyrod disease related to helicobacterer pylori contamination, [Online resource]
      
      <https://www.endocrine-abstracts.org/ea/0041/eposters/ea0041gp213_eposter.pdf>

[^3]: How your diet can trigger Hashimoto's, [Online resource]
      
      <https://www.boostthyroid.com/blog/2019/4/5/how-your-diet-can-trigger-hashimotos>
   
[^4]: Hashimoto’s Thyroiditis, A Common Disorder in Women: How to Treat It, [Online resource]
      
      <https://www.townsendletter.com/article/441-hashimotos-thyroiditis-common-disorder-in-women/>
      
[^5]: Hypothyroidism in Context: Where We’ve Been and Where We’re Going, [Online resource]
      
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6822815/>
      
[^6]: BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding, [Online resource]
       
       <https://arxiv.org/abs/1810.04805>
      
[^7]: Gensim Tutorial – A Complete Beginners Guide, [Onile resource]

      <https://www.machinelearningplus.com/nlp/gensim-tutorial/>
      
[^8]: Selenium Supplementation for Hashimoto's Thyroiditis, [Online resource]

     <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4005265/>
     
[^9]: Gregor von Laszewski, Cloudmesh StopWatch and Benchmark from the Cloudmesh Common Library, [GitHub] 
     
     <https://github.com/cloudmesh/cloudmesh-common>
     
[^10]: Pavan Sanagapati, Knowledge Graph & NLP Tutorial-(BERT,spaCy,NLTK), [Online resource]
     
     <https://www.kaggle.com/pavansanagapati/knowledge-graph-nlp-tutorial-bert-spacy-nltk>
     
[^11]: Julia Haskins, Thyroid Conditions Raise the Risk of Pregnancy Complications, [Online resource]

    <https://www.healthline.com/health-news/children-thyroid-conditions-raise-pregnancy-risks-052913>
    
[^12]: How your diet can trigger Hashimoto's, [Online resource]

    <https://www.boostthyroid.com/blog/2019/4/5/how-your-diet-can-trigger-hashimotos>
    
[^13]: Thyroid Cancer Treatment, [Online resource]

    <https://www.cancer.gov/types/thyroid/patient/thyroid-treatment-pdq>
    
[^14]: Hashimoto's Disease And Coronavirus (COVID-19), [Online resource]

    <https://www.palomahealth.com/learn/coronavirus-and-hashimotos-disease> 
    
[15]: How zebrafish research has helped in understanding thyroid diseases, [Online resource] 

    <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5730863/>

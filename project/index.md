---
date: 2021-06-16
title: "Project: Analyzing Hashimoto disease causes, symptoms and cases improvements using Topic Modeling"
linkTitle: "Hashimoto disorder, causes, symptoms and possible cure"
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

This project proposes a new view of Hashimoto’s disorder, its association with other pathologies, possible causes, symptoms, diets, and recommendations. The intention is to explore the association of the Hashimoto disorder with disease like h pylori bacteria, inappropriate diet, environmental factors, and genetic factors.
Topic modeling is a technic used to process large collection of data to identifying topics. It is a text-mining tool that help to correlate words with topics making the research process easy and organized with the purpose to get a better understanding of the disorder and the relationship that this has with other health issues hoping to find clear information about the causes and effect that can have on the human body.
The dataset was collected from silo breaker software, which contains information about news, reports, tweets, and blogs. The program will organize our findings highlighting key words related to symptoms, causes, cures, anything that can apport clarification to the disorder.

- [ ] abstract does not make clear how AI fits in 
 
Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** Thyroid disease, Hashimoto, H Pylori, Implants, Food Sensitivity, Diary sensitivity, Healthy Diets, Exercise, topic modeling, text mining, BERT model. 

## 1. Introduction

Hashimoto thyroiditis is an organ-specific autoimmune disorder. its symptoms were first described 1912 but the disease was not recognized until 1957. Hashimoto is an autoimmune disorder that destroys thyroid cells and is antibody-mediated [6]. In a female-to-men radio at least 10:4 women are more often affected than men. The diagnostic is often called between the ages of 30 to 50 years.[1] Pathologically speaking, Hashimoto stimulates the formation of antithyroid antibodies that attack the thyroid tissue, causing progressive fibrosis. Hashimoto is believe to be the concequence of a combination of mutated genes and eviromental factors[2]. The disorder is difficult to diagnose since in the early course of the disease the patients may or may not exhibit symptoms and/or laboratory findings of hyperthyroidism, it may show normal values because the destruction of the gland cells may be intermittent [6]. Clinical and epidemiological studies suggest worldwide that the most common cause of hypothyroidism is an inadequate dietary intake of iodine.

Due to the arduous labor to identify this disorder a Machine Learning algorithm based on prediction would help to identify Hashimoto in early stages as well as any other health issues related to it [3]. This will be helpful for patients that would be able to get the correct treatment in an early stage of the illness avoiding future complications. This research algorithm was mainly intended to find patient testimonies of improvements, completed healed cases, early symptoms, trigger factors or any useful information about the disorder.

Hashimoto autoimmune diseases have been linked to the infection caused by H pylori bacteria. H pylori is until the date the most common chronic bacterial infection, affecting half of the world's population and is known for the presence of Caga antigens which are virulent strains that have been found in organ and non-organ specific autoimmune diseases [1,2]. Another important trigger of Hashimoto disorder is the inadequate modern diet patterns and the environmental factors that are closely related to it [3]. For instance, western diet consumption is an essential factor that trigs the disorder since this food is highly preserved and predominate the consumption of artificial flavors and sugars which have dramatically increase in the past years, adding to it the use of chemicals and insecticides in the fruits and vegetables and the massive introduction of hormones for the meat production, all this can be the cause of the rise of autoimmune diseases [5].

We utilize deep learning BERT model to train our dataset. BERT is a superior performer Bidirectional Encoder, which superimposes 12 or 24 layers of multiheaded attention in a Transformer [6]. Bert stands for Bidirectional(read from left to right and vice versa with the purpose of an accurate understanding of the meaning of each word in a sentence or document) Encoder Representations from Transformers(the used of transformers and bidirectional models allows the learning of contextual relations between words). Notice that BERT uses two training strategies MLM and NSP. 

Masked LM process is made by masking around 15% of token making the model predict the meaning or value of each of the masked words. In technical word it requires 3 steps Adding a classification layer on top of the encoder output, Multiplying the output vectors by the embedding matrix, transforming them into the vocabulary dimension. And calculating the probability of each word in the vocabulary with SoftMax. Here we can see an image of the process [22].

![Table 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/MLMBertexPic1.png)

The NSP (Next Sentence Prediction) process is based in sentence prediction. The model obtains pair of sentences as inputs, and it is train to predict which is the second sentence in the pair. In The training process 50% of the input sentences are in fact first and second sentence and in the other 50% the second sentences are random sentences used for training purposes. 
The model is able to distinguish if the second sentence is connected to the first sentence by a 3-step process. An CLS (the reserved token to represent the start of sequence) is inserted at the beginning of the first sentence while the SEP (separate segments or sentence) is inserted at the end of each sentence. And embedding indicating sentence A or B is added to each token, and lastly a positional embedding is added to each token to indicate its position in the sequence like is shown on the image [22].

![Table 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/NSPBertexpic.png)

By the trained model Parameter learning we obtains the word embeddings of the input sentence or input sentence pair in the unsupervised learning framework proceeds by solving the following two tasks: Masked Language Model and Next Sentence Prediction.


We try to use Bert model in the small dataset Hashimoto without any success because the BERT model was overfitting the data points. We use LDA model to train the Hashimoto dataset which allow us to find topic probabilities that we compare with the thyroiditis dataset that was trained with the BERT model-framework. 

We used NLTK which is a module that uses the process of splitting sentences from paragraph, split words, recognizing the meaning of those words, to highlighting the main subjects, with the purpose to help to understand the meaning of the document [10]. For instance, in our NLTK model we used two data sets [Hashimoto and thyroiditis](https://drive.google.com/drive/u/0/folders/1Omtnn5e-yH3bbhW0-5fIbLgi8SEyfYBP) and we were able to identify the top 30 topics connected to these disorders. From the information collected we were able to identify general information like the association of this disorder with other health issues. The impact of Hashimoto patient with covid19, long term consequences of untreated Hashimoto, recommendation for advance cases, and diet suggestion for improvement. The used of Natural Language tool kit made a precise and less time consuming research process.


## 2. Images

**Table 1:** "Differences Between Hashimoto's Thyroiditis and Grave's Disease." [^4].

We can observe in this table the differences between this two similar disorders that are frequently misunderstood.

![Table 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/hertoghe-table-2.jpg)

**Table 2:** "Hashimoto’s thyroiditis is associated with other important disorders." [^4].
![Table 2](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/Thyroiditis%20Associated%20Pathologies.jpg)

**Table 3:** "Overview of the main dietary recommendations for patients with Hashimoto." [^4].
![Table 3](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/Dietary%20changes%20that%20reduce%20Antithyroid%20Antibody%20levels.jpg)

## 3. Datasets

Silobreaker software was used to obtain scientific information related to the Hashimoto disease coming from different sources such as journals, proceedings, tweets, and news. Our date consists in the fallowing feature: ID, cluster Id, Description, publication date, Source URL, publisher. And the purpose is to analyze the preform of the proposed approach to discover the hiding semantic structures related with Hashimoto and thyroiditis the description from the gather data is used to study the frequency of Hashimoto and thyroiditis appears in the documents and detecting words and phrases patterns within them to automatically clustering work groups.

This data was preprocessed dropping the columns 'Id', 'ClusterId', 'Language', 'LastUpdated','CreatedDate','FirstReported'. Also, stop words and punctuation were removed, we convert to lower case all the titles.

The dataset can be download [Here](https://drive.google.com/drive/u/0/folders/1Omtnn5e-yH3bbhW0-5fIbLgi8SEyfYBP)

## 4. Results

![Figure 0](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/wordCloudObject.png)

The figure is an example of a word cloud object and represent the difference words found in our dataset and the size of the words means the frequency of the given words in the document. Meaning that the size of the words is proportional to the frequency of its used.

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/IntertopicDistanceMap.png)

Figure 1. The following Intertopic Distance Map is a two-dimensional space filled with circles representing the proportional number of words that belongs to each topic making the distance to each other represent the relation between the topics, meaning that topics that are closer together have more words in common. For instance, in topic 1 we observed word like hypothyroidism, Morgan, symptoms after a small search we were able to find that Morgan is a well-known writer that presented thyroiditis symptoms after giving birth which is something that happen to some women’s and then recover after a couple of months, however this increments the risk of developing the syndrome later in their lives [11]. On topic 4 we see words like food, levothyroxine, liothyronine, selenium and dietary. the relationship between these words is symptom control, symptoms relive, some natural remedies and supplements [12,8].

![Figure 2](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/topic%20modeling%20picture.png)

Figure 2. Provide a bar chart that shows 30 major terms. The bars indicate the total frequency of the term across the entire corpus. The size of the bubble measures the importance of the topics, relative to the data. for example, for visualization purposes we used the first topic that include Hashimoto, thyroiditis, and selenium. Saliency is a measure of how much the term talks about the topic. And in terms of findings is important to mentions the relationship between Hashimoto thyroiditis and selenium. Selenium is a suplement recomended for patients with this disorder that have shown a reduction on antibody levels [8]. 

![Figure 3](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/HierarchicalClustering.png)

Figure 3. In this figure, we can see that the dendrograms have been created joining points 4 with 9, 0 with 2, 1 with 6, and 12 with 13. The vertical height of the dendrogram shows the Euclidean distances between points. It is easy to see that Euclidean distance between points 12 and 13 is greater than the distance between point 4 and 9. This is because the algorithm is clustering by similarity, differences, and frequency of words. We observed in the dark green dendrogram topic 7,3,4,9 which are all related to an advance stage of the disorder. we can find the information about certain treatments, causes of the disorder, level of damage at certain stages. On the reds dendrograms we observe topics 0,2,1,6 which are closely related to diagnosis, early symptoms and procedures used for the diagnosis of the disorder.

![Figure 4](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/SimilarityMatrix.png)

In figure 4 we observed a similarity matrix chart, the graph is build based on similarity reached from the volume of topic and association by document, therefore the graph show groups of documents that are cluster together based on similarities. in this case the blue square is an indication of a strong similarity, and the green and light green is an indication of different topics. for instance, we are able to derive as a conclusion that carcinoma cancer, carcinoma therapy, lymph papillary metastasis and hypothyroidism are closely related. in facts they are advance stages of the disorder. E.g. Carcinoma therapy is a type of treatment that can be used for this disorder [13].

![Figure 5](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/TermScoreDeclinePerTopic.png)

In figure 5, TF-IDF is an interesting technic used on machine learning that have the ability to give weight to those words that are not frequent in the document but can carry important information. In this example we can see how topic 12, covid19 pandemic patients is the at the top of the chart and then start declining when the rank term increase. The science behind this behave is explain by the TF-IDF which is term frequency - Inverse document frequency. Therefore, covid 19 was a relative new disease, and we do not expect to have a high frequency used in the document. In this case we were able to find information about Hashimoto patients and covid19 which it seems not to causes any extreme symptoms for patient with this disorder others than the ones expected from a healthy person in other words Hashimoto patients have the same risk of a healthy person [14].

![Figure 6](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/TopicProbability.png)

In figure 6, we show a probability distribution chart based on each topic frequency and its relationship with the main topic: Hashimoto thyroiditis causes or cure. We can see that topic 12 is the least frequent or least related since most of its content is about covid19. Then we have topic 11 zebrafish which is related to the investigation of the disorder but most of its content is about the research made on zebrafish and how had help researchers to understand thyroid diseases in other no mammals’ animals, but is not closely related to the major point of this project, however, is an interesting research which have provide useful information about thyroiditis [15].

![Figure 7](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/topicwordscore.png)

In figure 7, We have Topic Word Scores chart that provides a deep understanding of large corpus of texts trough topic extraction. for instance, the data used in this project provide 5 fundamental topics from 0 to 4. Essentially each topic provided closely related words with deep information about the disorder itself, treatments, diagnosis, and symptoms. E.g. in topic number 4 we find a specific word "eye" which it does not seem to have a close relationship with Hashimoto thyroiditis but in facts is related to one of the early symptoms that the human body experiment most likely when is still undiagnosed [16]. In the same topic we also find the word teprotumumab which is an eye relieve medication recommended from doctors to relive the symptoms, in other word is not the cure but it helps [17].

## 5. Hashimoto Findings

**Possible causes**

Genetic predispositions, Dietary errors, Nutritional deficiencies, Hormone deficiencies, Viral, bacterial, yeast, and parasitic infections [4].

**Hashimoto Trigger Food**

Some Food that can trigger Hashimoto are gluten, dairy, some type of grains, eggs, nuts or nightshades, sugar, sweeteners, sweet fruits, including honey, agave, maple syrup, and coconut sugar and high-glycemic fruits like watermelon, mango, pineapple, grapes, canned and dried fruits. Vegetable oil, specially hydrogenated oils, ad trans-fat. Patient with this disorder may experience symptoms of fatigue, rashes, joint pain, digestive issues, headaches, anxiety, and depression after eating some of these foods [19].

**Hashimoto recommended Diets**

The recommended foods are healthy fats like coconut, avocado, and olive oil, ghee, grass-fed and organic meat, wild fish, healthy fats, fermented foods like coconut yogurt, kombucha, fermented cucumbers and pickle ginger, and plenty of vegetable like Asparagus, spinach, lettuce, broccoli, beets, cauliflower, carrots, celery, artichokes, garlic, onions [19].

**Environmental causes of Hashimoto**

There have been an increase in the number of Hashimoto cases in the United States since 1950s. These is one of the reason research explain that Hashimoto disorder can be closely related to environmental causes since the rapid increase of cases can not only be related to family gens as it takes at least two generations to acquire and transfer gen mutation. Adding to this that for generation thru history human have been fitting microorganisms than enter our body but for the past centuries our environment has become very hygienic consequently our immune system suddeling was left without aggressors therefore humane start developing more allergies and autoimmune diseases.
Another important factor is the balance of iodine intake because too much is as dangerous for people with genetic Hashimoto predisposition but too littler can be also dangerous for patients with the disorder to reduce goiter which is the enlargement of the thyroid glands [20].

It is still not enough research to state that low vitamin D levels are a cause or a consequence of the Hashimoto disorder, but it is a fact that most patients with this disorder have low levels of vitamin D this insufficient this is closely related to insufficient sun exposure [20].

The exposure to certain synthetic pesticide. An important fact is that 9 out of 12 pesticides are dangerous and persistent pollutants [20]. 

**Symptoms of Hashimoto’s** 

Some of the symptoms are fatigue and sluggishness, sensitivity to cold, constipation, pale and dry skin, dry eyes, puffy face, brittle nails, hair loss, enlargement of the tongue, unexplained weight gain, muscle aches, tenderness and stiffness, joint pain and stiffness, muscle weakness, excessive or prolonged menstrual bleeding, depression, memory lapses, Another symptom reported by some patients was ablation, some patient described as an acceleration of the heart rhythm [21].

**Complications**
Tissue damage, Abnormal look of the thyroid gland (figure 2), goiter, Heart problems, mental health issues, myxedema, birth defects [21], Nodule (figure 4 Similarity Matrix topic 3), and High antibody level. It is important to mention an association between high levels of thyroid autoantibodies and the increased of mood disorders, thyroid autoimmunity disease, celiac disease, panic disorder and major depressive disorder [4].

**Recomendations**

Healthy diets, exercising, selenium supplementation [8], healthy sun exposure at an adequate time, getting enough sleep is primordial for the human body, in special for the metabolism regulation and the creation of normal hormones that the human body needs, [4] lowering stress levels by physical exercise is a good idea, exercise like yoga and reiki are valuable because it also exercise you brain with meditation which is a great stress reliever. 

## 6. Benchmark 

 ```
|--------------------------------------------------------------------------------------------|
| Name                                                            | Status  |Time | processor|
| ----------------------------------------------------------------|---------|-----|----------|
| parallel     Topic  Count                                       |         |     |          |
|-----------------------------------------------------------------|---------|-----|----------|
| 0      -1    164       -1_cancer_follicular_carcinoma_autoimmune|  ok     |0.53 | GPU      |
| 0      -1    190       -1_cancer_follicular_carcinoma_autoimmune|  ok     |0.002| TPU      |
|--------------------------------------------------------------------------------------------|
```
 
## 7. Conclusion

As expected, were able to derive helpful information of the Hashimoto thyroiditis disorder. we attempted to summarize our findings concerning Hashimoto thyroiditis in aspects of causes, symptoms, recommended diets and supplements, used medication...

 ```
|----------------------------------------------------------------------------------------------------|
| Possible Causes                                      | Description               | Recomendations  |
| -----------------------------------------------------|---------------------------|-----------------|
| Genetic predispositionsc                             | Genetically linked        | - stress levels |
|------------------------------------------------------|---------------------------|-----------------|
| Dietary errors                                       | Imbalance of iodine intake| Balance is key  |
|------------------------------------------------------|---------------------------|-----------------|
| Nutritional deficiencies                             | not enough veggies,       |yoga, meditation |
|                                                      | vitamins and minerals     | reiki           |
|------------------------------------------------------|---------------------------|-----------------|
| Hormone deficiencies                                 | lover levels of vit D     | Enough sleep    |
|------------------------------------------------------|---------------------------|-----------------|
|Viral, bacterial, yeast, and parasitic infections.    | H pylori, etc.            | food hygiene    |
|------------------------------------------------------|---------------------------|-----------------|
```
Our findings highlight the great potential of the model we used. certainly, topic modeling method was a precise idea for the optimization of the research process. We also used various features of genism, which allows to manipulate data texts on NPL projects. The use of clustering technics was very useful to label our findings on the large datasets. Each used graph provided useful details and key words that later help us to review each important topic in a faster manner and develop the research project with accurate results.

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

[^15]: How zebrafish research has helped in understanding thyroid diseases, [Online resource] 

    <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5730863/>

[^16]: Dry Eyes and Thyroid Disorders, [Online resource]

    <https://www.webmd.com/eye-health/dry-eyes-thyroid>

[^17]: Teprotumumab for the Treatment of Active Thyroid Eye Disease, [Online resource]

    <https://www.nejm.org/doi/full/10.1056/nejmoa1910434>

[^18]: Jillian Kubala, MS, RD,  Hashimoto Diet: Overview, Foods, Supplements, and Tips, [Online resource]
 
    <https://www.healthline.com/nutrition/hashimoto-diet#diet-tips>

[^19]: Hashimoto’s low thyroid autoimmune, [Online research]

    <https://www.redriverhealthandwellness.com/diet-hashimotos-hypothyroidism/>

[^20]: 11 environmental triggers of Hashimoto’s, [Online research]

    <https://www.boostthyroid.com/blog/11-environmental-triggers-of-hashimotos>

[^21]: Hashimoto's disease, [Online research]

    <https://www.mayoclinic.org/diseases-conditions/hashimotos-disease/symptoms-causes/syc-20351855>

[^22]: BERT Explained: State of the art language model for NLP

    <https://towardsdatascience.com/bert-explained-state-of-the-art-language-model-for-nlp-f8b21a9b6270>

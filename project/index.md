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

Datasets can be huge and GitHub has limited space. Only very small datasets should be stored in GitHub.
However, if the data is publicly available you program must contain a download function instead that you customize.
Write it using pythons `request`. You will get point deductions if you check-in data sets that are large and do not use
the download function.

this tutorial will perform topic modeling in Hashimoto and thyroiditis data specifically Thyroiditis data.csv and Hashimoto data.csv found in silo breaker software. From this sample data we are going to use some functions from libraries like pandas, re, WordCloud, gensim., etc. all the libraries used can be found in the requirements.

**Definition of Data Set**

we are going to used df_hsmto to define our data set with a name.
 
pd.read_csv() is a function from pandas library help us to identify the path where the data is stored in the computer in this case the path used was ("C:/Users/sheim/OneDrive/Desktop/AI Research/Hashimoto data.csv")

**Read Inside of Data**

Using -- df_hsmto -- line of code we are going to be able to see the information that is inside of the data.

**Drop Or Add Columns**

We can use this -- df_tyrdts.drop(columns=['Id', 'ClusterId', 'Language', 'LastUpdated','CreatedDate','FirstReported'], axis=1) -- line of code to drop any columns that we are not interesting in to focus only in what we are looking for.

**Display**

then we can use -- df_tyrdts.head() -- to display what we get after dropping some of the columns.

**re Library**

We use re library which is a regular expression function that allows us to clean text, check for matches etc.

**Remove Punctuation**

Using the function df_hsmto['Description_processed'] = \
df_hsmto['Description'].map(lambda x: re.sub('[,\.!?]', '', x)) 
we can remove punctuations.

**Converting to Lower Case**

using the function df_hsmto['Description_processed'] = \
df_hsmto['Description_processed'].map(lambda x: x.lower())
we convert title to lower case.

**Displaying Clean Data**

and using the function df_hsmto['Description_processed'].head() we can display the data showing all the change we made above.

**Using WordCloud Library**

Wordcloud is the library we are going to be using next. With this library we can represent text data, so basically the size of each word indicates the frequency and importance in which the word is used in the document.

**Manipulating Titles**
With the function long_string = ','.join(list(df_hsmto['Description_processed'].values)) we can join the different processed titles together.

**Creating an Object**

with wordcloud = WordCloud(background_color="white", max_words=5000, contour_width=3, contour_color='steelblue') we create a worldCloud object here is an example of an object created.

**Generating a worldcloud Object**

We can used this code to generate a word cloud wordcloud.generate(long_string)

**Visualization**

Using this line of code wordcloud.to_image() we display the word cloud to the screen.

**Example of a Created Object**

this is how it would look.
![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/wordCloudObject.png)

**Stop Words**

Using NLTK(Natural Language Toolkit) library we are able to ignore word that are commonly used such as “the”, “a”, “an”, “in” with the purpose of saving processing time.

**Gensim Library**

It is a natural language processing library used for unsupervised topic modeling task like Building document, word vector, corpora, topic identification, document comparison, and analyzing documents for semantic structure.

knowing this we can go ahead and use this lines of code to manipulate and clean the data to our convinience stop_words = stopwords.words('english')
stop_words.extend(['from', 'subject', 're', 'edu', 'use'])
def sent_to_words(sentences):
    for sentence in sentences:
        # deacc=True removes punctuations
        yield(gensim.utils.simple_preprocess(str(sentence), deacc=True))
def remove_stopwords(texts):
    return [[word for word in simple_preprocess(str(doc)) 
             if word not in stop_words] for doc in texts]
             
             
**what is this code used for I dont remember?**
data = df_hsmto.Description_processed.values.tolist()
data_words = list(sent_to_words(data))

**Print data words**
using this code print(data_words[:1][0][:30]) we are going to print the data word
and this is how it looks: ['hashimoto', 'thyroiditis', 'associated', 'elevated', 'serum', 'uric', 'acid', 'high', 'density', 'lipoprotein', 'cholesterol', 'ratio']

**Let's Create a Dictionary**
after import gensim.corpora as corpora we can used this function id2word = corpora.Dictionary(data_words) to create a dictionary 

using texts = data_words we create a corpus

Using corpus = [id2word.doc2bow(text) for text in texts] we document the frequency 

using print(corpus[:1][0][:30]) we can display it to the screen 

and this is how it looks like [(0, 1), (1, 1), (2, 1), (3, 1), (4, 1), (5, 1), (6, 1), (7, 1), (8, 1), (9, 1), (10, 1), (11, 1)] 

**pprint library**

then we can use the pprint library to choose the number of topics we want to see
num_topics = 10


**LDA Model**
LDA stand for Linear discriminant analysis and is a method used to find a linear combination of features that characterize or separates two or more classes of objects or events.

we can used this line of code lda_model = gensim.models.LdaMulticore(corpus=corpus,id2word=id2word,num_topics=num_topics) to build one.

**Print the keywords**
using this code pprint(lda_model.print_topics())doc_lda = lda_model[corpus] we obtian the key words and how often are being used in the data.

**pyLADvis Library**
This is wide used library that classify news, papers, tweets, etc. based on their topics. it filter out non relevant information making easier and faster the research process.

**Visualization of the topic**

Using this line code pyLDAvis.enable_notebook()
LDAvis_data_filepath = os.path.join('C:/Users/sheim/Documents/REU-DataScienceProgram'+str(num_topics)) please notice that the lines in the parenthesis is the path which should be different from everyone.

and finally with this code 
if 1 == 1:
    LDAvis_prepared = pyLDAvis.gensim_models.prepare(lda_model, corpus, id2word)
    with open(LDAvis_data_filepath, 'wb') as f:
        pickle.dump(LDAvis_prepared, f)

with open(LDAvis_data_filepath, 'rb') as f:
    LDAvis_prepared = pickle.load(f)
pyLDAvis.save_html(LDAvis_prepared, 'C:/Users/sheim/Documents/REU-DataScienceProgram'+ str(num_topics) +'.html')
LDAvis_prepared
we will be able to see an interactive picture. that looks like this:

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/su21-reu-372/main/project/images/topic%20modeling%20picture.PNG)

## 6. Benchmark

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

---
date: 2021-06-16
title: "Project: Analysing Hashimoto disease causes and spontaneous cured cases using AI"
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
The objective is to evaluate the association of the hashimoto disorder with a clear cause. Hence, the presence of h pylori bacteria, inappropriate diet, foreigent objects inserted on the body like breast implants etc. The idea is that the program came up with a clear conclusion of the factors that can cause hashimoto disorder since until this day is still unknown as well as with a detailed step by step guide of change behavior  based on patients testimonies that have shown improvements or have demonstrated to be completely healed with the intention to bring a cured to other patients with the same dificulties.

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** Thyroid disease, Hashimoto, H Pylori, Implants, Food Sensitivity, Diary sencitivity, Healthy Diets, Exercise. 

## 1. Introduction

Hashimoto thyroiditis is an organ-specific autoimmune disorder named after Japanese physician Hajaru Hashimoto, Hashimoto symptoms were first described 1912 but the disease was not recognized until 1957 before that year it was considered to be the early symptoms of Reidel's Thyroiditis. In 1957 Hashimoto was recognized as an autoimmune disorder that destroys thyroid cells and is antibody-mediated. Pathologically speaking, Hashimoto stimulates the formation of antithyroid antibodies that attack the thyroid tissue, causing progressive fibrosis. Hashimoto is believe to be the concequence of a combination of mutated genes and eviromental factors. The disorder is difficult to diagnose since in the early course of the disease the patients may or may not exhibit symptoms and/or laboratory findings of hyperthyroidism or normal values because the destruction of the gland cells may be intermittent. Clinical and epidemiological studies suggest worldwide that the most common cause of hypothyroidism is an inadequate dietary intake of iodine and is the most common cause of hypothyroidism in developed countries.

In a female-to-men radio at least 10:1 women are more often affected than men, and the diagnostics are called between the ages of 30 to 50 years. Studies suggest that an association between high levels of thyroid autoantibodies affect the increased frequencies of mood disorders and there was found a relation between thyroid autoimmunity disease, celiac disease and panic disorder and major depressive disorder.

Due to the arduous labor to identify this disorder a Machine Learning algorithm based on prediction from the early symptoms would be help Doctors to identify Hashimoto in early stages as well as any other health issues related to it like H pylori or inadequate diets this will be helpful for patients that would be able to get the correct treatment in an early stage of the illness avoiding future complications. Also a data research algorithm dedicated to find patient testimonies of improvements or even completed healed and how were these improvements obtained. 

Here comes a convincing introduction to the problem:
Hashimoto autoimmune diseases have been linked to the infection caused by H pylori bacteria. H pylori is until the date the most common chronic bacterial infection. Affecting half of the world's population and is known for the presence of Caga antigens which are virulents strains that have been found in organ and non organ specific autoimmune diseases. Another important trigger of hashimoto disorder is the inadequate modern diet patterns and the environmental factors that are closely related to it. For instance certain food consumption are an essential factor that trigs the disorder since The majority food being consumed is highly preserved and the consumption of artificial flavorings and sugars have dramatically increase in the past years, adding to it the use of chemicals and insecticides in the fruits and vegetables and the massive introduction of hormones for the meat production, all this can be the cause of the rise of autoimmune diseases.

## 2. Report Format

The report is written in (hugo) markdown and not commonmark. As such some features are not visible in GitHub. You can 
set up hugo on your local computer if you want to see how it renders or commit and wait 10 minutes once your report is 
bound into cybertraining.

To set up the report, you must first `replace` the word `hid-example in this example report with your hid. the hid will 
look something like `sp21-599-111`

It is to be noted that markdown works best if you include an empty line before and after each context change. 
Thus the following is wrong:

```
# This is My Headline
This author does ignore proper markdown while not using empty lines between context changes
1. This is because this author ignors all best practices
```

Instead, this should be 

```
# This is My Headline

We do not ignore proper markdown while using empty lines between context changes

1. This is because we encourage best practices to cause issues.
```

## 2.1. GitHub Actions

When going to GitHub Actions you will see a report is autmatically generated with some help on improving your markdown. 
We will not review any document that does not pass this check.

## 2.2. PAst Copy from Word or other Editors is a Disaster!

We recommend that you sue a proper that is integrated with GitHub or you use the commandline tools. We may include 
comments into your document that you will have to fix, If you juys past copy you will 

1. Not learn how to use GitHub properly and we deduct points
2. Overwrite our coments that you than may miss and may result in point deductions as you have not addressed them.

## 2.3. Report or Project

You have two choices for the final project 

1. Project, That is a final report that includes code
2. Report, that is a final project without code.
 
YOu will be including the type of the project as a prefix to your title, as well as in the Type tag
at the beginning of your project.

## 3. Using Images

![Figure 1](https://github.com/cybertraining-dsc/fa20-523-314/raw/main/project/images/chart.png)
![Figure 2](https://github.com/cybertraining-dsc/fa20-523-314/raw/main/project/images/hertoghe-table-1.jpg)

**Figure 1:** Images can be included in the report, but if they are copied you must cite them [^1].

## 4. Using itemized lists only where needed

Remember this is not a powerpoint presentation, but a report so we recommend

1. Use itemized or enumeration lists sparingly
2. When using bulleted lists use * and not -

## 5. Datasets

Datasets can be huge and GitHub has limited space. Only very small datasets should be stored in GitHub.
However, if the data is publicly available you program must contain a download function instead that you customize.
Write it using pythons `request`. You will get point deductions if you check-in data sets that are large and do not use
the download function.

## 6. Benchmark

Your project must include a benchmark. The easiest is to use cloudmesh-common [^2]
 
## 6. Conclusion

A convincing but not fake conclusion should summarize what the conclusion of the project is.

## 8. Acknowledgments

Please add acknowledgments to all that contributed or helped on this project.

## 9. References

Your report must include at least 6 references. Please use customary academic citation and not just URLs. As we will at 
one point automatically change the references from superscript to square brackets it is best to introduce a space before 
the first square bracket.

[^1]: Helicobacter pylori infection in women with Hashimoto thyroiditis, [Online resource]
      <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5265752/>

[^2]: I. Voloshyna, V.I Krivenko, V.G Deynega, M.A Voloshyn, Autoimmune thyrod disease related to helicobacterer pylori contamination, [Online resource]
      <https://www.endocrine-abstracts.org/ea/0041/eposters/ea0041gp213_eposter.pdf>
      
[^3]: How your diet can trigger Hashimoto's, [Online resource]
      <https://www.boostthyroid.com/blog/2019/4/5/how-your-diet-can-trigger-hashimotos>
      
[^4]: image: Hashimoto’s Thyroiditis, A Common Disorder in Women: How to Treat It, [Online resource]
      <https://www.townsendletter.com/article/441-hashimotos-thyroiditis-common-disorder-in-women/>

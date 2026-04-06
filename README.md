# **Report on Mental Health Sentiment Analysis**

## **Executive Summary**

This report analyzes over 50,000 text posts labeled with seven mental health categories: Anxiety, Depression, Suicidal, Bipolar, Stress, Personality disorder, and Normal (no diagnosis). Through a combination of linguistic analysis, topic modeling, and statistical comparisons, we uncovered distinct patterns in how each condition expresses itself. Key findings include:

- **Depression and Suicidal** posts share the most similar language (correlation 0.75), reflecting overlapping themes of pain and hopelessness.
- **Depression** has the highest rate of exposure to dismissive phrases like “get over it” or “just be happy,” highlighting a societal misunderstanding of the condition.
- **Personality disorder** posts contain the strongest “isolation” signals—people with this diagnosis frequently ask if they are “the only one” feeling a certain way.
- **Normal** posts are short, routine‑focused, and linguistically distinct from all clinical categories.
- **Word clouds and bigram analysis** reveal that the most common phrase across nearly all conditions is “feel like,” underscoring the challenge of articulating internal mental states.

These findings demonstrate that language can be a powerful window into mental health, and the methods used here can inform better support systems and automated screening tools.

## **1. Introduction**

Mental health challenges are often expressed in written language long before they are discussed with a professional. Understanding how different conditions manifest in text can help researchers, clinicians, and support communities recognize patterns and provide more effective help.

In this study, we analyzed a dataset of 52,681 posts, each labeled with one of seven mental health categories. Using a variety of text analysis techniques—ranging from simple word counts to advanced topic modeling and correlation analysis—we aimed to answer:

- What are the most common words and phrases used by each group?
- How do the categories differ in terms of text length, sentiment, and isolation language?
- Which conditions share similar vocabulary?
- How often are people struggling with mental health exposed to dismissive or unhelpful advice?

The following sections detail our findings, followed by a full explanation of the methodology.

## **2. Analysis and Findings**

### **2.1 Understanding the Data Distribution**

To grasp the composition of the dataset, we created a **bar chart** and a **pie chart** showing the number and percentage of posts per category.

| **Status** | **Count** | **Percentage** |
| --- | --- | --- |
| Normal | 16,340 | 31.4% |
| Depression | 15,094 | 29.5% |
| Suicidal | 10,644 | 20.8% |
| Anxiety | 3,623 | 7.1% |
| Bipolar | 2,501 | 4.9% |
| Stress | 2,296 | 4.5% |
| Personality disorder | 895 | 1.8% |

**Findings**

- Over 60% of the data falls into “Normal” and “Depression,” making them the dominant voices in the dataset.
- Suicidal posts constitute a significant 20.8%, indicating a substantial presence of high‑risk conversations.
- The smaller categories (Anxiety, Bipolar, Stress, Personality disorder) still provide valuable insights but should be interpreted with awareness of their lower sample sizes.

**Why this matters**

Understanding the distribution ensures that any patterns we later observe are based on a realistic representation of the data and helps us avoid over‑generalizing from rare categories.
![Mental Health Analysis](analysis_dashboard.png)
## 2.1 Understanding the Data Distribution

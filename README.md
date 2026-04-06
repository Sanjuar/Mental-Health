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
## 2.2 The Language of Mental Health: Word Clouds

We generated **word clouds** for each category after removing stopwords. In these images, the size of a word reflects its frequency within that group.

**Anxiety**

- Dominant words: *feel, know, time, work, think*
- The language centers on internal processes and their impact on daily life.

**Depression**

- Dominant words: *feel, life, want, people, friend*
- Heavy focus on social connection, life outlook, and desires.

**Suicidal**

- Dominant words: *want, end, life, die, feel*
- Distinctly serious vocabulary; words like “end” and “die” appear frequently, confirming the high‑risk nature of this group.

**Normal**

- Dominant words: *day, good, work, people, go*
- Conversations revolve around routines and everyday activities, with positive words like “good” appearing more often.

**Other categories** (Stress, Bipolar, Personality disorder) show intermediate patterns, with Bipolar posts containing clinical terms like “manic” and “medication,” and Personality disorder posts focusing on “avoid” and “people.”

**Key insight**

The word clouds reveal a clear “vocabulary shift” from routine (Normal) to internal struggle (Depression, Anxiety) to crisis (Suicidal). This validates the classification and shows that language meaningfully differentiates the conditions.
![Word Cloud](wordcloud_analysis.png)

### **2.3 Top Phrases Used by Category (Bigram Analysis)**

We counted the most common **two‑word combinations** in each group to capture context beyond single words.
| **Category** | **Top Phrases** |
| --- | --- |
| **Anxiety** | feel like, health anxiety, dont know, anyone else, like im |
| **Normal** | dont know, feel like, even though, dont want, last night |
| **Depression** | feel like, feels like, mental health, get better, every day |
| **Suicidal** | feel like, cannot take, want die, take anymore, anymore cannot |
| **Stress** | feel like, dont know, like im, dont want, im going |
| **Bipolar** | feel like, dont know, dont want, anyone else, like im |
| **Personality disorder** | feel like, dont know, like im, dont want, anyone else |

**Observations**

- **“Feel like”** is the most common phrase in almost all categories.
This shows that people are mainly trying to explain their **feelings and thoughts**, which are often hard to describe.
- In the **Suicidal** category, phrases like **“cannot take”** and **“take anymore”** appear often.
 This suggests people feel **overwhelmed and unable to handle things anymore**.
- In **Depression**, phrases like **“every day”** and **“get better”** are common.
 This shows that depression is often **long-lasting**, and people are **hoping to improve**.
- In the **Normal** category, phrases like **“last night”** are used more.
 This means people are usually talking about **specific events or situations**, not ongoing feelings.

---

### **2.4 Measuring the “Only Me” Feeling (Isolation Logic)**

We scanned all posts for **isolation phrases** expressions that signal a sense of being alone in one’s experience. Examples include:

- “Am I the only one?”
- “Is it just me?”
- “No one else...”
- “Everyone else [is happy/fine/normal]…”

**Findings**

- **Personality disorder** had the highest rate (≈0.061), meaning about 6 out of every 100 posts in this category contain such phrases.
- **Normal** had the lowest rate (≈0.002), confirming that people in a non‑clinical state rarely question whether they are alone in their feelings.
- Depression and Suicidal also showed elevated rates, though lower than Personality disorder.

**Why this matters**

Feeling uniquely alone is a core component of many mental health struggles. This analysis quantifies that isolation and identifies which groups experience it most intensely.

Anxiety                   0.0146  ███████

Normal                    0.0021  █

Depression                0.0384  ███████████████████

Suicidal                  0.0321  ████████████████

Stress                    0.0224  ███████████

Bipolar                   0.0346  █████████████████

Personality disorder      0.0613  ██████████████████████████████

---

### **2.5 The “Just Be Happy” Pattern (Dismissal Rate)**

We compiled a list of dismissive phrases often used to trivialize mental health struggles:

- “Get over it”
- “Just be happy”
- “Move on”

- “Stop overthinking”
- “Others have it worse”

**Findings**

| **Category** | **Dismissal Rate** |
| --- | --- |
| Depression | 0.0205 (highest) |
| Stress | 0.0174 |
| Suicidal | 0.0150 |
| Personality disorder | 0.0104 |
| Bipolar | 0.0082 |
| Anxiety | 0.0104 |
| Normal | 0.0012 (lowest) |

**Key insight**

Depression is statistically the most likely to be met with dismissive advice. This suggests a societal tendency to view depression as a “mood” that can be changed at will, rather than a serious condition. In contrast, Anxiety (despite its high frequency) receives dismissal roughly half as often.

---

### **2.6 Top Phrases Used by Category (Bigram Analysis)**

We used **Latent Dirichlet Allocation (LDA)** to uncover hidden topics within each category. Below are the most representative themes.

**Anxiety**

- *Physical symptoms*: heart, pain, symptoms
- *Nighttime struggle*: restless, sleep
- *Uncertainty*: worry, handle, stress

**Normal**

- *Daily life*: good, love, tired, morning, work, time

**Depression**

- *Social withdrawal*: people, hate, life
- *Career impact*: work, job

**Suicidal**

- *Seeking help*: help, need, suicide
- *Intensity*: die, hate, kill

**Stress**

- *Searching for solutions*: https, com, survey (online coping)
- *Physical impact*: pain, sleep, heart

**Bipolar**

- *Medication*: Lamictal, Lithium, dose
- *Cycling*: manic, episode, cycling

**Personality disorder**

- *Avoidance*: AvPD, people
- *Relationships*: therapy, partners, attachment

**Conclusion from topics**

Each category reflects real‑world situations:

- Anxiety is about the body and sleeplessness.
- Bipolar focuses on medication and mood swings.
- Personality disorder centers on relationships and therapy.
- Suicidal content mixes intense pain with cries for help.

---

### **2.7 The Relationship Map (Correlation Analysis)**

We converted each category’s aggregated text into a vector using TF‑IDF and then calculated **cosine similarity** between every pair. A score of 1.0 indicates perfect vocabulary overlap; lower scores indicate distinct language.

**Strongest connections**

- **Depression ↔ Suicidal** (0.75) – The highest correlation, reflecting shared words like “life,” “pain,” “feel,” and “want.”
- **Anxiety ↔ Stress** (0.68) – Both share words related to physical symptoms and feeling overwhelmed.
- **Bipolar ↔ Depression** (0.64) – Bipolar conversations often lean heavily into depressive language.

**Weakest connections**

- **Normal vs. all clinical categories** – Scores range from 0.20 to 0.40, confirming that “Normal” language is distinct and largely unrelated to mental health struggles.
- **Personality disorder** also shows relatively low similarity with others, indicating a unique vocabulary.

**How to read the heatmap**

- Dark/warm colors → high similarity (the two categories talk in similar ways).
- Light/cool colors → low similarity (they discuss different things).

This correlation map serves as scientific validation that our classification accurately separates groups, while also revealing the natural “clusters” (e.g., Depression‑Suicidal, Anxiety‑Stress) that exist in real‑world mental health language.

## 🔥 Keyword Heatmap Analysis

![Keyword Heatmap](keyword_heatmap.png)

## **3. How We Did It: Methodology**

### **3.1 Tools and Libraries**

| **Library** | **Purpose** |
| --- | --- |
| **pandas** | Data loading, manipulation, aggregation, and summary statistics. |
| **numpy** | Numerical operations (means, standard deviations). |
| **matplotlib** | Creating static plots (bar charts, pie charts). |
| **seaborn** | Enhanced visualizations (violin plots, heatmaps). |
| **collections.Counter** | Efficient counting of word frequencies. |
| **re** | Regular expressions for cleaning text (removing URLs, special chars). |
| **TfidfVectorizer** | Converting text into numerical features based on word importance. |
| **LatentDirichletAllocation** | Topic modeling to discover hidden themes in the text. |
| **cosine_similarity** | Measuring similarity between categories based on their text vectors. |
| **VADER** | Sentiment analysis (used for additional checks, though not detailed here). |
| **nltk** | Natural language toolkit: stopwords, lemmatization, tokenization. |
| **wordcloud** | Generating word clouds to visualize frequent terms. |

### **3.2 Step‑by‑Step Process**

1. **Data Loading**
    - Loaded the CSV using `pd.read_csv()`.
2. **Data Cleaning**
    - Removed the index column (`Unnamed: 0`) and duplicate rows.
    - Cleaned text: converted to lowercase, removed URLs, special characters, and extra spaces with regular expressions.
    - Removed stopwords (NLTK English stopwords) to focus on meaningful content.
    - Applied lemmatization to reduce words to their base forms.
3. **Exploratory Analysis**
    - **Class Distribution**: counted posts per status, created bar and pie charts.
    - **Text Length**: calculated word counts, grouped by status, plotted box and violin plots.
    - **Word Frequency**: concatenated text per status, tokenized, counted with `Counter`, and visualized with word clouds.
    - **Bigram Analysis**: extracted the most common two‑word phrases using `Counter` after tokenizing.
4. **Advanced Analysis**
    - **Isolation Phrases**: created a list of phrases (e.g., “am I the only one”) and counted occurrences per post; computed rates per category.
    - **Dismissal Phrases**: compiled a list of unhelpful advice phrases (e.g., “get over it”) and computed rates similarly.
    - **Topic Modeling**: used `TfidfVectorizer` to convert text to a term‑document matrix, then applied `LatentDirichletAllocation` to extract topics for each category.
    - **Correlation Analysis**: aggregated all text per category, transformed with `TfidfVectorizer`, and computed cosine similarity between vectors. Visualized with a heatmap.
5. **Interpretation**
    - Compared patterns across categories, linked findings to clinical knowledge, and synthesized conclusions.

---

## **4. Conclusion**

This study demonstrates that **textual data can reveal deep, meaningful differences between mental health conditions**. By applying a range of text analysis techniques, we uncovered:

- **Depression** is characterized by chronic language (“every day”), high dismissal rates, and strong similarity to Suicidal content.
- **Suicidal** posts contain distinct crisis phrases (“cannot take”) and high‑risk vocabulary.
- **Personality disorder** shows the strongest isolation signals and a unique focus on relationships and avoidance.
- **Normal** posts are short, routine‑oriented, and linguistically separate from all clinical categories.
- **Word clouds, bigrams, and topic models** each provide complementary views of the vocabulary, context, and themes within each condition.
- **Correlation analysis** validates the classification and reveals natural clusters (Depression–Suicidal, Anxiety–Stress).

These findings can inform the development of automated mental health screening tools, help support communities better understand the language of their members, and highlight areas where societal responses (like dismissive phrases) may be most harmful.

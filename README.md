# Social Media Impact on Student Life: An Exploratory Data Analysis

## 👋 About This Project
Does spending more time on social media actually affect how well students sleep, how stressed they feel, or how they perform academically? I decided to dig into real data and find out for myself, instead of just assuming the answer.

This project is my hands-on exploration of that question, built entirely in Python. Beyond just running code, I focused on something I think matters just as much: thinking critically about what the numbers actually mean, and being honest about what they don't.

## 🎯 What I Set Out to Answer
I wanted to know whether, and how strongly, social media habits like daily usage time, late-night scrolling, platform choice, and device type connect to student well-being. My approach throughout was simple: let the data guide the conclusion, not the other way around.

## 🗂️ About the Dataset
Source: [Impact of Social Media on Life — Kaggle](https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life)

The dataset brings together survey style data from students, covering:
- **Demographics**: Age, Gender, Academic Level
- **Usage behavior**: Daily Usage Hours, Weekend Extra Hours, Late Night Usage, Primary Platform, Device Type
- **Well-being indicators**: Sleep Duration, Sleep Quality Score, Perceived Stress Score, Mental Health Index, Social Comparison Frequency
- **Outcomes**: Academic Performance (GPA), Overall Impact

## 🛠️ Built With
- **Python 3**
- **pandas** for data manipulation and aggregation
- **matplotlib** for data visualization
- **seaborn** for the correlation heatmap
- **Google Colab** as the development environment

## 🔍 The Questions I Explored
1. Does gender relate to sleep duration?
2. Is there a relationship between social media platform and low academic performance?
3. Is there a relationship between device type and high perceived stress?
4. How does late night social media usage relate to sleep and stress?
5. Does age influence daily usage hours?
6. Which variables show the strongest overall correlation with well-being outcomes?
7. Does social comparison frequency relate to mental health?
8. Does academic level influence daily usage hours?

## 📊 What I Found

**The clearest finding by far:** how many hours a student spends on social media each day is strongly tied to their well-being. Here's how it stacked up against key indicators:

| Variable | Correlation with Daily Usage Hours |
|---|---|
| Mental Health Index | -0.85 (strong negative) |
| Perceived Stress Score | 0.75 (strong positive) |
| Sleep Duration | -0.72 (strong negative) |
| Academic Performance (GPA) | -0.71 (strong negative) |

**Late night usage** told a similar story. Students who scroll late at night sleep almost 40 minutes less on average and report noticeably higher stress than those who don't, making it the second strongest pattern in the whole dataset.

**A handful of things turned out not to matter much at all.** Gender, age, social comparison frequency, and academic level all showed only tiny differences across categories, nothing worth building a conclusion on.

**Two patterns looked meaningful at first glance, but weren't.** Instagram was the top platform among low performing students, and Smartphone was the top device among high stress students. But when I compared those numbers to the overall population, both patterns just mirrored what everyone was already doing, not something specific to those groups. This was probably my favorite lesson from the whole project: always check the baseline before trusting a pattern.

**One popular assumption didn't hold up.** It's commonly believed that comparing yourself to others on social media takes a real toll on mental health. In this dataset, that link barely showed up, less than a 1 point difference on a 0 to 100 scale. What seemed to matter far more was simply how much time was spent on social media overall, not how often students compared themselves to others.

## ⚠️ Correlation Isn't Causation
Every finding here describes an association, not a proven cause and effect. Heavy social media use might genuinely hurt sleep and raise stress, but it's just as possible that students who are already stressed or sleep deprived turn to social media more as a way to cope. Telling those two stories apart would need longitudinal data, tracking the same students over time, which this dataset doesn't have.

## 📈 Visuals in the Notebook
- A correlation heatmap covering all numeric variables
- A bar chart comparing sleep duration and stress levels between late night users and everyone else

## 🚀 Running This Project
1. Clone this repository
2. Open `social_media_impact_analysis.ipynb` in Google Colab or Jupyter Notebook
3. Upload the dataset CSV file to the same environment
4. Run all cells in order

## 💡 What This Project Taught Me
The biggest habit I built here was pausing before trusting a result: comparing every subgroup finding against the overall population baseline, and being disciplined about separating correlation from causation when writing up conclusions. Small checks like these are what turn a list of numbers into an analysis someone can actually trust.

## 📌 Where I'd Take This Next
- Build a simple predictive model (like linear regression) to estimate Overall Impact from usage patterns
- Compare these findings against longitudinal data, if it becomes available, to dig into the direction of causality

---
*Dataset used for educational and portfolio purposes.*

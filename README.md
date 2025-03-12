Prodigy Infotech Internship - Task 01

📌 Project Overview

This repository contains my solution for Task 01 of the Prodigy Infotech Internship. The task involves visualizing population data using Python and libraries like Pandas, Matplotlib, and Seaborn.

📊 Objective

Load and process World Bank Population Data.

Create bar charts and histograms for population distribution.

Push the project to GitHub and share insights on LinkedIn.

🚀 Getting Started

1⃣ Install Dependencies

pip install pandas matplotlib seaborn

2⃣ Download & Load Data

Dataset: World Bank Population Data

Save the file as population_data.csv in the project directory.

import pandas as pd
df = pd.read_csv("population_data.csv")
print(df.head())  # Check the dataset structure

3⃣ Data Visualization

🔹 Bar Chart - Top 10 Countries by Population (2022)

import matplotlib.pyplot as plt
import seaborn as sns

df_filtered = df[['Country Name', '2022']].dropna()
df_filtered = df_filtered.sort_values(by='2022', ascending=False).head(10)

plt.figure(figsize=(12, 6))
sns.barplot(data=df_filtered, x='Country Name', y='2022')
plt.xticks(rotation=45)
plt.title("Top 10 Countries by Population (2022)")
plt.xlabel("Country")
plt.ylabel("Population")
plt.show()

🔹 Histogram - Population Distribution

plt.figure(figsize=(10, 5))
sns.histplot(df['2022'], bins=20, kde=True)
plt.xlabel("Population")
plt.ylabel("Frequency")
plt.title("Population Distribution")
plt.show()

4⃣ Push Changes to GitHub

git add .
git commit -m "Added population visualization"
git push origin main

🎯 Conclusion

This project helped me explore data visualization techniques and GitHub version control. I also encountered and resolved data processing errors, such as column mismatches and sorting issues.

💎 Submission & LinkedIn Post 

LinkedIn Post: https://www.linkedin.com/in/sriraj-w-v-p-s-2b2854280/

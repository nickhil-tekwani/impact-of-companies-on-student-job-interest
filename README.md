# How are companies influencing Asian American students’ interests in AI industries they may want to explore?
Nickhil Tekwani

IS 4800 | Prof. Savage

## ABSTRACT

“Abstract intelligence (AI) is a human enquiry of both natural and artificial intelligence at the reductive embodying levels of neural, cognitive, functional, and logical from the bottom up” (Wang). Over the last several years, AI has become one of the quickest growing and most talked-about industries in the world. As interest in AI increases, there has been an associated increase in the number of students in universities studying computer science, and specifically concentrating in AI. NLP and computer vision continue to be the most discussed; however, many smaller AI industries (but equally as profitable) have popped up in regards to financial, government, and pharmaceutical data. Computer science students tend to naturally gravitate towards companies that have NLP or computer vision as those are the most well-known fields, leaving it much harder for smaller AI companies to garner the same number of applicants from collegiate computer science students that larger, better marketed, companies.

In this study, I ask the question: “How are companies influencing Asian American students’ interests in AI industries they may want to explore?”

I hypothesize that Asian American college students’ interests in jobs after undergraduate education are heavily influenced by what companies they see in the media, and which company’s products they recognize. Additionally, I hypothesize that more technically versed students have a more sophisticated understanding of their options.

## INTRODUCTION

As described in the abstract, the goal of this study is to delve into the details of what influences Asian American students’ interests in regards to AI for post-undergraduate job opportunities. My motivation for this research starts with an initial interest in computer science recruiting. From there, I researched what industries (especially with smaller companies) have the highest pain points in regards to the recruiting of computer science students in college. After user interviews and online research, it has been made clear that there is a large pain point to high-revenue AI companies that are not in NLP or computer vision, as students are not overtly knowledgeable in these specific fields. Therefore, these companies receive less organic applicants than larger/better-marketed AI companies, and deal with higher barriers of entry due to students not understanding their industry as well. Additionally, in regards to personal motivation, I am a large part of my local South Asian communities and therefore have focused this study on the Asian American college student demographic.

## RELATED WORK & DIFFERENTIATION

Both computer science recruiting and the AI industry have seen lots of research done into them over the last several years. However, much of this AI research has focused in the NLP and computer vision industries, not other sectors of AI. Additionally, little is known about the overlap between computer science recruiting and all sectors of AI.

Firstly, what major sectors of AI exist besides NLP and Computer Vision?

| AI Sector         | Market Size (in $ billions) | CAGR**        | Primary Generic Sector  |
|-------------------|----------------------------|---------------|-------------------------|
| AR/VR             | 28                         | 31.4%         | Private Sector          |
| Chatbots          | 17.7                       | 34.75%        | Private Sector          |
| NLP               | 10.7                       | 26.8%         | Private Sector          |
| Predictive Analytics | 10                      | 36.0%         | Private / Public Sector |
| Computer Vision   | 9.45                       | 16.0%         | Private Sector          |
| Healthcare        | 6.1                        | 48%           | Public Sector / Academia|
| Autonomous Driving| 1.64                       | 31.3%         | Private Sector          |
| AI Drug Discovery | 1                          | 36.0%         | Public Sector / Academia|

*Market size is for 2021  
**CAGR = compound annual growth rate for time period 2022-2030

From this chart, we see that some of the most discussed and researched AI sectors (such as Autonomous Driving) don’t have the largest market sizes, and some other sectors (like predictive analytics, healthcare, or chatbots) are less talked about but have higher market sizes!

While studies have been done on these individual AI sectors, none has been done on how companies branding can affect computer science, Asian American student recruiting into these sectors. A quick Google Scholar search returns 2.2 million articles for AI, 1.2 million for university recruiting, nearly 400k for CS recruiting, 800k for Asian American CS students, and only 28k for the overlap that I am researching (see Exhibit A).

## METHODS

### High Level Experiment Breakdown

- **Research Question**: How are companies influencing Asian American students’ interests in AI industries they may want to explore?
- **Hypotheses**:
  - Companies have a high influence on Asian American students’ interests.
  - Asian American college students’ interests for post-grad jobs are influenced by what companies and products they know.
  - More technically-versed students have a more sophisticated understanding of their options.
- **Variable Breakdown**:
  - Independent: Technical Experience with AI, Knowledge of AI Companies, AI Products Recognition
  - Dependent: AI Industries of Interest
  - Moderator: Major
- **Target Demographic**: Asian American college students

To gather data from my target demographic, I created a survey in the form of a Google Form. (See Exhibit B) I was able to get 64 total responses within my target demographic.

In this survey, I asked users for the following:
1. Generic Information about their experience with AI (qualitative and quantitative)
2. To rank their familiarity with 11 of the largest companies from different AI sectors
3. To rank their familiarity with 11 of the largest AI products associated with these 11 companies
4. Both qualitative and quantitative questions on their experience in undergrad with AI courses. Additionally, I quizzed their knowledge on which technical skills are most valuable for the AI industry
5. Industry-focused questions about past internships and work experience, as well as their opinion 3 major generic sectors (Academia, Public, and Private sectors)
6. Demographic information

Specifically for sections 2 and 3, I designed the questions to show me users’ recognition of popular AI companies OR associated products, as to see whether certain AI companies were identifiable by just their name, their products, or both. Question 4’s skill set quiz was used as a method of splitting up users into more or less knowledgeable groups for statistical analysis.

## FINDINGS

I tackled 2 main kinds of analyses when looking through this data, exploratory and statistical.

Firstly, I cleaned the data and created some calculated fields in Python. I computed 4 new columns: Quiz Score, Quiz Score Group, Avg Company Familiarity, and Avg Product Familiarity. Avg Company Familiarity and Avg Product Familiarity were computed within Excel itself by computing the average of each entry’s responses to the 11 company rankings and 11 product rankings, respectively.

For quiz score, I assigned a matrix of correct answers to the responses:
A score of 1 represents the correct answer, meaning that the best score anyone could get was a 14.0. In Python, I systematically calculated their sums, and created a new column for quiz scores. I also created a new categorical column representing above_50 or below_50 (above 50% on the quiz or below, which was determined by whether someone’s quiz score was above or below 7/14.

*Note: Full Python code can be found in Jupyter Notebooks in Github repositories shown in Exhibit C.

In terms of exploratory analysis, I loaded the data in Tableau to calculate my demographics, explore interesting company/product associations, and breakdown majors by the quiz score groups. See exhibit D for these figures.

In terms of demographics, the study had 64 respondents with an average age of 21.30 and average graduation year of 2022.27. Approximately 30% were software or engineering majors, and sex was a 50% split between male and female. 100% were Asian (as per target market).

In terms of familiarity, our figure shows us that for most companies the familiarity of the company name and associated product are roughly equivalent. A few stood out:
- AWS (4.6) → Snowflake (2.7)
- GM (4.3) → Cruise (2.3)
- IBM (4.3) → Watson (2.4)
- Tomorrow.io (1.6) → Weather.com (4.5)

Weather.com is the only product/partner that had more familiarity than its associated company.

For statistical analysis, I ran a multitude of T and Z tests. Quite a few resulted in not being statistically significant, but two primary ones were.

Firstly, I compared the mean product familiarity scores between the 2 quiz score groups, above_50 and below_50. A 2 Sample T test is an appropriate test here as the variances across both groups are equal, the distribution is roughly normal,
- 2 Sample T Test, 2 tailed, with Alpha level .05
- h0 = College students who are NOT as knowledgeable in AI technical skills are equally as familiar with major products in various AI industries as college students who ARE knowledgeable in AI technical skills
- h1 = College students who are MORE knowledgeable in AI technical skills are more familiar with major products in various AI industries than those who are NOT

The results were a T Stat of 2.10 and a P Value 0.04, therefore we reject the null hypothesis. This means that college students who are more knowledgeable in AI technical skills are more familiar with major products in various AI industries than those who are NOT as knowledgeable in AI technical skills

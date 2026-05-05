# NYC Public Schools SAT Performance Analysis

![New York City schoolbus](schoolbus.jpg)

*Photo by [Jannis Lucas](https://unsplash.com/@jannis_lucas) on [Unsplash](https://unsplash.com).*

## Overview

Every year, American high school students take the SAT — a standardized test that measures literacy, numeracy, and writing skills. The exam has three sections (reading, math, and writing), each scored out of **800 points**, for a total possible score of **2400**. SAT performance plays a pivotal role in college admissions, making school-level results valuable to policymakers, educators, researchers, and parents alike.

This DataCamp project analyzes a dataset of New York City (NYC) public schools (`schools.csv`) to answer three key questions about SAT performance across the city.

## Dataset

The `schools.csv` file contains the following columns:

| Column | Description |
|---|---|
| `school_name` | Name of the NYC public school |
| `borough` | Borough where the school is located |
| `building_code` | Building code identifier |
| `average_math` | Average math SAT score (out of 800) |
| `average_reading` | Average reading SAT score (out of 800) |
| `average_writing` | Average writing SAT score (out of 800) |
| `percent_tested` | Percentage of students tested |

## Project Files

- `notebook.ipynb` — Jupyter notebook with the full analysis
- `schools.csv` — Raw NYC public school SAT data
- `schoolbus.jpg` — Project cover image

## Key Questions

1. Which NYC schools have the **best math results**? (defined as scoring at least 80% of the 800-point maximum, i.e. ≥ 640)
2. What are the **top 10 performing schools** based on combined SAT scores across the three sections?
3. Which **single borough** has the **largest standard deviation** in combined SAT scores?

## Insights from the Analysis

### 1. Best Math Schools (average math ≥ 640)

The top performing schools in math are dominated by the city's specialized high schools:

| Rank | School | Average Math |
|---|---|---|
| 1 | Stuyvesant High School | 754 |
| 2 | Bronx High School of Science | 714 |
| 3 | Staten Island Technical High School | 711 |
| 4 | Queens High School for the Sciences at York College | 701 |
| 5 | High School for Mathematics, Science, and Engineering at CCNY | 683 |

**Insight:** All top-ranked math schools are NYC specialized high schools that admit students through the SHSAT exam, demonstrating the strong correlation between selective admissions and high math performance.

### 2. Top 10 Schools by Total SAT Score

By summing the math, reading, and writing averages, the highest combined-score schools are:

| Rank | School | Total SAT |
|---|---|---|
| 1 | Stuyvesant High School | 2144 |
| 2 | Bronx High School of Science | 2041 |
| 3 | Staten Island Technical High School | 2041 |
| 4 | High School of American Studies at Lehman College | 2013 |
| 5 | Townsend Harris High School | 1981 |

**Insight:** Stuyvesant leads by a notable margin (~100 points). The same specialized schools that excel in math also dominate the overall SAT rankings, confirming consistent high performance across all three sections.

### 3. Borough with the Largest Score Variation

Grouping schools by borough and computing the standard deviation of total SAT scores reveals:

| Borough | # of Schools | Average SAT | Std. Dev. |
|---|---|---|---|
| **Manhattan** | 89 | 1340.13 | **230.29** |

**Insight:** **Manhattan** has the largest spread in SAT performance among its 89 schools. This wide variability suggests significant educational inequality within the borough — Manhattan houses both elite top-performing schools (such as Stuyvesant) and many lower-performing schools, producing the highest score dispersion of any NYC borough.

## Overall Takeaways

- NYC's **specialized high schools** consistently rank at the top across both math and overall SAT performance.
- **Stuyvesant High School** is the clear standout, leading both individual-subject and combined SAT rankings.
- **Manhattan** exhibits the greatest internal disparity in school performance, highlighting an opportunity for targeted educational policy interventions.

## How to Run

1. Ensure Python 3 and the required libraries are installed:

```bash
pip install pandas jupyter
```

2. Launch Jupyter and open the notebook:

```bash
jupyter notebook notebook.ipynb
```

3. Run all cells to reproduce the analysis.

## Tools Used

- **Python 3**
- **pandas** — data manipulation and aggregation
- **Jupyter Notebook** — interactive analysis environment

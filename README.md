# Vaccine-Hesitancy-vs-Perceived-Corruption-by-Subregion
Python bivariate analysis of vaccine hesitancy versus perceived corruption per subregion of the world. 

## File Descriptions
Vaccine-Hesitancy-vs-Perceived-Corruption.ipynb: Data cleaning, analysis, and visualization of vaccine hesitancy and perceived corruption by sub-region 

corruption_perception_index_cpi.csv: Transparency International's score of perception of corruption by country. Higher values indicate less perceived corruption. Source: gapminder.org 

vccin_sfty_dag.csv: Proportion of people who disagree that "vaccines are safe for children to have". Higher values indicate higher vaccine hesitancy. Source: gapminder.org 

continents2.csv: Dataset of region and subregion label for each country in the world. Source: kaggle.com

## Introduction
Vaccine hesitancy is defined as a "delay in acceptance or refusal of vaccination despite availability of vaccination services" (MacDonald et al., 2015). Generally, vaccine hesitancy is influenced by factors such as perceived risks, accessibility to vaccines, and trust in healthcare workers and politicians. 

One case study analyzing national data in Serbia discovered that there is a positive association between voting populist and exhibiting vaccine hesistant beliefs (Kennedy, 2019). Populism is characterized by anti-establishment beliefs, so, it is hypothesized that a mistrust in elites is a factor that influences vaccine hesitancy. 

Therefore, I conducted this analysis to see if this trend between a mistrust in elites and vaccine hesitancy is apparent in other regions of the world.

## Hypothesis
There is a linear, negative relationship between disagreeing that vaccines are safe and perceiving corruption in one's country in all sub-regions of the world. 
In other terms, the higher the proportion of people who perceive corruption in their country, the higher the proportion of people who disagree that vaccines are safe. 

## Analysis

### Global Analysis 
First, I calculated the correlation coefficient and p-value of the relationship between vaccine hesitancy and perceived corruption as a whole, without grouping by region. 

The correlation coefficient is 0.0383, suggesting nearly no relationship between the two variables. Furthermore, the p-value is 0.77, which is less than 0.05, therefore, these results are not statistically significant. 

Below is a scatterplot showing the bivariate relationship of each country in the dataset, color coded by region. 

![vaccine-hesitancy-scatterplot](https://github.com/stacycaeiro/Vaccine-Hesitancy-Analysis/assets/120422997/fc92a065-d67a-4695-aa2d-8a2cf326e24a)

### Sub-Region Analysis
Next, I calculated the correlation coefficient and p-value of the relationship between vaccine hesitancy and perceived corruption grouped by sub-region. 

The sub-regions with statistically significant results were Eastern Europe (-0.842, 0.0353), Northern America (-0.842, 0.0353), and Northern Europe (-0.899, 0.0148). This means that in these 3 regions, there is a linear, negative relationship between disagreeing that vaccines are safe and perceiving corruption in one's country.

## Conclusions 
Overall, there is no statistically significant relationship between disagreeing that vaccines are safe and perceiving corruption in one's country on a global level, but a linear, negative relationship between the two exist in Eastern Europe, Northern America, and Northern Europe. 

This analysis supports the findings of the Kennedy, 2019 paper. However, this relationship cannot be applied to a global level. This is most likely due to the differing historical and political contexts of each of the world's sub-regions. 

One setback of my analysis is that it only included 60 countries due to missing data from both the Vaccine Survey and Corruption Perception Index datasets. Therefore, I recommend that future analysis includes data from a larger selection of countries in order to get a more accurate representation of each sub-region. 

## Citations
Kennedy, Jonathan. “Populist Politics and Vaccine Hesitancy in Western Europe: An Analysis of National-Level Data.” European Journal of Public Health, vol. 29, no. 3, 25 Feb. 2019, https://doi.org/10.1093/eurpub/ckz004.

MacDonald, Noni E. “Vaccine Hesitancy: Definition, Scope and Determinants.” Vaccine, vol. 33, no. 34, Aug. 2015, pp. 4161–4164, pubmed.ncbi.nlm.nih.gov/25896383/, https://doi.org/10.1016/j.vaccine.2015.04.036.


# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

## Problem Statement

<span style='color:green'> 
The new format for the SAT was released in March 2016. As an employee of the College Board - the organization that administers the SAT - we are a part of a team that tracks statewide participation and recommends where money is best spent to improve SAT participation rates.   

Based on 2017 and 2018 SAT data, there is a great disparity in SAT participation rates across states. College Board wants to improve SAT participation rates across US States. This project aims to investigate why certain states have low SAT participations rates and investigate whether there are any underlying trends or factors affecting a State’s SAT Participation Rate.


</span>

## Executive Summary

**SAT and ACT provide**
> SAT and ACT are inversely correlated with their participation rates. 

> In 2017-18, 10 states (Colorado, Connecticut, Delaware, Idaho, Illinois, Maine, Michigan, New Hampshire, Rhode Island, West Virginia, District of Columbia) administered the SAT to public school students for free. These have resulted a great improvement of SAT take up rate in these states.

> Promoting SAT Test to US States that predominantly administer ACT Test with better access through SAT School Day Programs will be the key on promoting SAT in the country.




### Contents:
- [Data Import & Cleaning](#Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualize-the-data)
- [Descriptive and Inferential Statistics](#Descriptive-and-Inferential-Statistics)
- [Outside Research](#Outside-Research)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)


## Data Import & Cleaning

Data were been abstracted, cleaned and aligned accordingly to the data type for follow up analysis.

#### 8. Data dictionary


|Variable|Type|Dataset|Description|
|---|---|---|---|
|**act17**|*dataframe*|ACT 2017 Results|Contain Means of 51 State ACT scores.| 
|**sat17**|*dataframe*|SAT 2017 Results|Contain Means of 51 State SAT scores.| 
|**final**|*dataframe*|Data from GA |2017 & 2018 ACT & SAT combined horizontally, with column name + _yr.|
|**final_v**|*dataframe*|Data from GA |2017 & 2018 ACT & SAT vertically horizontally.|
|**combined17**|*CSV file*|Data from GA |2017 ACT & SAT participation rate and its relevants scores.|
|**combined18**|*CSV file*|Data from GA |2018 ACT & SAT participation rate and its relevants scores.|
|**final**|*CSV file*|Data from GA |2017 & 2018 ACT & SAT combined horizontally.|


## Exploratory Data Analysis

The following provide a general view on the combined data:


<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>act_part_17</th>
      <th>act_english_17</th>
      <th>act_math_17</th>
      <th>act_reading_17</th>
      <th>act_science_17</th>
      <th>act_composite_17</th>
      <th>sat_part_17</th>
      <th>sat_ebrw_17</th>
      <th>sat_math_17</th>
      <th>sat_total_17</th>
      <th>act_part_18</th>
      <th>act_composite_18</th>
      <th>act_english_18</th>
      <th>act_math_18</th>
      <th>act_reading_18</th>
      <th>act_science_18</th>
      <th>sat_part_18</th>
      <th>sat_ebrw_18</th>
      <th>sat_math_18</th>
      <th>sat_total_18</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
      <td>51.00</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>65.25</td>
      <td>20.93</td>
      <td>21.18</td>
      <td>22.01</td>
      <td>21.04</td>
      <td>21.52</td>
      <td>39.80</td>
      <td>569.12</td>
      <td>547.63</td>
      <td>1126.10</td>
      <td>61.65</td>
      <td>21.49</td>
      <td>20.99</td>
      <td>21.13</td>
      <td>22.02</td>
      <td>21.35</td>
      <td>45.75</td>
      <td>563.69</td>
      <td>556.24</td>
      <td>1120.02</td>
    </tr>
    <tr>
      <th>std</th>
      <td>32.14</td>
      <td>2.35</td>
      <td>1.98</td>
      <td>2.07</td>
      <td>3.18</td>
      <td>2.02</td>
      <td>35.28</td>
      <td>45.67</td>
      <td>84.91</td>
      <td>92.49</td>
      <td>34.08</td>
      <td>2.11</td>
      <td>2.45</td>
      <td>2.04</td>
      <td>2.17</td>
      <td>1.87</td>
      <td>37.31</td>
      <td>47.50</td>
      <td>47.77</td>
      <td>94.16</td>
    </tr>
    <tr>
      <th>min</th>
      <td>8.00</td>
      <td>16.30</td>
      <td>18.00</td>
      <td>18.10</td>
      <td>2.30</td>
      <td>17.80</td>
      <td>2.00</td>
      <td>482.00</td>
      <td>52.00</td>
      <td>950.00</td>
      <td>7.00</td>
      <td>17.70</td>
      <td>16.60</td>
      <td>17.80</td>
      <td>18.00</td>
      <td>17.90</td>
      <td>2.00</td>
      <td>480.00</td>
      <td>480.00</td>
      <td>977.00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>31.00</td>
      <td>19.00</td>
      <td>19.40</td>
      <td>20.45</td>
      <td>19.90</td>
      <td>19.80</td>
      <td>4.00</td>
      <td>533.50</td>
      <td>522.00</td>
      <td>1055.50</td>
      <td>28.50</td>
      <td>19.95</td>
      <td>19.10</td>
      <td>19.40</td>
      <td>20.45</td>
      <td>19.85</td>
      <td>4.50</td>
      <td>534.50</td>
      <td>522.50</td>
      <td>1057.50</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>69.00</td>
      <td>20.70</td>
      <td>20.90</td>
      <td>21.80</td>
      <td>21.30</td>
      <td>21.40</td>
      <td>38.00</td>
      <td>559.00</td>
      <td>548.00</td>
      <td>1107.00</td>
      <td>66.00</td>
      <td>21.30</td>
      <td>20.20</td>
      <td>20.70</td>
      <td>21.60</td>
      <td>21.10</td>
      <td>52.00</td>
      <td>552.00</td>
      <td>544.00</td>
      <td>1098.00</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>100.00</td>
      <td>23.30</td>
      <td>23.10</td>
      <td>24.15</td>
      <td>22.75</td>
      <td>23.60</td>
      <td>66.00</td>
      <td>613.00</td>
      <td>599.00</td>
      <td>1212.00</td>
      <td>100.00</td>
      <td>23.55</td>
      <td>23.70</td>
      <td>23.15</td>
      <td>24.10</td>
      <td>23.05</td>
      <td>77.50</td>
      <td>610.50</td>
      <td>593.50</td>
      <td>1204.00</td>
    </tr>
    <tr>
      <th>max</th>
      <td>100.00</td>
      <td>25.50</td>
      <td>25.30</td>
      <td>26.00</td>
      <td>24.90</td>
      <td>25.50</td>
      <td>100.00</td>
      <td>644.00</td>
      <td>651.00</td>
      <td>1295.00</td>
      <td>100.00</td>
      <td>25.60</td>
      <td>26.00</td>
      <td>25.20</td>
      <td>26.10</td>
      <td>24.90</td>
      <td>100.00</td>
      <td>643.00</td>
      <td>655.00</td>
      <td>1298.00</td>
    </tr>
  </tbody>
</table>
</div>

## Visualize the data


#### Heatmap on the correlations between all numeric features


![png](output_107_0.png)

#### Heatmap on the correlations between SAT and ACT 2017/2018 

> We can observed that there is an inverse correlated with their participation rates. Therefore, it is important for us to capture the space from ACT dominating state

![png](output_108_0.png)

#### Histograms on Participation, Math and EBRW: Opportunity for improvement

> Note that there is number of states that is dominated by ACT,this provide an great opportunity for improvement
- North Dakota
- Wyoming
- South Dakota
- Iowa
- Utah
- Minnesota 
- Nebraska 
- Wisconsin 
- Mississippi

> Next, seems like SAT is having a higher score than ACT. As compare to Reading (ACT) vs SAT (EBRW), both are quite evenly distributed. Therefore, from strategic point of view, SAT is having advantage as there are only two key subject in SAT vs four in ACT.


![png](output_113_0.png)


#### Plot and interpret scatter plots

![png](output_116_0.png) ![png](output_117_0.png)

![png](output_121_1.png) ![png](output_120_1.png)

![png](output_127_0.png) ![png](output_128_0.png) 

![png](output_129_0.png) ![png](output_130_0.png)


## Descriptive and Inferential Statistics

#### Summarizing Distributions

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>act_part</th>
      <th>act_english</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_science</th>
      <th>act_composite</th>
      <th>sat_part</th>
      <th>sat_ebrw</th>
      <th>sat_math</th>
      <th>sat_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
      <td>102.0</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>63.5</td>
      <td>21.0</td>
      <td>21.2</td>
      <td>22.0</td>
      <td>21.2</td>
      <td>21.5</td>
      <td>42.8</td>
      <td>566.4</td>
      <td>551.9</td>
      <td>1123.1</td>
    </tr>
    <tr>
      <th>std</th>
      <td>33.0</td>
      <td>2.4</td>
      <td>2.0</td>
      <td>2.1</td>
      <td>2.6</td>
      <td>2.1</td>
      <td>36.3</td>
      <td>46.4</td>
      <td>68.7</td>
      <td>92.9</td>
    </tr>
    <tr>
      <th>min</th>
      <td>7.0</td>
      <td>16.3</td>
      <td>17.8</td>
      <td>18.0</td>
      <td>2.3</td>
      <td>17.7</td>
      <td>2.0</td>
      <td>480.0</td>
      <td>52.0</td>
      <td>950.0</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>31.0</td>
      <td>19.0</td>
      <td>19.4</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>4.0</td>
      <td>534.2</td>
      <td>522.2</td>
      <td>1055.2</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>66.5</td>
      <td>20.5</td>
      <td>20.9</td>
      <td>21.6</td>
      <td>21.2</td>
      <td>21.4</td>
      <td>45.5</td>
      <td>554.5</td>
      <td>545.5</td>
      <td>1099.0</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>100.0</td>
      <td>23.4</td>
      <td>23.1</td>
      <td>24.2</td>
      <td>23.1</td>
      <td>23.6</td>
      <td>70.0</td>
      <td>613.5</td>
      <td>595.0</td>
      <td>1209.5</td>
    </tr>
    <tr>
      <th>max</th>
      <td>100.0</td>
      <td>26.0</td>
      <td>25.3</td>
      <td>26.1</td>
      <td>24.9</td>
      <td>25.6</td>
      <td>100.0</td>
      <td>644.0</td>
      <td>655.0</td>
      <td>1298.0</td>
    </tr>
  </tbody>
</table>
</div>



#### Distributions in the data



![png](output_146_1.png)


> <span style='color:green'>From the graph observed for 102 samples each for two years, the distribution shown quite normally distributed except participation. For scores related, if we are able to construct using all scores instaed of mean of each state, a more "normal distributed" pattern should be observed. Similary for the participation, if we are able to obtain a smaller zone instead of at state level, a normal distributed pattern should be obtained. Bigger pool of samples will be the key on obtaining the normally distributed pattern.</span>

> <span style='color:green'> In principle, both SAT and ACT should provide a similar assessment on the competency, therefore, there should be no different between SAT or ACT math score assesment. </span> 
<span style='color:green'>Theoritically, both SAT and ACT generally cover the same topics, both ACT and SAT scores are used for college admissions decisions and awarding merit-based scholarships.</span> <span style='color:green'>The null hypothesis is the "status quo" hypothesis that you wish to prove wrong. We typically denote the null hypothesis with  𝐻0 .</span>

<span style='color:green'> However, we can perform a hypothesis test the subject Math to evaluate this.</span>

> <span style='color:green'> $H_0:$ There is NO difference in evaluating college student competency using both test</span>

> <span style='color:green'> $H_A:$ There is difference in evaluating college student competency using both test</span>

<span style='color:green'>**First group of tests, is to ensure there is no different within SAT or ACT**</span>
- <span style='color:green'> Test 1.1 :No different ACT 17 vs ACT 18 </span>
- <span style='color:green'> Test 1.2 :No different SAT 17 vs SAT 18 </span>


<span style='color:green'>**Second group of test, is to ensure there is no different between SAT or ACT**</span>
- <span style='color:green'> Test 2.1 :No different ACT 17 vs SAT 17 </span>
- <span style='color:green'> Test 2.2 :No different ACT 18 vs SAT 18 </span>
- <span style='color:green'> Test 2.3 :No different ACT 17 vs SAT 18 </span>
- <span style='color:green'> Test 2.4 :No different ACT 17/18 vs SAT 17/18 </span>

<span style='color:green'>**Group 1 Tests** </span>


    ACT 17 vs ACT 18 Math P-Value is 88.66%
    SAT 17 vs SAT 18 Math P-Value is 52.99%


> <span style='color:green'>From the above, we can observed that there is no significant within the similar tests</span>

<span style='color:green'>**Group 2 Tests** </span>


    ACT 17 vs SAT 17 Math P-Value is 19.3064%
    ACT 18 vs SAT 18 Math P-Value is 0.4945%
    ACT 17 vs SAT 18 Math P-Value is 0.6726%
    ACT 17/18 vs SAT 18/18 Math P-Value is 0.666%


> <span style='color:green'> **From the above tests, it suggest that there is a different between ACT and SAT after the introduction of SAT 18 into the scenario** </span>

## Outside Research

There are multiple research on providing different view on SAT and ACT. The data show a correlation between higher SAT scores and lower average student debt. 
According to the College Board Website:

> The SAT School Day Program, which allows students to take the SAT during regular school hours usually at no cost, continues to expand.

> More than 2.1 million students in the class of 2018 took the SAT, an increase of 25% over the class of 2017, according to the 2018 SAT Suite of Assessments Program Results.

> In 2014-15, only 4 states (Delaware, Idaho, Maine, District of Columbia) participated in SAT School Day.

> In 2017-18, 10 states (Colorado, Connecticut, Delaware, Idaho, Illinois, Maine, Michigan, New Hampshire, Rhode Island, West Virginia, District of Columbia) administered the SAT to public school students for free.

The above aligned with the finding from the following diagram:

![png](output_161_0.png)

From the above diagram, it seems like SAT is gaining more participation than ACT. Furthermore, the results and participation on both ACT and SAT is inversely related to each other. We could also observed few states with swing of participation corresponding with the relevant score swing as well (Illinois, Colorado...etc.) as mentioned above.

## Conclusions and Recommendations

Based on your exploration of the data, what are you key takeaways and recommendations? Choose one state with a lower participation rate and provide a suggestion for how the College Board might increase participation amongst graduating seniors in this state. Are there additional data you desire that would better inform your investigations?

**Key Take away**

> The ACT and SAT participation seems like inversely correlated with each others, with states that to profer one test than other. ACT seems like is having more 100 % committed states than SAT, this suggestted that ACT is much more popular than SAT. Which provide space for SAT penatration.

> With reference to the last few diagram, ACT and SAT scores are inversely correlated with their participation rates. Those state with lower participation tend to achieving higher score and vice versa. 

> The hypothesis test on SAT & ACT also suggested both tests are different. The tests suggest that there is a different between ACT and SAT after the introduction of SAT 18 into the scenario. One of the key areas could be from Math Subject.

> Therefore, aggressive promotion US States that predominantly administer ACT Test with better access through SAT School Day Programs or free access (or with lower rate) will be the key on promoting SAT in the country.


## Reference


- Ref 1: SAT / ACT Prep Online Guides and Tips](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent)
- Ref 2: SAT reclaims title of most widely used college admission test](https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/)
- Ref 3: Correlation between higher SAT scores and lower average student debt](https://www.nitrocollege.com/research/student-debt-future-earnings)
- Ref 4: Student Debt and future earning](https://www.nitrocollege.com/research/student-debt-future-earnings)
- Ref 5: Wheeler, Danny. “Colorado Changed to the SAT in 2017: What You Need to Know.” Testive, 10 July 2018, www.testive.com/colorado-sat-change-2017/
- Ref 6: Genota, Lauraine. “SAT Scores Rise as Number of Test-Takers Tops 2 Million.” Education Week, 20 Feb. 2019, www.edweek.org/ew/articles/2018/10/31/sat-scores-rise-as-number-of-test-takers.html
- Ref 7: “More Than 2 Million Students in the Class of 2018 Took the SAT, Highest Ever.” The College Board, 18 Mar. 2019, www.collegeboard.org/releases/2018/more-than-2-million-students-in-class-of-2018-took-sat-highest-ever
- Ref 8: “File:SAT-ACT-Preference-Map.svg.” File:SAT-ACT-Preference-Map.svg - Wikimedia Commons, commons.wikimedia.org/wiki/File:SAT-ACT-Preference-Map.svg
- Ref 9: “SAT School Day.” SAT Suite of Assessments, 11 May 2018, collegereadiness.collegeboard.org/sat/k12-educators/sat-school-day.
- Ref 10: Veiga, Christina. “New York City Offers SAT to All High School Juniors, Hoping to Clear a Path to College.” Chalkbeat New York, Chalkbeat New York, 3 Apr. 2017, ny.chalkbeat.org/2017/4/3/21099704/new-york-city-offers-sat-to-all-high-school-juniors-hoping-to-clear-a-path-to-college.



## Other Plots

![png](output_118_0.png) 
![png](output_133_1.png)
![png](output_134_0.png)
![png](output_165_0.png)
![png](output_166_0.png)
![png](output_167_0.png)
![png](output_168_0.png)

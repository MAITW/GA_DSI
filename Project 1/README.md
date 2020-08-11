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

![png](output_118_0.png) ![png](output_120_1.png)

![png](output_121_1.png) ![png](output_127_0.png)

![png](output_128_0.png) ![png](output_129_0.png)

![png](output_130_0.png)


#### Feel free to do additional plots below
*(do research and choose your own chart types & variables)*

Are there any additional trends or relationships you haven't explored? Was there something interesting you saw that you'd like to dive further into? It's likely that there are a few more plots you might want to generate to support your narrative and recommendations that you are building toward. **As always, make sure you're interpreting your plots as you go**.


```python
final_v.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
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
    <tr>
      <th>state</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Alabama</th>
      <td>100.0</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>5.0</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Particiation Rate between SAT vs. ACT
subplot_lmplot(final_v, 'sat_part','act_part', 
                    'SAT Participation rate', 'ACT Participation rate', 
                    'Particiation Rate between SAT vs. ACT')
```


    <Figure size 576x360 with 0 Axes>



![png](output_133_1.png)



```python
# sns.scatterplot(final.state, final.sat_part)
# plt.xticks( rotation= 60 )
# plt.title('SAT Participation Rete Each State');

df_final_NI = pd.read_csv('../data/final_v.csv') # 
df_final_NI.head()
df_final_NI.name ="state"
#df_final_NI.reset_index(inplace=True)`

# df_final_NI.head()
plt.figure(figsize=(15,4))
sns.scatterplot(df_final_NI.state, df_final_NI.sat_part)
plt.xticks( rotation= 90 )
plt.title('SAT Participation Rete Each State');
```


![png](output_134_0.png)



```python
df_final_NI.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>state</th>
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
      <th>0</th>
      <td>Alabama</td>
      <td>100.0</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>5.0</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alaska</td>
      <td>65.0</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>38.0</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Arizona</td>
      <td>62.0</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>30.0</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arkansas</td>
      <td>100.0</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>3.0</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>California</td>
      <td>31.0</td>
      <td>22.5</td>
      <td>22.7</td>
      <td>23.1</td>
      <td>22.2</td>
      <td>22.8</td>
      <td>53.0</td>
      <td>531.0</td>
      <td>524.0</td>
      <td>1055.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# final['sat_part_18'] # Alabama 6, Alaska 43
final['sat_part_17'] # Alabama 6, Alaska 43
```




    state
    Alabama                   5.0
    Alaska                   38.0
    Arizona                  30.0
    Arkansas                  3.0
    California               53.0
    Colorado                 11.0
    Connecticut             100.0
    Delaware                100.0
    District of Columbia    100.0
    Florida                  83.0
    Georgia                  61.0
    Hawaii                   55.0
    Idaho                    93.0
    Illinois                  9.0
    Indiana                  63.0
    Iowa                      2.0
    Kansas                    4.0
    Kentucky                  4.0
    Louisiana                 4.0
    Maine                    95.0
    Maryland                 69.0
    Massachusetts            76.0
    Michigan                100.0
    Minnesota                 3.0
    Mississippi               2.0
    Missouri                  3.0
    Montana                  10.0
    Nebraska                  3.0
    Nevada                   26.0
    New Hampshire            96.0
    New Jersey               70.0
    New Mexico               11.0
    New York                 67.0
    North Carolina           49.0
    North Dakota              2.0
    Ohio                     12.0
    Oklahoma                  7.0
    Oregon                   43.0
    Pennsylvania             65.0
    Rhode Island             71.0
    South Carolina           50.0
    South Dakota              3.0
    Tennessee                 5.0
    Texas                    62.0
    Utah                      3.0
    Vermont                  60.0
    Virginia                 65.0
    Washington               64.0
    West Virginia            14.0
    Wisconsin                 3.0
    Wyoming                   3.0
    Name: sat_part_17, dtype: float64




```python
final.head()
Different = final['sat_part_18']-final['sat_part_17']
```

#### (Optional): Using Tableau, create a choropleth map for each variable using a map of the US. 

Save this plot as an image file in an images directory, provide a relative path, and insert the image into notebook in markdown.

## Descriptive and Inferential Statistics

#### Summarizing Distributions

Above, we used pandas `describe` to provide quick summary statistics of our numeric columns. We also demonstrated many visual relationships.

As data scientists, having a complete understanding of data is imperative prior to modeling.

While we will continue to build our analytic tools, we know that measures of *central tendency*, *spread*, and *shape/skewness* provide a quick summary of distributions.

For each variable in your data, summarize the underlying distributions (in words & statistics)
 - Be thorough in your verbal description of these distributions.
 - Be sure to back up these summaries with statistics.


```python
round(final_v.describe(),1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
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



Answers:


#### Distributions in the data

In this dataset, each data represents a sample from a population.                        
For example, for ACT math test:
- Population: the test results of all the students who take this test, nation-wide.
- Population mean: is the national average of ACT math test (total scores/total no. of test takers) 
- Sample: the state means of ACT math test. We have 51 samples (51 states)

***According to CLT, we generally assuming that data we sample from a population will be normally distributed. Do we observe this trend?***

Answer:

Does This Assumption Hold for:
    - Math
    - Reading
    - Rates
Explain your answers for each distribution and how you think this will affect estimates made from these data.


```python
sns.set(style="darkgrid", palette="coolwarm_r", color_codes=True)
fig, axes = plt.subplots(2, 3, sharex=True, figsize=(30,10))
fig.suptitle('ACT sample distribution', fontsize=50)
plot1 = (final_v['act_math']/32)*100
plot2 = (final_v['act_reading']/32)*100
plot3 = final_v['act_part']
plot4 = (final_v['sat_math']/800)*100
plot5 = (final_v['sat_ebrw']/800)*100
plot6 = final_v['sat_part']
sns.distplot(plot1, kde=True, color="g", ax=axes[0,0])
sns.distplot(plot2, kde=True, color="g", ax=axes[0,1])
sns.distplot(plot3, kde=True, color="g", ax=axes[0,2])
sns.distplot(plot4, kde=True, color="g", ax=axes[1,0])
sns.distplot(plot5, kde=True, color="g", ax=axes[1,1])
sns.distplot(plot6, kde=True, color="g", ax=axes[1,2])
fz = 30
axes[0,0].set_title('ACT 17/18 Math Score Distribution in %', fontsize=fz)
axes[0,1].set_title('ACT 17/18 Reading Score Distribution in %', fontsize=fz)
axes[0,2].set_title('ACT 17/18 Participation Distribution in %', fontsize=fz)
axes[1,0].set_title('SAT 17/18 Math Score Distribution in %', fontsize=fz)
axes[1,1].set_title('SAT 17/18 Reading Score Distribution in %', fontsize=fz)
axes[1,2].set_title('SAT 17/18 Participation Distribution in %', fontsize=fz)
```




    Text(0.5, 1.0, 'SAT 17/18 Participation Distribution in %')




![png](output_146_1.png)


<span style='color:green'>**Answer:** </span>
<span style='color:green'>From the graph observed for 102 samples each for two years, the distribution shown quite normally distributed except participation. For scores related, if we are able to construct using all scores instaed of mean of each state, a more "normal distributed" pattern should be observed. Similary for the participation, if we are able to obtain a smaller zone instead of at state level, a normal distributed pattern should be obtained. Bigger pool of samples will be the key on obtaining the normally distributed pattern.</span>

#### Estimate Limits of Data

Suppose we only seek to understand the relationship between SAT and ACT participation rates in 2017. 

##### Does it make sense to conduct statistical inference given these data specifically? 

Why or why not?

<span style='color:green'>**Answer:** </span>
- <span style='color:green'>Yes, since we only have a sample of two years, we should be able to perform the statistical inferencing. </span>
- <span style='color:green'>There are some convolution on the data as people who took both SAT and ACT test. </span>

*(think about granularity, aggregation, the relationships between populations size & rates...consider the actually populations these data describe in answering this question)*

##### Is it appropriate to compare *these* specific SAT and ACT math scores  - can we say students with higher SAT math score is better than those with lower ACT math score, or vice versa?

Why or why not? 

<span style='color:green'> **Answer:** </span>
<span style='color:green'> In principle, both SAT and ACT should provide a similar assessment on the competency, therefore, there should be no different between SAT or ACT math score assesment. </span> 
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


```python
Score_A = (final['act_math_17'])
Score_B = (final['act_math_18'])
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("ACT 17 vs ACT 18 Math P-Value is {}%".format(round(p_value*100,2)))

Score_A = (final['sat_math_17'])
Score_B = (final['sat_math_18'])
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("SAT 17 vs SAT 18 Math P-Value is {}%".format(round(p_value*100,2)))
```

    ACT 17 vs ACT 18 Math P-Value is 88.66%
    SAT 17 vs SAT 18 Math P-Value is 52.99%


<span style='color:green'>From the above, we can observed that there is no significant within the similar tests</span>

<span style='color:green'>**Group 2 Tests** </span>


```python
Score_A = (final['act_math_17']/32)*100
Score_B = (final['sat_math_17']/800)*100
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("ACT 17 vs SAT 17 Math P-Value is {}%".format(round(p_value*100,4)))
Score_A = (final['act_math_18']/32)*100
Score_B = (final['sat_math_18']/800)*100
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("ACT 18 vs SAT 18 Math P-Value is {}%".format(round(p_value*100,4)))
Score_A = (final['act_math_17']/32)*100
Score_B = (final['sat_math_18']/800)*100
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("ACT 17 vs SAT 18 Math P-Value is {}%".format(round(p_value*100,4)))
Score_A = (final_v['act_math']/32)*100
Score_B = (final_v['sat_math']/800)*100
t_stat, p_value = stats.ttest_ind(Score_A, Score_B, equal_var=False)
print("ACT 17/18 vs SAT 18/18 Math P-Value is {}%".format(round(p_value*100,4)))
```

    ACT 17 vs SAT 17 Math P-Value is 19.3064%
    ACT 18 vs SAT 18 Math P-Value is 0.4945%
    ACT 17 vs SAT 18 Math P-Value is 0.6726%
    ACT 17/18 vs SAT 18/18 Math P-Value is 0.666%


<span style='color:green'> **Answer:** </span>
<span style='color:green'> From the above tests, it suggest that there is a different between ACT and SAT after the introduction of SAT 18 into the scenario </span>

#### Statistical Evaluation of Distributions 

**If you feel it's appropriate**, using methods we discussed in class, run hypothesis tests to compare variables of interest in our dataset. 

## Outside Research

Based upon your observations, choose **three** states that demonstrate interesting trends in their SAT and/or ACT participation rates. Spend some time doing outside research on state policies that might influence these rates, and summarize your findings below. **Feel free to go back and create new plots that highlight these states of interest**. If you bring in any outside tables or charts, make sure you are explicit about having borrowed them. If you quote any text, make sure that it renders as being quoted. (Make sure that you cite your sources -- check with you local instructor for citation preferences).

- [Ref1: SAT / ACT Prep Online Guides and Tips](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent)
- [Ref2: SAT reclaims title of most widely used college admission test](https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/)
- [Ref3: Correlation between higher SAT scores and lower average student debt](https://www.nitrocollege.com/research/student-debt-future-earnings)
- [Ref4: Student Debt and future earning](https://www.nitrocollege.com/research/student-debt-future-earnings)

<span style='color:green'> **Answer:** </span>
<span style='color:green'> According to the web as shown in above the link, there are multiple research on providing different view on SAT and ACT. The data show a correlation between higher SAT scores and lower average student debt{Ref 4}. More time will be needed to perform data collection and cleaning in order to perform the necessary analysis. </span>


```python
ACT_SAT = final[['act_part_17','act_part_18', 'sat_part_17','sat_part_18',
                 'act_composite_17','act_composite_18','sat_total_17','sat_total_18']
               ].sort_values(by = ['act_part_17'], ascending=True)
ACT_SAT.reset_index(inplace=True)
ACT_SAT['act_part_delta'] = ACT_SAT['act_part_18'] - ACT_SAT['act_part_17']
ACT_SAT['sat_part_delta'] = ACT_SAT['sat_part_18'] - ACT_SAT['sat_part_17']
ACT_SAT['act_composite_17'] = round((ACT_SAT['act_composite_17']/32)*100,2)
ACT_SAT['act_composite_18'] = round((ACT_SAT['act_composite_18']/32)*100,2)
ACT_SAT['sat_total_17'] = round((ACT_SAT['sat_total_17']/1600)*100,2)
ACT_SAT['sat_total_18'] = round((ACT_SAT['sat_total_18']/1600)*100,2)
ACT_SAT['act_composite_delta'] = ACT_SAT['act_composite_18'] - ACT_SAT['act_composite_17']
ACT_SAT['sat_total_delta'] = ACT_SAT['sat_total_18'] - ACT_SAT['sat_total_17']
ACT_SAT[['act_part_delta','sat_part_delta','act_composite_delta','sat_total_delta']]

plt.figure(figsize=(8,10))
plt.style.use('seaborn-bright')

y11 = ACT_SAT['state']
x11 = ACT_SAT['act_part_delta']
plt.plot(x11, y11, label = "ACT Participation differences between 2018/2017 ",linestyle='-', color='b',lw=1.5)
y12 = ACT_SAT['state']
x12 = ACT_SAT['act_composite_delta']
plt.plot(x12, y12, label = "ACT Composite differences between 2018/2017 ", linestyle='--',color='b',lw=1)


y21 = ACT_SAT['state']
x21 = ACT_SAT['sat_part_delta']
plt.plot(x21, y21, label = "SAT Participation differences between 2018/2017",linestyle='-',color='g',lw=1.5)
y22 = ACT_SAT['state']
x22 = ACT_SAT['sat_total_delta']
plt.plot(x22, y22, label = "SAT Total differences between 2018/2017 ", linestyle='--',color='g',lw=1)

plt.title('ACT vs SAT 2017/2018 Participation vs Composite/Total Score', fontsize=20)
# plt.axvline(25, linestyle='--', lw = 1, color="r", label= "25%")
# plt.axvline(75, linestyle='--', lw = 1, color="r", label= "75%")
# plt.axvline(50, linestyle='-', lw = 1, color="r", label= "50%")
plt.legend(loc='upper left',prop={'size': 7})
plt.rc('xtick',labelsize=9)
plt.rc('ytick',labelsize=9)
plt.show()

```


![png](output_161_0.png)


<span style='color:green'> **Answer:** </span>
<span style='color:green'> From the above diagram, it seems like SAT is gaining more participation than ACT. Furthermore, the results and participation on both ACT and SAT is inversely related to each other. We could also observed few states with swing of participation corresponding with the relevant score swing as well (Illinois, Colorado...etc.)</span>


```python
ACT_LowestParticipation = final[['act_part_17','act_part_18','act_math_17',
                                 'act_math_18','act_reading_17','act_reading_18',
                                 'act_composite_17','act_composite_18']
                               ].sort_values(by = ['act_part_17','act_part_18'], ascending=True)
ACT_LowestParticipation.reset_index(inplace=True)
ACT_LowestParticipation['act_composite_17'] = round((ACT_LowestParticipation['act_composite_17']/32)*100,2)
ACT_LowestParticipation['act_composite_18'] = round((ACT_LowestParticipation['act_composite_18']/32)*100,2)
ACT_LowestParticipation['act_math_17'] = round((ACT_LowestParticipation['act_math_17']/32)*100,2)
ACT_LowestParticipation['act_math_18'] = round((ACT_LowestParticipation['act_math_18']/32)*100,2)
ACT_LowestParticipation['act_reading_17'] = round((ACT_LowestParticipation['act_reading_17']/32)*100,2)
ACT_LowestParticipation['act_reading_18'] = round((ACT_LowestParticipation['act_reading_18']/32)*100,2)
```


```python
SAT_LowestParticipation = final[['sat_part_17','sat_ebrw_17','sat_math_17',
                                 'sat_total_17','sat_part_18','sat_ebrw_18',
                                 'sat_math_18','sat_total_18']
                               ].sort_values(by = ['sat_part_17','sat_part_18'], ascending=True)
SAT_LowestParticipation.reset_index(inplace=True)
SAT_LowestParticipation['sat_total_17'] = round((SAT_LowestParticipation['sat_total_17']/1600)*100,2)
SAT_LowestParticipation['sat_total_18'] = round((SAT_LowestParticipation['sat_total_18']/1600)*100,2)
SAT_LowestParticipation['sat_ebrw_17'] = round((SAT_LowestParticipation['sat_ebrw_17']/800)*100,2)
SAT_LowestParticipation['sat_ebrw_18'] = round((SAT_LowestParticipation['sat_ebrw_18']/800)*100,2)
SAT_LowestParticipation['sat_math_17'] = round((SAT_LowestParticipation['sat_math_17']/800)*100,2)
SAT_LowestParticipation['sat_math_18'] = round((SAT_LowestParticipation['sat_math_17']/800)*100,2)
```


```python
y1 = ACT_LowestParticipation['state']
x1 = ACT_LowestParticipation['act_part_17']
plt.figure(figsize=(8,10))
# plt.xticks( rotation= 90 )
plt.style.use('seaborn-bright')
plt.plot(x1, y1, label = "ACT2017 Participation", color='b',lw=2)

y11 = ACT_LowestParticipation['state']
x11 = ACT_LowestParticipation['act_composite_17']
plt.plot(x11, y11, label = "ACT2017 Score", color='g',lw=2)
plt.title('ACT 17 Score and Participation in%', fontsize=20)
plt.axvline(25, linestyle='--', lw = 1, color="r", label= "25%")
plt.axvline(75, linestyle='--', lw = 1, color="r", label= "75%")
plt.axvline(50, linestyle='-', lw = 1, color="r", label= "50%")
plt.legend(loc='upper left',prop={'size': 7})
plt.rc('xtick',labelsize=7)
plt.rc('ytick',labelsize=7)
plt.show()
```


![png](output_165_0.png)



```python
ACT_LowestParticipation = final[['act_part_18','act_composite_18']
                               ].sort_values(by = ['act_part_18'], ascending=True)
ACT_LowestParticipation.reset_index(inplace=True)
ACT_LowestParticipation['act_composite_18'] = round((ACT_LowestParticipation['act_composite_18']/32)*100,2)

y1 = ACT_LowestParticipation['state']
x1 = ACT_LowestParticipation['act_part_18']
plt.figure(figsize=(8,10))
# plt.xticks( rotation= 90 )
plt.style.use('seaborn-bright')
plt.plot(x1, y1, label = "ACT2018 Participation", color='b',lw=2)

y11 = ACT_LowestParticipation['state']
x11 = ACT_LowestParticipation['act_composite_18']
plt.plot(x11, y11, label = "ACT2018 Score", color='g',lw=2)
plt.title('ACT 18 Score and Participation in%', fontsize=20)
plt.axvline(25, linestyle='--', lw = 1, color="r", label= "25%")
plt.axvline(75, linestyle='--', lw = 1, color="r", label= "75%")
plt.axvline(50, linestyle='-', lw = 1, color="r", label= "50%")
plt.legend(loc='upper left',prop={'size': 7})
plt.rc('xtick',labelsize=7)
plt.rc('ytick',labelsize=7)
plt.show()
```


![png](output_166_0.png)



```python
plt.figure(figsize=(8,10))
y2 = SAT_LowestParticipation['state']
x2 = SAT_LowestParticipation['sat_part_17']
plt.plot(x2, y2, label = "SAT2017 Participation", color='b',lw=2)

y21 = SAT_LowestParticipation['state']
x21 = SAT_LowestParticipation['sat_total_17']
plt.plot(x21, y21, label = "SAT2017 Score", color='g',lw=2)
plt.title('SAT 17 Score and Participation in%', fontsize=20)
plt.axvline(25, linestyle='--', lw = 1, color="r", label= "25%")
plt.axvline(50, linestyle='-', lw = 1, color="r", label= "50%")
plt.axvline(75, linestyle='--', lw = 1, color="r", label= "75%")
plt.legend(loc='upper left',prop={'size': 10})
plt.rc('xtick',labelsize=9)
plt.rc('ytick',labelsize=9)
plt.show()
```


![png](output_167_0.png)



```python
SAT_LowestParticipation = final[['sat_part_18','sat_total_18']
                               ].sort_values(by = ['sat_part_18'], ascending=True)
SAT_LowestParticipation.reset_index(inplace=True)
SAT_LowestParticipation['sat_total_18'] = round((SAT_LowestParticipation['sat_total_18']/1600)*100,2)

plt.figure(figsize=(8,10))
y2 = SAT_LowestParticipation['state']
x2 = SAT_LowestParticipation['sat_part_18']
plt.plot(x2, y2, label = "SAT2018 Participation", color='b',lw=2)

y21 = SAT_LowestParticipation['state']
x21 = SAT_LowestParticipation['sat_total_18']
plt.plot(x21, y21, label = "SAT2018 Score", color='g',lw=2)
plt.title('SAT 18 Score and Participation in%', fontsize=20)
plt.axvline(25, linestyle='--', lw = 1, color="r", label= "25%")
plt.axvline(50, linestyle='-', lw = 1, color="r", label= "50%")
plt.axvline(75, linestyle='--', lw = 1, color="r", label= "75%")
plt.legend(loc='upper left',prop={'size': 10})
plt.rc('xtick',labelsize=9)
plt.rc('ytick',labelsize=9)
plt.show()
```


![png](output_168_0.png)


## Conclusions and Recommendations

Based on your exploration of the data, what are you key takeaways and recommendations? Choose one state with a lower participation rate and provide a suggestion for how the College Board might increase participation amongst graduating seniors in this state. Are there additional data you desire that would better inform your investigations?

<span style='color:green'>**Key Take away**</span>
<span style='color:green'>Preliminary analysis can conclude the following:</span>
><span style='color:green'>The ACT and SAT participation seems like inversely correlated with each others, with states that to profer one test than other. ACT seems like is having more 100 % committed states than SAT, this suggestted that ACT is much more popular than SAT.</span>

><span style='color:green'> With reference to the last few diagram, ACT and SAT scores are inversely correlated with their participation rates. Those state with lower participation tend to achieving higher score and vice versa. 

><span style='color:green'>The hypothesis test on SAT & ACT also suggested both tests are different. The tests suggest that there is a different between ACT and SAT after the introduction of SAT 18 into the scenario </span>
    
><span style='color:green'>More data sets will need to be introduced in oder to have a more comprehensive and in depth conclusion on both SAT and ACT. Theses data sets should include (but not limited) race, gendar, school acceptance level (in quantity) on both ACT and SAT. </span>


## Other Plots



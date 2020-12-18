---
layout: page
title: Are racial bias and political orientation correlated in police stops?
subtitle: Study of concrete parameters in red and blue regions of the US
comments: False
cover-img: /assets/img/1280px-Red_state,_blue_state.png

---
# A worrying political context

<img style="padding-right: 15px" align="left" width="250" src="assets/img/manif.png">
At a time where the Black Lives Matter movement has gone global and with an overall denunciation of police violence in many countries we have decided to take a closer look at the police arrests in the USA. What we want to know is: is there a racist bias in police stops in the US ? If so, what link could it have with the political inclination of the region studied ?

Stanford's open policing study has shown how police behaviour can suggest presence of prejudice towards different ethnic origins. Needless to say that, if significant, correlations between political inclination and racial disparities in police stops would cause even more questioning on the values represented by certain political parties. 

<img style="padding-right: 15px" align="right" width="225" src="assets/img/blacklivesmatter.png">

# Let's quantify racial bias
## What data are we looking at ?
For this study we used a dataset of 100 million traffic stops across the United States aggregated over varying time periods between 2000s and 2018. We compare this data with the results of the 2016 US presidential elections taken from [The New York Times website](https://www.nytimes.com/elections/2016/results/president).

## Is racial bias measurable ?
This is difficult to quantify because many parameters are subjective. This is why we are interested in car stops and the potential searches to which they lead. This makes it possible to study uniform and more concrete characteristics: location, reason for the arrest, decision to search, "success" of the search, and colour of the driver.
We focus on two parameters:
- the **hit rate**, the "success" rate of searches for drug possession during police arrests. 
A lower hit rate may indicate that the police officer initiated a search with less evidence, which may be biased by the colour of the driver's skin.  
- the **threshold**: the level of evidence necessary for the police officer to decide to search someone.
If it is lower, it may also show a bias on the part of the police officer.
.
After counting these parameters we will **compare the results between <span style="color:Maroon">red</span> and <span style="color:Navy">blue</span> states** !

> **Quick note for better understanding:**  As stated in the paper, the hit rate is "_the proportion of searches that successfully turn up contraband_". The inferred threshold is calculated thanks to the threshold test and is also found in the dataset of the paper. It is known to "_incorporates both the rate at which searches occur, as well as the success rate of those searches_" and reflects the level of the "_evidentiary bar applied when making search decisions_". Therefore, a lower inferred threshold shows an inclination of searching a driver without evidence against him or her, as well as a lower hit rate.

# Comparing red and blue states
## Which states and why ?
Selecting which state to represent requires multiple steps. 
First of all, not all states have all of the required information for our study, that is the calculations of hit rate and threshold test. This first narrows us down to the states of: **_Connecticut, Illinois, North Carolina, Rhode Island, South Carolina, Texas, Washington, and Wisconsin_**. 
Now, let's select states that seem to be most significant: that is, the ones that had the highest percentage of votes for the party that won. This takes out North Carolina, which had a major percentage very close to 50%. Finally, we took out Wisconsin, since it tends to be a swing state.

This divides our 6 remaining states into two groups: <span style="color:Maroon">South Carolina and Texas</span> in the red group, and <span style="color:Navy">Illinois, Connecticut, Rhode Island and Washington</span> in the blue group.

## Data vizualization 

Before plotting our rates, we first want to check if our dataset is big enough: are there enough police stops and searches for our results to be significant? The results are in the following table: 

<center>
<table class="tg">
<tbody>
  <tr>
    <td align = "center" class="tg-0lax">State group</td>
    <td align = "center" class="tg-0lax">Number of stops per year</td>
    <td align = "center" class="tg-0lax">Number of searches per year</td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax"><span style="color:Maroon">Red</span></td>
    <td align = "center" class="tg-0lax"><span> 2 104 964.4</span></td>
    <td align = "center" class="tg-0lax"><span> 47 958.6 </span></td>
  </tr>
    <tr>
    <td align = "center" class="tg-0lax"><span style="color:Navy">Blue</span></td>
    <td align = "center" class="tg-0lax"><span> 1 071 249.6</span></td>
    <td align = "center" class="tg-0lax"><span> 29 642.0 </span></td>
  </tr>
</tbody>
</table>
</center>

Okay, we're talking _millions_ of samples. Looks big enough! Let's proceed with our plots for hit rates and threshold tests.

## Hit rates and threshold in blue states compared to red states

Let's have a first look at our data through the following visualization:

![Hit and threshold, vizualization](/assets/img/Unknown.png){: .mx-auto.d-block :}

Here we _normalized_ black and hispanic hit rates in each state to the respective white hit rate. That allows to have only numbers between zero and one and visualize in a clearer way the difference between them. Also, a state could have only low hit rates for every ethnic origins, without this indication more or less discrimination.

- Can you see how **all thresholds** (_right plot_) **for minorities are lower than the one for white drivers** ?
- It's almost **the same for the hit rates** (_left plot_) ! Can you spot the two states that make an exception ? (it's Illinois and South Carolina)
- All **parameters for hispanic drivers are lower than for black drivers**, with a few exception where they're the same (hit rate in Connecticut, threshold in Connecticut and Illinois)

But ... Can we **_really_** see a difference between red and blue states here ?

Now, let's look at the **distribution** of these findings. We plot a parameter for a minority (_ex. the hit rate for black drivers_) against the one for white drivers. **The ratio minority/white should be 1** if there is no disparity, with a point on the plot at the level of the diagonal we plot. See the results here:

![Hit, national](/assets/img/hit rate, national.png){: .mx-auto.d-block :}
![Threshold, national](/assets/img/threshold, national.png){: .mx-auto.d-block :}

Oops, can you see how **the majority of the points are below the diagonal**, with a particulary long distance in the threshold plot in blue states (_left plot, below_).

More generally, we can observe that: 
- there are clearly more points below the diagonal than on and above it
- for the **hit rates, it doesn't matter if you're in a <span style="color:Navy">blue</span> or <span style="color:Maroon">red</span> state**: hispanic drivers are even further below the diagonal than for black drivers. This means that **searches on hispanic drivers have lower relative hit rates** than the ones on black drivers.
- for the **threshold**: in **<span style="color:Maroon">red states</span>**, we observe the same pattern, with **lower threshold for hispanic drivers** than for black drivers. In **<span style="color:Navy">blue states</span>** however, we observe the **same disparity for both race**.

But be careful: there are a large amount of points in red states and far less in blue states, which can trouble and bias visualization. Note that the size of the points correspond to the number of police search per year for this race in the county considered

As a conclusion : **Non-Caucasian drivers have lower values for hit rates and threshold, in _all_ color of state, than white drivers. Moreover, this gap widens even more for hispanic drivers** !

## Statistics
### Tableau avec normalized and weighted mean:
<p float="left">
  <img src="/assets/img/blue_national.png" width="350" />
  <img src="/assets/img/red_national.png" width="350" /> 
</p>
 
Here we have two tables. They contain normalization of party average race specific hit rates and inferred thresholds with respect to white values, and weighted average of normalized data.
Let's compare red vs blue: normalized means are lower in blue states than in red states. Also, while weighted means tend to be lower than their unweighted equivalent in blue states, the opposite trend is seen with weighted averages in red states. What does this mean? Well, we have differences between the normalized means that are even **bigger** between red and blue states when weighing our data.

Regardless, statistical tests are necessary in order to quantify the **significance** of these differences.

### Mann-Whitney U test
Okay, but which test is appropriate? After trying out different tests on the distribution of the variables, we prefered to use the Mann-Whitney U test to compare the means because we assume that the distributions are not normal. Our null hypothesis: means from blue and red states are the same. 
The null hypothesis will be rejected in the case that the p value is less than 0.05. Rejection of the null hypothesis will support the claim that the means are significantly better.

The results are as follows:

<center>
<table class="tg">
<tbody>
  <tr>
    <td align = "center" class="tg-0lax"></td>
    <td align = "center" class="tg-0lax">p-value</td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Non-normalized</td>
    <td align = "center" class="tg-0lax"> <span style="font-weight:normal;font-style:normal;text-decoration:none">2.2283e-06</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Normalized</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.14982</span></td>
  </tr>
</tbody>
</table>
</center>

We can see that normalizing is important: without normalization the means are clearly not the same! The non-normalized hit rates test supports the claim that the means are significantly different. Meanwhile, the test for normalized hit rates does not enable us to reject the hypothesis that the means are the same. Therefore, from now on, we will only compare normalized values.

Okay, let's run some more tests! This time on the mean hit rates and thresholds for black and hispanic people:
<center>
<table class="tg">
<tbody>
  <tr>
    <td align = "center" class="tg-0lax"></td>
    <td align = "center" class="tg-0lax">p-value</td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Black hit rate</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">3.5143e-16</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Hispanic hit rate</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.08968</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Black threshold</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.19645</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Hispanic threshold</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.14982</span></td>
  </tr>
</tbody>
</table>
</center>

Given these p values we can only reject the null hypothesis for **mean black thresholds**, suggesting bias in black thresholds for blue states. The rest of p values are small but not low enough to reject the null hypotheses.

## Prediction model
We also trained models on the data that predict the normalised, weighted average for both hit rate and threshold. Our goal was to see whether it associated a significant coefficient to parameters like the party of the state. No such coefficient were found, with large pvalue that cannot allow us to conclude anything.

## Our first observations
Oops. Apparently there is a significant difference according to our statistical tests. But it's not obvious! How can we sharpen our study?
The election results we used are state-wide. As they cover a very large population and a very large number of counties, they average and homogenize the results ! For example, a **blue county within a red state will distort our correlation study**. In order to have more accurate results and more representative percentages of the population in each county, we will study blue counties VS red counties, and we will use the results **county by county**.

# Let's take a closer look !
## Texas counties: <span style="color:Navy">blue</span> and <span style="color:Maroon">red</span> repartition
As a start, here's a map of election results in Texas, each portion being a county. See how many blue counties there are even when Texas is a traditionnal red state ?
Also, note that big cities tend to be located in blue counties, whereas more rural areas represent red counties. Dallas is the little blue squared, isolated amoung red ones in the top right region !
<p align="center">
  <img width="425" src="assets/img/texas.png" />
</p>

Let's look at how the hit rate and threshold repartition changes based on the county color.

Once again, we are looking at large numbers of police stops - no worries for the significancy of our results ! See by yourself : 

| Texas county group | Number of stops per year | Number of searches per year|
| :------ |:--- | :--- |
| <span style="color:Maroon">Red counties</span> | 2 827 560 | 23681 |
| <span style="color:Navy">Blue counties</span> | 1 107 608 | 4153.9 |

## Comparison of red and blue counties
Again, let’s have a first look at our data through the following visualization:
<p align="center">
  <img width="600" src="/assets/img/visual_county.png" />
</p>

This plot shows normalized hit rates and threshold for both blue and red counties.
- Same pattern as at the state-level (almost all values below one, so lower than the equivalent for white drivers)
- Always **lower values for hispanic drivers** than black drivers
- **Not so big differences in hit rates** between red and blue counties
- For **thresholds**, a small gap with **lower values for <span style="color:Maroon">red counties</span>**.

Following we have the equivalent of the previous plots, but at the Texas level, where the points take the color of the county, not of the state:
![Hit, Texas](/assets/img/hit_rate_tx.png)
![Threshold, Texas](/assets/img/threshold_tx.png)

## Our observations
First, let's specify that we have clearly _too few points_ in blue states to allow a global visualization and obvious conclusion drawing from these plots. But still, we can make a few observations :
About disparities : 
- **a disparity remains between black and hispanic drivers**, with hispanic hit rates and thresholds further from the diagonal than black ones. **This is seen in county groups** and for all parameters.
- some relative hit rates and thresholds for black drivers are even above the diagonal, but almost none for hispanic drivers

About red and blue differences:
- Red counties tend to have very <span style="color:Maroon">spread points</span>and some are <span style="color:Maroon">really far below the diagonal</span>. In the blue states we don't see points that far away.
- Blue counties points are not numerous, but some represent a large numbers of police searches. Their repartition is <span style="color:Navy">globally close to the diagonal</span>.
- all parameters seem to be higher in red counties, even for white drivers: the dots are located in the middle of the diagonal, with no dot close to the origin. Why is that ? We will try to answer this question at the end of our data story.

## Statistics
### Tableau avec normalized and weighted mean:
<p float="left">
  <img src="/assets/img/blue_tx.png" width="350" />
  <img src="/assets/img/red_tx.png" width="350" /> 
</p>
**ajouter discussion**

### Mann-Whitney U test
Okay, juste like with the states' comparison, let's run the Mann-Whitney U test on the normalized values for each parameter and each race:

<center>
<table class="tg">
<tbody>
  <tr>
    <td align = "center" class="tg-0lax"></td>
    <td align = "center" class="tg-0lax">p-value</td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Black hit rate</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.64224</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Hispanic hit rate</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.14101</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Black threshold</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.00734</span></td>
  </tr>
  <tr>
    <td align = "center" class="tg-0lax">Mean Hispanic threshold</td>
    <td align = "center" class="tg-0lax"><span style="font-weight:normal;font-style:normal;text-decoration:none">0.00641</span></td>
  </tr>
</tbody>
</table>
</center>

Given these p values we can only reject the null hypothesis for **mean black and thresholds**, suggesting bias in these thresholds for blue states. The rest of p values are small but not low enough to reject the null hypotheses.

## Investigation of other parameters
What if other parameters comes into play ? Blue counties are also where cities take place. Apart from their political orientation in which they usually differ from the countryside, other parameters are to be taken into account. For example, there are more police searches there. We checked if there was a link between the number of searches and the hit rate or threshold, thanks to the Spearman test that measures the dependency between two variables. We found none. This allows us to take away another variable. 

# Can we conclude anything ?
## What we cannot say
Don't draw conclusions too quickly !

It is very important to remember that we are only _observing_ certain characteristics. They have certainly been chosen because they allow a quantification of clear parameters that can be linked to, among other things, the race of the driver. 
However, **it is important to remember that this is an observational study** and not an experiment: we do not know all about the environment in which these arrests took place, nor the various parameters that could have affected them - even though we thought of some. **We point out that disparities in these parameters seem correlated to the race of the driver**, but **we do not establish a causal link**, due to the lack of a sufficiently rigorous and varied investigation (historical and political context, sociological study, comparison with other countries, comparison with other types of police intervention, etc.) to conclude in this way.

## What we can say...
### Clear conclusions on Non-Caucasian drivers hit rates and thresholds
As stated in the Stanford University paper, we did observe lower hit rate and threshold values for non-Caucasian drivers, suggesting a bias in the decision of conducting of search by police officer for these drivers. In addition, the values for Hispanic drivers differed even more markedly from their equivalent for white drivers.

### No clear conclusion about state major political party
Although the averages of the normalised parameters are **lower in the red states than in the blue states** (found thanks to the Mann-Whitney test), the global distributions are not obviously different between the two groups of states. Our data and therefore our results remain heterogeneous and have no clear trend according to the colour of the state. As the states include a large number of counties that are themselves very various in terms of police stops and political orientation, we cannot base our study on the state level. If there is a correlation, it is normal that it is not or hardly visible at this level. We have to look at the counties to find out more !

### 
 ???? 

# References
- [New York Times, 2016 Presidential Election Results](https://www.nytimes.com/elections/2016/results/president), consulted in 2020
[NYT]: https://www.nytimes.com/elections/2016/results/president

- [Stanford Computational Journalism Lab and the Stanford Computational Policy Lab](https://openpolicing.stanford.edu/), The Stanford Open Policing Project, 2020
[Stanford]: https://openpolicing.stanford.edu/

- [Unsplash](https://unsplash.com/): photo for everyone, consulted in december 2020: 

- [Wikipédia, 2016 United States presidential election](https://en.wikipedia.org/wiki/2016_United_States_presidential_election)

# Thank you for your attention ! 

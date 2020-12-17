---
layout: page
title: Are racism and political orientation correlated ?
subtitle: Study of concrete parameters in red and blue regions of the US
comments: False
cover-img: /assets/img/1280px-Red_state,_blue_state.png

---
![police](assets/img/fucklapolice.png = 100){: .mx-auto.d-block :}

test:
<img align="left" width="100" src="assets/img/fucklapolice.png">
# A worrying political context
At a time of the _Black Lives Matter_ movement, the denunciation of police violence in many countries, with a change of president of the USA approaching, we have decided to take a closer look at the police arrests in the USA. What we want to know is: is there a racist bias in police stops in the US ? If so, what link could it have with the political inclination of the region studied ?

![manif](assets/img/blacklivesmatter.png = 100){: .mx-auto.d-block :}


Today, we study the police behaviour as a barometer of prejudices toward different ethnic origins. No need to tell you that any correlation with a political inclination would be even more questioning about the values spread by certain political parties...

# Let's quantify racism
## What data are we looking at ?
For this study we used a dataset of **100 million traffic stops** across the United States, with various time ranges for each state. We also compare this data with the [New York Times website](https://www.nytimes.com/elections/2016/results/president), which reports the results to the **US presidential elections of 2016**.

## Is racism measurable ?
This is difficult to quantify because many parameters are subjective. This is why we are interested in car stops and the potential searches to which they lead. This makes it possible to study uniform and more concrete characteristics: location, reason for the arrest, decision to search, "success" of the search, and colour of the driver.
We focus on two parameters:
- the hit rate, the "success" rate of searches for drug possession during police arrests. 
A lower hit rate may indicate that the police officer initiated a search with less evidence, which may be biased by the colour of the driver's skin.  
- the threshold: the level of evidence necessary for the police officer to decide to search someone.
If it is lower, it may also show a bias on the part of the police officer.

After counting these parameters we will **compare the results between red and blue states** !

# Comparing red and blue states
## Which states and why ?
Selecting which state to represent requires multiple steps. 
First of all, not all states have all of the required information for our study, that is the calculations of hit rate and threshold test. This first narrows us down to the states of: Connecticut, Illinois, North Carolina, Rhode Island, South Carolina, Texas, Washington, and Wisconsin. 
Now, let's select states that seem to be most significant: that is, the ones that had the highest percentage of votes for the party that one. This takes out North Carolina, which had a major percentage very close to 50%. Finally, we took out Wisconsin, since it tends to be a swing state.

This divides our 6 remaining states into two groups: South Carolina and Texas in the red group, and Illinois, Connecticut, Rhode Island and Washington in the blue group.

## Data vizualization 

Before plotting our rates, we first want to check if our dataset is big enough: are there enough police stops and searches for our results to be significant? The results are in the following table: 

| State group | Number of stops per year | Number of searches per year|
| :------ |:--- | :--- |
| Red | 2 104 964.4 | 47 958.6 |
| Blue | 1 071 249.6 | 29 642.0 |

Okay, we're talking millions of data points. Looks big enough! Let's proceed with our plots for hit rates and threshold tests.

## Hit rates and threshold in blue states compared to red states

Let's have a first look at our data through the following visualization:

![Hit and threshold, vizualization](/assets/img/Unknown.png){: .mx-auto.d-block :}

Ajouter les observations sur ce plot

Now, let's look at the distribution of these findings.
The results are shown here:
![Hit, national](/assets/img/hit rate, national.png){: .mx-auto.d-block :}
![Threshold, national](/assets/img/threshold, national.png){: .mx-auto.d-block :}

Visually, one can see that the hit rates and thresholds for non-Caucasian minorities are generally lower than their equivalent for white drivers. Note that we have grouped hispanic and black drivers together as non-Caucasian and put them in the same plot in order to check any differences within the minorities compared to white drivers.

## Statistics

## Our first observations
Oops. Apparently there is a significant difference according to our statistical tests. But it's not obvious! How can we sharpen our study?
The election results we used are state-wide. As they cover a very large population and a very large number of counties, they average and homogenize the results! For example, a blue county within a red state will distort our correlation study. In order to have more accurate results and more representative percentages of the population in each county, we will study blue counties VS red counties, and we will use the results county by county. 

# Let's take a closer look !
## Texas counties blue/red repartition
For our study, we has a closer look at Texas counties, which, as a red states, includes both red and blue counties. Big cities tend to be located in blue counties, whereas more rural areas represent red counties. Let's look at how the hit rate and threshold repartition changes based on the county color.

Once again, we are looking at large numbers of police stops - no worries for the significancy of our results ! See by yourself : 

| Texas county group | Number of stops per year | Number of searches per year|
| :------ |:--- | :--- |
| Red | remplir | remplir |
| Blue | remplir | remplir |

## Comparison of red and blue counties
Following we have the equivalent of the previous plots, but at the Texas level, where the points take the color of the county, not of the state:
![Hit, Texas](/assets/img/hit_rate_tx.png){: .mx-auto.d-block :}
![Threshold, Texas](/assets/img/threshold_tx.png){: .mx-auto.d-block :}

## Observations again

## Rajouter les tests sur les counties

## Conclusion


## trucs potentiellement utiles que je laisse au cas où :
### y a comment faire un tableau, ref à un site, à une image, ligne de codes etc

How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

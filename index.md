---
layout: page
title: Are racism and political orientation correlated ?
subtitle: Study of concrete parameters in red and blue regions of the US
comments: False
cover-img: /assets/img/1280px-Red_state,_blue_state.png

---

# A worrying political context
No need to remind you of the many criticisms to Donald Trump about his various forms of discrimination, especially racism. His image and lack of ideology is worrying, especially as it could reflect an atmosphere within his electorate, with racism between individuals and also in official institutions such as the police.
At a time when the Black Lives Matter movement, the denunciation of police violence in many countries, with a change of president of the USA approaching, we have decided to take a closer look at the police arrests in the USA... What we want to know is: is there a racist bias in police stops in the US ? Is there any link between our future results and the political inclination of the region studied ? 

# Let's quantify racism
## What data are we looking at ?
For this study we confined ourselves to the year 2016. We use a dataset of **100 million traffic stops** across the United States. We also compare this data with the [the New York Times website](https://www.nytimes.com/elections/2016/results/president) website which reports the results to the **US presidential elections of 2016**.

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

Okay, we're talking millions of data points. This looks big enough! Let's proceed with our plots for hit rates and threshold tests.

## Hit rates and threshold in blue states compared to red states

![Hit and threshold, national level](data:image/png;base64,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)

## Our first observations
Oops. Apparently there is a significant difference according to our statistical tests. But it's not obvious! How can we sharpen our study?
The election results we used are state-wide. As they cover a very large population and a very large number of counties, they average and homogenize the results! For example, a blue county within a red state will distort our correlation study. In order to have more accurate results and more representative percentages of the population in each county, we will study blue counties VS red counties, and we will use the results county by county. 

# Let's take a closer look !
## Texas counties blue/red repartition

## Comparison of red and blue counties

## Observations again




## trucs potentiellement utiles que je laisse au cas où :
### y a comment faire un tableau, ref à un site, à une image, ligne de codes etc
Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


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

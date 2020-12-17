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
## What states and why ?

## Hit rates and threshold in blue states compared to red states

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

---
title: Introduction
feature_text: |
  ## Philosophy and Data Analysis
  A quick peak into a vast field of though
feature_image: "https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/phil_banner.png?raw=true"
excerpt: "Alembic is a starting point for [Jekyll](https://jekyllrb.com/) projects. Rather than starting from scratch, this boilerplate is designed to get the ball rolling immediately. Install it, configure it, tweak it, push it."
---

We have chosen to dig into the vast world of great thinkers throughout history. Our motivation is to learn more about the thinkers and the ideas that have helped shape how the world and the cultures in it have evolved. We are interested in, how the sentiment of philosophy has evolved over time. Whether is has notably evolved a all. If it in, one way or another, correlates with renowned periods history, and maybe even whether philosophers are a driving force in the development of society or whether they are mere products of their time representing the contemporary ideas.

In addition to that we will look at how, the philosophers have influenced one another throughout time - and whether mutual influence have created anachronical _communities_ in the history of philosophy.




# The History of Philosophy

First we are to see, how the world of philosophy have evolved throughout history and who, have been the driving forces in this development - and whether we find, what we expect, or discover something unexpected!

How to _bin_ the list of names is a topic that has spiked a lot of discussion - which we are to have a small taste of here:
Ideally one would have some evenly spaced bins representing the entire data set, but unfortunately history is not always linear; some periods of history hardly has any known influential philosophers, some periods have plenty. In addition to the latter there is furthermore a very noticable skew in sheer number of philosophers towards our time. We assume the reason for this is based in two major factors that both have increased drastically throughout history: Access to knowledge/education and record keeping of history. That in itself would be subject for an entire thesis, which regarding this Project would be slightly off-topic, albeit very interesting.

No matter the cause of the rise in number of philosophers over time, we can conclude, that the number increases exponentially as we close in on our time.

![image](https://Graph_of_number_of_philosophers)

Now, back to the issue of _binning_ this data: If we were to bin the entire data set with a fixed interval, we would bin a very large portion of the philosophers in very few bins. Correspondingly we would have a lot of bins with very few philosophers or none at all. Since a substantial part of our analysis is based on the statistics and emergent phenomena of a collection of philosophers, having to analyze a lot of bins with very little data makes no sense - the bins have to contain some minimum number of data. This could be prevent having non-fixed intervals.

Eventually we settled on the (to us) quite aesthethic compromise:
__10 historic intervals__ which are mostly divided into centuries, with the exclusion of the time before year 1500 AD, which is divided into the intervals of 500 years until year 0, where we have binned the entire ancient philosophy from year 1000 BC to year 0 into one ancient bin. Another exception is the 20th century, which we have divided in "Pre-World War II" and "Post-World War II"; from 1900 to 1950 and 1950 to 2000 respectively.


## The Ancient Philosophers: Year 1000 BC to 0

![image](https://-5000_0_wordcloud)
_Acting as a frame for our wordcloud: Parthenon_

![image](https://-5000_0_network)

## Age of the Roman Empire: Year 0 to 500

![image](https://0_500_wordcloud)
_Acting as a frame for our wordcloud: Colosseum (in a more contemporary condition)_

![image](https://0_500_network)

## The Islamic Golden Age: Year 500 to 1000

![image](https://500_1000_wordcloud)
_Acting as a frame for our wordcloud: A Mosque in front of a Crescent_

![image](https://500_1000_network)

## Late Middle Ages: Year 1000 to 1500

![image](https://1000_1500_wordcloud)
_Acting as a frame for our wordcloud: A Cross_

![image](https://1000_1500_network)

## The Renaissance: Year 1500 to 1600

![image](https://1500_1600_wordcloud)
_Acting as a frame for our wordcloud: Da Vinci's Vitruvian Man_

![image](https://1500_1600_network)

## The Scientific Revolution: Year 1600 to 1700

![image](https://1600_1700_wordcloud)
_Acting as a frame for our wordcloud: Isaac Newton's Apple Tree Shone Upon By a Full Moon_

![image](https://1600_1700_network)

## Peak Enlightenment: Year 1700 to 1800 

![image](https://1700_1800_wordcloud)
_Acting as a frame for our wordcloud: Immanuel Kant_


![image](https://1700_1800_network)

## Industrialization: Year 1800 to 1900

![image](https://1800_1900_wordcloud)
_Acting as a frame for our wordcloud: Industrialization_


![image](https://1800_1900_network)

## Beginning of Contemporary History: Year 1900 to 1950

![image](https://1900_1950_wordcloud)
_Acting as a frame for our wordcloud: An Artistic Interpretation of Rubin's Vase_


![image](https://1900_1950_network)

## Current Historic Period: Year 1950 until Now

![image](https://1950_2000_wordcloud)
_Acting as a frame for our wordcloud: Technology and Stuff_

![image](https://1950_2000_network)


## Summarizing Remarks

![image](https://conclusion_wordcloud)

![image](https://conclusion_network)



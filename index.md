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

### Convenient Binning of the Data
How to _bin_ the list of names is a topic that has spiked a lot of discussion - which we are to have a small taste of here:
Ideally the binning would also encapsulate the movements of history; in an ideal scenario a bin would resemble of historic period to be analyzed solely. This would have to be combined with, ideally, having some evenly spaced intervals representing the entire data set. Unfortunately history is not always linear: some periods of history hardly has any known influential philosophers, some periods have plenty. In addition to the latter there is furthermore a very noticable skew in sheer number of philosophers towards our time. We assume the reason for this is based in two major factors that both have increased drastically throughout history: Access to knowledge/education and improved record keeping of history. That in itself would be subject for an entire thesis, which regarding this Project would be slightly off-topic, albeit very interesting.

No matter the cause of the rise in number of philosophers over time, we can conclude, that the number increases exponentially as we close in on the present.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Number_o_phils.png?raw=true)

Now, back to the issue of _binning_ this data: If we were to bin the entire data set with a fixed interval, we would bin a very large portion of the philosophers in very few bins. Correspondingly we would have a lot of bins with very few philosophers or none at all. Since a substantial part of our analysis is based on the statistics and emergent phenomena of a collection of philosophers, having to analyze a lot of bins with very little data makes no sense - the bins have to contain some minimum number of data. This could be prevent having mathematically projected non-fixed intervals, but that would likely conflict with one of the prime ideals: attempting to make the bins resemble historic periods.

Eventually we settled on the (to us) quite aesthethic compromise:
__10 historic intervals__ which are mostly divided into centuries, with the exclusion of the time before year 1500 AD, which is divided into the intervals of 500 years until year 0, where we have binned the entire ancient philosophy from year 1000 BC to year 0 into one ancient bin. Another exception is the 20th century, which we have divided in "Pre-World War II" and "Post-World War II"; from 1900 to 1950 and 1950 to 2000 respectively.

The philosophers are binned based on "in which historic period, they were half their total age", e.g. if Arthur Schopenhauer, born 1788 and died 1860, were to be assigned a historic bin, he would be "half his full age" in: _(1860-1788)/2 + 1788 = 1824_, thus assigning him to the bin containing philosophers from year 1800 to 1900.

### Network Analysis
As mentioned we will look at how, the philosophers have influenced one another throughout time. We will do this by first narrowing in on the philosophers of the _bins_ we have chosen, and look for both expected and surprising results of smaller networks. The nodes of the smaller networks are shown with the size correlated with their influence throughout all of history. To be able to plot the networks, we had to convert them from directed to undirected - for the same reason only a general average degree is shown. This is concluded by an analysis of the entire network of philosophers.

Without further ado, let's examine the history of philosophy:

## The Ancient Philosophers: Year 1000 BC to Year 0 AD

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/-5000-0.png?raw=true)
_Acting as a frame for our wordcloud: Parthenon_

The most prominent themes of this period is, as one would expect, very centered around the greek world. There are a number of Chinese philosophers (Confucius for one), but they are greatly outnumbered by the Greeks, whom also had a grand tradition for practicing philosophy, thus producing a proportionally very large number of philosophers for the time.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph0_pre_0_meh.png?raw=true){:height="70px" width="40px"}
<img src="https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph0_pre_0_meh.png?raw=true" margin-top: -500px; margin-left: -500px;>

Number of nodes: 53 <br>
Number of edges: 90 <br>
Average degree: 1.6981 <br>

Most influential persons of the period:
- Plato _(15)_
- Sokrates _(10)_
- Aristotle (likely the most influential philosopher of all time - but we'll get back to that) _(9)_

As expected a very interwoven network of philosophers.

## Age of the Roman Empire: Year 0-500

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/0-500.png?raw=true)
_Acting as a frame for our wordcloud: Colosseum (in a more contemporary condition)_

Now, the picture changes (both literally and regarding the data).

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph1_0_500.png?raw=true)

Number of nodes: 32 <br>
Number of edges: 18 <br>
Average degree: 0.5625 <br>

- Plotinus _(6)_
- Proclus _(4)_
- Pseudo-Dionysius the Areopagite _(4)_

The time of the ancient Greek philosophers has peaked, but the Greek presence is still very prominent. There has been a significant increase in names relating to the Roman Empire - names ending with the latin suffix "-us" and quite a lot of persons named "of Alexandria" (although located in Egypt, Alexandria was a flourishing part of the Roman Empire - until 641 AD, but that's a different story). The three most influential persons of the time are people we have never heard of (which in itself is interesting), they all have Greek roots.

Now, with some working knowledge of western philosophy, one might ask: Where is Augustine of Hippo? He is probably the most renowned person in philosophy and theology from that time. Fear not: with respect to most people influenced throughout history Augustine of Hippo is second highest in this bin, only surpassed by Plotinus.

## The Islamic Golden Age: Year 500-1000

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/500-1000.png?raw=true)
_Acting as a frame for our wordcloud: A Mosque in front of a Crescent_

The Roman Empire was crumbling, and Europe delved into the Middle Ages - a time with little to no focus on the education of common people, and some level of disregard for ideas that were not aligned with the teachings of the Bible. While this was happening, the Middle East flourished and a lot of great thinkers had the opportunity to have their ideas developed and recorded for history to remember.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph2_500_1000.png?raw=true)

Number of nodes: 7 <br>
Number of edges: 2 <br>
Average degree: 0.2857 <br>

- Al-Farabi _(2)_
- Yahya ibn Adi _(1)_
- Al-Kindi _(1)_

As expected all of the (although few) philosophers are from the Arab world (present day Syria, Iraq and Iraq respectively). Compared to the other historic time spans, this is very deprived of philosophers. A reason for this could be a cultural skew of our analysis: we have only analyzed english wikipedia-pages, which will likely have a tendency towards having more elaborate information on persons from the Anglo-Saxon and Western world - and during this time period, the Anglo-Saxon and Western world was not the epicenter of historic progress, mildly speaking.

## Late Middle Ages: Year 1000-1500

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1000-1500.png?raw=true)
_Acting as a frame for our wordcloud: A Cross_

During this time the Catholic Church has become very prosperous, and teachings of the Bible were vividly studied by theologians.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph3_1000_1500.png?raw=true)

Number of nodes: 65 <br>
Number of edges: 93 <br>
Average degree: 1.4308 <br>

- Averroes _(14)_
- William of Ockham _(12)_
- Thomas Aquinas _(12)_
- Avicenna _(10)_

Yet, the Islamic Golden age is by no means over: Averroes is the latinized version of _Ibn Rushd_, and Avicenna is the latinized version of _Ibn Sina_. Then there's of course Thomas Aquinas, who is very renowned.

## The Renaissance: Year 1500-1600

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1500-1600.png?raw=true)
_Acting as a frame for our wordcloud: Da Vinci's Vitruvian Man_

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph4_1500_1600.png?raw=true)

Number of nodes: 26 <br>
Number of edges: 7 <br>
Average degree: 0.2692 <br>

- Michel de Montaigne_(2)_
- Pierre Charron_(2)_
- Francis Bacon_(2)_
- Paracelsus_(2)_


## The Scientific Revolution: Year 1600-1700

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1600-1700.png?raw=true)
_Acting as a frame for our wordcloud: Isaac Newton's Apple Tree Shone Upon By a Full Moon_

This was indeed the century of science. It had already started in the 16th century with Copernicus, followed by Galilei and Kepler and now - propelled by Newton's Principia - a new generation of scientists were to propel the world forward.
But that's the science part, we are to continue with the philosophy (even though Newton did make it onto the list of persons who has influenced most philosophers in this bin). 

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph5_1600_1700.png?raw=true)

Number of nodes: 41 <br>
Number of edges: 35 <br>
Average degree: 0.8537 <br>

- René Descartes _(10)_
- Hugo Grotius _(7)_
- John Locke _(5)_
- Thomas Hobbes _(5)_

Regarding philosophers this period is dominated by Rene Descartes. Being the genius he was, this is not unexpected at all.


## Peak Enlightenment: Year 1700-1800 

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1700-1800.png?raw=true)
_Acting as a frame for our wordcloud: Immanuel Kant_


![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph6_1700_1800.png?raw=true)

Number of nodes: 68 <br>
Number of edges: 72 <br>
Average in degree: 1.0588 <br>

- Immanuel Kant _(10)_
- Christian Wolff _(10)_
- David Hume _(9)_
- Joseph Butler _(8)_
- Thomas Paine _(7)_
- Voltaire _(7)_

## Industrialization: Year 1800-1900

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1800-1900.png?raw=true)
_Acting as a frame for our wordcloud: Industrialization_


![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph7_1800_1900_meh.png?raw=true)

Number of nodes: 167 <br>
Number of edges: 250 <br>
Average degree: 1.4970 <br>

- William James _(18)_
- Karl Marx _(17)_
- Charles Darwin _(17)_
- John Stuart Mill _(16)_

## Beginning of Contemporary History: Year 1900-1950

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1900-1950.png?raw=true)
_Acting as a frame for our wordcloud: An Artistic Interpretation of Rubin's Vase_


![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph8_1900_1950.png?raw=true)

Number of nodes: 182 <br>
Number of edges: 170 <br>
Average in degree: 0.9341 <br>

- Ludwig Wittgenstein _(14)_
- Martin Heidegger _(11)_
- Bertrand Russell _(10)_

## Current Historic Period: Year 1950 until Now

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1950-2000.png?raw=true)
_Acting as a frame for our wordcloud: Technology and Stuff_

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph9_1950_2000_meh.png?raw=true)

Number of nodes: 192 <br>
Number of edges: 233 <br>
Average in degree: 1.2135 <br>

- Hilary Putnam _(14)_
- Jacques Derrida _(14)_
- Michel Foucault _(13)_
- Cornelius Castoriadis _(13)_
- Louis Althusser _(12)_

This was where my personal knowledge of contemporary philosophy was tested - I'm only familiar with Foucault.

## Summarizing Remarks

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/MasterGraph0.png?raw=true)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/all_wikitexts.png?raw=true)

### Interconnectedness

A peculiar characteristic we noticed when analyzing the historical bins: the probability of the nodes being connected varied vividly, but had a general decline. We attribute this to the record keeping and/or education scarcity; only the most influential philosophers got to be remembered by time, and were able to be granted the honor of having a Wikipedia-page - and in times with scarce educational resources, renowned thinkers were more likely to influence one another. Today there has never been more philosophers worthy of a Wikipedia-page alive, but the likelihood of them influencing each other is declining. It's like the strange situation we're facing with regards to reading: never hve there been such a steep decline in people reading books, yet more books are being printed than ever before.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/connected_p.png?raw=true)

### An Unexpected Bias

Something we didn't consider before gathering the data was the language bais of the data: western philosophers and people from the Anglo-Saxon history seems to be slightly over-represented - which in hindsight does make perfect sense, but we were only to realize this in the late phase of the analysis. To improve the analysis, a more broad gathering of data should be performed.





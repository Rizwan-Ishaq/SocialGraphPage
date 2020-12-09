---
title: A Brief History of Philosophy
feature_text: |
  <h2 id="top">Philosophy and Data Analysis</h2>
  A peak into a vast world of thoughts 
feature_image: "https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/phil_banner.png?raw=true"
excerpt: "Alembic is a starting point for [Jekyll](https://jekyllrb.com/) projects. Rather than starting from scratch, this boilerplate is designed to get the ball rolling immediately. Install it, configure it, tweak it, push it."
---

Welcome to the culmination of what we have learned from the course Social Graphs and Interactions at DTU, 2020. We have created a _time line_ inspired by the layout of [_The Network Science Book_](http://networksciencebook.com/). In this time line we first analyze the history of philosophy in a chronological order, then dig deeper into properties and achronological aspects of the data. Each section contains a visualization of the most frequent, unique words of the philosophers of the time, and a visualization of the network of the influence each person have had on one another in the historic period. 

# Overview
- [__Introduction__](#introduction)
- [__A Brief Discussion of the Data__](#a_brief_discussion_of_the_data)
    - [__Source of the Data__](#source_of_the_data)
    - [__Convenient Binning of the Data__](#convenient_binning_of_the_data)
    - [__Network Analysis__](#network_analysis)
- [__The History of Philosophy__](#the_history_of_philosophy)
    - [__The Ancient Philosophers: Year 1000 BC to Year 0 AD__](#the_ancient_philosophers)
    - [__Age of the Roman Empire: Year 0-500__](#age_of_the_roman_empire)
    - [__The Islamic Golden Age: Year 500-1000__](#the_islamic_golden_age)
    - [__Late Middle Ages: Year 1000-1500__](#late_middle_ages)
    - [__The Renaissance: Year 1500-1600__](#the_renaissance)
    - [__The Scientific Revolution: Year 1600-1700__](#the_scientific_revolution)
    - [__Peak Enlightenment: Year 1700-1800__](#peak_enlightenment)
    - [__Industrialization: Year 1800-1900__](#industrialization)
    - [__Beginning of Contemporary History: Year 1900-1950__](#beginning_of_contemporary_history)
    - [__Current Historic Period: Year 1950 until Now__](#current_historic_period)
    - [__The Entire History of Philosophy: Pre-History - Now__](#the_entire_history_of_philosophy)
- [__Concluding Remarks__](#concluding_remarks)
    - [__Scale-Free Properties of the Network__](#scale_free_properties_of_the_network)
    - [__Interconnectedness__](#interconnectedness)
    - [__Unexpected Biases__](#unexpected_biases)
    - [__Surprising Discoveries__](#surprising_discoveries)
    - [__Further Reading__](#further_reading)
- [__The Sentiment of Philosophy Throughout History__](#the_sentiment_of_philosophy_throughout_history)
- [__Achronological Communities__](#achronological_communities)
    - [__The Ancient Greek World__](#ac1)
    - [__The Time-Transcending Influence of Plato and Aristotle__](#ac2)
    - [__The Impact of Kant__](#ac3)
    - [__The Impact of Marx__](#ac4)
    - [__Eastern Philosophy__](#ac5)
    - [__The 20th Century__](#ac6)
    - [__Extended Further Reading__](#extended_further_reading)
- [__List of Figures__](#list_of_figures)
- [__References__](#references)




<h1 id="introduction">Introduction</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

We have chosen to dig into the vast world of great thinkers throughout history. Our motivation is to learn more about the thinkers and the ideas that have helped shape how the world and the cultures in it have evolved.

Especially whom the most influential people have been in this development - those who have made the greatest impact on other philosophers. Our theory is that the most influential philosophers are the ones whom have proposed the most radical and original ideas - and that's worth further analysis!

We are also interested in, how the sentiment of philosophy has evolved over time. How it has evolved through time - if at all. Whether it, in one way or another, correlates with renowned periods of history, and maybe even whether philosophers are either greatly influenced by the their contemporary time or immune to changes in sentiment.

In addition to that we will look at how the philosophers (and other influential individuals) have influenced one another throughout history - and whether mutual influence have created achronological _communities_ in the history of philosophy.

And then, to be frank, it would be quite awesome to discover highly influential/important people of this field, whom may previously have been completely unknown to us (kept of the record this might be one of our primary goals actually).

When analyzing the results, the terms _philosophers_, _thinkers_ and _people_ will be used interchangeably. When referring to _influential persons_ or anything regarding the _most influential_ or _most connected_ we refer specifically to the philosophers of our network.


<h1 id="a_brief_discussion_of_the_data">A Brief Discussion of the Data</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

Before we start, we present an elaboration on some of our thoughts about the data that has made the foundation for the analysis. If this seems tiresome, feel free to skip to main content, [__The History of Philosophy__](#the_history_of_philosophy) and if the historical context is of little interest, feel free to skip to [__Concluding Remarks__](#concluding_remarks).


<h3 id="source_of_the_data">Source of the Data</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

To obtain data for this project this, we have relied on Wikipedia to provide a list with names. The names for out network originates from the four Wikipedia-lists of philosophers throughout history listed alphabetically[[1](#references)]. The lists are very inclusive. In the analysis we have encountered persons not usually associated (at least primarily) with philosophy. That be people more commonly associated with politics (Vladimir Lenin, Leon Trotsky, Benjamin Franklin), science (Isaac Newton, Hans Christian Ørsted, Nikolau Copernicus), psychology (Sigmund Freud, Carl Jung) and writing (Fyodor Dostoyevsky, Marcel Proust, C.S. Lewis). We have chosen to keep these people in the list - both because it, to us, show how the world history in intertwined among all different fields of human culture, thus making the analysis deprived, if we were to remove them, and also because the term "philosopher" is not necessarily a strictly defined term. If someone by their acts or writings have help spark new ideas or the mind of forthcoming people, is he or she not a philosopher? We are not the ones who are to settle that question. But we have chosen to regard every influential individual in the lists as a philosopher.


<h3 id="convenient_binning_of_the_data">Convenient Binning of the Data</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

How to _bin_ the list of names is a topic that has spiked a lot of discussion - which we are to have a small taste of here:
Ideally the binning would also encapsulate the movements of history; in an ideal scenario a bin would resemble of historic period to be analyzed solely. This would have to be combined with, ideally, having some evenly spaced intervals representing the entire data set. Unfortunately history is not always linear: some periods of history hardly has any known influential philosophers, some periods have plenty. In addition to the latter there is furthermore a very noticable skew in sheer number of philosophers towards our time. We assume the reason for this is based in two major factors that both have increased drastically throughout history: Access to knowledge/education and improved record keeping of history. That in itself would be subject for an entire thesis, which regarding this Project would be slightly off-topic, albeit very interesting.

No matter the cause of the rise in number of philosophers over time, we can conclude, that the number increases exponentially as we close in on the present.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Number_o_phils.png?raw=true)
_Figure 1: The number of philosophers_

Now, back to the issue of _binning_ this data: If we were to bin the entire data set with a fixed interval, we would bin a very large portion of the philosophers in very few bins. Correspondingly we would have a lot of bins with very few philosophers or none at all. Since a substantial part of our analysis is based on the statistics and emergent phenomena of a collection of philosophers, having to analyze a lot of bins with very little data makes no sense - the bins have to contain some minimum number of data. This could be prevent having mathematically projected non-fixed intervals, but that would likely conflict with one of the prime ideals: attempting to make the bins resemble historic periods.

Eventually we settled on the (to us) quite aesthethic compromise:
__10 historic intervals__ which are mostly divided into centuries, with the exclusion of the time before year 1500 AD, which is divided into the intervals of 500 years until year 0, where we have binned the entire ancient philosophy from year 1000 BC to year 0 into one ancient bin. Another exception is the 20th century, which we have divided in "Pre-World War II" and "Post-World War II"; from 1900 to 1950 and 1950 to 2000 respectively.

The philosophers are binned based on "in which historic period, they were half their total age", e.g. if Arthur Schopenhauer, born 1788 and died 1860, were to be assigned a historic bin, he would be "half his full age" in:

_(1860-1788)/2 + 1788 = 1824_

thus assigning him to the bin containing philosophers from year 1800 to 1900. We are well aware that this is a somewhat crude division, as some philosophers may have lived several decades in a different century than they were assigned, perhaps even producing some of their most influential works in that century. To cope with this, we have talked about having philosophers 


<h3 id="network_analysis">Network Analysis</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

As mentioned we will look at how, the philosophers have influenced one another throughout time. We will do this by first narrowing in on the philosophers of the _bins_ we have chosen, and look for both expected and surprising results of smaller networks. The nodes of the smaller networks are shown with the size correlated with their influence throughout all of history. To be able to plot the networks, we had to convert them from directed to undirected - for the same reason only a general average degree is shown. This is concluded by an analysis of the entire network of philosophers.

We will use this color scheme to distinguish philosophers of different time periods:
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/color_legend.png?raw=true)
_Figure 2: Color Scheme of the Networks of the Time Line_


Without further ado, let's examine the history of philosophy:


<h1 id="the_history_of_philosophy">The History of Philosophy</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

First we are to see, how the world of philosophy have evolved throughout history and who, have been the driving forces in this development - and whether we find, what we expect, or discover something new!

<h2 id="the_ancient_philosophers">The Ancient Philosophers: Year 1000 BC to Year 0 AD</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/-5000-0.png?raw=true)
_Acting as a frame for our wordcloud: Parthenon_

The most prominent themes of this period is, as one would expect, very centered around the greek world. There are a number of Chinese philosophers (Confucius for one), but they are greatly outnumbered by the Greeks (in our list), whom also had a grand tradition for practicing philosophy, thus producing a proportionally very large number of philosophers for the time.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph0_pre_0_meh.png?raw=true)
_Network of the Philosophers of the Years Before 0 AD_

Number of nodes: 53 <br>
Number of edges: 90 <br>
Average degree: 1.6981 <br>

Most influential persons of the period:
- Plato _(15)_
- Sokrates _(10)_
- Aristotle (likely the most influential philosopher of all time - but we'll get back to that) _(9)_

The number succeeding the name is the degree of the philosopher in this subsection of the whole network. As expected we see a very interwoven network of (predominantly Greek) philosophers with Plato and Aristotle - and Sokrates - as very influential figures.


<h2 id="age_of_the_roman_empire">Age of the Roman Empire: Year 0-500</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/0-500.png?raw=true)
_Acting as a frame for our wordcloud: Colosseum (in a more contemporary condition)_

Now, the picture changes (both literally and with regards to the data). Greek themes are still present, but now themes of the Roman world are most dominant - including a lot of names ending with the latin suffix "-us".

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph1_0_500.png?raw=true)
_Network of the Philosophers of the Years 0 to 500_

Number of nodes: 32 <br>
Number of edges: 18 <br>
Average degree: 0.5625 <br>

- Plotinus _(6)_
- Proclus _(4)_
- Pseudo-Dionysius the Areopagite _(4)_

The time of the ancient Greek philosophers has peaked, but the Greek presence is still very prominent. There has been a significant increase in names relating to the Roman Empire. Together with names ending with the latin suffix "-us" (like the themes in the wordcloud), quite a lot of persons are named "of Alexandria" (although located in Egypt, Alexandria was a flourishing part of the Roman Empire - until 641 AD, but that's a different story). The three most influential persons of the time are people we have never heard of (which in itself is interesting), they all have Greek roots indicating the Greeks still had a great impact on the ideas of the Roman world.

Now, with some working knowledge of western philosophy, one might ask: Where is Augustine of Hippo? He is probably the most renowned person in philosophy and theology from that time. Fear not: with respect to most people influenced throughout history Augustine of Hippo is second highest in this bin, only surpassed by Plotinus.


<h2 id="the_islamic_golden_age">The Islamic Golden Age: Year 500-1000</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/500-1000.png?raw=true)
_Acting as a frame for our wordcloud: A Mosque in front of a Crescent_

The Roman Empire was crumbling, and Europe delved into the Middle Ages - a time with little to no focus on the education of common people, and some level of disregard for ideas that were not aligned with the teachings of the Bible. While this was happening, the Middle East flourished and a lot of great thinkers had the opportunity to have their ideas developed and recorded for history to remember.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph2_500_1000.png?raw=true)
_Network of the Philosophers of the Years 500 to 1000_

Number of nodes: 7 <br>
Number of edges: 2 <br>
Average degree: 0.2857 <br>

- Al-Farabi _(2)_
- Yahya ibn Adi _(1)_
- Al-Kindi _(1)_

As expected all of the (although few) philosophers are from the Arab world (present day Syria, Iraq and Iraq respectively). Compared to the other historic time spans, this is very deprived of philosophers. A reason for this could be a cultural skew of our analysis: we have only analyzed english wikipedia-pages, which will likely have a tendency towards having more elaborate information on persons from the Anglo-Saxon and Western world - and during this time period, the Anglo-Saxon and Western world was not the epicenter of historic progress, mildly speaking.


<h2 id="late_middle_ages">Late Middle Ages: Year 1000-1500</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1000-1500.png?raw=true)
_Acting as a frame for our wordcloud: A Cross_

During this time the Catholic Church has become very prosperous, and teachings of the Bible were vividly studied by theologians, whom also formed new interesting ideas of the time. 

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph3_1000_1500.png?raw=true)
_Network of the Philosophers of the Years 1000 to 1500_

Number of nodes: 65 <br>
Number of edges: 93 <br>
Average degree: 1.4308 <br>

- Averroes _(14)_
- William of Ockham _(12)_
- Thomas Aquinas _(12)_
- Avicenna _(10)_

Yet, the Islamic Golden age is by no means over: Averroes is the latinized version of _Ibn Rushd_, and Avicenna is the latinized version of _Ibn Sina_[[2,3](#references)]. Then there's of course Thomas Aquinas, who is a very renowned thinker ... who also fits perfectly on the stereotype of European thinkers of the time, being a catholic priest and a theologian[[4](#references)].

With this number of nodes in the network, the visualizations start to become a little difficult to read, but we have made an attempt to have a high enough resolution to at least be able to see the names of the most prominent nodes when zooming in. They should all look pretty decent when zooming in.


<h2 id="the_renaissance">The Renaissance: Year 1500-1600</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1500-1600.png?raw=true)
_Acting as a frame for our wordcloud: Da Vinci's Vitruvian Man_

The Renaissance marked the end of the Middle Ages with a return to some of the ideas of the Ancient Greeks. To confine this period to only last the century from year 1500 to 1600 is definitely a bit of a stretch, but we concluded "The Renaissance" was the most fitting title for this period of time[[5](#references)].

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph4_1500_1600.png?raw=true)
_Network of the Philosophers of the Years 1500 to 1600_

Number of nodes: 26 <br>
Number of edges: 7 <br>
Average degree: 0.2692 <br>

- Michel de Montaigne _(2)_
- Pierre Charron _(2)_
- Francis Bacon _(2)_
- Paracelsus _(2)_

Of these people only Francis Bacon is familiar to us. Which is somewhat surprising: we had at least expected to find Da Vinci in this group as one of the most influential people. But this leaves room for a lot of new stuff to learn of the influential people of this period. As one might say: _knowledge is power_.

Now, having this somewhat limited number of nodes is a result of our _binning_. When considering the distribution of number of philosophers over time, bins that have intervals that decreased exponentially would have made a more even distribution of people in each bin. Our choice of not having bins with steadily increasing intervals and instead having a very sharp shift in the size of the bins (from a period of 500 years to a period of 100 years) is likely to blame for the size of this bin. We have already discussed that in the section __Convenient Binning of the Data__. In hindsight we should perhaps have made a "middle bin", containing for instance the years 1400 to 1600.


<h2 id="the_scientific_revolution">The Scientific Revolution: Year 1600-1700</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1600-1700.png?raw=true)
_Acting as a frame for our wordcloud: Isaac Newton's Apple Tree Shone Upon By a Full Moon_

This was indeed the century of science. It had already started in the 16th century with Copernicus, followed by Galilei and Kepler and now - propelled by Newton's Principia - a new generation of scientists were to propel the world forward. This is also quite clear from the reccurent words of the philosophers of the time.

But that's it for science at the moment! We are to continue with the philosophy. The network of the 1700th century philosophers look like this:

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph5_1600_1700.png?raw=true)
_Network of the Philosophers of the Years 1600 to 1700_

Number of nodes: 41 <br>
Number of edges: 35 <br>
Average degree: 0.8537 <br>

- René Descartes _(10)_
- Hugo Grotius _(7)_
- John Locke _(5)_
- Thomas Hobbes _(5)_

Regarding philosophers this period is dominated by Rene Descartes. Being the genius he was, this is not unexpected at all. He also has a significantly higher degree than the runner ups, of which Locke and Hobbes are pretty well-known individuals. One thing that may have settled Descartes' place in the top is his influence on both philosophy and science, as he was involved both. Especially math with regards to science[[6](#references)]. Then there is Hugo Grotius, who was a dutch humanist, diplomat, lawyer, theologian, jurist, poet and playwright[[7](#references)]. We had never heard of him, but he apparantly had great impact on the philosophers of his time.


<h2 id="peak_enlightenment">Peak Enlightenment: Year 1700-1800</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1700-1800.png?raw=true)
_Acting as a frame for our wordcloud: Immanuel Kant_

This section literally has _Kant_ written all over it. The Enlightenment was a period of _ideas centered on the sovereignty of reason and the evidence of the senses as the primary sources of knowledge and advanced ideals such as liberty, progress, toleration, fraternity, constitutional government and separation of church and state_[[8](#references)], themes which - along with the names of the famous people of the time - are represented in the wordcloud of this period.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph6_1700_1800.png?raw=true)
_Network of the Philosophers of the Years 1700 to 1800_

Number of nodes: 68 <br>
Number of edges: 72 <br>
Average in degree: 1.0588 <br>

- Immanuel Kant _(10)_
- Christian Wolff _(10)_
- David Hume _(9)_
- Joseph Butler _(8)_
- Thomas Paine _(7)_
- Voltaire _(7)_

We picked the frame for the wordcloud even before we knew this result: of course Kant would be essential to this time period. Being the philosophical equivalent of Copernicus (or in terms of impact, more like Newton) in the history of science, Kant would, not surprisingly, be one of the most influential people of the time. It's not surprising to see Hume and Voltaire in the list as well - and thinking of the history of the Americas, it's not surprising to find Thomas Paine, whose writings had a lot of impact on the American Revolutionary War[[9](#references)], here as well. Surprising though is the presence of Christian Wolff, who is unfamiliar to us - but apparently as influential as Kant in their contemporary time. Wikipedia states that _Wolff was the most eminent German philosopher between Leibniz and Kant_[[10](#references)], which indeed would explain his notoriety.


<h2 id="industrialization">Industrialization: Year 1800-1900</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1800-1900.png?raw=true)
_Acting as a frame for our wordcloud: Industrialization_

This is a time of great development - especially in Europe. It is also the time of imperialism, causing great pain to people falling victim to the processes, and also defining the geography of the world we inherited. This was also a time of much turmoil with the dust of the french revolution still settling - and with this a plethora of new thoughts emerging on how to run a state[[11,12](#references)]. This was also the time of the great existentialist philosophers, who contemplated questions of ones conscient life and its meaning[[13](#references)].

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph7_1800_1900_meh.png?raw=true)
_Network of the Philosophers of the Years 1800 to 1900_

Number of nodes: 167 <br>
Number of edges: 250 <br>
Average degree: 1.4970 <br>

- William James _(18)_
- Karl Marx _(17)_
- Charles Darwin _(17)_
- John Stuart Mill _(16)_

John Stuart Mill and Karl Marx were not unexpected to have present on this list. Marx did write the Communist Manifesto in this century - a book that without doubt has had a great impact on the world. Slightly unexpected is it to see Darwin as one of the most influential thinkers of the time. Yet, when considering the still largely christian population of Europe and how radical his ideas presented in _Origin of the Species_. Then there is William James as the - for this period - most influential person. He is conseridered _The Father of American psychology_[[14](#references)], which of course puts him in place as important (yet he was until this very moment unbeknownst to me). 


<h2 id="beginning_of_contemporary_history">Beginning of Contemporary History: Year 1900-1950</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1900-1950.png?raw=true)
_Acting as a frame for our wordcloud: An Artistic Interpretation of Rubin's Vase_

Probably the most defining 50 years of history for the entire northen hemisphere. Namely because of the two world wars and the entrance of communism on the world stage of governmental systems. Focus on the _world_, the _state_ and _psychology_ becomes important topics (yet still being surpassed in frequency by _life_).

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph8_1900_1950.png?raw=true)
_Network of the Philosophers of the Years 1900 to 1950_

Number of nodes: 182 <br>
Number of edges: 170 <br>
Average in degree: 0.9341 <br>

- Ludwig Wittgenstein _(14)_
- Martin Heidegger _(11)_
- Bertrand Russell _(10)_

No surprises here. Both Wittgenstein, Heidegger and Russell have had a great impact on the time to succeed them, so they most likely have have a great impact on their contemporaries. The number of nodes in the network starts to grow quite excessive.


<h2 id="current_historic_period">Current Historic Period: Year 1950 until Now</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/1950-2000.png?raw=true)
_Acting as a frame for our wordcloud: Technology and Stuff_

Now we approach our time. The World Wars are over. Now the focus has become more on the _social_ and _political_ aspects of existence.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/Subgraph9_1950_2000_meh.png?raw=true)
_Network of the Philosophers of the Years 1950 to 2000_

Number of nodes: 192 <br>
Number of edges: 233 <br>
Average in degree: 1.2135 <br>

- Hilary Putnam _(14)_
- Jacques Derrida _(14)_
- Michel Foucault _(13)_
- Cornelius Castoriadis _(13)_
- Louis Althusser _(12)_

This was where my personal knowledge of contemporary philosophy was tested - I'm personally only familiar with Foucault.


<h2 id="the_entire_history_of_philosophy">The Entire History of Philosophy: Pre-History - Now</h2> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)


![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/all_wikitexts.png?raw=true)
_The most frequently occuring words throughout the texts of our people_

Throughout the entire history (as far as this data set concerns us) philosophy has been closely associated with the movements of society both with regards to religion, state, science and political and economic issues. Whether ideas and thoughts are shaping the world around the thinkers, or whether the movements of history manifests itself as reflections of witted individuals, is most likely not the ideal question to ask; throughout history philosophers have (as we are about to see in the image just beneath this paragraph) influenced one another in a very non-linear way.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/MasterGraph0.png?raw=true)
_Network of the most influential Philosophers of all time_

Number of nodes: 833 <br>
Number of edges: 2389 <br>
Average degree: 2.8679 <br>

The top 10 of most influential philosophers throughout time are:
1. Aristotle _(90)_
2. Immanuel Kant _(86)_
3. Karl Marx _(80)_
4. Plato _(71)_
5. Ludwig Wittgenstein _(45)_
6. Friedrich Nietzsche _(44)_
7. William James _(38)_
8. René Descartes, Sigmund Freud _(34)_
9. Martin Heidegger, Baruch Spinoza, John Stuart Mill _(32)_
10. David Hume, Thomas Aquinas, Edmund Husserl _(31)_

Some of them come across quite clearly as huge planets in the universe of connections: Aristotle and Plato are the two large purple bulbs to the left (the network is designed to have people from way back in the past tend towards the right side, and people from the present tend toward the right). Kant and Marx are the large bulbs in the bottom of the network in green and yellow respectively.

The list of overall most influential individuals in the field of philosophy almost looks like the result of a survey asking a number of people to name 15 philosophers they know. The list is like a Hall of Fame of philosophers. The only unexpected presences to us were William James, Sigmund Freud and Edmund Husserl. William James, we already earlier in the time line, had a great impact on the field of psychology and is regarded _The Father of American Psychology_[[14](#references)]. Sigmund Freud was unexpected - mainly because we did not realize how great an impact he had had on thinkers to succeed him, but he has without doubt been one of the most impactful people of his time. Edmund Husserl was not known to us. He was apparently the founder of the field of phenomenology[[15](#references)], which says something about our philosophic illiteracy.

<h1 id="concluding_remarks">Concluding Remarks</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

Some interesting aspects of the data arises, when we take a closer look...

<h3 id="scale_free_properties_of_the_network">Scale-Free Properties of the Network</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

Something worth noticing is how the _degree_ (the number to the right of the names in the list, _(k)_) changes as we approach the less influential philosophers - and how the number of philosophers with a lower degree increases. This does indeed appear to be an exponential decline, which means the network of all the philosophers may have scale-free properties.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/scale_free_dir.png?raw=true)
_Figure 3: The Out-Degree Distribution of the Entire Network on a log-log-scale_

Here we have shown the distribution of out-degrees of the network on a _log-log_-scale, (since _"If a network is directed, the scale-free property applies separately to the in- and the out-degrees"_), and there is indeed a linear tendency in the log-log-distribution of the degrees of the philosophers. This means the network likely has scale-free properties, which is an interesting aspect of network science. _"The term 'scale-free' is rooted in a branch of statistical physics called the Theory of Phase Transitions that extensively explored power laws in the 1960s and 1970s"_[[16](#references)].

This could indicate

<h3 id="interconnectedness">Interconnectedness</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

A peculiar characteristic we noticed when analyzing the historical bins: the probability of the nodes being connected varied vividly, but had a general decline. We attribute this to the record keeping and/or education scarcity; only the most influential philosophers got to be remembered by time, and were able to be granted the honor of having a Wikipedia-page - and in times with scarce educational resources, renowned thinkers were more likely to influence one another. Today there has never been more philosophers worthy of a Wikipedia-page alive, but the likelihood of them influencing each other is declining. It's like the strange situation we're facing with regards to reading: never hve there been such a steep decline in people reading books, yet more books are being printed than ever before.

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/connected_p.png?raw=true)

<h3 id="unexpected_biases">Unexpected Biases</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

Something we didn't consider before gathering the data was the language bias of the data: western philosophers and people from the Anglo-Saxon history seems to be slightly over-represented - which in hindsight does make perfect sense, but we were only to realize this in the late phase of the analysis. To improve the analysis, a more broad gathering of data should be performed.

<h3 id="surprising_discoveries">Surprising Discoveries</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

The main surprises we encountered analyzing the networks of the different historic periods were the influence of the two persons: Hugo Grotius (of the 17th century) and Christian Wolff (of the 18th century). Grotius surpassing Locke and Hobbes and with an incredibly extensive field of interest has to be an interesting person to learn more about. Likewise Wolff, rivalling Kant in being the most influential person of the 18th century and being _the most eminent German philosopher between Leibniz and Kant_[[10](#references)] has to make his ideas worth a read. It was also a major discovery to learn about Edmun Husserl, who seems to have had some essential ideas to modern philosophy. Yet he had eluded our knownledge of philosophy - until now.

Whether or not it was a major discovery, we realized that we have little to know knowledge of the philosophers of the 16th century (now, admittedly that is also a narrow field of interest), but something we would take a closer look at were we to dig deeper into this part of history would be the persons: Francis Bacon, Pierre Charron, Michel de Montaigne and Paracelsus. We also came to realize that we have disproportionately little knowledge of our contemporary philosophers. Hilary Putnam, Jacques Derrida, Cornelius Castoriadis and Louis Althusser were all unfamiliar names to us, but are names we will bear in mind and study, whenever this exam period is over.

Something that came across as quite surprising was the total absence of women in the among the most influential philosophers - not even in the more recent periods of history (we had a small glimpse of hope, when we saw the name _Hilary Putnam_ - but we were too assumptious, _Hilary_ was indeed an American man).

Concluding on the discoveries, we have made a list of what we now know, we know too little of, __Further Reading__, for us to dig more into in the future.


<h4 id="further_reading">Further Reading</h4>

- Hugo Grotius
- Christian Wolff
- Edmund Husserl
- 16th century philosophers, especially Francis Bacon, Pierre Charron, Michel de Montaigne and Paracelsus
- Contemporary philosophy in general, especially Putnam, Derrida, Castoriadis and Althusser


<h1 id="the_sentiment_of_philosophy_throughout_history">The Sentiment of Philosophy Throughout History</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

Before we began working on this project we had a theory: We assumed the sentiment of philosophy throughout history would change and that it would change for the worse, i.e. we assumed that the mean value for the sentiment of the texts describing the philosophers would drop as we approached the 20th century (and then perhaps increase a little throughout the 20th century). We made the assumption that philosophy dealing with the hard questions of life and the world, would generally have a lower value for the sentiment of the texts, than the average. We thought this effect would increase as the world becomes more and more complex with harder questions to consider, leading to lower and lower sentiment values. Then in the 19th and 20th century we have the rise of existentialism followed by absurdism and nihilism, which we assumed to tend towards sad sentiment values.

We performed a _sentiment analysis_ on the philosophers of each of the historic periods and binned them to get a view of the sentiment distribution in general:

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SentimentHist.png?raw=true)
_Figure 4: Distribution of Sentiment Values_

To our surprise the philosophers were in general more _happy_ than the average sentiment value of the reference list of words (this can be found in the _explainer notebook_).

The most _happy_:
1. Ibn Bajjah           5.870000
2. Lorraine Code        5.797871
3. Richard Schacht      5.784569
4. Émilie du Châtelet   5.733795
5. Francisco Varela     5.731777
6. Susanne Langer       5.727356
7. Swami Vivekananda    5.722132
8. David Papineau       5.715101
9. Mir Damad            5.713425
10. Alan Watts          5.709035

The most _sad_:
1. Emile Meyerson                           4.775
2. Felix Ravaisson-Mollien                  4.775
3. Teresa of Avila                          4.808
4. Gottfried Leibniz                        5.040
5. Theodor Adorno                           5.095
6. Thomas Malthus                           5.110
7. Louis Gabriel Ambroise de Bonald         5.128
8. James of Viterbo                         5.150
9. Timon of Phlius                          5.180
10. Samuel Pufendorf                        5.210

There were not any predominant trends neither among the _happiest_ nor the _saddest_ philosophers - most of the people are completely unknown to us.

The average sentiment value of the philosophers of the historic periods was largely unchanged throughout history. Through all periods, the sentiment varied only by 1.05 %. So in general we have to conclude that our hypothesis of a steadily declining sentiment value of philosophers was wrong.

One of the key aspect in this conclusion is the change in sentiment over time:

![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SentimentPlot4.png?raw=true)
_Figure 5: Evolution in Sentiment of Philosophers (x-axis is to show the difference in the groups and does not scale with actual time)_

Within that negligible change of 1.05 % one could argue that the sentiment appears to follow a pattern of a slight decline in sentiment value - with a dive around the years 1800-1900, but within this margin of error, this is likely rather hope than anything near a decent conclusion. The errorbars represent one standard deviation of the sentiment values of particular historic period. They look huge compared to the course of the sentiment, but bear in mind the scaling of the y-axis (to the left). The values are minute. Errorbars of this magnitude indicate a very uniform set of values. This is further certified by the very constant magnitude of the standard deviation - even with the very varying number in "sample size".

If we were to conclude something with certainty, we would have had to compare our results from this sentiment analysis with a control group of (human) non-philosophers, ideally from the same time periods in history. That will have to be a topic for a Version 2.0 of this site (we did check the values of the Superheroes-Network from Assignment 2 to see, if we could use this as a control group, but our sentiment values didn't seem to differ significantly - if this was to indicate anything, it would be that the philosophers do not differ significantly with regards to sentiment ... from texts about superheroes).

Another potential topic for Version 2.0 would be to do the analysis on the works of the philosopher - instead of the texts about them, written mainly by people in the 21th century with an internet access. That would be interesting to analyze.

We can safely say that we cannot prove of hypothesis, on the contrary the sentiment of the philosophers appears to be quite constant over time.



<h1 id="achronological_communities">Achronological Communities</h1> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

We analyzed our network to detect communities using the Louvain-algorithm. The algorithm is chosen because of is swiftness, being one of the swiftest ways to detect communities in a network. The algorithm works by optimizing _modularity_ which (in very short terms) is a measure of how well partioned a network is, i.e. how closely connected the partition of nodes are. Optimizing the modularity means finding the natural clusters or _communities_ in a network[[17, 18](#references)].

The number of communties is not completely constant throughout iterations. This is probably due to some partitions being equally good, making the result of the modularity optimization ambiguous. We have chosen to present the most stable communities, the ones that are almost always (to the extend we have run the algorithm) are grouped together.


<h4 id="ac01">The Ancient Greek World</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_04.png)


<h4 id="ac02">The Time-Transcending Influence of Plato and Aristotle</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_01.png)


<h4 id="ac03">The Impact of Kant</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_03.png)

<h4 id="ac04">The Impact of Marx</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_06.png)


<h4 id="ac05">Eastern Philosophy</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_11.png)


Wittgenstein, Hume, Russell
<h4 id="ac06">Something something</h4>
![image](https://github.com/Rizwan-Ishaq/SocialGraphPage/blob/master/assets/SubgraphCommunity_05.png)



Apart from these communities, there are some small partitions of the network, which does fit neatly into the general trends of history. Some of the minor communities (often only consisting of two nodes), do show some close connections, for instance James Clerk Maxwell and Michael Faraday are (for what we know) always grouped in a community of just those two, which makes a lot of sense since they worked in the same rather narrow (compared to this list of philosphers) field of physics.






<h4 id="extended_further_reading">Extended Further Reading</h4>

- Hugo Grotius
- Christian Wolff
- Edmund Husserl
- 16th century philosophers, especially Francis Bacon, Pierre Charron, Michel de Montaigne and Paracelsus
- Contemporary philosophy in general, especially Putnam, Derrida, Castoriadis and Althusser


<h3 id="list_of_figures">List of Figures</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)

- {1} The number of philosophers
- {2} Color Scheme of the Networks of the Time Line
- {3} The Out-Degree Distribution of the Entire Network on a log-log-scale
- {4} Distribution of Sentiment Values
- {5} Evolution in Sentiment of Philosophers

<h3 id="references">References</h3> [Top](https://rizwan-ishaq.github.io/SocialGraphPage/#)


[1] : 
- [List of Philosophers (A-C)](https://en.wikipedia.org/wiki/List_of_philosophers_(A%E2%80%93C) "Philosophers (A-C)")
- [List of Philosophers (D-H)](https://en.wikipedia.org/wiki/List_of_philosophers_(D%E2%80%93H) "Philosophers (D-H)")
- [List of Philosophers (I-Q)](https://en.wikipedia.org/wiki/List_of_philosophers_(I%E2%80%93Q) "Philosophers (I-Q)")
- [List of Philosophers (R-Z)](https://en.wikipedia.org/wiki/List_of_philosophers_(R%E2%80%93Z) "Philosophers (R-Z)")

[2] : [Averroes](https://en.wikipedia.org/wiki/Averroes "Averroes' Wikipedia-page") <br>
[3] : [Avicenna](https://en.wikipedia.org/wiki/Avicenna "Avicenna's Wikipedia-page") <br>
[4] : [Thomas Aquinas](https://en.wikipedia.org/wiki/Thomas_Aquinas "Thomas Aquinas' Wikipedia-page") <br>
[5] : [Renaissance](https://en.wikipedia.org/wiki/Renaissance "The Renaissance's Wikipedia-page") <br>
[6] : [Rene Descartes](https://en.wikipedia.org/wiki/Ren%C3%A9_Descartes "Rene Descartes' Wikipedia-page") <br>
[7] : [Hugo Grotius](https://en.wikipedia.org/wiki/Hugo_Grotius "Hugo Grotius's Wikipedia-page") <br>
[8] : [Age of Enlightenment](https://en.wikipedia.org/wiki/Age_of_Enlightenment "The Age_of_Enlightenment's Wikipedia-page") <br>
[9] : [Thomas Paine](https://en.wikipedia.org/wiki/Thomas_Paine "Thomas Paine's Wikipedia-page") <br>
[10] : [Christian Wolff](https://en.wikipedia.org/wiki/Christian_Wolff_(philosopher) "Christian Wolff's Wikipedia-page") <br>
[11] : [Industrial Revolution](https://en.wikipedia.org/wiki/Industrial_Revolution "The Industrial Revolution's Wikipedia-page") <br>
[12] : [19th century](https://en.wikipedia.org/wiki/19th_century "19th_century's Wikipedia-page") <br>
[13] : [Existentialism](https://en.wikipedia.org/wiki/Existentialism "Existentialism's Wikipedia-page") <br>
[14] : [William James](https://en.wikipedia.org/wiki/William_James "William James' Wikipedia-page") <br>
[15] : [Edmund Husserl](https://en.wikipedia.org/wiki/Edmund_Husserl "Edmund Husserl's Wikipedia-page") <br>
[16] : [The Network Science Book](http://networksciencebook.com/chapter/4 "Network Science Book, Chapter 4")

[17] : [The Network Science Book, Ch.:9](http://networksciencebook.com/chapter/9 "Network Science Book, Chapter 4")
[18] : [Documentation on Community](https://python-louvain.readthedocs.io/en/latest/api.html
 "Community-module Documentation")

[Link to this pages GitHub repository](https://github.com/Rizwan-Ishaq/SocialGraphPage) <br>
[Link to banner picture](https://park-tavern.co.uk/wp-content/uploads/sites/3/2018/02/philosophy-banner.jpg) <br>
[Link to logo picture](https://www.flaticon.com/free-icon/book_2490419?term=brain&page=1&position=24&related_item_id=2490419) <br>
[Link to the theme which this GitHub page is based upon](https://github.com/daviddarnes/alembic) <br>

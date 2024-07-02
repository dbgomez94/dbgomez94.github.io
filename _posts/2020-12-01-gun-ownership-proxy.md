---
layout: post
title: Improving the Gun Ownership Proxy for Firearm-related Research
subtitle: A synapsis of a journal article
thumbnail-img: "/assets/img/go-proxy-graphical-abstract.png"
tags: [machine learning, deep learning, statistical learning, linear regression, regression analysis, firearm, suicides]
--- 


**From regression analysis to deep learning: development of improved proxy measures of state-level household gun ownership** \
Patterns: Cell Press (2021) \
[David Gomez](https://dbgomez94.github.io/), 
[Zhaoyi Xu](https://www.linkedin.com/in/zhaoyi-xu-89789a110/), 
[Joseph Saleh](https://www.linkedin.com/in/joseph-homer-saleh-8b8773119/) 
\
[Project](pages/projects/2022-07-26-go-proxy.md) |
[Code](https://github.com/dbgomez94/gun-ownership-proxy) |
[DOI](https://www.cell.com/patterns/fulltext/S2666-3899(20)30202-6) |
[PDF](pdfs/go-proxy.pdf)


> [!NOTE] TL;DR:
> - In the absence of direct measurements of state-level household gun ownership, the quality and accuracy of proxy measures for this variable are essential for ﬁrearm-related research and policy development. 
> - In this work, we develop two significantly improved proxy measures of state-level household gun ownership via two methods: first using regression analysis, then using deep learning. 
> - We subject the new regression-based and deep-learning proxies to critical examination, and we benchmark our new proxies against existing ones for accuracy and validity. 
> - Our new proxies significantly outperform the old in term of residual symmetry, robustness to outliers, and accuracy on never-before-seen test data.

![Performance Comparison of the Old and New Proxy Measures of State-Level Household Gun Ownership](/assets/img/go-proxy-performance.png)


This work stemmed from a term project for a course tought by my late advisor, Dr. Joseph Saleh. For this project, which is entitled, Challenging the inevitability of suicide, my teammates and I examined the state-level relationship between gun laws and suicides. We used the tools of machine learning, specifially linear regression, to argue that methods to reduce suicides by one means do not exacerbate suicides by other methods. The basic idea is that suicide attempts by firearm are far more lethul than by other methods, and by putting certain barriers in place to prevent suicide attempts by firearm (e.g., gun laws), overall suicide rates drop. This was a topic that was very close to my heart, and when we presented our work to my advisor, he encouraged us to persue a journal article with him.

One element that was missing from the term project was controlling for state-levels of gun ownership. As with all statistical analyses of this kind, one must control for such measures of exposure. So we began searching for these figures, and to our horror, we discovered that no such figures exist. In the United States, there are certain laws in place that prevent federal agencies from inquiring about gun ownership. We don't know how many guns there are in each state. As a result, reserachers have had to rely on _proxies_ for this indispensible variable. A proxy is simply something that is available that tracks well with something unavailble. For example, there's a strong correlation between ice cream sales on a summer day and the temperature. It's not a perfect correlation, but it's strong enough that in the absence of temperature measurements, one could use ice creams sales as a proxy for temperature. Such is the case with gun ownership. But what correlates well with gun ownership?

There are a plethora of proposed proxy measures of gun ownership. Some better than others. At the time of our literature review, it was well established that the best proxy measure of state-level household gun ownership was the ratio between the number of suicides committed by firearm to all suicides within a given state (such is the relationship between guns and suicides). We denote this proxy as FS/S. The questions comes up, how does one evaluate how good a proxy measure of gun ownership really is? In the absence of actual gun ownership rates, how can we say that something correlates well with it? Answer: surveys. You call lots people, and ask them how many guns they have. The largest and most comprehensive survey of state-level household gun ownership was conducted by the CDC in between the years 2001-2002 with 200,000+ responses each year. These surveys are recognized in the literature as the closest thing we have to actual state-level household gun ownership rates. So we simply examined the correlation between the proxies and these gun ownership rates, to determine which proxies are better than others. If there is a strong correlation, it's a good proxy, a weak correlation, it's bad. How good is FS/S? Not bad: this simple model predicts about 60-70% of the variability in gun ownership rates. For most epidemiological studies, R2 of 60-70% is a great accomplishment, but for proxies, especially for one as utilized and important as the proxy for gun ownership, this mere expressivity simply will not suffice.

One researcher made the excellent observation that most firearm suicides are committed via handgun, and thus, the FS/S proxy may be somewhat blind to rifles and shotguns. So they created a new model that incorporates both FS/S and hunting license rates per capita (abbreviated, HLR). This simple addition improved the performance of the proxy from 60-70% to almost 90%--which was welcomed improvement by the firearm research community--but we still had to ask: Can we do better?

This is what we set out to do in this paper. We wanted to improve the proxy measure of gun ownership, specifically, without adding any extra predictors. The key idea we tried to convey to this community through our work is the idea of non-linear transformations of the predictors (in our case, FS/S or HLR). There is no reason to expect that gun ownership is best modeled as a linear combination of FS/S and HLR as opposed to some non-linear transformation of those variables. We gave the models a little bit of flexibility to conform to any non-linearities in the data. We did this via two avenues: with linear regression and with deep learning. The new regression model accounts for non-linearities in the predictors as well as their statistical interaction, and improved the performance slightly (up to 92%), but more importantly, we showed is was more robust to outliers. The deep learning model, knocked everybody out of the water, and improved the proxy's performance to 95%. In addition to these improvements, we found several flaws in the traditional FS/S proxy and discouraged its use in future studies from firearm research community.

We published this article Dec 11, 2020.

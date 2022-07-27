---
layout: post
title: Publications
subtitle: A collection of my journal and conference papers
comments: true
--- 

## Journal Articles
### From Regression Analysis to Deep Learning: Development of Improved Proxy Measures of State-Level Household Gun Ownership	
* [PDF](https://www.cell.com/action/showPdf?pii=S2666-3899%2820%2930202-6)
* [CODE](https://github.com/dbgomez94/gun-ownership-proxy.git)


This work stemmed from a term project for a course tought by my late advisor, Dr. Joseph Saleh. For this project, which is entitled, Challenging the inevitability of suicide, my teammates and I examined the state-level relationship between gun laws and suicides. We used the tools of machine learning, specifially linear regression, to argue that methods to reduce suicides by one means do not exacerbate suicides by other methods. The basic idea is that suicide attempts by firearm are far more lethul than by other methods, and by putting certain barriers in place to prevent suicide attempts by firearm (e.g., gun laws), overall suicide rates drop. This was a topic that was very close to my heart, and when we presented our work to my advisor, he encouraged us to persue a journal article with him. 

One element that was missing from the term project was controlling for state-levels of gun ownership. As with all statistical analyses of this kind, one must control for such measures of exposure. So we began searching for these figures, and to our horror, we discovered that no such figures exist. In the United States, there are certain laws in place that prevent federal agencies from inquiring about gun ownership. We don't know how many guns there are in each state. As a result, reserachers have had to rely on _proxies_ for this indispensible variable. A proxy is simply something that is available that tracks well with something unavailble. For example, there's a strong correlation between ice cream sales on a summer day and the temperature. It's not a perfect correlation, but it's strong enough that in the absence of temperature measurements, one could use ice creams sales as a proxy for temperature. Such is the case with gun ownership. But what correlates well with gun ownership?

There are a plethora of proposed proxy measures of gun ownership. Some better than others. At the time of our literature review, it was well established that the best proxy measure of state-level household gun ownership was the ratio between the number of suicides commited by firearm to all suicides within a given state (such is the relationship between guns and suicides). We denote this proxy as FS/S. The questions comes up, how does one evaluate how good a proxy measure of gun ownership actually is? In the absence of actual gun ownership rates, how can we say that something correlates well with it? Answer: surveys. You call lots people, and ask them how many guns they have. The largest and most comprehensive survey of state-level household gun ownership was conducted by the CDC in the early 2001-2022 with 200,000+ responses each year. These surveys are recognized in the literature as the closetest thing we have to actuall state-level household gun ownership rates. So we simply examine the correlation between the proxies and these gun ownership rates, to determine which proxies are better than others. If there is a strong correlation, it's a good proxy, a weak correlation, it's bad. How good is FS/S? Not bad: this simple model predicts about 60-70% of the variability in gun ownership rates. But can we do better?

That's what we set out to do in this paper. One reseracher made the excellent observation that most firearm suicides are commited via handgun, and thus, the FS/S proxy may be somewhat blind to rifles and shotguns. So they created a new model that incorporates both FS/S and hunting license rates per capita (abbreviated, HLR). This simple addition improved the performance of the proxy from 60-70% to almost 90%--a welcomed improvement by the community, but we still had to ask: Can we do better?

This is what we set out to do in this paper: improve the proxy measure of gun ownership. The key idea we wanted to convey to this community is the idea of non-linear transformations of the predictor variables (in our case, FS/S or HLR). There is no reason to expect that gun ownership is best modeled as a linear combination of FS/S and HLR as opposed to some non-linear transformation of those variables. That's all we did: we gave the models a little bit of flexibility to conform to any non-linearities in the data. We did this via two avenues: with linear regression and with deep learning. The new regression model accounts for non-linearities in the predictors as well as their statistical interaction, and improved the performance slightly (up to 92%), but more importantly, we showed is was more robust to outliers. The deep learning model, knocked everybody out of the water, and improved the proxy's performance to 95%.

We felt these contributions to the firearm research community were useful, and we published this article Dec 11, 2020.
---
layout: post
title: Suicides, Firearms, and Proxies
subtitle: From Term Project to Publication
thumbnail-img: "/assets/img/fsr-vs-ngl.png"
---

In the Fall of 2019, I was obtaining my Master's degree in Aerospace Engineering, when I took a course in taught by Dr. Joseph Homer Saleh -- who would become an important influence in my life. The course was called Accident Causation and System Safety, and in it, our professor included four lectures on Applied Linear Regression. At the end of this course was an open-ended term project with the only requirements that (1) it use the material covered in the course and (2) it seeks to promote the welfare of humanity.

I formed a team consisting of my fellow AE colleagues: [Jose Sanchez](https://www.linkedin.com/in/jose-c-sanchez/), [Danial Baum](https://www.linkedin.com/in/daniel-baum-ae/), and [Abdulrahman Shurayma](), and we pursued a topic that was close to my heart: suicide. Specifically, we sought to investigate the relationship between firearms and suicide in the United States. 

Our preliminary analysis revealed the acute lethality of firearms in completed suicides. In 2017, more than 47,000 Americans died by suicide (this number is closer to 50,000 in 2022); that is roughly 129 suicides per day or one suicide every 11 minutes. It's estimated that more than 90% of suicide attempts are committed using non-firearm methods (e.g., suffocation, poisoning, cutting, etc.); **only about 10% of attempters use a gun. However, firearm-suicides account for over half of all suicide fatalities** -- nearly 24,000 in 2017 (or 27,000 in 2022).  It's [estimated](https://www.sciencedirect.com/science/article/pii/S0165032721013732?casa_token=6K-gYl6rGwsAAAAA:Zfv4hB3OkqvsKG0oHqekLQ6DDQuXMv-pJ9P1lU5L2FKfPSHCQdFTtuS_XOhtWj7QXeOZz-3uzkU) that nearly 90% of those who attempt suicide with a firearm *succeed*, for lack of a better word.

Some people may say that suicide is inevitable -- that those committed to killing themselves will find a way to do so. If this were true, it would mean that measures to reduce suicide by one method, if effective, will only exacerbate suicides by other methods. In our report, we set out to challenge this notion by highlighting the effectiveness of one such measure—firearm regulations—to reduce firearm suicides and show that they do not exacerbate suicides by other means, thus reducing overall suicide rates.

Shown below are plots of the **Number of Gun Laws** and suicide rates by firearm (left panel), non-firearms (middle panel), and all methods (right panel) for each states. The states are sorted according to the number of gun laws, such that states at the top have the most gun laws and those at the bottom have the fewest.

![suicide rates vs number of gun laws](/assets/img/suicide-rates-vs-num-gun-laws.png)

This figure provides our first indication that there is an association between the number of gun laws and suicide rates. For example, consider the left panel. It shows that, generally speaking, as the number of gun laws increase, the firearm suicide rates decrease. This trend appears to be absent in the middle panel but reappears in the right panel. We then statistically assessed these (apparent) associations via regression analysis.

![firearm suicide rates vs number of gun laws](/assets/img/fsr-vs-ngl.png)

**We found that as the number of gun laws increased, the rates of firearm suicide decreased, and that this association is statistically significant.**

Now, the notion of the inevitability of suicide implies that where there are reduced firearm suicides, there will be an increase in suicides by other means. So let's examine non-firearm suicides:

![non-firearm suicides vs number of gun laws](/assets/img/nfsr-vs-ngl.png)

Absolutely flat. **Statistical tests revealed that there is no statistically significant association between non-firearm suicide rates and number of gun laws.** 

These results directly contradict the inevitability of suicide. Measures that reduce suicides by firearms do not exacerbate suicide by other means. One interpretation of our findings is as follows. **It is not that people who live in states with fewer gun laws are more suicidal, it is that these people have access to much more lethal means.**

To drive this point home, consider the following statistic: nearly 90% of people who attempt suicide *and survive* go on to live and not die by suicide. Means matter, and means reduction can save lives.


(in progress)
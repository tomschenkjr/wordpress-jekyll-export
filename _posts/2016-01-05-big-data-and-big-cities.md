---
id: 2756
title: Big Data and Big Cities
date: 2016-01-05T17:48:30+00:00
author: tom_schenk
layout: post
guid: http://tomschenkjr.net/?p=2756
permalink: /blog/big-data-and-big-cities/
categories:
  - Urban Sciences
tags:
  - big data
  - data science
  - research
  - urban
---
Naturally, a paper titled <a href="http://people.hbs.edu/mluca/BigDataBigCities.pdf"><em>Big Data and Big Cities: The Promise and Limitations of Improved Measures of Urban Life</em></a> piqued my interest. From the discussion, of <a href="https://www.thalesgroup.com/en/worldwide/big-data/four-vs-big-data">"big data" four V's</a>, Glaeser et al. focused on large volumes of data. The paper discussed two types of big data: while researchers typically used aggregated data, such as totals by ZIP codes derived from Census surveys, one dimension of "big data" comes via administrative data sources such as individual IRS tax returns. The other type of source is from public, social media sources like Facebook, Twitter, and Google Streetview.

There is something rather quixotic about arguing over the definition of <a href="https://www.perceptualedge.com/blog/?p=1349">big data to the point of being unhelpful</a>, so I want to leave that aside and focus on the author's arguments. In this case, it's helpful to peel back the onion to understand what Glaeser et al. see as the potential virtue of their definition of big data and what it cannot do. Here, the authors make their most important thesis statement:
<blockquote>
<p class="p1">...big data on its own establishes only correlation—not causality. Even if the data show that urbanites walk more and that people who walk more are healthier, we cannot interpret this as meaning that walking causes health generally or the healthy of urbanites in particular. We would need some alternative source of variation.</p>
</blockquote>
"Big data", in this context, though isn't sufficient to determine the causality that's typically interesting for policy analysis. In this context, "big data" and treating it as a panacea can be equally dangerous. In Kenneth Cukier and Viktor Mayer-Schönberger's <a href="http://www.amazon.com/Big-Data-Revolution-Transform-Think/dp/0544227751"><em>Big Data: A Revolution That Will Transform How We Live, Work, and Think</em></a>, they ambitiously and incorrectly suggest that correlations within big data are enough to determine causation. But this type of big data is observational, so the endogenous factors that lead to things, like segregation, are problematic.

This is fundamental statistics and unfortunately getting lost in the "big data" discussions. It is still necessary that data reflect the populations or groups you are trying to understand. Social media data, for instance, is a great tool to study younger users, technically literate users regardless of age, or of course, to study social media users. However, that data is not a useful measure of older populations, those without internet connections, or Luddites. "Big data" does not solve this problem, no more than traditional surveys.

But, a large volume of data does have its benefits. One benefit of "big data" is the ability to eschew and sacrifice a large number of observations for pseudo-experimental methods. In one vivid example outlined by Glaeser et al. is suppose, for instance, we want to estimate the willingness-to-pay for a park. Typically, this would be done by comparing aggregations from ZIP codes or other large geography. But this is misleading since ZIP codes are not going to be similar. As a whole, ZIP codes have distinct characteristics. Even better, comparing records of housing which are across the street is a far better.

With "big data", it's possible to do this sort of comparison for at least two reasons: first, the individual-level observations let researchers match homes. Second, presumably, millions of observations gives researchers enough robustness to derive estimates. Interestingly, it's unlikely <em>all</em> of the data will be used. A large share of it will likely be disregarded. When starting with millions of observations, there is plenty to lose and still retain robust estimates.

Big data is "cheap", in the sense that millions of observations can be ignored. In the above example--where we're interested in measuring willingness-to-pay for parks--we are only interested in matching homes that are next to the park. Thousands of homes, though, aren't relevant to this analysis and can be removed from the observations. When using survey or smaller data samples, researchers often find themselves desperately trying to keep any viable observations at the risk of hurting the robustness of the statistical models.

<hr />

The authors, though, seem to slip into some fundamental understanding--big data versus a system to record data. In a particularly confusing paragraph, Glasear <em>et al.</em> notes "big data makes it easier to have systems for citizen complaints that enable citizens and public monitors to monitor progress". Of course, this is a reference to 311 systems--a generator of big data, not an enabler of residential complaints. This is where, clearly, big data is be pointed and confused with other technology.

Unfortunately, the authors also seem to fall into their own trapping of "big data". The authors suggest that LinkedIn data be used to measure job search habits. This is helpful, but limited because of selection-bias. LinkedIn applications are likely white-collar job seekers, not construction workers or other industries that tend to be more tied to the business cycle. The value of this data is limited because it's audience--although voluminous and complex--is endogenous to other factors which undermine the analysis.

As typical, the end of the paper wrapped-up with further suggestions on how big data can be useful for cities. For instance, the authors mention the use of data to predict food inspections has been done in Chicago, Boston--which is referenced in the paper--and other locations. But, it seems to miss the nuance of the challenges facing cities. Another proposal--using police records to predict recidivism--has been widely discussed. At this point, the idea is not new but work needs to be finished on the ethical and practical implications.

Besides the obvious ethical implications, there are practical issues as well. In Chicago, a shooting victim was notified about his <a href="http://articles.chicagotribune.com/2013-08-21/news/ct-met-heat-list-20130821_1_chicago-police-commander-andrew-papachristos-heat-list">presence on a "heat list"</a>--a likely shooting victim. Within two weeks, he was dead. The practical question on how to intervene is more crucial than the statistical exercise at this point. However, these is plenty of opportunity, in this respect, to judge which interventions help avoid recidivism.

<hr />

In some respects, the authors are implying that big data can let you be lazy. Instead of designing careful surveys, there is a world of data available for the taking. Of course, this is a bit harsh. Surveys are also expensive and there is<a href="http://fivethirtyeight.com/features/is-the-polling-industry-in-stasis-or-in-crisis/"> evidence that people are avoiding responding to them</a>. But the ubiquitous nature of these data sources has another advantage: automation.

In a lovely example, the authors show how images from Google Street View could be used to predict household incomes. The authors took data from New York City and created a computer vision model to create descriptors of a buildings geometry, color, and other attributes to predict household incomes at a Census block-group. The variables did well and seemed to be a feasible way to estimate this data.

The practical improvement on this approach is it can be done annually. Typically, Google Street View is updated once-a-year in big cities. While the timing of the images is important and left alone in this paper, it is a practical method to boost American Community Surveys, which are not widely available at granular levels on an annual basis. Moreover, this types of approaches can be used each year, providing a more regular stream of feedback to community planners.
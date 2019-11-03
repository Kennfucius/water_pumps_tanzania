# Improving Access to Clean, Safe Drinking Water in Tanzania
Classification model for predicting functional status of water pumps in Tanzania.

The original data source is hosted on DrivenData at:
<a href="https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/23/">Original data source<a>

A full report of the results can be found on my portfolio here:
<a href="https://kennfucius.github.io/0005-water-tanzania/">https://kennfucius.github.io/0005-water-tanzania/</a>

The full analysis is broken into the 3 notebooks:
<br>
<a href="https://nbviewer.jupyter.org/github/Kennfucius/water_pumps_tanzania/blob/master/Tanzania%20Water%20Pumps%20-%20EDA%20Part%201.ipynb">Tanzania Water Pumps - EDA Part 1</a>
<br>
<a href="https://nbviewer.jupyter.org/github/Kennfucius/water_pumps_tanzania/blob/master/Tanzania%20Water%20Pumps%20-%20Data%20Munging.ipynb">Tanzania Water Pumps - Data Munging</a>
<br>
<a href="https://nbviewer.jupyter.org/github/Kennfucius/water_pumps_tanzania/blob/master/Tanzania%20Water%20Pumps%20-%20Model.ipynb">Tanzania Water Pumps - Model</a>

Slides for a 15 min talk of this project:
<a href="https://docs.google.com/presentation/d/1tpjoIbZpF_rh90Ll9jmOdtcqJTNruEpbDJcpelXd3rA/edit?usp=sharing">Slide Deck</a>

## Motivation
Tanzania is recognized by the UN as a least developed country, or LDC<sup>1</sup>. LDCs are, in part, defined by the UN as "low-income countries confronting severe structural impediments to sustainable development"<sup>2</sup>. One critical impediment the country has struggled with for decades has been supplying and maintaining access to clean and safe drinking water for its population. In 2017, a reported 24.8 million citizens lacked access to 'at least basic' water<sup>3</sup>. For those fortunate enough to have access to this life-essential resource at any given time, it is never gauranteed.

In most rural parts of the country, much of the potable water is accessed via water pumps that draw water from local sources. Around 60,000 hand-pumps are installed in sub-Saharan Africa every year, but between 30 to 40% of those do not function at anyone one time<sup>4</sup>! When pumps no longer function, they are often abandoned. These non-functioning pumps have realized an estimated loss of $1.2 billion USD over the last 2 decades<sup>4</sup>. The first step in addressing this problem is identifying the functional status of water pumps. Once the functional status of a pump is known, the appropriate resources can be deployed to target sites in need of repair or replacement. Unfortunately, there is currently no efficient or accurate system to tackle this monumental problem. The status of a pump must be physically checked but local governments and organizations battling the water crisis simply do not possess enough time, resources, or man-power to check the millions of pumps distributed throughout the country. Alternative methods to identifying the functional status of these water pumps is therefore critical to ensuring access to clean drinking water and is the focus of this work.

The problem statement can be phrased as follows. Data exists for tens of thousands of pumps which are assumed to be functional, but we don't actually know until someone is sent out to physically check the pump's status. Rather than physically checking every pump, can we predict with some accuracy better than random, which pumps will be functional and which will be non functional? The desired out come is to improve on the current state by more allocating resources for pump maintenance more efficiently, reducing pump downtime, and ensuring basic water access for tens of millions of Tanzanians.

## Conclusions

A random forest classification model was used to predict the functional status of water pumps in Tanzania. A Bayesion optimization algorithm was used to tune the hyperparameters of the model. A precision of 0.84 and a recall of 0.79 was achieved on a test dataset, while the overall classification rate was 0.81. The model offers average savings in resources of 19.2% over the current state. This savings could be used to deploy additional pump replacements in places with critical need. Finally, a simple calculator is offered to help organization involved in tackling the water crisis to estimate the savings they could realize if employing the model presented in this work.

There are several next steps to explore for this project. The first is to engineer new features based on the questions answered in the EDA section. The second is to deep dive the misclassified cases for the non functional class and understand why the model has a hard time predicting those particular pumps. Finally, an ensemble of several models may aid the overall classification rate by allowing the models to compensate each other’s weaknesses.

## References

1. https://www.un.org/development/desa/dpad/wp-content/uploads/sites/45/publication/ldc_list.pdf
2. https://www.un.org/development/desa/dpad/least-developed-country-category.html
3. https://washwatch.org/en/countries/tanzania/summary/statistics/
4. https://www.theguardian.com/global-development-professionals-network/2016/mar/22/how-do-you-solve-a-problem-like-a-broken-water-pump
5. https://en.wikipedia.org/wiki/India_Mark_II
6. http://www.ropepumps.org/uploads/2/9/9/2/29929105/rope_pump_-_piston_pumps._comp._study_tz.pdf
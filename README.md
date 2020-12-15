<!-- README.md is generated from README.Rmd. Please edit that file -->
Open Case Studies: Mental Health of American Youth
==================================================

<!-- badges: start -->
[![render-README](https://github.com/opencasestudies/ocs-bp-youth-mental-health/workflows/render-README/badge.svg)](https://github.com/opencasestudies/ocs-bp-youth-mental-health/actions)
[![render-index](https://github.com/opencasestudies/ocs-bp-youth-mental-health/workflows/render-index/badge.svg)](https://github.com/opencasestudies/ocs-bp-youth-mental-health/actions)
<!-- badges: end -->

### Important links

-   HTML:
    <a href="https://www.opencasestudies.org/ocs-bp-youth-mental-health" class="uri">https://www.opencasestudies.org/ocs-bp-youth-mental-health</a>
-   GitHub:
    <a href="https://github.com/opencasestudies/ocs-bp-youth-mental-health" class="uri">https://github.com/opencasestudies/ocs-bp-youth-mental-health</a>
-   Bloomberg American Health Initiative:
    <a href="https://americanhealth.jhu.edu/open-case-studies" class="uri">https://americanhealth.jhu.edu/open-case-studies</a>

### Disclaimer

The purpose of the [Open Case Studies](https://www.opencasestudies.org)
project is **to demonstrate the use of various data science methods,
tools, and software in the context of messy, real-world data**. A given
case study does not cover all aspects of the research process, is not
claiming to be the most appropriate way to analyze a given dataset, and
should not be used in the context of making policy decisions without
external consultation from scientific experts.

### License

This case study is part of the [Open Case
Studies](https://www.opencasestudies.org) project. This work is licensed
under the Creative Commons Attribution-NonCommercial 3.0 ([CC BY-NC
3.0](https://creativecommons.org/licenses/by-nc/3.0/us/)) United States
License.

### Citation

To cite this case study:

Wright, Carrie and Ontiveros, Michael and Jager, Leah and Taub, Margaret
and Hicks, Stephanie C. (2020).
<a href="https://github.com/opencasestudies/ocs-bp-youth-mental-health" class="uri">https://github.com/opencasestudies/ocs-bp-youth-mental-health</a>.
Mental Health of American Youth.

### Acknowledgments

We would like to acknowledge [Tamar
Mendelson](https://www.jhsph.edu/faculty/directory/profile/1770/tamar-mendelson)
for assisting in framing the major direction of the case study.

We would also like to acknowledge the [Bloomberg American Health
Initiative](https://americanhealth.jhu.edu/) for funding this work.

### Title

Mental Health of American Youth

### Motivation

Rates of depression appear to have been increasing among American youths
since around 2010 according to a recent
<a href="https://content.apa.org/record/2019-12578-001" target="_blank">report</a>.
A
<a href="https://pubmed.ncbi.nlm.nih.gov/24285382/" target="_blank">recent study</a>)
also shows that youths appear to be seeking more care from mental health
services.

We will explore the rate of self-reported depression among American
youths age 12-17 from roughly 2004 to 2018. We will also explore data
about the rate at which youths that have experienced depression symptoms
are receiving mental health services. We also investigate where youths
are receiving care.

### Motivating question

1.  How have depression rates in American youth changed since 2004,
    according to the NSDUH data? How have rates differed between
    different youth subgroups (age, gender, ethnicity)?
2.  Do mental health services appear to be reaching more youths? Again,
    how have rates differed between different youth subgroups (age,
    gender, ethnicity)?

### Data

We will use data from the
<a href="https://www.samhsa.gov/data/sites/default/files/cbhsq-reports/NSDUHDetailedTabs2018R2/NSDUHDetTabsSect11pe2018.htm" target="_blank">National Survey on Drug Use and Health (NSDUH)</a>
about the mental health status of youths in the United States of America
age 12-17.

This annual survey is conducted by interviewers that go door to door to
perform the survey.

See
<a href="https://nsduhweb.rti.org/respweb/about_nsduh.html" target="_blank">here</a>
for more details about the Survey and
<a href="https://www.samhsa.gov/data/sites/default/files/cbhsq-reports/NSDUHDetailedTabs2018R2/NSDUHDetailedTabs2018.pdf" target="_blank">here</a>
for the 2018 NSDUH Survey report.

Importantly, there is no obvious way to download the data directly from
this [particular
website](https://www.samhsa.gov/data/sites/default/files/cbhsq-reports/NSDUHDetailedTabs2018R2/NSDUHDetTabsSect11pe2018.htm).
Thus, we demonstrate how to scrape the data directly from the website.

#### Learning Objectives

The skills, methods, and concepts that students will be familiar with by
the end of this case study are:

<u>**Data Science Learning Objectives:**</u>

1.  Scrape data directly from a website (`rvest`)  
2.  Subset and filter data (`dplyr`)  
3.  Write functions to wrangle data repetitively  
4.  Work with character strings (`stringr`)  
5.  Reshape data into different formats (`tidyr`)  
6.  Create data visualizations (`ggplot2`) with labels (`directlabels`)
    and facets for different groups  
7.  Combine multiple plots (`cowplot`)  
8.  Optional: Create an animated gif (`magick`)

<u>**Statistical Learning Objectives:**</u>

1.  Discuss the impact of self-reporting bias on survey responses  
2.  Define and create a contingency table  
3.  Implementation of a chi-squared test for independence  
4.  Interpretation of a chi-squared test for independence

#### Data import

In this case study particularly covers data import directly from a
website using
<a href="https://en.wikipedia.org/wiki/Web_scraping?oldformat=true" target="_blank">web scraping</a>.

#### Data wrangling

This case study is covers many details about wrangling data from excel
files with unusual header structures and with similar data in multiple
tables within the same file. This involves using the `stringr` package
to split, subset, detect, extract, and modify patterns of text. This
also involves using the `tidyr` package to change data shape and using
the `dplyr` package to summarize, select, filter, modify, and join data.
They case study also covers using various `map_*()` functions of the
`purrr` package to perform functions across tibbles within lists and the
`across()` function of the `dplyr` package to perform functions across
columns of an individual tibble. This case study provides especially
diverse material about data wrangling.

#### Data Visualization

In this case study we provide a brief introduction to the `ggplot2`
package and provide several examples of using the `directlabels` package
to directly add labels to plots. We also demonstrate how to use the
`dl.trans()` and `dl.move()` functions. We especially demonstrate how to
visualize many overlapping groups longitudinally using direct labels and
faceting. We also provide a thorough explanation of how to combine plots
using the `cowplot` package. In doing so, we also demonstrate how to
modify the layout of a legend using the `guides()` function of the
`ggplot2` package.

### Analysis

In this case study we provide an introduction to the
<a href="https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test#:~:text=Pearson&#39;s%20chi%2Dsquared%20test%20is,differs%20from%20a%20theoretical%20distribution." target="_blank">Pearson’s chi-squared test</a>
for independence, as well as
<a href="https://en.wikipedia.org/wiki/Contingency_table" target="_blank">contingency tables</a>.
We demonstrate how to manually calculate the *χ*<sup>2</sup> and degrees
of freedom, as well as how to implement the test in R using the
`chisq.test()` function of the `stats` package. We also discuss how to
interpret the results. We perform the test to compare the frequency of
individuals reporting a major depressive episode in the past year among
two groups across two years.

### Other notes and resources

<a href="https://rstudio.com/products/rstudio/features/" target="_blank">RStudio</a>  
<a href="https://github.com/rstudio/cheatsheets/raw/master/rstudio-ide.pdf" target="_blank">Cheatsheet on RStuido IDE</a>  
<a href="https://rstudio.com/resources/cheatsheets/" target="_blank">Other RStudio cheatsheets</a>  
<a href="https://www.tidyverse.org/" target="_blank">Tidyverse</a>  
<a href="https://en.wikipedia.org/wiki/Selection_bias?oldformat=true" target="_blank">Selection bias</a>  
<a href="https://en.wikipedia.org/wiki/Sampling_(statistics)?oldformat=true" target="_blank">Sampling methods</a>  
<a href="https://en.wikipedia.org/wiki/Sampling_frame?oldformat=true" target="_blank">Sampling frame</a>  
<a href="https://en.wikipedia.org/wiki/DSM-5" target="_blank">DSM 5</a></summary>  
<a href="https://nsduhweb.rti.org/respweb/homepage.cfm" target="_blank">National Survey on Drug Use and Health (NSDUH)</a>  
<a href="https://www.samhsa.gov/" target="_blank">Substance Abuse and Mental Health Services Administration (SAMHSA)</a>  
<a href="https://www.hhs.gov/" target="_blank">U.S. Department of Health and Human Services (DHHS)</a>  
<a href="https://www.samhsa.gov/data/sites/default/files/cbhsq-reports/NSDUHDetailedTabs2018R2/NSDUHDetTabsSect11pe2018.htm" target="_blank">NSDUH Survey Results Website</a>
(where we got the data for this case study)  
<a href="https://nsduhweb.rti.org/respweb/about_nsduh.html" target="_blank">Details about the Survey</a>  
<a href="https://www.samhsa.gov/data/sites/default/files/cbhsq-reports/NSDUHDetailedTabs2018R2/NSDUHDetailedTabs2018.pdf" target="_blank">Report about the 2018 NSDUH Survey</a>  
<a href="https://en.wikipedia.org/wiki/Web_scraping?oldformat=true" target="_blank">Web scraping</a>  
<a href="https://cran.r-project.org/web/packages/rvest/vignettes/selectorgadget.html" target="_blank">Selectorgadget Tool</a>  
See this
<a href="http://research.libd.org/rstatsclub/post/introduction-to-scraping-and-wranging-tables-from-research-articles/#.Xw878ZNKhQJ" target="_blank">blog post</a>,
this
<a href="http://blog.corynissen.com/2015/01/using-rvest-to-scrape-html-table.html" target="_blank">blog post</a>,
and this
<a href="https://rstudio-pubs-static.s3.amazonaws.com/266430_f3fd4660b2744751ab144aa130768a06.html" target="_blank">vignette</a>
for more information about web scraping  
<a href="http://flukeout.github.io/#" target="_blank">CSS selectors tutorial</a>
(and the
<a href="https://gist.github.com/chrisman/fcb0a88459cd98239dbe6d2d200b02d1" target="_blank">answers</a>)  
<a href="https://cran.r-project.org/web/packages/magrittr/vignettes/magrittr.html" target="_blank">Piping in R</a>  
<a href="https://r4ds.had.co.nz/functions.html" target="_blank">Writing functions</a>
Also see
<a href="https://www.opencasestudies.org/ocs-bp-vaping-case-study/" target="_blank">this case study</a>
for more information on writing functions.  
<a href="https://rstudio.com/resources/cheatsheets/" target="_blank">String manipulation cheatsheet</a>  
<a href="https://en.wikipedia.org/wiki/Wide_and_narrow_data" target="_blank">Table formats</a>
<a href="https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test#:~:text=Pearson&#39;s%20chi%2Dsquared%20test%20is,differs%20from%20a%20theoretical%20distribution." target="_blank">Pearson’s chi-squared test</a>  
<a href="https://en.wikipedia.org/wiki/Contingency_table" target="_blank">contingency table</a>  
<a href="https://en.wikipedia.org/wiki/Chi-squared_test#/media/File:Chi-square_distributionCDF-English.png" target="_blank">Chi-square distribution</a>  
<a href="http://homepage.divms.uiowa.edu/~mbognar/applets/chisq.html" target="_blank">chi-square distribution applet</a>  
See here for a more thorough explanation of the
<a href="https://www.ling.upenn.edu/~clight/chisquared.htm" target="_blank">chi-square test</a>  
<a href="http://ggplot2.tidyverse.org" target="_blank"><code>ggplot2</code> package</a>  
Please see
<a href="https://www.opencasestudies.org/ocs-bp-co2-emissions/" target="_blank">this case study</a>
for more details on using `ggplot2`.
<a href="http://vita.had.co.nz/papers/layered-grammar.html" target="_blank">grammar of graphics</a>  
<a href="https://ggplot2.tidyverse.org/reference/ggtheme.html" target="_blank"><code>ggplot2</code> themes</a>  
<a href="http://directlabels.r-forge.r-project.org/docs/index.html" target="_blank"><code>directlabels</code> package methods</a>  
<a href="https://cran.r-project.org/web/packages/viridis/vignettes/intro-to-viridis.html" target="_blank">Viridis palette for colorblind friendly plots</a>  
<a href="https://pubmed.ncbi.nlm.nih.gov/30869927/" target="_blank">Motivating article for this case study about depression rates</a>
(Access is possible for those at Hopkins by using their email address)

<a href="https://pubmed.ncbi.nlm.nih.gov/24285382/" target="_blank">Motivating article about the rate of youths seeking mental health services</a>

<a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3330161/" target="_blank">Cross-cultural review article about possible causes for increased depression</a>

<a href="https://childmind.org/article/is-social-media-use-causing-depression/" target="_blank">Review article about social media and depression</a>

<u>**Packages used in this case study:** </u>

<table>
<colgroup>
<col style="width: 43%" />
<col style="width: 56%" />
</colgroup>
<thead>
<tr class="header">
<th>Package</th>
<th>Use in this case study</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="https://github.com/jennybc/here_here" target="_blank">here</a></td>
<td>to easily load and save data</td>
</tr>
<tr class="even">
<td><a href="https://github.com/tidyverse/rvest" target="_blank">rvest</a></td>
<td>to scrape web pages</td>
</tr>
<tr class="odd">
<td><a href="https://dplyr.tidyverse.org/" target="_blank">dplyr</a></td>
<td>to subset and filter the data for specific groups, to replace specific values with <code>NA</code>, rename variables, and perform functions on multiple variables</td>
</tr>
<tr class="even">
<td><a href="https://cran.r-project.org/web/packages/magick/vignettes/intro.html#Kernel_convolution">magick</a></td>
<td>to create a gif <a href="https://magrittr.tidyverse.org/" target="_blank">magrittr</a></td>
</tr>
<tr class="odd">
<td><a href="https://stringr.tidyverse.org/" target="_blank">stringr</a></td>
<td>to manipulate strings</td>
</tr>
<tr class="even">
<td><a href="https://tidyr.tidyverse.org/" target="_blank">tidyr</a></td>
<td>to change the shape or format of tibbles to wide and long</td>
</tr>
<tr class="odd">
<td><a href="https://tibble.tidyverse.org/" target="_blank">tibble</a></td>
<td>to create tibbles and convert values of a column to row names</td>
</tr>
<tr class="even">
<td><a href="https://purrr.tidyverse.org/" target="_blank">purrr</a></td>
<td>to apply a function to each column of a tibble or each tibble in a list</td>
</tr>
<tr class="odd">
<td><a href="https://ggplot2.tidyverse.org/" target="_blank">ggplot2</a></td>
<td>to create plots</td>
</tr>
<tr class="even">
<td><a href="http://directlabels.r-forge.r-project.org/docs/index.html" target="_blank">directlabels</a></td>
<td>to add labels directly to lines in plots</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/scales/scales.pdf">scales</a></td>
<td>to get the current linetype options</td>
</tr>
<tr class="even">
<td><a href="https://forcats.tidyverse.org/" target="_blank">forcats</a></td>
<td>to reorder factor for plot</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/ggthemes/ggthemes.pdf">ggthemes</a></td>
<td>to create a plot to see what the different linetypes look like</td>
</tr>
<tr class="even">
<td><a href="https://cran.r-project.org/web/packages/cowplot/vignettes/introduction.html" target="_blank">cowplot</a></td>
<td>to combine plots together</td>
</tr>
</tbody>
</table>

#### 

If you are in crisis and need help, call this toll-free number for the
**National Suicide Prevention Lifeline (NSPL)**, available 24 hours a
day, every day: **1-800-273-TALK (8255)**. The service is available to
everyone. The deaf and hard of hearing can contact the Lifeline via TTY
at 1-800-799-4889. All calls are confidential. You can also visit the
Lifeline’s website at
<a href="www.suicidepreventionlifeline.org" target="_blank">www.suicidepreventionlifeline.org</a>.

The **Crisis Text Line** is another free, confidential resource
available 24 hours a day, seven days a week. Text “HOME” to **741741**
and a trained crisis counselor will respond to you with support and
information over text message. Visit
<a href="www.crisistextline.org" target="_blank">www.crisistextline.org</a>.

#### 

Also see
<a href="https://www.mhanational.org/depression-teens-0" target="_blank">here</a>
for more information about how to recognize and help youths experiencing
symptoms of depression.

#### For instructors

Instructors can start at the Data Analysis or Data Visualization section
if they choose to skip the Data Import and Data Wrangling sections.

#### Target audience

For individuals or classes with some familiarity with R programming.

#### Suggested homework

Ask students to scrape tables 11.5A and 11.5B from the website which
contain data about the receipt of treatment among youths who reported
having a severe episode. Ask students to create plots and perform
chi-square tests to evaluate how groups compare over time.

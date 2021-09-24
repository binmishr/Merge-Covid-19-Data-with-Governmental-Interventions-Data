# Merge-Covid-19-Data-with-Governmental-Interventions-Data

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

A Brief Introduction
========================

While analyzing the data on the virus spread from the Johns Hopkins University can be insightful, one of the most pressing questions that we currently face is whether the non-pharmaceutical inventions (NPIs) that we observe around the globe will eventually be effective to contain the spread of the virus, aka to #FlattenTheCurve.

While it is most likely too early to tell (also see below), one key requirement for such analyses is the availability of both, high quality data on the virus spread at country and regional level as well as finely grained data on governmental measures that implement (and enforce) these non-pharmaceutical interventions.

Data on the spread of SARS-CoV-2 is readily available, thanks to the effort of the Johns Hopkins CSSE team. However, it is much harder to obtain high quality information on NPIs. While I was searching through various web resources, luckily, I received the new edition of the fabulous ‘Data are Plural’ newsletter by Jeremy Singer-Vine. It contained two pointers to NPI data and after a quick screening of those along the ones that I was able to detect (full list in the Github repository), I decided to settle with the data provided by the Assessment Capacities Project (ACAPS) as this dataset seems well maintained and also reasonably well documented.

The code directory in the repository contains the following R code files:

    1.import_jhu_csse_covid19_data.R Imports the JHU CSSE data on the global spread of the Covid-19 pandemic, aggregates the data at the country level, and adds ISO3c country indicators. 
    2.import_acaps_npi.R Imports the ACAPS Government measures data, and fixes some minor inconsistencies in the category labels.
    3.import_wbank_data.R Imports current country-level World Bank data.
    4.merge_data.R Merges data from the three data sources into a country-day panel data set.
    5.descriptive_analyses.R: Generates some descriptive visualizations of the data, some of which you see below. You can use it as a starting point for your own analyses.

While I will not replicate the data retrieval and merging code in this blog post I will show you what you can do with the merged data by providing some descriptives on governmental NPIs.

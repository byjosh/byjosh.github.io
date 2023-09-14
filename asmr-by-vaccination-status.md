
## Age standardised mortality by vaccination status
<span id="main"></span>
At the bottom is R code to produce age standardised mortality rate
(ASMR) by vaccination status plots for the data source.

## Confidence intervals for the novice

{::nomarkdown}

<details open="">
<summary><em>click to close this explanation if familiar with error bars and confidence intervals</em>
</summary>
The vertical lines with bars at the ends above and below the lines on the graph are <a href="https://en.wikipedia.org/wiki/Error_bar">error bars</a> showing the 95% <a href="https://en.wikipedia.org/wiki/Confidence_interval">confidence interval</a>.
<p>
In other words: non-overlapping 95% confidence intervals for two groups (where the vertical error bars do not overlap) signify that 19 times out of 20 (or more frequently) the lack of overlap signals we would be right in thinking there is a real difference between the groups. Whereas when the confidence intervals overlap we would be less sure of being right if we assert the two groups are different - rather than the difference we are seeing in the sample being a product of the same underlying group value with random variation being the cause of the apparent difference.
<p>
As examples in the 18-39yr olds second dose at least 21 days ago vs unvaccinated graph below:
<ul> 
<li> for March, April, May 2022 all cause and non COVID-19 deaths have lines and confidence intervals that are all close together. We cannot reject the idea that the groups face the same risk of death during these months from these cause categories and the differences seen are due to random variation. <strong>However a reason that the risk is now more similar is due to earlier months where people got infected and some died - the groups in 2022 have more people in it who had COVID-19 earlier and had at least survived. Having a load of teacups, dropping them on the floor and then picking up the unbroken ones and dropping those again and seeing that none break does not allow you to conclude from the 2nd drop that being dropped on the floor is not a risk for a teacup! It only means it is less of a risk for those who survived the earlier drop!</strong>
<li> for December 2021 those meeting the criteria for deaths involving COVID-19 (see below) have clearly distinct lines with clearly non-overlapping confidence intervals - we can reject the idea that that risk of death while with an acute COVID infection (my reading of the definition in next section) is the same for both the vaccinated and unvaccinated groups.<strong>However: one needs to look at vaccination efficacy studies rather than this data to draw strong conclusions about the vaccines being effective. That is because who gets vaccinated and when is not random in this data - unlike in a vaccination efficacy study. Folks who get vaccines are likely to be more educated, higher socioeconomic status etc. So vaccinated groups have a <a href="https://en.wikipedia.org/wiki/Healthy_user_bias">healthy user bias</a>. Likewise for 18-39yr olds second dose at least 21 days ago vs unvaccinated graph the fact that the vaccinated group have higher all cause mortality in May 2021 may be simply explained by noting that, as seen in <a href="https://www.bbc.co.uk/news/explainers-54880084">this BBC explainer</a>, those under 64 with an underlying health condition were early recipients - so if, by vaccination, you effectively split 18-39yr olds into those with an underlying health condition and those mostly without any grave health issues it should be unsurprising if the first group has higher mortality - as they have health conditions serious enough to see them given priority for vaccination. Another reason one needs vaccination studies is context changes: in May 2021 the UK was still coming out of lockdown and with little coronavirus around there was little detectable advantage to vaccination in these figures - fast forward to August 2021 with the Delta variant around unconstrained by lockdown and one can see that the unvaccinated 18-39yr olds have a higher mortality rate that only declines to a level in which it might be the same as the vaccinated from January 2021 at which point A) Omicron is now dominant variant and B) unvaccinated folks have died - meaning the unvaccinated group is now the survivors.</strong>
</ul>
</details>
{:/nomarkdown}

## The data

Following graphs are of data from [ONS deaths by vaccination status, England](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/datasets/deathsbyvaccinationstatusengland) - specifically [Table 2: Monthly age-standardised mortality rates by vaccination status by age group for all cause deaths, deaths involving COVID-19 and deaths not involving COVID-19, per 100,000 person-years, England, deaths occurring between 1 January 2021 and 31 May 2022 in the version to 31st May edition](https://www.ons.gov.uk/file?uri=/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/datasets/deathsbyvaccinationstatusengland/deathsoccurringbetween1january2021and31may2022/referencetable06072022accessible.xlsx) (ONS data under [Open Government v3 license](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)).

Deaths involving COVID-19: are deaths involving COVID-19 (not "due to COVID-19" which indicates it was the underlying cause in ONS terminology). From the [definition sheet](https://www.ons.gov.uk/file?uri=/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/datasets/deathsbyvaccinationstatusengland/deathsoccurringbetween1january2021and31may2022/referencetable06072022accessible.xlsx):-
<blockquote>For this analysis we define a death as involving COVID-19 if either of the ICD10 codes U07.1 (COVID-19, virus identified) or U07.2 (COVID-19, virus not identified) is mentioned on the death certificate. In contrast to the definition used in the weekly deaths released, deaths where the ICD10 code U09.9 (Post-COVID condition, where the acute COVID had ended before the condition immediately causing death occurred) is mentioned on the death certificate and neither of the other two COVID-19 codes are mentioned are not included, as they are likely to be the result of an infection caught a long time previously, and therefore not linked to the vaccination status of the person at date of death
</blockquote>

## The graphs

<img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-1.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-2.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-3.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-4.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-5.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-6.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-7.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-8.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-9.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-10.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-11.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-12.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-13.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-14.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-15.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-16.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-17.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-18.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-19.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-20.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-21.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-22.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-23.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-24.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-25.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-26.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-27.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-28.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-29.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-30.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-31.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-32.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-33.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-34.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-35.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-36.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-37.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-38.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-39.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-40.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-41.svg" width="100%" /><a href="#main" class="totop">Back to top</a><br><img src="/assets/img/uploads/asmr-by-vaccination-status_files/ASMR by vaccination status-42.svg" width="100%" />


## Discussion

The theme to this discussion it is that the above graphs don't really contradict the body of scientific evidence on the vaccine (which says the vaccine does produce differences & is effective while also being capable of causing serious complications but at a much lower rate than serious complications from a COVID-19 infection) and at the same time one cannot think that a difference seen in the graphs is wholly or necessarily due to the vaccine - rather than due to group differences in what kind of person would have a particular vaccination status at a particular point in time.

The above graph comparing 60 to 69yr olds who are unvaccinated vs. those
with a 2nd dose at least 21 days ago shows a common issue with looking
at mortality rate by vaccination status: self-selection effects.

One might think from the rise in all cause mortality in December 2021
among the vaccinated compared to the unvaccinated: uh-oh, maybe the
antivaxers are right. But the issue - evidenced by the larger
errorbars - is actually people in that age group who have only had a 2nd
dose (as compared to a third dose that was available under the autumn
booster campaign) are becoming quite rare. That rarity shows up as
larger error bars - in [a standard formula for a confidence interval - based on a t-distribution -  the size of the interval is inversely proportional to the square root of the sample size while proportional to the standard deviation](https://crumplab.com/statistics/04-SamplesPopulations.html#estimating-a-confidence-interval) - so for same standard deviation one can infer a smaller sample size from a larger confidence interval and in this case we do not need inference - [from the uptake statistics one can see that even by mid December 2022 those who are double vaccinated but not triple vaccinated in that age group consists of a minority - i.e. a smaller sample](https://www.gov.uk/government/statistics/national-flu-and-covid-19-surveillance-reports-2021-to-2022-season) . And the things that have people in that group might
be things that do not help their mortality rate. For instance:
scepticism of doctors might obviously lead to them missing treatment
until it is too late, or the lack of vaccination may reflect living in
an under-served area or having mobility issues - both of which might
affect ability to access both the vaccine - and other medical care (with
lack of this other medical care driving the higher all cause mortality).

Given the body of evidence regarding vaccines and the overall picture in the graphs that a doubling of all cause mortality in the unvaccinated compared to vaccinated see an increase greater than a doubling of deaths involving COVID-19 we can discard the idea that higher deaths involving COVID-19 is due entirely to hospital aquired COVID-19 - that the unvaccinated get through need for more frequent admissions for non-COVID related reasons. But that doesn't mean that the entire difference between the groups seen in the graphs above is due to the effect of the vaccine alone - for instance the vaccinated groups may also have greater ability to shield themselves from infection - e.g. by working from home or being able to afford high quality masks - or greater propensity (e.g. by social distancing and wearing masks). 

## The code

The `deaths_vaccination_prep_func` allows one to select the age group of
interest. Then the `mortality_graph_func` takes the prepared data for
the age group and you give it the two vaccination statuses you wish to
compare.

``` r
# Set earlier the following line to put output dev to svg after an { r setup, include= FALSE}
# knitr::opts_chunk$set(dev = 'svg')
# set following for good graphics output in R markdown - width, fig height & width in inches and svg as output format
# {r `ASMR by vaccination status`, message = FALSE, warning = FALSE, out.width='100%', fig.height=5, fig.width=11, fig.ext='svg' }

library(readxl)
library(tidyr)
library(dplyr)
library(ggplot2)


referencetable06072022accessible <- read_excel("referencetable06072022accessible.xlsx", 
    sheet = "Table 2", skip = 3)


deaths_vaccination_prep_func <- function(data,group) {
    data$asmr <- paste(replace_na(as.numeric(data$`Age-standardised mortality rate / 100,000 person-years`),0))
    data$date <- paste(data$Year, sprintf("%02d", as.integer(factor(data$Month,levels = month.name))), sep ="-")
    data$cause <- paste(as.numeric(factor(data$`Cause of Death`, levels = c("Deaths involving COVID-19","Non-COVID-19 deaths","All causes"))))
    data$lcl <- paste(replace_na(as.numeric(data$`Lower confidence limit`),0))
    data$ucl <- paste(replace_na(as.numeric(data$`Upper confidence limit`),0))
    outputdata <- data %>% select(date,asmr,cause,lcl,ucl,`Age group`,`Vaccination status`) %>% filter(`Age group` == group)
    
    
    
    outputdata
    
}

mortality_graph_func <- function(data,status1,status2)  {
  ## status1 and status2 are vaccination statuses
  ## "Unvaccinated" ,
  ## "First dose, less than 21 days ago" ,  "First dose, at least 21 days ago" 
  ## "Second dose, less than 21 days ago" , "Second dose, at least 21 days ago"
  ## "Third dose or booster, less than 21 days ago" ,
  ## "Third dose or booster, at least 21 days ago"
  ##
  series_char <- ""
  for (val in c(status1,status2)) {
    for(v in c("Deaths involving COVID-19", "Non-COVID-19 deaths", "All causes")) {
      series_char <- paste(series_char,paste(val,"-",v),":")
    }
  }
  ##print(series_char)
  ## series_labels = unlist(strsplit(series_char,"\\:"))
  
  data <- data %>% filter(`Vaccination status` == status1 | `Vaccination status` == status2)
  
  data$series <- paste(data$`Vaccination status`,"-",factor(data$cause, labels =c("Deaths involving COVID-19", "Non-COVID-19 deaths", "All causes")))
  series_labels <- sort(unique(data$series))
  ##print(series_labels)
  # set page margins
  par(mar = c(4, 4, .2, .1), las =2)
  
  # For setting linetype and colour and size and then consolidating into one legend:-
  # use of linetype = interaction(series) - interaction for the line type
  # and scale_size_manual(name ="Deaths by vaccination status & cause group", values = c(0.9,0.75,0.9, 0.9,0.75,0.9)) +
  # and scale_linetype_manual(name ="Deaths by vaccination status & cause group", values = c("solid", "solid", "twodash", "longdash", "solid", "twodash"))
  # where the name is identical is key to consolidating and manually labelling the legend
  ggplot(data, aes(x = date, y = as.numeric(asmr), linetype = interaction(series), group = interaction(series),size= interaction(series), color = factor(series, labels = series_labels))) +
    geom_line(aes(x = date, y = as.numeric(asmr))) + 
    geom_errorbar(aes(ymin = as.numeric(lcl) , ymax = as.numeric(ucl), group= series,  color = factor(series, labels = series_labels), width = .2) )+ 
    labs(title = paste(data$`Age group`,"year olds"," ASMR per 100k person-years by month"), subtitle = paste(sort(c(status1,status2))[1], " vs. ", sort(c(status1,status2))[2]), x = "date", y = "Age standardised mortality rate per 100 thousand person-years", las = 2) + 
    scale_colour_manual(name ="Deaths by vaccination status & cause group", values = c("yellow","lightblue","green","orange","blue","purple")) +
    scale_size_manual(name ="Deaths by vaccination status & cause group", values = c(0.9,0.75,0.9, 0.9,0.75,0.9)) +
    scale_linetype_manual(name ="Deaths by vaccination status & cause group", values = c("solid", "solid", "twodash", "longdash", "solid", "twodash"))+
    theme(axis.text.x = element_text(angle = 90, vjust = 0.5, hjust=1), plot.title = element_text(size = 12), plot.subtitle = element_text(size = 12), axis.title.y = element_text(size = 8))
  }
for( g in c("18-39","40-49","50-59","60-69","70-79","80-89","90+")) {
  test <- deaths_vaccination_prep_func(referencetable06072022accessible,g)
  print(mortality_graph_func(test,"Unvaccinated","First dose, less than 21 days ago"))
  print(mortality_graph_func(test,"Unvaccinated","First dose, at least 21 days ago"))
  print(mortality_graph_func(test,"Unvaccinated","Second dose, less than 21 days ago"))
  print(mortality_graph_func(test,"Unvaccinated","Second dose, at least 21 days ago"))
  print(mortality_graph_func(test,"Unvaccinated","Third dose or booster, less than 21 days ago"))
  print(mortality_graph_func(test,"Unvaccinated","Third dose or booster, at least 21 days ago"))
}
```


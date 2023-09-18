
I used a combination of <a class="external" href="https://matplotlib.org/">Matplotlib</a> (a graphics package for Python), <a class="external" href="https://flask.palletsprojects.com/">Flask</a> (micro webframework for Python that has been used by a company as big as <a class="external" href="https://www.youtube.com/watch?v=OXN3wuHUBP0#t=46">LinkedIn</a>) and <a class="external" href="https://www.heroku.com">Heroku</a> (for being able to put them online - before Heroku axed their free tier) to do a variety of graphs earlier in the pandemic. 

## Dual axis charts

There are <a class="external" href="https://blog.datawrapper.de/dualaxis/">some good reasons to not do dual axis charts</a> - but I wanted to do some and you can do them in Matplotlib (while <a class="external" href="https://hadley.nz/">Hadley Wickham</a> has <a class="external" href="https://stackoverflow.com/questions/3099219/ggplot-with-2-y-axes-on-each-side-and-different-scales/3101876#3101876"> arguments against them</a> and does not support them in his popular R charting library, ggplot2). 
 
### Cases &amp; admissions

<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/cases_admissions_all-2022-10-12.svg">
<caption>Cases and admissions from start of pandemic data to 2022/10/12</caption>
</figure>

Note that cases data is heavily dependent on testing - which has varied in the pandemic. There was relative scarcity of testing initially - then there was the development of lateral flow tests and their free supply to the public and then that free supply was terminated. So cases to admissions ratio comparisons only make sense within short time periods - when one is sure the testing policy and supply of tests is comparable.

<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/cases_admissions_180d-2022-10-12.svg">
<caption>Cases and admissions for the 180 days leading to 2022/10/12</caption>
</figure>


### Cases - by publication date and rolling 7 day average

A more prosaic use of plotting dual axes shows the rolling 7 day average and the cases by publication date.
<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/cases_180d-2022-10-12.svg">
<caption>This graph shows rolling 7 day average cases for the UK and the figures by publication date - the broad difference being due to new cases being reported on a weekly basis.</caption>
</figure>
<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/cases_all-2022-10-12.svg">
<caption>This graph shows rolling 7 day average cases for the UK and the figures by publication date - the transition to weekly reporting shows up clearly as a divergence of the rolling average and publication date figures.</caption>
</figure>

## The rise of Omicron

As you'd expect the rise of the Omicron variant shows up in the charts.
<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/cases_135d-2021-12-20.svg">
<caption>In this graph of cases in 135 days to 2021/12/20 one can see the step change occasioned by the spread of the Omicron variant.</caption>
</figure>
<figure>
<img src="/assets/img/uploads/covid_matplotlib_graphs/london_cases_admissions-2021-12-20.svg">
<caption>In this graph of the 3 months leading to 2021/12/20 one can see even in the hospital admissions data and cases for London that Omicron is bringing about a rise in December 2021 that is beyond that of having Delta.</caption>
</figure>


<p>Data retrieved from <a class="external" href="https://coronavirus.data.gov.uk/details/developers-guide">UK government API</a> (data believed to be under <a class="external" href="https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/" rel="license">Open Government Licence v3.0</a>). <br>
            Note that 7d averages seen above were calculated using <a class="https://pandas.pydata.org/docs/reference/api/pandas.core.window.rolling.Rolling.mean.html">pandas <code>.rolling(7).mean()</code> method</a> on the dataframe and unlike the <a class="external" href="https://coronavirus.data.gov.uk/">UK government dashboard</a> includes figures from previous 5 days (which may be incomplete) - so accuracy for the latest 7d average was sacrificed in favour of including the latest data.<br>Note also that graphs were the data as available at the time and there may have been revisions (e.g. <a class="external" href="https://www.bbc.co.uk/news/uk-england-58978762">issues</a><a class="external" href="https://www.bbc.co.uk/news/uk-england-birmingham-60940877"> with lab tests</a>).

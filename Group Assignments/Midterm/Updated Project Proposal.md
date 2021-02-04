# **Project Proposal: Updated**

### An introduction of your research question
In this research project, we will analyze public transit access to 17 Regional Recreation Parks in LA County. We will examine which neighborhoods can access those recreation areas in a trip of 45 minutes or less of walking and public transit, and which forms of public transit are available to them. These 17 parks are the parks in LA County that each encompass over 100 acres and contain 3 or more active amenities, such as swimming pools or athletic fields. 

We selected these parks because they draw users from across the county; sometimes drawing people from over 25 miles away. In this way, we’re using this definition of parks as a proxy for the most heavily used parks. Since users can live so far from these parks, they raise the question of how people get to the parks. Additionally, our research project has grown out of the LA Parks Needs Assessment project, which examined access to parks based on walking distance. That project inventoried over 3,000 parks and open spaces across the county, and divided them into four categories: Local Parks, Regional Recreation Parks, Regional Open Spaces, and Natural Areas. We selected the Regional Recreation Parks category for our analysis based on the reasoning above.

We will also be presenting census-tract level demographics on LA County; specifically, on race, income, and level of education. We want to examine whether there's a relationship between any of those demographics and access to parks.

Finally, we will aim to create a metric that measures the level of transit access to one or more of the regional parks, that we can assign to each census tract. This will likely be determined by measuring how many transit stops are available within the census tract that would take a rider to one or more of the 17 parks in less than 45 minutes total.

_Sources:_  
  * https://lacountyparkneeds.org/wp-content/uploads/2016/06/FinalReport.pdf
  * https://www.ppic.org/content/pubs/cacounts/CC_206EBCC.pdf

### An explanation of why it is important to you, why it matters to others, and what is at stake 
There is extensive and widely documented evidence about inequities in neighborhood park access along the lines of race, socioeconomic status, and education level in cities across the country. Neither the City of LA nor the larger LA County are exempt from this. As a result of these inequities, many LA residents living in lower-income communities of color must travel to access parks that are larger, better maintained, and have more amenities. However, low-income households tend to have less access to cars and tend to take shorter trips by car than middle- or high-income households. This suggests that public transit routes to well-maintained parks are crucial for low-income households.

Park access supports physical and mental health in a number of direct and indirect ways. In parks, residents can use the space and facilities for physical activity, enjoy the physiological and mental benefits of being around trees and greenery, gather with friends and family to support their social wellbeing, and so much more. For low-income households, parks serve to replace the yards and play spaces they lack in their homes. 

Parks have become a particularly essential facility during the COVID-19 pandemic, as residents have flocked to them to escape their homes, exercise, or more safely socialize. Paralleling the inequitable distribution of parks, COVID-19 disproportionately impacts low-income communities and communities of color. Equitable park access takes on new urgency to ensure that these communities have safe recreation options to combat the physical, mental, and social toll of the COVID-19 pandemic. 

_Sources:_
* https://www.sciencedirect.com/science/article/abs/pii/S0169204618307710?via%3Dihub
* https://www.tandfonline.com/doi/pdf/10.2747/0272-3638.26.1.4
* https://journals.sagepub.com/doi/pdf/10.1068/a42198
* https://nationalhealthfoundation.org/unveiling-the-root-causes-of-park-inequity-in-south-los-angeles/
* https://journals.sagepub.com/doi/pdf/10.3141/2320-04
* https://www.sciencedirect.com/science/article/pii/S0749379704003046
* https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4082954/
* https://www.theeastsiderla.com/parks_recreation/whats-open-and-closed-in-l-a-parks-during-the-pandemic/article_c47da724-8661-11ea-83a5-4f6cc9dff688.html
* https://nyulangone.org/news/racial-disparities-covid-19-related-deaths-exist-beyond-income-differences-large-us-cities


### A description of the spatial scope (e.g. Boyle Heights or Hong Kong), and why space and/or time matters for your project
This research project will focus on the selected 17 parks across LA County. We chose to consider LA County as a whole, rather than just the City of LA, because the LA region is highly interconnected, and residents frequently travel across city lines to reach work, school, and leisure destinations across the county. Furthermore, much of LA County’s public transportation system is regional rather than limited to a single city.

We will be measuring demographics and park access on a census tract level. Since census tracts tend to be small and relatively homogenous, we can consider our findings for each census tract as a rough estimate of the experience of all the people within a given tract.

### A preliminary but definitive description of data sources (at least two) that you will use 

*Census Reporter: LA County demographics by census tract* 
* Race: https://censusreporter.org/data/table/?table=B02001&geo_ids=05000US06037,140|05000US06037&primary_geo_id=05000US06037
* Household income: https://censusreporter.org/data/table/?table=B19001&geo_ids=05000US06037,140|05000US06037,140|05000US06037&primary_geo_id=05000US06037
* Education level: https://censusreporter.org/data/table/?table=B15003&geo_ids=05000US06037,140|05000US06037&primary_geo_id=05000US06037

These data sets provide some basic demographics on the makeup of LA County, by census tract.

*LA County: County-wide Parks and Open Space:* https://egis-lacounty.hub.arcgis.com/datasets/countywide-parks-and-open-space-public-hosted/

This data set provides information on the 3,000+ parks and open spaces in LA County, including their size, facilities, and coordinates. After sorting by type (NDS_AN_TYPE), we can extract the 17 regional recreation parks that we’re studying and use the coordinates and shape provided.

*LA Metro: Documentation:* https://developer.metro.net/docs/

This website provides multiple data sets including the Metro Bus Schedule and GIS data. The bus schedule comes in a gitlab repository that includes stops, trips, and routes. The GIS files provide the bus routes in a shapefile. 

*LA Metro: Riding Schedules:* https://www.metro.net/riding/schedules/
If we are unable to calculate the bus schedules off of the LA Metro documentation, we may reference this beta bus schedule viewer to determine travel times. This data set provides PDFs of bus schedules by stop and arrival times. 

### A scope that explains the intended analysis and resulting visualizations for your project (flowchart)

This research project is intended to analyze who has access to LA County parks classified as Regional Recreation Parks via public transit. This analysis will be done through establishing walk sheds along transit routes that lead to an entrance for each park. By mapping walksheds around each park, we will be able to determine which transit routes pass within a 10 minute walk of a park entrance. 
From there, we can work backwards and build walksheds around all the stops that are within 45 minutes of the stop closest to the park.
These walksheds will form a visual of to show who can access these parks. 

We are defining "access" to a park by public transit as areas from which a person can reach a Regional Recreation Park from their home within 45 minutes or less, including walk times to and from transit and time on transit.
We chose 45 minutes as the maximum number of time because the average LA commute by public transit takes 54 minutes, and we assumed that most people would not want to travel for longer than their commute to reach a park. 45 minutes seemed like a good upper limit at which a resident might decide to either drive instead, or not go to the park at all.

*Flowchart*

Project Proposal (includes creating scope and selecting parameters) -> Gather datasets -> Map coordinates to entrance(s) of each of the 17 parks -> Create walk sheds of 5 and 10 minutes around each entrance -> Determine which transit routes are available within a 10 minute walkshed -> Use established travel times to find all accessible stops along bus and train routes  -> Create walksheds around those stops -> From those walksheds, determine the level of access (high, medium, low) for each census tract

###  A concluding paragraph of what insights you expect to gain from your research

Our data on the level of transit access for Regional Recreation Parks in LA County will complement existing data on the level of walking access for these parks. Unfortunately, we expect to find that levels of transit access to parks will not be much better than levels of walking access in census tracts that have lower-incomes and levels of education, or that have a greater proportion of people of color.

The results of our analysis will provide insight on spatial access disparities that relate to public health, recreation, and transit investment. We expect that certain neighborhoods will have greater access to parks and/or transit than others, reflecting differential patterns of investment. Finally, the project will show how much travel time residents of certain census tracts must invest in order to reach recreational spaces.

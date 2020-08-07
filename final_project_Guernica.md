# Data-Driven Police Reform (Final Project Page) 
View [Part I](final_project_RosanaGuernica.md), [Part II](final_project_2_RosanaGuernica.md), the [Final Data Story](https://carnegiemellon.shorthandstories.com/data-driven-police-reform/index.html) or go back to my [Home Page](README.md)                                                                                                   

## Introduction 

In the summer of 2020 there were over 6,600 protests across the United States calling for police reform, according to estimates from the [Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0). 


All of these protests demanded change. But where do we start? The answer is one not unfamiliar to Heinz students - data! Across the country, police departments have been publicizing their data in order to increase transparency, accountability, and community relations. 

These datasets help both the public and supervisors better understand behaviors and trends. Datasets that track police activity help both supervisors and the public better understand and track behaviors and trends: Use of Force, Searches and Seizures, Calls for Service, Hiring and Promotions. These, and other, datasets help us identify: Discriminatory Policing, Excessive Uses of Force, Resource Needs and Allocations, Discriminatory Hiring and Promotional Practices.

I built a Call for Service dashboard for the Cincinnati Police Department to serve as an example. Call For Service (CFS) data is already gathered at most police departments across the country. These databases record all calls for service to emergency operatiors, 911, alarms, police radio and non-emergency calls. We can use CFS data as a rich source of information on police activity. This can be tedious since most CFS databses are large, raw, and messy. But it's for precisely those same reasons that we can use it to produce a variety of insights, such as how police officers spend their time, or whether their crime rates are being suppressed. Building effective dashboards that are automatically updated with new data entries can make this information accessible to the general public, supervisors, and city council members. 

I'll demonstrate some of these insights on shorthand, using an embedded dashboard built on Tableau.

- Story Outline

<a href="https://ibb.co/259vKf5"><img src="https://i.ibb.co/CWcb0TW/IMG-2750.jpg" alt="IMG-2750" border="0"></a>

- Story Arc

<a href="https://ibb.co/3CCQw6b"><img src="https://i.ibb.co/rwwNg8h/IMG-2749.jpg" alt="IMG-2749" border="0"></a>



## The Data 

This project uses the Cincinnati Police Department's Call for Service dataset, using specifically their data entries from 2015 - 2018. The department's CFS data is captured by the City of Cincinnati's Computer Aided Dispatch (CAD) system. This system records all calls for service and their dispatch information. Officers who answer a call update the system to reflect on-scene findings. 

This dataset is updated daily and is publicly accessible. It can be acccessed on the [Cincinnati's Police Data Initiatve webpage](https://data.cincinnati-oh.gov/Safety/PDI-Police-Data-Initiative-Police-Calls-for-Servic/gexm-h6bt). In compliance with privacy laws, the dataset has been anonymized and redacted. 


The data set was used to analyze the following: 

- Total number of calls for service, by time of day, day of the week, month, and year. 

- Distribution of calls for service across neighborhoods in the City of Cincinnati, Ohio. Neighborhoods were determiend using the [Statistical Neighborhood Approximation (SNA) Boundary](https://data-cagisportal.opendata.arcgis.com/datasets/572561553c9e4d618d2d7939c5261d46_0). This distribution can be further broken down by cumulative years. 

- Total number of calls for service by call category, which can be further filtered by cumulative years. 


## Intial Sketches and Wireframes


- Sketches - these are sample sketches of what visualizations will be included in the dashboard. A crucial element of the dashboard is that users can customize to the visualizations to their specific needs and interests. I sketched the 'Select Type' and 'Select Time Period' features to highlight this. 

<a href="https://ibb.co/DPFQ6xB"><img src="https://i.ibb.co/WNXfdbr/IMG-2742.jpg" alt="IMG-2742" border="0"></a>
<a href="https://ibb.co/MZ5BjZM"><img src="https://i.ibb.co/VJpwhJ2/IMG-2744.jpg" alt="IMG-2744" border="0"></a>
<a href="https://ibb.co/0J0WY2c"><img src="https://i.ibb.co/yszMgPX/IMG-2745.jpg" alt="IMG-2745" border="0"></a>
<a href="https://ibb.co/SQLNpLg"><img src="https://i.ibb.co/1sSZxSN/IMG-2747.jpg" alt="IMG-2747" border="0"></a>

## User Persona Storyboard

<a href="https://ibb.co/5sP5qYb"><img src="https://i.ibb.co/h2SKpX3/Storyboard.jpg" alt="Storyboard" border="0"></a>

## User Research Protocol and Findings
- Target audience: Average civilian concerned about police reform. I approached three individuals who have a diverse set of occupational backgrounds and skills: a social worker, a film editor, and a data scientist. 

- Goals and Questions: 
    - Intuitiveness -> How much time does it take to understand what the visualizations are communicating?
    - Completeness -> Is there information missing that you wish you saw?
    - Perception/Aesthetics -> Do you find the visualizations appealing?
    
- Methods: Remotely conducted 3 seperate 10-minute interviews and recorded notes on a word processor. 
- Script:

Interview 1 
  
  	Q: How much time did it take you to understand what the visualizations were communicating?
	A: None. But I look at data like that a lot for work, so may not be the average person?
	Q: Is there information missing that you wish you saw?
	A: Looks like the first two are by zip code or parts of a city- I would love that for the second two as well.
	Q: Do you find the visualizations appealing?
  	A: Yes. 
  
Interview 2 

	Q: How much time did it take you to understand what the visualizations were communicating?
	A: It differed for each. The ‘Calls by Year’ was the easiest, followed by the ‘Response Time to Call Destination”. ‘Distribution of Violent Call Types’ took me longer because the word ‘distribution’ threw me off. I didn’t understand what it meant. “Percent of Calls by Category” took me the longest. I wasn’t sure what I was looking at in terms of category comparison. It took me a while to figure out the comparisons of both charts. 
	Q: Is there information missing that you wish you saw?
	A: I guess I just wish that the “Percent of Calls by Category” were more lined up. I didn’t realize that the words in the middle of the graph were the same call type categories. 
	Q: Do you find the visualizations appealing?
	A: Yes. I like the mapping visualizations the best. The Calls by Year gave me the most information the fastest, but the maps painted a complete picture for me. 

Interview 3

	Q: How much time did it take you to understand what the visualizations were communicating?
	A: The most confusing one was the last [% of calls by category]. The heatmaps were dead giveaways. I think the heatmaps are the best way to present the 	information. The last one [% of calls by category] was just too confusing - there must be better ways to present it. 
	Q: Is there information missing that you wish you saw?
	A: Not that I can think of. 
	Q: Do you find the visualizations appealing?
	A: Other than the last one [% of calls by category] - yes. 

- Revisions based on findings: 

 I changed my visualizations to more straightforward charts such as heatmaps, bar graphs, and a drop down menu. I also made certain to include axis labels and legends for each visualization. 

## Final Data Story

- Intended Audience: 

This presentation was curtailed to provide the general public with an introductory understanding of how data can be used to change in police reform and management decisions. To make my final data story work for this audience, I used straight forward analyses such as calls by category, time, and place, rather than moving averages or forecasts. I also made sure that the visualizations could be understood by people with no formal background in data analysis or visualizations. These decisions were informed by user research interviews. For example, I thought that the visualizations used in the dashboard were self-explanatory. I didn't include a legend for all of them because I thought it was intutive. One of the interviewees asked me what the differences in color meant to check their understanding. After that, I included a legend in the visualizations keeping in mind that not everyone who sees them will have the chance to verify. 

I wanted to make sure that the audience had a concrete understanding of how this data is implementable. The most straightforward changes in police reform come internally. I demonstrated examples of internal data-drive decision making to drive this home.  In the presentation I used the example of how analyzing the total number of calls by time/day/month, as well as geographic distribution, could help inform resource and staff allocation, thus using public funds more efficiently. 

- Design Process: 

I changed my visualizations to more straightforward charts such as heatmaps, bar graphs, and a drop down menu. I also made certain to include axis labels and legends for each visualization. See some of the revised sketches below: 

<a href="https://ibb.co/w0rL2fK"><img src="https://i.ibb.co/X2k4Gqz/Screen-Shot-2020-08-06-at-11-21-42-PM.png" alt="Screen-Shot-2020-08-06-at-11-21-42-PM" border="0"></a>

<a href="https://ibb.co/z88fmB7"><img src="https://i.ibb.co/9wwYp1V/Screen-Shot-2020-08-06-at-11-29-09-PM.png" alt="Screen-Shot-2020-08-06-at-11-29-09-PM" border="0"></a> 

<a href="https://ibb.co/YLTgxPp"><img src="https://i.ibb.co/gRFYxmz/Screen-Shot-2020-08-06-at-11-28-53-PM.png" alt="Screen-Shot-2020-08-06-at-11-28-53-PM" border="0"></a>


For the introduction of this data story I wanted to encapsulate the timeliness of the topic. I found data on the number of black lives matter and police reform protets that have taken place this summer on the[Crownd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/home). I wanted to include this statistic - 6,600 protets across the U.S. from May - July 2020 - as a visualization. I played around with a few ideas, including a geographical map showing how these protest took place across the country (see below). After showing it to a few people the feedback I received indicated that it distracted from the real story - which is using data for reform, not the number of protets or their locations.  From this process, I learned that not EVERY statistic has to be represented in a visualization. Some, such as the one that I used, are helpful to provide context, but not meaningful enough to attract the audiences attention to its visualization.


<a href="https://ibb.co/MBvsbtB"><img src="https://i.ibb.co/y49XDZ4/Screen-Shot-2020-08-06-at-11-19-42-PM.png" alt="Screen-Shot-2020-08-06-at-11-19-42-PM" border="0"></a>



- Check out my final data story [here](https://carnegiemellon.shorthandstories.com/data-driven-police-reform/index.html). 

## References

All references used to create this project have been cited throughout this projects write up. I've also created a comprhensive list below for your convenience. 

### Data Sources

-[Cincinnati SNA Boundary](https://data-cagisportal.opendata.arcgis.com/datasets/572561553c9e4d618d2d7939c5261d46_0) was used to create the map boundaries included in the dashboard. 

-[Cincinnati PD's Call for Service Data](https://data.cincinnati-oh.gov/Safety/PDI-Police-Data-Initiative-Police-Calls-for-Servic/gexm-h6bt) 

-[U.S. Protest Data 2020 from the Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0)

### Images and Media Used on my [shorthand page](https://carnegiemellon.shorthandstories.com/data-driven-police-reform/index.html) 

-The background video clip played on the Shorthand front page was created by [Kelly Lacey](https://www.pexels.com/video/policemen-on-the-street-keeping-public-order-against-protesters-4623605/). 
	
-Image 2, "Hollywood Portrait of Protestor in Front of Police" was taken by [Videv](https://www.videvo.net/video/hollywood-portrait-of-protester-in-front-of-police/531468/).
	
-Image 3, "Men Working at Night" was procured via [Pexel](https://www.pexels.com/photo/men-working-at-night-256219/). Photo information notes that no attribution is required. 
	
### Links used for Call to Action 

- [Police Data Initiative](https://www.policedatainitiative.org/participating-agencies/)
- [Mapping Police Violence](https://mappingpoliceviolence.org/)
- [The Stanford Open Policing Project](https://openpolicing.stanford.edu/) 


View [Part I](final_project_RosanaGuernica.md), [Part II](final_project_2_RosanaGuernica.md), the [Final Data Story](https://carnegiemellon.shorthandstories.com/data-driven-police-reform/index.html) or go back to my [Home Page](README.md)      

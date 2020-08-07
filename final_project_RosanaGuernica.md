# Data-Driven Police Reform
Final Project - Part I
View [Final Project - Part II](final_project_2_RosanaGuernica.md) , or go back to my [Home Page](README.md)                                                                                                   

## Introduction 

With all the current discussion surrounding police reform, I wanted to introduce an aspect of policing that is often overlooked: data. I'm not referring to predictive-policing or investigative analytics but rather data for the purposes of police management, oversight, and reform. You're probably already familiar with the concept, and the importance, of data-driven decision making. One of the problems in police reform is the lack of data. Especially for organizational purposes. 

Fortunately, Call For Service (CFS) data is already gathered at most police departments across the country. These databases record all calls for service to emergency operatiors, 911, alarms, police radio and non-emergency calls. We can use CFS data as a rich source of information on police activity. This can be tedious since most CFS databses are large, raw, and messy. But it's for precisely those same reasons that we can use it to produce a variety of insights, such as how police officers spend their time, or whether their crime rates are being suppressed. Building effective dashboards that are automatically updated with new data entries can make this information accessible to the general public, supervisors, and city council members. 

I'll demonstrate some of these insights on shorthand, using an embedded dashboard built on Power BI.

- Story Outline

<a href="https://ibb.co/259vKf5"><img src="https://i.ibb.co/CWcb0TW/IMG-2750.jpg" alt="IMG-2750" border="0"></a>

- Story Arc

<a href="https://ibb.co/3CCQw6b"><img src="https://i.ibb.co/rwwNg8h/IMG-2749.jpg" alt="IMG-2749" border="0"></a>

## The Data 

This project uses the Cincinnati Police Department's Call for Service dataset. The department's CFS data is captured by the City of Cincinnati's Computer Aided Dispatch (CAD) system. This system records all calls for service and their dispatch information. Officers who answer a call update the system to reflect on-scene findings. 

This dataset is updated daily and is publicly accessible. It can be acccessed on the [Cincinnati's Police Data Initiatve webpage](https://data.cincinnati-oh.gov/Safety/PDI-Police-Data-Initiative-Police-Calls-for-Servic/gexm-h6bt). In compliance with privacy laws, the dataset has been anonymized and redacted. 


I'll be using the dataset to analyze and visualize the following 

- The call 'category': Medical, Responsive (incidents not iniated by an officer, such as burglar alarms, distrubances, or assisting other agencies), Non-UCR Crime (incidents that criminal but do not fit the FBI's Uniform Crime Report), Proactive (incidents initiative by a police offcier, such as a follow-up investigation or routine patrol), Property Crime, Traffic, and Violent Crime;

- Time spent on calls and time spent on calls by category 

- Call category by disposition (whether the call resulted in an arrest, the towing of a vehicle, if there was no one at the scene when the officers arrived, if it was a false alarm, for example);

- The geographic distribution of call categories; 

- Call category by time of day, week, month, and year;

- Average time between intial call, dispatch, and arrival.

## Intial Sketches and Wireframes


- Sketches - these are sample sketches of what visualizations will be included in the dashboard. A crucial element of the dashboard is that users can customize to the visualizations to their specific needs and interests. I sketched the 'Select Type' and 'Select Time Period' features to highlight this. 

<a href="https://ibb.co/DPFQ6xB"><img src="https://i.ibb.co/WNXfdbr/IMG-2742.jpg" alt="IMG-2742" border="0"></a>
<a href="https://ibb.co/MZ5BjZM"><img src="https://i.ibb.co/VJpwhJ2/IMG-2744.jpg" alt="IMG-2744" border="0"></a>
<a href="https://ibb.co/0J0WY2c"><img src="https://i.ibb.co/yszMgPX/IMG-2745.jpg" alt="IMG-2745" border="0"></a>
<a href="https://ibb.co/SQLNpLg"><img src="https://i.ibb.co/1sSZxSN/IMG-2747.jpg" alt="IMG-2747" border="0"></a>

## User Persona Storyboard

<a href="https://ibb.co/5sP5qYb"><img src="https://i.ibb.co/h2SKpX3/Storyboard.jpg" alt="Storyboard" border="0"></a>

### Research and Interviews
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


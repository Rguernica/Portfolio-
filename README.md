# About me 
Hi - my name is Rosana. I'm a Public Policy and Management master's candidate at Carnegie Mellon University. I graduate in August. After graduation I will be continuing my work at AH Datalytics - a consulting firm focused on bringing cutting edge analytics to public organizations. My primary focus is on harnessing data to help police departments in their reform efforts. 

# What I hope to learn 
I hope to learn how to create clean and thought-provoking visualizations that communicate their data's stories. 

Data can effect real and meaningful change in the world, and for the better. The caveat with data-driven change is that the people operationalizing data don't read data files the same ways computers to do. We need storytellers to act as an intermediary - to visualize problems, models, predictions, and solutions. I hope to develop the skills needed to begin telling those stories. 

# Portfolio-
See below to view my first attempts at storytelling with data!
## Workbook Sketches 
## Visualization Critiques and Redesigns
## Final Project - Part I 
## Final Project - Part II 
## Data Critique and Redesign: Police Killings 2019 
  **Original Visualization**

  Police and policing data is a crucial component of police reform. For this redesign I chose a chart from Mapping Police Violence. The specific visualizatoin I    redesigned can be found on their home page:https://mappingpoliceviolence.org/. I chose this visualization in particular because it was a) communicating importnat data, and b) so close to doing so effectively. I thought one or two tweaks could radically change the visualizations impact. 
 

 
 <a href="https://ibb.co/BqyvyhZ"><img src="https://i.ibb.co/yW6K6zy/Screen-Shot-2020-07-24-at-1-08-08-PM.png" alt="Screen-Shot-2020-07-24-at-1-08-08-PM" border="0"></a>

  **Process**
  
  After a thorough critique of the visualization I realized the chart is presenting more information than was necessary. The visualizatoin is titled 'There were only 27 days in 2019 where police did not kill someone'. It's a striking statistic. Yet the message gets lost with plethora of colors and white space. The audience does not need to know how many killings took place, but rather, if any killings took place at all. By changing the criteria from 'number of killings per day' to 'was someone killed on this day' we eliminate the need for so many colors. 
  
  This turned out to be harder than I anticipated and took some data prep. The data file used (which can also be found on Mapping Police Violence's website)is a list of police killings. It doesn't include days in which no killings took place, because they don't record the absence of the event. I had to go row by row and figure out which days were skipped. Then I added a row for the missed day and gave it a null value in the column for victims name. There may be a way to do it automatically, but I couldn't figure out how. 
 
 Once the data file was ready and uploaded to Tableau, I created a chart only to painfully realize that because there are not an equal number of days in each month, there were gaps in my chart which could be mistaken for 'days without any killings'. I reordered the orietnation of the months so that the months with fewer days were at bottom right hand side. I also made sure to include gridlines to emphasize what squares were 'days' and which were simply blank space. It's not as symmetrical as I would have liked. I showed the final result to a few people and they were shocked by the statistic. Since that was my primary goal, I'm happy with this final version. 
  
  
  **Final Visualization**
  
  <a href="https://ibb.co/fG0NCNs"><img src="https://i.ibb.co/7NypGpq/Screen-Shot-2020-07-24-at-4-24-13-PM.png" alt="Screen-Shot-2020-07-24-at-4-24-13-PM" border="0"></a>


## Visualizing Government Debt

<iframe src="https://data.oecd.org/chart/62iY" width="860" height="645" style="border: 0" mozallowfullscreen="true" webkitallowfullscreen="true" allowfullscreen="true"><a href="https://data.oecd.org/chart/62iY" target="_blank">OECD Chart: General government debt, Total, % of GDP, Annual, 2018</a></iframe>


<div class="flourish-embed flourish-chart" data-src="visualisation/3280777" data-url="https://flo.uri.sh/visualisation/3280777/embed"><script src="https://public.flourish.studio/resources/embed.js"></script></div>




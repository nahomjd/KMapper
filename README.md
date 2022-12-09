# KMapper
 Repository for mapper project

## Intro
This project will use a topological data analysis tool called Mapper to improve the quality of the data we feed into machine learning models. In this project, we will use a data set from a video game called Football Manager. The game is best described as a spreadsheet simulator where you manage a soccer team. The game is so detailed that some professional teams use its database as a tool in their scouting process. I did a project using multiple machine learning techniques, using the game's data to predict three questions. What is a player's Current Ability? What is a player's Potential Ability? Does a player play in a top-ten league? This project aims to use Mapper from Scikit-TDA's KMapper package to pick better quality features for machine learning rather than using all. We will be looking at 47 features known as the player's attributes in this case.

## Mapper
Mapper is an algorithm that constructs graph of simplicial complex from data. Mapper splits the data into bins. In these bins similar data is clustered together. Then these bins known a vertices of the graph are connected by vertices represnted by lines. Bins are connected when their clusters share vertices with other bins. This is how we visualize the map. Below is a picture example of that happens through the algorithm. Mapper is a tool that can help connect data visually. It can be use to aid in data processes whether it is a data analysis, visual analysis, or help pick the best features for machine learning. As data scientists we look at numbers so much we forget that visuals can shed as much if not more light on our data.

## Observations
We observe a horshoe like simplex with an strut out of the side. Looking at the Current Ability (CA) and Potential Ability (PA) nodes on average gets larger. This gives the simplex a distiguished visual where we can see a distinct difference between one side to the other. This allows us to look into each attribute and see if they correlate whether positivly or negativly with CA and PA. While looking at the different attributes we see that the adnormal shape sticking out are some of the better goalkeepers. While investigating different Mapper Visualizes I found that goalkeepers and their attributes are so different sometimes they become their own simplexes all together. This could indicate that it might be benificail to remove goalkeepers from the Machine Learning modeling altogether or create a seperate model for just them. For the purpose of this project we still conserder goalkeepers.

### Positive Correlating Attributes
- Wor
- Vis
- Tec
- Tea
- Tck
- Str
- Sta
- Pos
- Pen
- Pas
- OtB
- Mar
- L Th
- Lon
- Hea
- Fla
- Flr
- Fin
- Dri
- Det
- Cro
- Cnt
- Cmp
- Bra
- Bal
- Ant
- Agg

### Negative Correlating Attributes
None

### Nuetral Correlating Attributes
- Pac
- Nat
- Jum
- Dec
- Acc
- Cor

### Goalkeeper Positive Correlating Attributes
- Thr
- Tro
- Ref
- Pun
- 1v1
- Kic
- Han
- Ecc
- Com
- Cmd
- Aer

### Goalkeeper Negative Correlating Attributes
None

### Goalkeeper Nuetral Correlating Attributes
None

From here, my suggestions would be to remove the following: 
- Pac
- Nat
- Jum
- Dec
- Acc
- Cor

from or analysis because they give no indication of helping to predict the better players. The next step would be to remove both goalkeepers from the data set, and the attributes considered goalkeeper attributes from the analysis. Once those two steps are done, the analysis should be repeated to see if any more features portray neutrality after the changes are made. Then we can use the remaining features for machine learning models with the confidence that there will be less garbage data.
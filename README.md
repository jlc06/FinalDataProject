# FinalDataProject
Final bootcamp project_
Emery's First commit test_
Herbert table scrape_
Rodgers table scrape_


Testing commit on new computer. 

SLIDE 1 

We came to the decision to use a linear regression model instead of using binary classifiers given the continuous data inputs and outputs we were expecting. We did not change our model choice through the course of the project


Originally for our variables, we used basic stats to create our model and test the accuracy. We tried simply passing yards per game, rush attempts and yards per game, receiving yards per game and a few other stats such as targets and attempts per game. This resulted in accuracy of roughly 45-57% among the 4 models. So clear room for improvement in our next attempt. 
 
![image](https://user-images.githubusercontent.com/100726716/184048584-41409daf-5fe2-436a-9fbe-cc012ca6f2bf.png)
SLIDE 2
 Looking specifically at QBs,  we started thinking about easy ways we could improve the model to account for players who were the starter in the current year and the starter the following year, instead of being either a backup or out of the league. So as John touched on, we then added the “Next Year Starter” and “Starter” features. This was our most successful variable overall I would say because of the huge jump in accuracy in the qb model.   Adding the “next year starter” variable alone changed the QB model accuracy to be 70% which was up from 45%.  
![image](https://user-images.githubusercontent.com/100726716/184048622-3143eb34-75d9-4566-9f8d-057021818f96.png)

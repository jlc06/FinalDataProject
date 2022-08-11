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
Once we had a working model, we then added a few stats to the running back and receivers/TE models. We added stats such as target share and rush share as John mentioned earlier. This shows pretty clearly which players are getting the most touches and therefore the most opportunity to score fantasy points.  Even after those additions, We still weren’t quite satisfied with the overall accuracy of our skill position models which were just over 50%, so we then decided to add some advanced stats in order to hopefully help the accuracy. 

SLIDE 3
We now were happy with the QB Model, and after some research The advanced stats we settled on adding to our WR and TE model were Average Depth of Target, (which is how far the receiver runs downfield before the ball is thrown to him), Yards before and after Catch per game, yards before and after catch per reception, and QB passer rating.  


# Predicting Conmebol Game Results
## by Anthony Verdesca

This code intends to estimate the future results of the matches in the WC CONMEBOL Qualifiers.

We will answer the following questions:

1) What teams will win matches?
2) What are the final positions of teams on WC?
3) Who will qualify to the WC? 


# Executive Summary
1. [Introduction](#introduction)
2. [Methodology](#methodology)
3. [Results](#results)

# Introduction
The CONMEBOL World Cup qualifications is known as one of the toughest qualification events in the world.  The first six teams qualify directly to the world and the seventh goes to a knock-out game with a team in Asia from the Qualifiers in Asia.

It has been known that a simple way to estimate what clubs will win matches is to use their Transfer Market Value and compare them, usually the more expensive team is likely to have better players and thus, more likely to win the matches. Following the path used by Stephan Sczymanski on his Cousera's lab "Predicting EPL Table", we will calculate the logarithm of the proportion between transfer values of the Home Team and Away Team.

The games used to train models will be games played between 2009 and 2024, and for the sake of simplicity, the transfer market value of each team will be extracted based on the final year of that qualification cycle. Keep in mind that the transfer value does not necessarily track the value of the Lineups but the value of the whole teams. Tracking the lineups would probably yield more accurate results, but it does require a lot more tracking and data extraction.

Four different Classification models were implemented:
1) Lasso - lasso
2) Decision Tree Classifier (With Grid Search Cross Validation) - dtc
3) Random Forest Classifier (With Random Search Cross Validation) - rfc
4) Logistic Regression (with Optimized Parameters based on rfc) - logit

Being the fourth one the most accurate with at least 60% accuracy. 

The data was scrapped from Transfermarkt.com (matches, game results, and transfer market values). Transfermarkt.com is a public and popular webpage that share estimated values on teams and players, as well as transfer news and/or rumours. 

![image](https://github.com/user-attachments/assets/e61cbc99-d548-402d-92bf-b5b78c6338f4)

# Methodology

The process consisted in 4 stages:
1) [Scraping and Cleaning data]()
2) [Creating features and Organizing data]()
3) [Model Creation]()
4) [Final table of results]()

1) The webscrapping was used on Transfermarkt.com

# Results

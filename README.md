# Presence
A submission to the 2026 Big Data Bowl - Student track - Analytics [Kaggle](https://kaggle.com/competitions/nfl-big-data-bowl-2026-analytics/writeups/new-writeup-1765933172824)

Atul Venkatesh | Dartmouth College Class of 2027 | [LinkedIn](https://www.linkedin.com/in/atul-venkatesh-8a4b87204/)

Gavin Bulthuis | University of Minnesota Class of 2025 | [LinkedIn](https://www.linkedin.com/in/gavin-bulthuis/)

Levon Sarian | Dartmouth College Class of 2027 | [LinkedIn](https://www.linkedin.com/in/levon-sarian/)

Alexander Nanda | Dartmouth College Class of 2027 | [LinkedIn](https://www.linkedin.com/in/alexander-nanda/)

# Directory
## Code
Wrangling/modeling - Contains the code for our initial data wrangling, completion probability, xYAC, and Presence models
Pairwise - Contains the code for the pairwise and synergy analysis
## Appendices
### Appendix A
Contains the most important features for the Completion Probability model
### Appendix B
Contains the most important features for the Expected Yards After Catch model
## Figures
Contains the relevant figures from the Kaggle write-up
# Glossary
Completion Percentage (CP) - XGBoost model trained to predict the probability of a completed pass

Expected Yards After Catch (xYAC) - XGBoost model trained to estimate the yards after catch

Receiver Value Score (RVS) - CP*(Air Yards + xYAC)

Defenderless Receiver Value Score (DRVS) - RVS when the defender is removed

Value Change - RVS - DRVS

Presence Score - Value Change at catch point - Value Change at time of throw

Synergy Score - Calcualted by the Actual Pair Presence - (Single Effect of D1 + Single Effect of D2)

# Bibliography
da Silva, G. P., & de Andrade Moral, R. (2021). Frame by frame completion probability of an NFL pass (arXiv:2109.08051). arXiv. https://doi.org/10.48550/arXiv.2109.08051

Davis, T [DNVR Sports]. (2023, Dec 4). Todd Davis breaks down how Derek Stingley Jr. baited Russell Wilson into throwing an interception. YouTube. https://www.youtube.com/watch?v=Yv4oSGNCnYU

Lopez, M., Bliss, T., Blake, A., & Howard, A. (2025). NFL Big Data Bowl 2026 – Analytics. Kaggle. https://kaggle.com/competitions/nfl-big-data-bowl-2026-analytics

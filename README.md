## Introduction
Predict the youtube video views of the K-pop group NCT using different types machine learning techniques on features to achieve the best model.

## Prospective
K-pop groups are becoming more and more famous globally. The groups themselves and their content creaters are working harder to fulfill 
their fans' needs. The data analysis of NCT's youtube data could give a visual understanding of which content people enjoy more.

<!--- ## Reason for Data Selection
NCT is a K-pop group with three subgroups. Thus, they have four youtube accounts in total. This helps to generalize data to a wider audience of
K-pop fans. On top of this, because of the larger number of people in a regular K-pop
group, we can always find more reasons affecting youtube video views. -->

## Data Collection Process
* Created a Python script using GCP and Youtube API to collect all videos and their statistics
* Added more features on top of the collected data that are important to the K-pop fan culture

### Potential Problems and fixes
* Views always increase over time. However, the increase rate decreases substantially over time. K-pop fans usually watch new videos as soon as possible especially if they are active online in any K-pop fan community. This is because of the constant exposure they get online about the new content(and also fomo). So, the first few days is the most significant increase in views. After a month, the increase rate of the views generally drop down to less than 1% and after three months, it drops to less than 0.1%. We include a feature called "daysPassed", but the expected importance of this feature would be very low due to the reason above.
* Video views of K-pop groups are heavily reliant on the number of fans they have. The simple way to determine the number of fans is through checking the trend of the number of subscribers. Daily subscribers are not given in youtube API, so checking 3rd party resources would be necessary. Third party resources do not give daily subscriber count for all days, so predicting this could potentially be useful in implementing in models.
* Even with number of subscribers per day is not the most reliable because the number of subscribers has not been the most accountable for the number of views. While number of subscribers will be included in the model, I will be researching more ways to interpret trend of number of fans through twitter api.
* There are certain types of videos that fans are more likely to watch. Interpreting each video into exclusive categories will not work because each video may contain multiple categories that will lead to high views.

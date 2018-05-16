# Reuters 2012-17 News Headline Analysis

* This analysis consists of analyzing Reuters 6 million news headline data from 2012 to 2017, downloaded from Kaggle. This dataset can be found [here](https://www.kaggle.com/therohk/reuters-news-wire-archive/data)

* The main idea is TOPIC-MODELLING, to find out how news headlines can be related and classified into different subgroups using LDA (Linear Discriminant Analysis) and applying t-SNE.

### Data Pre-processing

* The first step was to clean the data and convert it into the usable form. The raw data had 'headlines' and 'publishtime' column which was in the form where the data and time were just nubers combined together. Had to be seperated and converted into date-time format before it was used for further analysis.

![](images/1.png?raw=true)
<br>
<br>
![](images/2.png?raw=true)
<br>
<br>

### Finding most headlines of certain lenght and finding most used words in headlines other than articles like a, the etc. and creating a word cloud.
* Headlines were converted into lowercase letter and cleaned using regular expressions.
* Most used words were found by calculating the frequency of the words that appeared in all the headline since 2012 to 2017.
* To calculate the length of headlines, each word of every headline were counted for every entry in the dataset.
**It turned out that most of the headlines published between 2012 and 2017 consisted of 9 words.**

![](images/3.png?raw=true)
<br>
<br>

**Word Cloud of most used word pairs in the published headlines**

![](images/4.png?raw=true)
<br>
<br>

### Classifying the news headlines into different categories using LDA and applying t-SNE
* Before classifying the headlines, they have to vectorized. 
* As there were 6 million headlines, it made no sense to apply LDA and check whether it was working as expected. So before applying LDA to the whole dataset, 10000 random samples were selected. 
* LDA was applied on the samples to discover 20 different classification topics.

![](images/5.png?raw=true)
<br>
<br>

* After applying LDA, decided to apply t-SNE to find a representation of the input in low dimensional space such that similar points in the original space are also similar in the representation space.
* Also the dimensions has to be reduced to 2 in order to visualize the classifications and also to overcome hardware limitation and time.
* Plotting the classifications of topics on the sample data

![](images/6.png?raw=true)
<br>
<br>

* The headlines have been clustered into 20 different topics as follows:
  *<li>Topic 0:  present ceo
 *<li>Topic 1:  update fund
 --Topic 2:  brief reg
Topic 3:  brief announces
Topic 4:  new says
Topic 5:  preview dividend
Topic 6:  rate reg
Topic 7:  research markets
Topic 8:  china shares
Topic 9:  brief profit
Topic 10:  new program
Topic 11:  business technology
Topic 12:  stocks india
Topic 13:  bank national
Topic 14:  launches deal
Topic 15:  quarter results
Topic 16:  fitch outlook
Topic 17:  reg asset
Topic 18:  new high
Topic 19:  update announces

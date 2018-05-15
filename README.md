# Reuters 2012-17 News Headline Analysis

* This analysis consists of analyzing Reuters news headline data from 2012 to 2017, downloaded from Kaggle. This dataset can be found [here](https://www.kaggle.com/therohk/reuters-news-wire-archive/data)

* The main idea is to find out how news headlines can be related and classified into different subgroups using LDA (Linear Discriminant Analysis) and t-SNE and comapring them with each other.

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
<br>
<br>
![](images/3.png?raw=true)
<br>
<br>
**Word Cloud of most used word pairs in the published headlines**
<br>
<br>
![](images/4.png?raw=true)
<br>
<br>

### Classify


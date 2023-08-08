# Sentiment-Analysis
# Introduction
Sometimes it becomes difficult for a human brain to pass a judgement due to abundance of information. There comes into play the role of data science and AI to foster the decision making process for humans, in an efficient and an effective way. This project tries to fill the gap between the cumbersomeness of humans and the effectiveness of machines while trying to make a judgment from large data.
The project aims at analysing certain text parameters and finding the sentiments behind the text for the urls given in the input excel file
where each url shows an article with a certain number of paragraphs.

# Inputs
The following is the list of the available input:<br />
1. Input-  A list of URLs given in a rowwise fashion in excel format.
2. Positive words - A list of positive words stored in .txt format.
3. Negative words - A list of positive words stored in .txt format.
4. Stop words -  A list of stop words stored in .txt format.
6. Formulae list for paramters - Where the formulas for certain parameters are given
5. Output Structure - An Excel file that describes the structure of the output.

# Required parameters
The following is the list of parameters that needs to be calculated:
1.Positive Score:Total count of positive words for the relevant paragraphs in the given url
2.Negative Score: Total count of negative words for the relevant paragrpahs in the given url a given url
3.Polarity Score: This is the score that determines if a given text is positive or negative innature. It is calculated by using the formula:
 Polarity Score = (Positive Score – Negative Score)/ ((Positive Score + Negative Score) +0.000001)
 Range is from -1 to +1
4.Subjectivity Score: This is the score that determines if a given text is objective or subjective.It is calculated by using the formula:
 Subjectivity Score = (Positive Score + Negative Score)/ ((Total Words after cleaning) +0.000001)
5.Average Sentence Length = the number of words / the number of sentences
6.Percentage of Complex words = the number of complex words / the number of words
7.Fog Index = 0.4 * (Average Sentence Length + Percentage of Complex words)
8.Average Number of Words Per Sentence = the total number of words / the total number of sentences
9.Count of complex words : Complex words are words in the text that contain more than two syllables.
10.Word count = Total number of word counts in the relevant paragraphs after cleaning.
11.Count of personal pronouns
12.Average Word Length = Sum of the total number of characters in each word/Total number of words.

# Procedure 
1. The complete project is built on object oriented programming in python using a single class and multiple methods.
2. Firstly the input data frame is loaded as a dataframe. Later, the text files of positive,negative annd stop words are stored in list format.
3. For each url the data is extracted using beautiful soup.
4. Nltk library is used to calculated the total number of sentecnes in each paragraphs. For calulating the number of pronouns regular expression can be applied to each paragraph.
5. For each word in each line, cleaning of stop words is performed and the counts of positive and negative words are also calculated.
6. Complex words are calculated using certain lines of code which are mentioned in the main code.
7. Based on the above calculated parameters the other required parameters is also calculated.
8. Finally the data acquired for all the parameters of the corresponding URL is loaded in the output data frame.
9. Then we go for the next url.





 

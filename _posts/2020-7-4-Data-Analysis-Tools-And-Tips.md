---
layout: post
title: Data Analysis — Tools & Languages — A quick Review
---

R, Python, Tableau, Qlikview — what to chose and why & when.


My inbox gets regular questions on the topics I usually write about. This time, on [my blog on medium] ("https://www.medium/@pyarisingh"), since there were two back to back posts on data, I got lot of questions on data.

In this post, I will try and put in some “whys and why nots” on some of the languages and tools used in data analysis.

I think I connect well with people who are not in the IT industry well. At least 25% of the questions are from friends who would want to step into IT out of interest. So, there were questions like: data is trending; what tools or languages are good to pick up at this stage.

There were also questions like: when you already knew Qlikview, why did you move to Tableau?
Is it necessary to have programming skills to be a data enthusiast. etc.
I will try and answer these here based on my small experiences.

Here, I am going to deal with 4 tools/programming languages. Infact, 5 including spreadsheets.
* Spreadsheet
* R
* Python
* Qlikview
* Tableau

Spreadsheet — The first and foremost tool or software, we still turn into for data collection is a spreadsheet or google forms, which in turn gives the data in a spreadsheet. We can use Microsoft excel or Google Sheets for the same. We should not be surprised to know that there are people who still prefer to use Microsoft excel over Google Sheets. It is just an inhibition to move out of a comfort zone. For those, who still have that problem, I am adding a line here. On your browser, just type in:

```drive.google.com
Sign in with 
Click on New -> Google Sheets
```
Oh yes, You caught me off guard. I am a big fan of Google. ;) The formulae works almost the same way as that of MS Excel. The formulae and charts together should help us do a good amount of data analysis work with the help of spreadsheets.
The problem with spreadsheets is the readability and maintainability. That way, it is a bit difficult for someone to pass on your work to someone else. There is yet  another issue. When dealing with bigger data, spreadsheets start giving performance issues, especially if you are working on Windows and Microsoft excel. 

*R & Python*
R — Is a programming language. Python too.
Infact, while learning, I used to wonder, why we have two different languages doing the same thing. I personally liked R a bit more. Not because of any big feature or anything. But, I experienced **faceting in data** with R for the first time and it was just great to see the faceted data plots. Here are the 4 blogs that I have written about R. [R - blog 1](https://medium.com/@pyarisingh/my-quick-notes-on-r-a-cheat-blog-2291931b097d), [R - blog 2](https://medium.com/@pyarisingh/r-continuation-advanced-topics-73f30fb780bb) and [R - blog 3](https://medium.com/@pyarisingh/back-to-basics-r-2464fb3de339). You can quickly take a look at them to get a glance of what R can do to manipulate the data.

Python has a good number of libraries like pandas, numpy, matlplotlib, seaborn etc which helps with data analysis. Also, Google Drive and github integration is now possible with an ipython note book using the Google Colab. That way, Python now seems to have an advantage over R now. Here are two blogs which can be browsed for to understand how Python can be used for data analytics. [Blog 1](https://medium.com/@pyarisingh/data-wrangling-some-tips-during-this-covid-season-9ac7e3a726c1), [Blog - 2](https://medium.com/@pyarisingh/getting-started-with-google-colab-3252ba9cd74a)

If you are a programmer, R and Python can be chosen to replace the formula that you use on a spreadsheet. Or if you are a spreadsheet user and if you would like to switch to programs for doing some data analysis, working with Python would be the best way to start is what I feel.

*Qlikview and Tableau:*
Qlikview and Tableau are data visualisation tools. To make colorful visualisations and to tell stories with your data, [Qlikview](https://www.qlik.com) and [Tableau](https://www.tableau.com/) are better. For sure, R and Python can do graphics too. 

```df.pivot_table(index=['year','month'],columns='class',aggfunc='size').plot(kind='bar')```

Above is a code which has to be written to do a bar plot in Python. For lazy programmers like me ;) Qlikview and Tableau are better options to bring up neater visualisations.


Can qlikview and Tableau manipulate the data and help with data wrangling too? Yes it can, but, the features might not be as powerful as what we get through programming languages like Python or R. If you have a decently clean data, quick manipulation might be easier here.
Why qlikview over Tableau or the other way round? I switched to Tableau because I was working on a Mac and Qlikview personal edition was not compatible with Mac. Though, it was a super cool tool which as the name suggests could bring in visualisations by a “click and view”, their non compatibility with Macintosh machines, made me switch to Tableau. I still have a softcorner towards Qlikview, though.

Probably, this turned out to be one of my longest blogs. So, ending this abruptly. :)


---
layout: post
title: Data Wrangling — Some Tips during this covid season
---


In this covid season, thought of sharing some tips and sample codes on Data Wrangling. After getting a glance of Google Colab, my go to language for data wrangling has been Python. This blog hence uses Colab and Pandas on Python for data wrangling.

Most of the data collected has format related issues because they are collected without the use of a software. These days, with tools like Google Forms coming into picture, it is much better, but when you have old data to deal with in its row form, there is no escape from formatting it and getting it to the shape that you need it to be in.

This blog demonstrates how to use colab, pandas and lambda functions to quickly format some data.
I had written an [earlier blog few days back on Colab](https://pyarisinghk.github.io/Getting-Started-With-Google-Colab/) and how to import data from excel to Colab. So, I shall skip that part now.
Let us say, the below is the data that we need to format (the admission number column) and we need all the data to be in the format: YYYY-Num

 ![_config.yml]({{ site.baseurl }}/images/raw_data.png)


We can do this quickly using dataframes and lambda functions in Python.
The below is what we can do to do the transformation:
Import the data into a dataframe using pandas.
Then, write a normal function in Python which will replace the slash in a string with a “-”. Later, apply a lambda function on the column “Admission Number” and pass this function which we just wrote.
We can repeat the same with another function to format the date. In the second function we can split the data with “-” and check for the format of the year and replace it if required in the YYYY format. Apply this lambda function again on the column which requires the data to be formatted.
The resulting data can be exported to another .csv on the drive too. A piece of demo code is written to show this. The note book has been uploaded to my Github from Colab directly and is available [here](https://github.com/pyarisinghk/Colab_Sandbox/blob/master/ShowCase_Blog.ipynb). Below are the screenshots of the relevant pieces of code.

 ![_config.yml]({{ site.baseurl }}/images/code_1_lambda.png)
 ![_config.yml]({{ site.baseurl }}/images/code_2_lambda.png)


Might sound simple. But, these simple tools worked like magic on my old Mac with performance issues to transform 1000s of records and to get some “visualisable” data quickly.


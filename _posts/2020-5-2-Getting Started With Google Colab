---
layout: post
title: Getting Started with Google Colab
---


(Migrating a [slighly old blog from medium](https://medium.com/@pyarisingh/getting-started-with-google-colab-3252ba9cd74a) "Getting started with Google Colab") to here)

#### Here is what you could do to get started with Google Colab
Search for “Google Colab” on Google. Find the link corresponding to https://colab.research.google.com/ and login with your gmail account

Google Colab — Search Results

![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

Google Drive — Path for the files
Step 2 - Upload the required files as .csv onto Google Drive. In the above, you can see that my files are on My Drive->ColabDemo folder
Step 3 — Create a new Notebook. Use the File Menu — New Notebook option (picture attached below)

Creating a new Notebook
Step 4 — Tadang! The notebook is ready to use! Rename the notebook to have the name you like to have. Run the python code like using a usual jupyter note book.

A ready to use Notebook on Colab
To import a set of files which are there on the drive, do the below:
(I had in fact forgotten, how to do this. I found this on stack overflow here: https://stackoverflow.com/questions/48340341/read-csv-to-dataframe-in-google-colab)
Step 5
Run the below code on the first cell of the notebook, follow the instructions and complete the authentication.
from google.colab import drive
drive.mount('/content/gdrive/')
On successful authentication, you get an output which looks like the below.

Drive Successfully Mount
Woohoo… We have a good platform to start playing with our files now.
Step 6 — Add the next cell as usually done on a Jupyter Notebook by clicking on the “+ Code”
Time to bring in our favorite Pandas. :) Below is a code that I have pasted for reference.
import pandas as pd
df=pd.read_csv('gdrive/My Drive/ColabDemo/class 3A.csv')
df.head()
Let us now view the output before we close the session.

Successfully imported the file using pandas
I hope you like the blog. :)
5

---
layout: post
title: Getting Started with Google Colab
---

Does technology distract you? As far as I am concerned, the answer is yes. Since the time I completed two nano degrees (one on Android Basics and another on Data Analysis) from Udacity, I keep switching between Data and Android. I recently got another scholarship, which is the Bertelesmann Scholarship, but, considering the advices of my well-wishers, I have finally decided to let go of the scholarship and focus on Android alone. Also, listening to my inner voice to stay focused. ;) 

But yeah, I have this problem. I take up some or other thing in tech and it demands a change of focus. When India is in the mid of the lockdown due to Covid 19, I decided to work a bit on data again as part of a small work that I am doing. Now, that made me start on Google Colab again and this long pending blog, I thought I will complete today.
I had attended [Ms.Usha Rangaraju’s](https://medium.com/@usharengaraju) session on Colab sometime back through GDG, the only one which I attended with GDG Bangalore. It was a good one and I wanted to keep some notes for myself and this blog was pending since then.


#### Why Google Colab
Today, I have a set of excel files with me. As we know, the more the number of excel files we work on, the more it becomes difficult to manage things at a later stage. When we want to get a feel of the data in these excel sheets and want to try manipulating them, the best option is always to bring it on a data frame using pandas in python. I had lost touch with Python completely and wanted to have a readymade set up to do this. That is when I remembered about Colab again.


#### Here is what you could do to get started with Google Colab
* Step 1 - Search for “Google Colab” on Google. Find the link corresponding to https://colab.research.google.com/ and login with your gmail account


![_config.yml]({{ site.baseurl }}/images/search_results.png)


![_config.yml]({{ site.baseurl }}/images/google_drive_path.png)

* Step 2 - Upload the required files as .csv onto Google Drive. In the above, you can see that my files are on My Drive->ColabDemo folder

* Step 3 — Create a new Notebook. Use the File Menu — New Notebook option (picture attached below)
![_config.yml]({{ site.baseurl }}/images/create_new_notebook.png)



* Step 4 — Tadang! The notebook is ready to use! Rename the notebook to have the name you like to have. Run the python code like using a usual jupyter ipython note book.

#### A ready to use Notebook on Colab
To import a set of files which are there on the drive, do the below:
(I had in fact forgotten, how to do this. I found this on stack overflow here: https://stackoverflow.com/questions/48340341/read-csv-to-dataframe-in-google-colab)

* Step 5
Run the below code on the first cell of the notebook, follow the instructions and complete the authentication.
from google.colab import drive
drive.mount('/content/gdrive/')
On successful authentication, you get an output which looks like the below.

![_config.yml]({{ site.baseurl }}/images/drive_mount.png)


Woohoo… We have a good platform to start playing with our files now.


* Step 6 — Add the next cell as usually done on a Jupyter Notebook by clicking on the “+ Code”
Time to bring in our favorite Pandas. :) Below is a code that I have pasted for reference.

import pandas as pd
df=pd.read_csv('gdrive/My Drive/ColabDemo/class 3A.csv')
df.head()

Let us now view the output before we close the session.

![_config.yml]({{ site.baseurl }}/images/imported_file.png)


I hope you like the post and will soon start using Google Colab. :)


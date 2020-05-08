threehyphens
layout: post
title: Moving to a new platform - Hello from Github Pages :)
threehyphens

In the new app that I am developing, I am using Room to store data. Room is an abstraction over SQLite. One of the difficulties that I faced with Room was to view the saved data. The data is saved on our phone and how do we view this DB?

This [code](https://github.com/pyarisinghk/SampleCodes/tree/master/RoomWithoutLiveData) on Github demonstrates the creation of tables using Room and displaying the data on a recylcerview on android. As an intermediate step, if we would like to see the data created, what do we do?
When I started using Room, I was confident that I can view the tables using the method followed in one of my [earlier blogs on sqlite](https://medium.com/@pyarisingh/sqlite-cheat-sheet-cf0d6bc3f0c6). However, for some reason, when I tried to list the databases, I could never get the databases listed with this & hence this approach.

The below are the steps that can be followed to view the database created by Room. 
* Step 1 — Download an SQLite Browser application. I downloaded it from [here](https://sqlitebrowser.org/). You might have to go to the [downloads tab](https://sqlitebrowser.org/dl/) to download it.
* Step 2 — Copy the database created on the mobile on to your machine. There are several ways to do this. I followed this approach using the Android Studio.
 `View->Tools Windows->Device File Explorer `
 
 ![_config.yml]({{ site.baseurl }}/images/Device_Explorer_Android_Studio.png)
 
 The namespace for my app, if you see [the code](https://github.com/pyarisinghk/SampleCodes/tree/master/RoomWithoutLiveData) on my Gitub is com.example.android.todolist

 ![_config.yml]({{ site.baseurl }}/images/package_name_from_code.png)
 
 Navigate to the below path through the device explorer:

`data/data/com.example.android.todolist/databases`

 ![_config.yml]({{ site.baseurl }}/images/data_base_files_on_the_device_file_explorer.png)


Click on the databases folder and save all the three files. In my case, it is questionBank, questionBank-shm and questionBank-wal
* Step 3: Open DB Browser for SQLite.
Click on Open Database and browse for the questionBank file (without extension) and import the DB into the browser.

 ![_config.yml]({{ site.baseurl }}/images/db_browser_for_sqlite.png)
 
 Click on Browse Database tab and select the table to view the data.
Happy Coding!


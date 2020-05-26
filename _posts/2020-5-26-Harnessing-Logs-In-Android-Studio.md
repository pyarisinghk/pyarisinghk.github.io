---
layout: post
title: Harnessing Logs in Android Studio (Java & Kotlin)
---

Does something like this happen to you? All these days, whenever I hear “mutable” variable, I use to first think that it cannot be changed because it will be “muted”. Then, I see the code and wonder, how it gets changed. It is then that I have to tell myself again that, ok, mutable variables are variables whose value can be changed. Was not happy about this counter intuitive thing. Today when I was going through a video by Lyla Fujiwara on LiveData on Android, I heard her say that the a MutableLiveData is mutatable Live data. Wow! She really is a good computer science teacher. The way she emphasised on that mutatable ensures that now on, there is no more confusions related to mutable variables. A mutable (otherwise called mutatable) variable obviously can be changed as the name clearly suggests. There are small little things like this, I keep struggling in the initial days of learning any new tech.
Likewise, until I learnt to apply filters in excel, excel sheets were a nightmare during the initial days!
In this blog, I am addressing logs in Android Studio. Another simple thing which I overlooked in the initial days.
Whenever there was a crash, peers ask us to look through the logs and on debug mode, we keep seeing multiple lines of logs getting written in a second. It took some time for me to figure out how to manage logs.
If you are using a manual “search” like me, to search for the logs, this post is for you.
Logs in Android are typically written as

```
Log.d("MyActivityTag", "Test Log")

"MyActivityTag" is the tag used to identify the log & 
"Test Log" is the log message.
```

or
```
Log.i("MyActivityTag", "Test Log 1")
Log.i("MyActivityTag", "Test Log")
```
Based on whether we use info logs or error logs or debug logs, we use the .i, .d or .e
The full list of log levels are listed [here](https://developer.android.com/studio/debug/am-logcat) on the Android documentation
Now, to view these, usually I give a full search. It is only recently when I saw a video on Udacity, I realised that these can be filtered out.
Sharing a screen shot of the logcat window to filter out Logs written like above.

 ![_config.yml]({{ site.baseurl }}/images/InfoLogs.png)
The above image shows how to filter out the Info logs written using Log.i
Note that we set the log level to “Info” and searched for I/TagName to do the filtering of Info logs.
ie, we set two filters:
(i) Log level as Info and
(ii) Search parameter as I/tag name we used in the code. ie, I/MyActivityTag in the case of our code written above.

 ![_config.yml]({{ site.baseurl }}/images/DebugLogs.png)
The above image shows how to filter out the Debug logs written using Log.d

Again, note that we set the log level to “Debug” and searched for D/TagName to do the filtering of Debug logs.
ie, the two filters we set are:
(i) Log level as Debug and
(ii) Search parameter as D/tag name we used in the code. ie, D/MyActivityTag in the case of our code written above.
Something which is trivial and everyone knew! But, as a newbie, I am excited to find this now!
Happy logging. :-)


---
layout: post
title: Styles in Android
---
I am a very lazy developer. Because I code mainly for my own apps, I’m very lazy to go back and refactor my codes.


I started training recently and one of the habits that I try to inculcate in my students (without much emphasis on it) is the skill of writing clean codes. Today when I happened to talk about the DRY principle in two of my classes, I was visualising one of my codes where I went on repeating stuffs just because I was lazy to go and browse on how to implement styles and the resource dimen in Android. (Though I remember seeing these in others’ codes very often)
I felt a bit ashamed to preach something without practising it. Also, one of my XML files for a single screen app has started giving me issues because the code has become a spaghetti code because of redundancy. While in my class, I decided to go back and clean my code and as I cloned my old code now, I thought I will make a write up about styles in android here.


Thanks to my students. One good thing about training is that you get to reinforce the concepts which you picked up earlier. And it is because I refreshed styles for my students that I am finding the energy and enthusiasm to go back and make my code clean.


##### Into the implementation:
Let us say, we are trying to achieve something like the attached screen. 4 buttons, all with the same attributes.

![_config.yml]({{ site.baseurl }}/images/styles.png)


Pasted below is a sample code (without using styles) which has been written to create 4 buttons of the same style. All the text has to be the same. The font colour has to be white. The corner radius has to be some 5 dp. The padding and margin are to be of the standard sizes, 8dp. Here we have written each of the attributes of the button separately and we repeated it every time.
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="@dimen/margin_standard"
        android:background="@drawable/orange_button_with_round_border"
        android:padding="@dimen/padding_standard"
        android:text="@string/next"
        android:textColor="@color/colorWhite" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="8dp"
        android:background="@drawable/orange_button_with_round_border"
        android:padding="8dp"
        android:text="@string/next"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="8dp"
        android:background="@drawable/orange_button_with_round_border"
        android:padding="8dp"
        android:text="@string/next"
        android:textColor="#ffffff" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="8dp"
        android:background="@drawable/orange_button_with_round_border"
        android:padding="8dp"
        android:text="@string/next"
        android:textColor="#ffffff" />
</LinearLayout>
```
However, this code can easily be refactored by defining a style and moving all the view attributes to it. Pasted below are the codes to demonstrate the usage of styles which reduces the redundancy.
Style is being defined first: (notice that all the repeating attributes are moved into a style by name Next button)
```
<resources>
     <style name="NextButton">
        <item name="android:background">@drawable/orange_button_with_round_border</item>
        <item name="android:layout_width">184dp</item>
        <item name="android:layout_height">36dp</item>
        <item name="android:textColor">@color/colorWhite</item>
        <item name="android:text">@string/next</item>
        <item name="android:layout_margin">@dimen/margin_standard</item>
        <item name="android:padding">@dimen/padding_standard</item>
    </style>
</resources>
```
Once this is done, the activity page can be reduced to something like this:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <Button style="@style/NextButton" />
    <Button style="@style/NextButton" />
    <Button style="@style/NextButton" />
    <Button style="@style/NextButton" />

</LinearLayout>
```
I think with this refactoring, I am going to fix a long pending bug on my app. The code is definitely going to look much cleaner and fixing a bug on a clean code is in fact a very satisfying job. :)
A big thank you to my Android UI students once again. :)




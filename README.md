Discrollview  
==================

Regularly, I am pleasantly surprised by websites using a pattern I called the discrollver pattern. I'm sure you already know what I'm talking about but if not, http://vimeo.com/player is a good example. When you scroll, widgets appear from nowhere by fade, translation or scale.

With DiscrollView, I wanted to import this pattern on Android. This is an 0.0.1 alpha version because you have to do all the transformation work (fade, translation, scale etc) yourself base on a ratio value. I'm going to add some transformation presets (translation from left to right + fade in for example) to make the library more ready to use for lazy developers.

![Animated gif][4] ([on youtube][1])

Try out the sample APK [here][2]

Or browse the [source code of the sample application][3] for a complete example of use.

Including in your project
-------------------------

Just add the library to your application as a library project.

Compatibilty
------------

API 14+

Usage
---------

Using the library is simple, just look at the source code of the provided sample [here][3]

### build.gradle

```
compile 'com.github.flavienlaurent.discrollview:library:0.0.2@aar'
```

### The main layout

You must use the DiscrollViewContent view.

```xml
<com.flavienlaurent.discrollview.lib.DiscrollView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:discrollve="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <com.flavienlaurent.discrollview.lib.DiscrollViewContent
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <!-- here you put discrollvable views -->

    </com.flavienlaurent.discrollview.lib.DiscrollViewContent>

</com.flavienlaurent.discrollview.lib.DiscrollView>
```

### Discrollvable views

You can apply some transformation on discroll:

- alpha
- scale
- translation (fromLeft, fromBottom, fromRight, fromTop)
fromLeft+fromRight and fromBottom+fromTop are forbidden couples.
- bgcolor

```xml
discrollve:discrollve_alpha="true"
discrollve:discrollve_translation="fromLeft|fromBottom"
discrollve:discrollve_scaleX="true"
discrollve:discrollve_scaleY="true"
discrollve:discrollve_fromBgColor="#88EE66"
discrollve:discrollve_toBgColor="#000000"
discrollve:discrollve_threshold="0.3"
```

The threshold attribute is used to trigger the discrollve at a specified ratio. For example, if threshold=0.3, the discrollve starts when the ratio >= 0.3.

### A simple example

```xml
<com.flavienlaurent.discrollview.lib.DiscrollView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:discrollve="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <com.flavienlaurent.discrollview.lib.DiscrollViewContent
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="600dp"
            android:background="@android:color/white"
            android:textColor="@android:color/black"
            android:padding="25dp"
            android:textSize="72sp"
            android:gravity="center"
            android:fontFamily="serif"
            android:text="Do you love cheese?" />

        <View
            android:layout_width="match_parent"
            android:layout_height="200dp"
            android:background="#007788"
            discrollve:discrollve_alpha="true"
            discrollve:discrollve_threshold="0.3" />

        <ImageView
            android:layout_width="200dp"
            android:layout_height="120dp"
            discrollve:discrollve_alpha="true"
            discrollve:discrollve_translation="fromLeft|fromBottom"
            android:src="@drawable/cheese1" />

        <View
            android:layout_width="match_parent"
            android:layout_height="200dp"
            discrollve:discrollve_fromBgColor="#88EE66"
            discrollve:discrollve_toBgColor="#000000" />

        <ImageView
            android:layout_width="220dp"
            android:layout_height="110dp"
            android:layout_gravity="right"
            android:src="@drawable/cheese2"
            discrollve:discrollve_translation="fromRight" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:padding="20dp"
            android:fontFamily="serif"
            android:gravity="center"
            android:text="When the cheese comes out everybody's happy pecorino red leicester"
            android:textSize="18sp"
            discrollve:discrollve_alpha="true"
            discrollve:discrollve_translation="fromBottom" />

        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_margin="20dp"
            android:layout_gravity="center"
            android:src="@drawable/ilovecheese_heart"
            discrollve:discrollve_scaleX="true"
            discrollve:discrollve_scaleY="true"  />

    </com.flavienlaurent.discrollview.lib.DiscrollViewContent>
</com.flavienlaurent.discrollview.lib.DiscrollView>
```

License
-----------

    Copyright 2013 Flavien Laurent

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

 [1]: http://youtu.be/FGYaweSP3sA
 [2]: https://github.com/flavienlaurent/discrollview/raw/master/sample.apk
 [3]: https://github.com/flavienlaurent/discrollview/tree/master/sample
 [4]: https://raw2.github.com/flavienlaurent/discrollview/master/discrollview.gif

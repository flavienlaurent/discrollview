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

Usage
---------

Using the library is simple, just look at the source code of the provided sample [here][3]

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

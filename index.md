---
layout: default
---

{% include title.html %}

<h2 id="features">Features</h2>

### Simple and Fast Search

This is the syntax to make searching easier:

<div class="search_logo"><img src='assets/image/Search.svg'>One Two</div>

This search argument markes every result containing «One» and «Two». The order does not matter.

<div class="search_logo"><img src='assets/image/Search.svg'>"One Two"</div>

This search argument markes every result containing exactly «One Two».

<div class="search_logo"><img src='assets/image/Search.svg'>Go * </div>

The * sign means that it can be followed or started by any word character.

<div class="search_logo"><img src='assets/image/Search.svg'>GEN 1,1</div>

To get text passages, type its name in the standart bible notation.

<div class="search_logo"><img src='assets/image/Search.svg'>Word @ GEN</div>

To get words in just a passage.

### Write Notes

You can open a note for a verse by clicking the circle button next to the verse header.

<div class="active_verse">
	VERSE 42,42 <span class="dot" id="inactive"></span><br>
	The verse at the top of the window is called «active verse» it is marked at the left side.	
</div>
<div class="active_verse">
	VERSE 43,43 <span class="dot" id="active"></span><br>
	If the verse header has a colored dot next to the header, there is a saved note for this verse.
</div>

You can write notes using *Markdown*.

### Strong Search

You can search for *strong numbers* by right-click on a word and clicking *Strong Search*. This feature is only available for sources containing *strong numbers*.

### Compare Sources

With the *source tabs* you can view several sources at once. This feature makes it possible to see the other versions of a passage.

<h2 id="build">Build</h2>

If you do not want to build *LibreTextus* by yourself, just get it from the [*snap-store*](https://snapcraft.io/libretextus)
To build it by yourself, do the following:

First of all you need following libraries:

* cmake
* build-essential
* gettext
* boost-regex
* boost-program-options
* rapidxml
* gtkmm

You need to clone the source:
```
git clone https://github.com/LibreTextus/LibreTextus.git
```

Then compile the source with *CMake*:
```
mkdir build
cd build
cmake ..
make -j$(nproc)
```

Now you can run *LibreTextus* by typing:
```
./LibreTextus
```

<h2 id="get_involved">Get Involved</h2>

### Coding

If you want to help coding here some tips for starting:
If there is a feature you miss, add it then create a pull request, fork it or what ever you want. The *LibreTextus* source code is under [CC0](https://github.com/LibreTextus/LibreTextus/blob/master/LICENSE), so do what ever you want with it.

### Design

If you want to write own themes, you can import the template CSS file.

{% highlight css %}
@import "template.css";

@define-color theme_text_color #HEX-CODE;
@define-color theme_text_background_color #HEX-CODE;
@define-color theme_background_color #HEX-CODE;
@define-color theme_highlight_color #HEX-CODE;
@define-color theme_accent_color #HEX-CODE;

#history_button button {
	background-image: url('path/to/your/image');
}

#add_button {
	background-image: url('path/to/your/image');
}

#close_button {
	background-image: url('path/to/your/image');
}
{% endhighlight %}

If you want to write your whole theme by yourself here a little list of the objects:

* Every window: *window*
* Splash screen: *#splash_screen*
* Search entry: *#search_entry*
* Search entry progress: *#search_entry progress*
* TextView: *#text_view*
* Verse container: *#verse_box*
* Active verse (The one at the top): *#active_verse*
* Add buttons: *#add_button*
* Close buttons: *#close_button*
* Note section: *#note_toggle*
* Note headerbar: *#note_header*
* Note title: *#note_header_title*
* History Button: *#history_button*

If you want to modify more, just compile *LibreTextus* and run:

{% highlight bash %}
GTK_DEBUG=interactive ./LibreTextus
{% endhighlight %}


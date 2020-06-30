---
layout: default
title: Get Involved
---

# Get Involved

* [Code](#code)
* [Design](#design)


## Code

After pulled the repository you can start to code. Here some hints to make coding together easier:

First of all every function you add you should write a comment above it what the function does:

{% highlight c++ %}
// ----------------------------------------------------------------------------
// WRITE HERE WHAT YOUR FUNCTION DOES
// ----------------------------------------------------------------------------

void your_amazing_function() {
	…
}
{% endhighlight %}

Split your code into passages and comment them so everyone can understand your code.

{% highlight c++ %}
// -----------------------------------------
// THIS PASSAGE DOES THIS
// -----------------------------------------

…

// -----------------------------------------
// THEN IT DOES THIS BECAUSE OF REASONS
// -----------------------------------------

…
{% endhighlight %}

If your commenting like this, it is easy for others to understand your code and for new members to join.

## Design

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



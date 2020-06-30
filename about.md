---
layout: default
title: About
permalink: /about/
---

# About

*LibreTextus* is the Bible reader software. With *LibreTextus* you are able to search, write note s, compare translations in one application. The feature *Strong Search* allows you to analyze your translations and get its origin from old Greek or Hebrew.

# Get It

You can get *LibreTextus* from the [SnapStore](https://snapcraft.io/libretextus) or pull it directly from [GitHub](https://github.com/LibreTextus/LibreTextus) and build it by yourself.

## Build it from source

### Dependencies

* cmake
* build-essential
* gettext
* boost-regex
* boost-program-options
* rapidxml
* gtkmm

First of all, you have to clone the repository.

{% highlight bash %}
git clone https://github.com/LibreTextus/LibreTextus
{% endhighlight %}

Then you can build it:

{% highlight bash %}
mkdir build
cd build
cmake ..
make -j$(nproc)
{% endhighlight %}

Now you can run it with:

{% highlight bash %}
./LibreTextus
{% endhighlight %}

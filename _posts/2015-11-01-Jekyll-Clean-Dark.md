---
layout: post
title: "Installation"
date: 2015-11-01 16:25:06
description: Here you'll find out how to install this theme
tags: 
 - jekyll
---

# Jekyll Clean Dark

## Installation

If you dont't have your own blog you can clone this repository and put your articles in a `_posts` folder.
If you already have your own blog then I think you can clone this repository and copy-paste content keeping your `_posts` folder.

After you will have to set up your `_config.yml`

## License

The content of this theme is distributed and licensed under a [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)

> This license lets others distribute, remix, tweak, and build upon your work,
> even commercially, as long as they credit you for the original creation. This
> is the most accommodating of licenses offered. Recommended for maximum
> dissemination and use of licensed materials.

In other words: you can do anything you want with this theme on any site, just please
provide a link to the original theme on github.

This theme includes the following files which are the properties of their
respective owners:

* js/bootstrap.min.js - [bootstrap](http://getbootstrap.com)
* css/bootstrap.min.css - [bootstrap](http://getbootstrap.com)
* js/jquery.min.js - [jquery](https://jquery.com)

## Images

### Introduction

This theme supports two types of images:

- inline images: ![Battery Widget](E:\github\blog\_posts\{{ '\assets\images\batWid1.png' | relative_url }})

{% highlight html %}
{% raw %}
![Battery Widget](E:\github\blog\_posts\{{ '\assets\images\batWid1.png' | relative_url }})
{% endraw %}
{% endhighlight html %}

- centered images with caption (optional):

![img](E:\github\blog\_posts\{{ '\assets\images\deer.jpg' | relative_url }}){: .center-image }*(°0°)*

{% highlight html %}
{% raw %}
![img](E:\github\blog\_posts\{{ '\assets\images\deer.jpg' | relative_url }}){: .center-image }*(°0°)*
{% endraw %}
{% endhighlight html %}

You can apply your own styles to image by creating css class with style:

{% highlight css %}
.custom-image-style
{
/* your style */
}
{% endhighlight css %}

And then applying your style just after the image in curly brackets with colon:

{% highlight html %}
{% raw %}
[!image](path to image){:.custom-image-style}
{% endraw %} 
{% endhighlight html %}

## Analytics, tags and comments

### Analytics

#### [Google Analytics](http://www.google.com/analytics/)

To enable Google Analytics create an account [here](https://analytics.google.com). Then add your tracking id in `config.xml`, it should look something like `UA-********-1`

#### [Yandex Metrica](http://metrica.yandex.com)

To enable Yandex Metrica you need to register, create a 'counter' and then copy-paste it's code in `/_includes/yandex-metrica.html` file.

### Tags

To use this feature you simply will need to create a markdown file for each tag which you are using in you site in **tag** folder. To simplify this procedure there is an [/admin]({{site.baseurl}}/admin) page, which outputs the bash command which you just need to run inside **tag** folder of your site. Also don't forget to rerun it when you add a post with new tag.

### Comments

To enable [Disqus](http://disqus.com) register on the site and then just put your name in `_config.xml`. Comments could be switched on and off on per post basis, just put `comments: true` to enable them.

## Be social

### Social icons

You can have social icons which could lead to your social profile.
Out-of-the box it has: 

<ul class="social-media">
  <li>
    <a title="Github"
      href="https://github.com/{{ site.social.github }}"
      target="_blank"><i class="fab fa-github fa-2x"></i></a>
  </li>
  <li>
    <a title="StackOverflow"
      href="http://stackoverflow.com/users/1252056/{{ site.social.stackoverflow }}"
      target="_blank"><i class="fab fa-stack-overflow fa-2x"></i></a>
  </li>
  <li>
    <a title="LinkedIn"
      href="https://www.linkedin.com/in/{{ site.social.linkedin }}"
      target="_blank"><i class="fab fa-linkedin fa-2x"></i></a>
  </li>
  <li>
    <a title="Instagram"
      href="https://instagram.com/{{ site.social.instagram }}"
      target="_blank"><i class="fab fa-instagram fa-2x"></i></a>
  </li>
  <li>
    <a title="Last.fm"
      href="http://lastfm.com/user/{{ site.social.lastfm }}"
      target="_blank"><i class="fab fa-lastfm fa-2x"></i></a>
  </li>
  <li>
    <a title="RSS"
      href="{{site.url}}/{{ site.social.rss }}"
      target="_blank"><i class="fa fa-rss fa-2x"></i></a>
  </li>
</ul>


They could be setup in `_config.yml`.

To add more icons do following steps:

 - choose an icon you want to use: [Font Awesome Icons](https://fortawesome.github.io/Font-Awesome/icons/)
 - add variable in `_config.yml`
 - add icon in `social.html` with check if variable exists:

{% highlight html %}
{% raw %}
{% if site.social.rss %}
  <li>
    <a title="{{ site.social.<your_social_variable> }}" 
       href="{{site.url}}/{{ site.social.<your_social_variable> }}" 
       target="_blank"><font_awesome_icon></i></a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight html %}


### Share buttons

This theme comes with built-in share buttons. You can see them in the bottom of this post.
To turn them on in the header of your post add:

{% highlight yml %}
layout: post
title: "Be sociable"
date: 2016-05-15 16:25:06
description: Built-in share buttons!
share: true <-- here
{% endhighlight yml %}

If you want to disable some of them - go to **_config.yml**:

>_config.yml
>{:.filename}
>{% highlight yml%}
>share:
>facebook: true
>twitter: true
>gplus: true
>linkedin: true
>pinterest: true
>email: true
>{% endhighlight yml%}

To add new buttons:

1. add icon name in **_config.yml**;
2. add section in **_includes/share.html**;
3. add styles in **css/theme.css**.

## Customizations

### Accent color

Accent color is color for some important elements, such as links, buttons, icons. Currently accent color is <button class="btn" style="background-color:#3CA2A2; color:#444444">#3CA2A2</button>. This theme has some more predefined colors available in **theme.scss**:

>theme.scss
>{:.filename}
>{% highlight scss %}
>// Several accent colors, choose one or create your own!
>$accent-color: #3CA2A2;     // original =)
>// $accent-color: #C38FD6;   velvet
>// $accent-color: #8FD6B3;   greenish
>// $accent-color: #35B4DE;   bluish
>// $accent-color: #D2E354;   yellowish
>// $accent-color: #52B54B;   green

{% endhighlight %}

You can use one of them (just click the button below to see accent color in action) or define your own!

<button class="btn" style="background-color:#C38FD6; color:#444444">#C38FD6</button>, <button class="btn" style="background-color:#8FD6B3; color:#444444">#8FD6B3</button>, <button class="btn" style="background-color:#35B4DE; color:#444444">#35B4DE</button>, <button class="btn" style="background-color:#D2E354; color:#444444">#D2E354</button>, <button class="btn" style="background-color:#52B54B; color:#444444">#52B54B</button>.

<script>
  $('.btn').click(function(){
    var color = $(this).text();
    [].forEach.call($('a'), function(item) {
      item.style.color = color
    })
  })
</script>


<style>
  .label{
    cursor: default;
    border-radius: 5px;
    padding: 5px 8px;
  }
</style>


### Other colors

As Jekyll comes with support of SASS I put colors in variables. Here are the ones which could be easily changed:

>theme.scss
>{:.filename}
>{% highlight scss %}
>$font-color: #dddddd;
>$background-color: #292929;
>$post-panel-color: #444;
>$footer-background-color: #292c2f;
>$note-color: #87CEFA;
>$warning-color: #ffff00;
>{% endhighlight %}

### Background

It is also possible to change the background pattern and color. This theme comes with few patterns pre-installed -- you can check them by clicking on the images below. Or check the [transparenttextures.com](https://www.transparenttextures.com/) -- it has tons of different patterns for background.

<style>
.pattern-list{
    list-style-type: none;
    padding: 0;
}
.pattern{
    height: 100px;
    box-shadow: 0 0 3px 2px rgba(0,0,0,.1);


}
.pattern:hover {
    box-shadow: 0 0 3px 2px rgba(0,0,0,.3);
    transition: box-shadow .2s ease;
    cursor: pointer;
}
.smthg{
    max-width: none !important;
}
.col-sm-6 {
    padding: 5px !important;
}
</style>

<ul class="pattern-list">
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/3px-tile.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/asfalt-light.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/black-linen.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/food.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/gplay.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/green-dust-and-scratches.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/hexellence.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/random-grey-variations.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/shley-tree-1.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/subtle-grey.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/xv.png' | relative_url }}')"></div></li>
<li class="col-sm-6"><div class="pattern" style="background-image:url('{{ '/assets/css/pics/background/triangles.png' | relative_url }}')"></div></li>
</ul>


<script>
  $('.pattern').click(function(){
    var source = this.style.backgroundImage;
    document.getElementsByTagName('body')[0].style.backgroundImage = source;
    console.log("url('" + source + "'))");
  })
</script>


To change the color go to the **theme.scss** and change the `background-pattern` variable to the name of the pattern image file. To use custom pattern, download it from [transparenttextures.com](https://www.transparenttextures.com/) and place it under **css/pics/background/**.

>theme.scss
>{:.filename}
>{% highlight scss %}
>// use this or pick any from /css/pics/background folder or from transparenttextures.com
>$background-pattern: 'random-grey-variations.png';
>{% endhighlight %}

## Code snippets

### Introduction

For code syntax coloration I'm using Darcula theme from Intellij IDEA, which I've found in this post [Darcula theme for Pygments](http://smasue.github.io/pygments-darcula).

XML with line numbers (linenos flag), `{{ "{%" }} highlight xml linenos %}`:
{% highlight xml linenos %}
{% raw %}
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
  <channel>
    <title>{{ site.name }}</title>
    <description>{{ site.description }}</description>
    <link>{{site.baseurl | prepend:site.url}}</link>
    <atom:link href="{{site.baseurl | prepend:site.url}}/feed.xml" rel="self" type="application/rss+xml" />
    {% for post in site.posts limit:10 %}
      <item>
        <title>{{ post.title }}</title>
        <description>{{ post.content | xml_escape }}</description>
        <pubDate>{{ post.date | date: "%a, %d %b %Y %H:%M:%S %z" }}</pubDate>
        <link>{{post.url | prepend:site.baseurl | prepend:site.url}}</link>
        <guid isPermaLink="true">{{post.url | prepend:site.baseurl | prepend:site.url}}</guid>
      </item>
    {% endfor %}
  </channel>
</rss>
{% endraw %}
{% endhighlight xml %}

>JSON
>{:.filename}
>{% highlight json %}
>{"employees":[
>{"firstName":"John", "lastName":"Doe"},
>{"firstName":"Anna", "lastName":"Smith"},
>{"firstName":"Peter", "lastName":"Jones"}
>]}
>{% endhighlight %}

>SQL
>{:.filename}
>{% highlight SQL %}
>select count(*) as cm_content_nodes
>from alf_node nd, alf_qname qn, alf_namespace ns
>where qn.ns_id = ns.id
>and nd.type_qname_id = qn.id
>and ns.uri = 'http://www.alfresco.org/model/content/1.0'
>and qn.local_name = 'content';
>{% endhighlight %}

>Java
>{:.filename}
>{% highlight java %}
>private String getToken(HttpClient client) throws UnsupportedEncodingException{
>Cookie[] cookies = client.getState().getCookies();
>for (Cookie cookie : cookies){
>if (cookie.getName().equals("Alfresco-CSRFToken")){
>return URLDecoder.decode(cookie.getValue(), "UTF-8");
>}
>}
>return null;
>}
>{% endhighlight %}

To add name to the code snippet, as in the examples above, add following construction before the snippet:

{% highlight bash %}
{% raw %}

>Java
>{:.filename}
>{% highlight java %}
>...
>{% endraw %}
>{% endhighlight %}

## Jekyll Dark Clean Theme

Here is a sample post for Jekyll-Clean-Dark theme. 

* get it from [github](https://github.com/streetturtle/jekyll-clean-dark)
* see the [live demo](http://pavelmakhov.com/jekyll-clean-dark)
* see it [in action on my blog](http://pavelmakhov.com)

This theme was created on top of [Jekyll Clean theme](https://scotte.github.io) by Scotte.

This theme uses some parts of Twitter Bootstrap, which allows it looks nice on a mobile devices using a collapsable nav bar and hiding the sidebar.

Here how it looks like on some portable devices:

![My helpful screenshot](E:\github\blog\_posts\{{ '\assets\images\iphone_portrait.PNG' | relative_url }}){: .center-image }*iPhone 5 portrait*

![My helpful screenshot](E:\github\blog\_posts\{{ '\assets\images\iphone_landscape.PNG' | relative_url }}){: .center-image }*iPhone 5 landscape*

![My helpful screenshot](E:\github\blog\_posts\{{ '\assets\images\ipad_portrait.PNG' | relative_url }}){: .center-image }*iPad mini portrait*

![My helpful screenshot](E:\github\blog\_posts\{{ '\assets\images\ipad_landscape.PNG' | relative_url }}){: .center-image }*iPad mini landscape*

## Table styles

Below are the examples of the default table styling.

### Simple table

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |

>Markdown
>{:.filename}
>{% highlight raw %}

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |
| {% endhighlight %}          |                              |

### Custom styles

It is also possible to change a bit table styles by applying CSS classes. By default there are two classes available:

 - `.wide` - makes table width 100%

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |
| {:.wide}                    |                              |

>Markdown - note the last line
>{:.filename}
>{% highlight markdown %}

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |
| {:.wide}                    |                              |
| {% endhighlight %}          |                              |

 - `.inner-borders` - shows inner borders

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |
| {:.inner-borders}           |                              |

>Markdown - note the last line
>{:.filename}
>{% highlight raw %}

| First Header                | Second Header                |
| --------------------------- | ---------------------------- |
| Content from cell 1         | Content from cell 2          |
| Content in the first column | Content in the second column |
| {:.inner-borders}           |                              |
| {% endhighlight %}          |                              |

You can add more such classes by putting them inside **theme.scss**. Here is how the above mentioned classes are defined:

{% highlight scss %}
table.wide {
  width: 100%;
  max-width: 100%;
}

table.inner-borders {
  border-collapse: collapse;
  border-style: hidden;
  td {
    border: 1px solid #5e5e5e;
  }
}
{% endhighlight %}


### Few more examples from kramdown [documentation](https://kramdown.gettalong.org/syntax.html#tables):

|-----------------+------------+-----------------+----------------|

| Default aligned                                              | Left aligned | Center aligned | Right aligned |
| ------------------------------------------------------------ | :----------- | :------------: | ------------: |
| First body part                                              | Second cell  |   Third cell   |   fourth cell |
| Second line                                                  | foo          |   **strong**   |           baz |
| Third line                                                   | quux         |      baz       |           bar |
| -----------------+------------+-----------------+---------------- |              |                |               |
| Second body                                                  |              |                |               |
| 2 line                                                       |              |                |               |
| =================+============+=================+================ |              |                |               |
| Footer row                                                   |              |                |               |
| -----------------+------------+-----------------+---------------- |              |                |               |

>Table header row, two table bodies and a table footer row
>{:.filename}
>{% highlight raw %}
>|-----------------+------------+-----------------+----------------|
>
>| Default aligned                                              | Left aligned | Center aligned | Right aligned |
>| ------------------------------------------------------------ | :----------- | :------------: | ------------: |
>| First body part                                              | Second cell  |   Third cell   |   fourth cell |
>| Second line                                                  | foo          |   **strong**   |           baz |
>| Third line                                                   | quux         |      baz       |           bar |
>| -----------------+------------+-----------------+---------------- |              |                |               |
>| Second body                                                  |              |                |               |
>| 2 line                                                       |              |                |               |
>| =================+============+=================+================ |              |                |               |
>| Footer row                                                   |              |                |               |
>| -----------------+------------+-----------------+---------------- |              |                |               |
>| {% endhighlight %}                                           |              |                |               |

---

|---

| Default aligned | Left aligned | Center aligned | Right aligned |
| --------------- | :----------- | :------------: | ------------: |
| First body part | Second cell  |   Third cell   |   fourth cell |
| Second line     | foo          |   **strong**   |           baz |
| Third line      | quux         |      baz       |           bar |
| ---             |              |                |               |
| Second body     |              |                |               |
| 2 line          |              |                |               |
| ===             |              |                |               |
| Footer row      |              |                |               |

>Same as above but shorter
>{:.filename}
>{% highlight raw %}
>|---

| Default aligned    | Left aligned | Center aligned | Right aligned |
| ------------------ | :----------- | :------------: | ------------: |
| First body part    | Second cell  |   Third cell   |   fourth cell |
| Second line        | foo          |   **strong**   |           baz |
| Third line         | quux         |      baz       |           bar |
| ---                |              |                |               |
| Second body        |              |                |               |
| 2 line             |              |                |               |
| ===                |              |                |               |
| Footer row         |              |                |               |
| {% endhighlight %} |              |                |               |

## Table of content

Above you can see how it looks like. 

To enable it add a `toc` variable to the front matter of your post:

{% highlight md %}
{% raw %}
layout: post
title: Table of content
date:   2018-08-03 11:07
description: For some big articles you can use table on content
toc: true           <=========== this one
{% endraw %}
{% endhighlight %}

You can also customize it by styling `.toc` class in **theme.scss** 

This solution is based on [github.com/allejo/jekyll-toc](https://github.com/allejo/jekyll-toc).

### Some random text

Moments its musical age explain. But extremity sex now education concluded earnestly her continual. Oh furniture acuteness suspected continual ye something frankness. Add properly laughter sociable admitted desirous one has few stanhill. Opinion regular in perhaps another enjoyed no engaged he at. It conveying he continual ye suspected as necessary. Separate met packages shy for kindness. 

#### Second level random text

Boy favourable day can introduced sentiments entreaties. Noisier carried of in warrant because. So mr plate seems cause chief widen first. Two differed husbands met screened his. Bed was form wife out ask draw. Wholly coming at we no enable. Offending sir delivered questions now new met. Acceptance she interested new boisterous day discretion celebrated. 

#### Another second level random text

Both rest of know draw fond post as. It agreement defective to excellent. Feebly do engage of narrow. Extensive repulsive belonging depending if promotion be zealously as. Preference inquietude ask now are dispatched led appearance. Small meant in so doubt hopes. Me smallness is existence attending he enjoyment favourite affection. Delivered is to ye belonging enjoyment preferred. Astonished and acceptance men two discretion. Law education recommend did objection how old. 

##### Third level text

How promotion excellent curiosity yet attempted happiness. Gay prosperous impression had conviction. For every delay death ask style. Me mean able my by in they. Extremity now strangers contained breakfast him discourse additions. Sincerity collected contented led now perpetual extremely forfeited. 

### Some more random text

Over fact all son tell this any his. No insisted confined of weddings to returned to debating rendered. Keeps order fully so do party means young. Table nay him jokes quick. In felicity up to graceful mistaken horrible consider. Abode never think to at. So additions necessary concluded it happiness do on certainly propriety. On in green taken do offer witty of. 

#### Second level random text

Received overcame oh sensible so at an. Formed do change merely to county it. Am separate contempt domestic to to oh. On relation my so addition branched. Put hearing cottage she norland letters equally prepare too. Replied exposed savings he no viewing as up. Soon body add him hill. No father living really people estate if. Mistake do produce beloved demesne if am pursuit. 

#### Another second level random text

Her old collecting she considered discovered. So at parties he warrant oh staying. Square new horses and put better end. Sincerity collected happiness do is contented. Sigh ever way now many. Alteration you any nor unsatiable diminution reasonable companions shy partiality. Leaf by left deal mile oh if easy. Added woman first get led joy not early jokes. 

#### And one more

It allowance prevailed enjoyment in it. Calling observe for who pressed raising his. Can connection instrument astonished unaffected his motionless preference. Announcing say boy precaution unaffected difficulty alteration him. Above be would at so going heard. Engaged at village at am equally proceed. Settle nay length almost ham direct extent. Agreement for listening remainder get attention law acuteness day. Now whatever surprise resolved elegance indulged own way outlived. 
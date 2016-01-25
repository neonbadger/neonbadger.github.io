---
layout: post
title: "Blog Guide"
excerpt: "How to write blog post."
modified: 2016-01-18
categories: articles
tags: [sample-post, test, image]
image:
  feature: so-simple-sample-image-1.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
link: http://mademistakes.com
comments: true
share: true
---

`_posts` directory - edit this post and re-build (or run with the `-w` switch) to see your changes!

To add new posts, simply add a file in the `_posts` directory that follows the convention: YYYY-MM-DD-name-of-post.ext.

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### Body text


### Blockquotes

> Lorem ipsum dolor sit amet.

### Emphasis

`This is a highlight`

**This is strong**.

*This is emphasized*.

Water is H<sub>2</sub>O.

The New York Times <cite>(That’s a citation)</cite>.

<u>Underline</u>.

[FitVids](http://fitvidsjs.com/)

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll]:    http://jekyllrb.com


**link posts**, made famous by John Gruber. To activate just add `link: http://url-you-want-linked` to the post's YAML front matter and you're done.

Footnote place.[^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>


button link

<a markdown="0" href="{{ site.url }}/theme-setup" class="btn">Install So Simple Theme</a>
f

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3   |
{: .table}

## Buttons

Make any link standout more when applying the `.btn` class.

<div markdown="0"><a href="http://mademistakes.com" class="btn">This is a button</a></div>


## Images

![Smithsonian Image]({{ site.url }}/images/3953273590_704e3899d5_m.jpg)
{: .pull-right}

## 

## Figures (for images or video)

If you want to display two or three images next to each other responsively use `figure` with the appropriate `class`.

Each instance of `figure` is auto-numbered and displayed in the caption.

### One Up

<figure>
    <a href="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_b.jpg"><img src="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg" alt="image"></a>
    <figcaption><a href="http://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>

### Two Up

Apply the `half` class like so to display two images side by side that share the same caption.

{% highlight html %}
<figure class="half">
    <img src="/images/image-filename-1.jpg" alt="image">
    <img src="/images/image-filename-2.jpg" alt="image">
    <figcaption>Caption describing these two images.</figcaption>
</figure>
{% endhighlight %}

### Three Up

Apply the `third` class like so to display three images side by side that share the same caption.

{% highlight html %}
<figure class="third">
    <a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg" alt="image"></a>
    <a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg" alt="image"></a>
    <a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg" alt="image"></a>
    <figcaption>Caption describing these three images.</figcaption>
</figure>
{% endhighlight %}

## Video

<iframe width="560" height="315" src="//www.youtube.com/embed/pdSp4Y4GOQs" frameborder="0"> </iframe>

### Youtube

To fix add a space between the `<iframe>` tags and remove `allowfullscreen`. Example below:

{% highlight html %}
<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>
{% endhighlight %}

### Vimeo

And here's a Vimeo embed for testing purposes.

<iframe src="//player.vimeo.com/video/98146708?title=0&amp;byline=0" width="500" height="281" frameborder="0"> </iframe>



## Code Snippets

Syntax highlighting via Pygments and Rouge.
To modify styling and highlight colors edit `/_sass/_syntax.scss`.

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

{% highlight html %}
{% raw %}
<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->
{% endraw %}
{% endhighlight %}


{% highlight ruby %}
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
{% endhighlight %}



Non Pygments/Rouge code example

    <div id="awesome">
        <p>This is great isn't it?</p>
    </div>

### Standard Code Block

    {% raw %}
    <nav class="pagination" role="navigation">
        {% if page.previous %}
            <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
        {% endif %}
        {% if page.next %}
            <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
        {% endif %}
    </nav><!-- /.pagination -->
    {% endraw %}

### Fenced Code Blocks ~~~

To modify styling and highlight colors edit `/_sass/_coderay.scss`. Line numbers and a few other things can be modified in `_config.yml`. Consult [Jekyll's documentation](http://jekyllrb.com/docs/configuration/) for more information.

~~~ css
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
~~~

~~~ html
{% raw %}<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->{% endraw %}
~~~

~~~ ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
~~~

### Override Author Byline Test

Start by modifying or creating a new `authors.yml` file in the `_data` folder and add your authors using the following format.

{% highlight yaml %}
# Authors

billy_rick:
  name: Billy Rick
  web: http://thewhip.com
  email: billy@rick.com
  bio: "What do you want, jewels? I am a very extravagant man."
  avatar: bio-photo-2.jpg
  twitter: extravagantman
  google:
    plus: BillyRick

cornelius_fiddlebone:
  name: Cornelius Fiddlebone
  email: cornelius@thewhip.com
  bio: "I ordered what?"
  avatar: bio-photo.jpg
  twitter: rhymeswithsackit
  google:
    plus: CorneliusFiddlebone
{% endhighlight %}

To assign Billy Rick as an author for our post. You'd add the following YAML front matter to a post:

{% highlight yaml %}
author: billy_rick
{% endhighlight %}

### MathJax

[MathJax](http://www.mathjax.org/) is a simple way of including Tex/LaTex/MathML based mathematics in HTML webpages.

To get up and running you need to include the MathJax script in the header of your github pages page, and then write some maths. For LaTex, there are two delimiters you need to know about, one for block or displayed mathematics `\[ ... \]`, and the other for inline mathematics `\( ... \)`.

To enable MathJax support be sure Kramdown is your Markdown flavor of choice and MathJax is set to true in your `_config.yml` file.

~~~
markdown: kramdown
mathjax: true
~~~

~~~
Here is an example MathJax inline rendering \\( 1/x^{2} \\), and here is a block rendering: 
\\[ \frac{1}{n^{2}} \\]
~~~

The only thing to look out for is the escaping of the backslash when using markdown, so the delimiters become `\\[ ... \\]` and `\\( ... \\)` for inline and block maths respectively.

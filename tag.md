---
title: Tags
permalink: tag/
profile: false
---

<!-- Get the tag name for every tag on the site and set them
to the `site_tags` variable. -->
{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}

<!-- `tag_words` is a sorted array of the tag names. -->
{% assign tag_words = site_tags | split:',' | sort %}

<article class="post">
    <header>
        <h1>Tags</h1>
    </header>
  <!-- List of all tags -->
  <tag class="tag">
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tag_words[item] }}{% endcapture %}
        <a href="#{{ this_word | cgi_escape }}">#{{ this_word }}</a>
    {% endunless %}{% endfor %}
  </tag>
  <hr>
  <!-- Posts by Tag -->
  <div>
    {% for item in (0..site.tags.size) %}{% unless forloop.last %}
      {% capture this_word %}{{ tag_words[item] }}{% endcapture %}
      <h2 class="tag-title" id="{{ this_word | cgi_escape }}">#{{ this_word }}</h2>
      {% for post in site.tags[this_word] %}{% if post.title != null %}
        <div>
          <span style="float: left;">
            <a href="{{ post.url }}">{{ post.title }}</a>
          </span>
        </div>
        <div style="clear: both;margin-bottom:15px;"></div>
      {% endif %}{% endfor %}
      <div style="margin-bottom:40px;"></div>
    {% endunless %}{% endfor %}
  </div>
</article>

<footer id="post-meta" class="clearfix">
    <a href="/about">
        <img class="avatar" src="/assets/images/profile.png">
        <div>
            <span class="dark">Khoerodin</span>
            <span>Web developer</span>
        </div>
    </a>
    <section id="sharing">
        {% include share.html %}
    </section>
</footer>
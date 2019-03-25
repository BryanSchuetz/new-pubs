---
title: DEVELOPMENTS
publication: Developments
layout: default
---

<div class="home grid">
  {% assign currentPosts = site.posts | where_exp: "post", "post.publication == 'Developments'" %}
  {% assign posts = currentPosts | sort: 'date' | reverse %}
  {% for post in posts %}
  <div class="post grid-item {% for tag in post.tags %}{{ tag | slugify }} {% endfor %}">
    <a href="{{ post.url }}" class="no-style"><h1 class="post-title">{{ post.title }}</h1></a>
    <div class="post-details">
      <!-- <p class="post-details--date">{{ post.date | date: "%b %-d, %Y" }}</p>
      <p class="post-details--byline">{% if post.author %}By <a href="#" class="without-style">{{ post.author }}</a>{% endif %}</p> -->

      <p class="post-details--byline">By {{ post.author | markdownify | remove:"<p>" | remove:"</p>" }}</p>
      <p class="post-details--tags">Tags: {% for tag in post.tags %}<span class="post-topic"><a href="/tags/?tag={{ tag | downcase | split:' ' | join: '-'}}" class="without-style">{{ tag }}</a></span>{% unless forloop.last %} • {% endunless %}{% endfor %}</p>
    </div>
    {{ post.excerpt }}
    <p class="more"><a class="without-style more-button" href="{{ post.url }}"><svg class="svg-more" viewBox="0 0 157 157" preserveAspectRatio="xMinYMax meet"><use xlink:href="#more"></use></svg>READ MORE</a></p>
    {% unless forloop.last %}<hr>{% endunless %}
  </div>
  {% endfor %}
  <hr>
</div>

<script>
  $(window).load(function () {
  $('.grid').isotope({
    // options
    itemSelector: '.grid-item',
    layoutMode: 'vertical'
  });
  // init Isotope
  var $grid = $('.grid').isotope({
    // options
  });
  // filter items on button click
  $('.filter-button-group').on('click', 'button', function () {
    var filterValue = $(this).attr('data-filter');
    $grid.isotope({ filter: filterValue });
  });
  // change is-checked class on buttons
  $('.filter-button-group').each(function (i, buttonGroup) {
    var $buttonGroup = $(buttonGroup);
    $buttonGroup.on('click', 'button', function () {
      $buttonGroup.find('.is-checked').removeClass('is-checked');
      $(this).addClass('is-checked');
    });
  });
})
</script>
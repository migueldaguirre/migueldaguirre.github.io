---
title: Work
layout: empty
---

<html>
<head>
  <title>David Aguirre - Work</title>
  <meta charset='UTF-8'>
  <meta content='width=device-width, initial-scale=1' name='viewport'/>
  <meta name='description' content='David Aguirre is a Designer and Business Analyst'>
  <meta name='keywords' content='
  ux,
  it,
  business analysis,
  erp,
  ui,
  design thinking,
  prototyping,
  user research
  '>
  <meta name='author' content='David Aguirre'>
  <link rel="icon" type="image/png" href="/assets/img/favicon.png"/>
  <link rel='shortcut icon' href='/favicon.png?v=e' />
  <link href='/css/styles.css' rel='stylesheet'/>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700;1,900&display=swap" rel="stylesheet">
</head>
<body>
  <!-- {% include nav.html %} -->
  <div class='nav'>
    <ul class='wrap'>
      <span class="nav-name">DAVID AGUIRRE | BA & UX </span>
      <li><a id='about'  href='/'>About</a></li>
      <li><a id='work' class="selected" href='/work' >Work</a></li>
    </ul>
  </div>
  <div id='blog' class=''>
    <div id='intro'>
      <br>
    </div>
    <div id='posts' class='section mosaic-container'>
      {% for post in site.posts %}
        <a href="{{ post.url }}" style="text-decoration: none;">
      <div class='post-row' class="post-container {% if post.underconstruction == true %}under-construction{% endif %}">
          <img src="{{ post.thumbnail | prepend: '/assets/img/thumbnails/' | append: '.png' | relative_url }}" class="project-thumbnail">
          <div class="project-info-container">
            <div class="post-label">
              {{ post.keywords | upcase }}
            </div>
            <img src="{{post.client-logo}}" class="logo-thumbnail"><br>
            <h2 class='post-title'>
              {{ post.title }}
            </h2>
            <p class='post-subtitle'>
              {{ post.subtitle }}
            </p>
            <br>
            <p class='post-date'>
              {{ post.year}}
            </p>
          </div>
        </div>
      </a>
      <span class='hidden'>{{ forloop.index }}</span>
      {% endfor %}
    </div>
  </div>
</body>
</html>

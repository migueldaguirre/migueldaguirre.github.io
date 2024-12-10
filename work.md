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
  <link rel="apple-touch-icon" href="/assets/img/favicon.png">
  <link rel='shortcut icon' href='/assets/img/favicon.png' />
  <link href='/css/styles.css' rel='stylesheet'/>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;0,900;1,200;1,300;1,400;1,600;1,700;1,900&display=swap" rel="stylesheet">
  <link rel="apple-touch-icon" href="assets/img/favicon.png"/>
</head>
<body>
  <!-- {% include nav.html %} -->
  <div class='md-nav'>
    <ul class='wrap'>
      <li><a id='about'  href='/'>About</a></li>
      <li><a id='work' class="selected" href='/work' >Work</a></li>
    </ul>
  </div>
      <br>
<!--     <div id='intro' style="margin-left: auto; margin-right: auto; text-align:center; width: 100%;border: 1px solid gainsboro; color: var(--md-color); padding-top:1em; padding-bottom:1em; max-width:600px; border-radius: 5px; opacity: 40%">
<span>Content is under construction</span> (<span id="datetime"></span>) <br>
    </div> -->
  <div id='blog' class=''>
    <div id='posts' class='section mosaic-container'>
      {% for post in site.posts %}
        <a href="{{ post.url }}" style="text-decoration: none;">
      <div class='post-row' class="post-container {% if post.underconstruction == true %}under-construction{% endif %}">
          <div class="project-info-container">
            <div class="post-label">
              {{ post.keywords | upcase }}
            </div>
            <img src="{{post.client-logo}}" class="logo-thumbnail">
            <h2 class='post-title'>
              {{ post.title }}
            </h2>
            <p class='post-subtitle'>
              {{ post.subtitle }}
            </p>
            <p class='post-date'>
              {{ post.year}}
            </p>
            <img src="{{ post.thumbnail | prepend: '/assets/img/thumbnails/' | append: '.png' | relative_url }}" class="project-thumbnail">
          </div>
        </div>
      </a>
      <span class='hidden'>{{ forloop.index }}</span>
      {% endfor %}
    </div>
  </div>
</body>
<script>
var dt = new Date();
document.getElementById("datetime").innerHTML = dt.toLocaleDateString();
</script>
</html>

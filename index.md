---
layout: default
name: HOME
---
<main role="main">

  <!-- Main jumbotron for a primary marketing message or call to action -->
  <div class="jumbotron">
    <div class="container">
      <h1 class="display-3">{{ site.title }}</h1>
      <p>{{ site.intro }}</p>
    </div>
  </div>

  <div class="container">
    <div class="row">
    {% assign services = site.data.pagelist.pages | where: 'type', 'service' | sort: 'nav.order' %}  
    {% for item in services %}
      <div class="col-md-4">
        <h2>{{ item.title }}</h2>
        <p>{{ item.intro }}</p>
        <p><a class="btn btn-secondary" href="{{ item.nav.link }}" role="button">Read more &raquo;</a></p>
      </div>
    {% endfor %}
    </div>
    <hr>
  </div>
</main>
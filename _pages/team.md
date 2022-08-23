---
title: "Dupont Laboratory - Team"
layout: gridlay
excerpt: "Pediatric Cardiac Bioengineering Lab: Team members"
sitemap: false
permalink: /team/
---

### Group Members

 **We are  looking for new Postdocs to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


<!---Jump to [Director](#director), [postdocs](#fellows), [alumni](#alumni).--->

#### Director
{% assign number_printed = 0 %}
{% for member in site.data.director %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix" style="text-align: justify">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4><br>
   {{ member.info }}<br>
   <ins>Contact:</ins> <{{ member.email }}>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


#### Post-doctoral Research Fellows
{% assign number_printed = 0 %}
{% for member in site.data.fellows %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row align-items">
{% endif %}

  <div class="col-sm-6 clearfix" style="text-align: justify">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <ins>Interests:</ins>
  {{ member.interests }} 
  <br>
  <ins>Contact:</ins> <{{ member.email }}><br>
  <ins>Bio:</ins> {{ member.bio }} 
</div>
    
    {% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}


#### Alumni 
<div class="row" style="text-align: justify">
{% for member in site.data.alumni %}
{{ member.name }}
{% endfor %}
</div>

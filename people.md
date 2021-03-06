---
layout: default
title: People
description: Workshop folks
---

<style>
.img-holder {
  width: 20%;
  position: relative;
  min-width:100px;
  max-width:150px;
  padding: 10px;
}
.img-holder img {
  top: 0;
  left: 0;
}
</style>

{% assign mentors = site.data.people | where:'role', 'mentor' | sort: "nick" %}
{% assign participants = site.data.people | where:'role', 'participant' | sort: "nick" %}
{% assign friends = site.data.people | where:'role', 'other'  | sort: "nick" %}
{% assign shuffle = site.data.people | sample: 100 %}


<div style="display: flex; justify-content: center; flex-wrap: wrap; width: 100vw; margin-left: -50vw; left: 50%; position: relative;">
{% for person in shuffle %}

  <div class="img-holder">
    <a href="#{{person.github}}">
      <img src="{{ site.baseurl }}/assets/headshots/square-{{ person.github }}.png">
    </a>
  </div>
{% endfor %}
</div>

# Participants

![clouds]({{ site.baseurl }}/assets/gifcities-clouds.gif){:width="100%"}

{% for person in participants %}

<div style="display: flex; flex-wrap: wrap; justify-content: center;">

  <div class="img-holder">
    <img src="{{ site.baseurl }}/assets/headshots/square-{{ person.github }}.png">
  </div>

  <div style="padding-left: 10px; width: 80%; flex-grow: 1;">
    <span class="h3"> {{ person.nick }} </span>
    | {{ person.institution}}
    | <a name="{{ person.github }}" href="#{{ person.github }}">🔗</a>
    | <a href="https://github.com/{{ person.github }}">github</a>
    {% if person.twitter %}
    |  <a href="https://twitter.com/{{ person.twitter }}">twitter</a>
    {% endif %}
    {% if person.href %}
    |  <a href="{{ person.href }}">www</a>
    {% endif %}
    |
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl;"
      id="{{ person.github }}-show"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = 'initial'; document.getElementById('{{ person.github }}-hide').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = 'none';"
    > » </a>
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl; display:none;"
      id="{{ person.github }}-hide"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = '3em'; document.getElementById('{{ person.github }}-show').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = '';"
    > « </a>

    <blockquote id="{{ person.github }}-bio" style="max-height: 3em; overflow: hidden;">
    {{ person.bio }}
    </blockquote>
    <blockquote id="{{ person.github }}-ellipsis" style="margin-top: -1em;">
    ...
    </blockquote>
  </div>

</div>

{% endfor %}

# Mentors

![twisting]({{ site.baseurl }}/assets/gifcities-twist.gif){:width="100%"}

{% for person in mentors %}

<div style="display: flex; flex-wrap: wrap; justify-content: center;">

  <div class="img-holder">
    <img src="{{ site.baseurl }}/assets/headshots/square-{{ person.github }}.png">
  </div>

  <div style="padding-left: 10px; width: 80%; flex-grow: 1;">
    <span class="h3"> {{ person.nick }} </span>
    | {{ person.institution}}
    | <a name="{{ person.github }}" href="#{{ person.github }}">🔗</a>
    | <a href="https://github.com/{{ person.github }}">github</a>
    {% if person.twitter %}
    |  <a href="https://twitter.com/{{ person.twitter }}">twitter</a>
    {% endif %}
    {% if person.href %}
    |  <a href="{{ person.href }}">www</a>
    {% endif %}
    |
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl;"
      id="{{ person.github }}-show"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = 'initial'; document.getElementById('{{ person.github }}-hide').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = 'none';"
    > » </a>
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl; display:none;"
      id="{{ person.github }}-hide"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = '3em'; document.getElementById('{{ person.github }}-show').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = '';"
    > « </a>

    <blockquote id="{{ person.github }}-bio" style="max-height: 3em; overflow: hidden;">
    {{ person.bio }}
    </blockquote>
    <blockquote id="{{ person.github }}-ellipsis" style="margin-top: -1em;">
    ...
    </blockquote>
  </div>

</div>

{% endfor %}

# Friends

![sheep]({{ site.baseurl }}/assets/gifcities-sheep.gif){:width="100%"}

{% for person in friends %}

<div style="display: flex; flex-wrap: wrap; justify-content: center;">

  <div class="img-holder">
    <img src="{{ site.baseurl }}/assets/headshots/square-{{ person.github }}.png">
  </div>

  <div style="padding-left: 10px; width: 80%; flex-grow: 1;">
    <span class="h3"> {{ person.nick }} </span>
    | {{ person.institution}}
    | <a name="{{ person.github }}" href="#{{ person.github }}">🔗</a>
    | <a href="https://github.com/{{ person.github }}">github</a>
    {% if person.twitter %}
    |  <a href="https://twitter.com/{{ person.twitter }}">twitter</a>
    {% endif %}
    {% if person.href %}
    |  <a href="{{ person.href }}">www</a>
    {% endif %}
    |
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl;"
      id="{{ person.github }}-show"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = 'initial'; document.getElementById('{{ person.github }}-hide').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = 'none';"
    > » </a>
    <a
      href="javascript:;"
      style="writing-mode:vertical-rl; display:none;"
      id="{{ person.github }}-hide"
      onclick="this.style.display = 'none'; document.getElementById('{{ person.github }}-bio').style.maxHeight = '3em'; document.getElementById('{{ person.github }}-show').style.display = 'initial'; document.getElementById('{{ person.github }}-ellipsis').style.display = '';"
    > « </a>

    <blockquote id="{{ person.github }}-bio" style="max-height: 3em; overflow: hidden;">
    {{ person.bio }}
    </blockquote>
    <blockquote id="{{ person.github }}-ellipsis" style="margin-top: -1em;">
    ...
    </blockquote>
  </div>

</div>

{% endfor %}

---
layout: default
title: Home
---

Welcome! I’m **KC1ZTY**, an amateur-radio operator in the Boston area.

This site is where I document antenna builds, radio setup, measurements, operating experiences, and things I learn along the way.

## Latest posts

{% if site.posts.size > 0 %}

{% for post in site.posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %-d, %Y" }}*

{% if post.image %}
<a href="{{ post.url | relative_url }}" aria-label="Read {{ post.title | escape }}">
	<img src="{{ post.image | relative_url }}" alt="{{ post.image_alt | default: post.title | escape }}" loading="lazy" style="display: block; width: 100%; max-height: 360px; object-fit: cover; margin: 1rem 0; border-radius: 6px;">
</a>
{% endif %}

{{ post.excerpt }}

[Read the full post →]({{ post.url | relative_url }})

---

{% endfor %}

{% else %}

_No posts yet._

{% endif %}

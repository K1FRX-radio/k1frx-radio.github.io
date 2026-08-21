---
layout: default
title: Home
---

Welcome! I'm **K1FRX**, an amateur-radio operator in the Boston area.

This site is where I document antenna builds, radio setup, measurements, operating experiences, and things I learn along the way.

## Latest posts

{% if site.posts.size > 0 %}

{% for post in site.posts %}

<article>
	<h3 style="margin-top: 0;"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
	<p><em>{{ post.date | date: "%B %-d, %Y" }}</em></p>
	<div style="display: flex; align-items: flex-start; gap: 1.25rem;">
		<div style="flex: 1; min-width: 0;">
			{{ post.excerpt }}
			<p><a href="{{ post.url | relative_url }}">Read the full post →</a></p>
		</div>
		{% if post.image %}
		<a href="{{ post.url | relative_url }}" aria-label="Read {{ post.title | escape }}" style="flex: 0 0 180px;">
			<img src="{{ post.image | relative_url }}" alt="{{ post.image_alt | default: post.title | escape }}" loading="lazy" style="display: block; width: 180px; height: 120px; object-fit: cover; border-radius: 6px;">
		</a>
		{% endif %}
	</div>
</article>

---

{% endfor %}

{% else %}

_No posts yet._

{% endif %}

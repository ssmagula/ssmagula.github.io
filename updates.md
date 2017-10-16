---
layout: page
flytitle:
hed: Blog posts
dek: Notes and ideas about creativity, technology, and design
permalink: blog

---
<!-- SMAG displays recent posts   -->

<div class="container">
	{% for post in site.posts %}
	<div class="row">
		<div class="col-lg-3 col-lg-offset-2 col-md-3 col-md-offset-2">
		<a href="{{ post.url | relative_url }}">
			<img src=" {{ post.img-large | escape }} " class="img-responsive" style="margin-top:7px">
		</a>
		</div>
		<div class="col-lg-5 col-md-5 col-sm-10">
			<div class="flytitle" style="padding-bottom:10px; font-size:1.1em">
				{{ post.flytitle | escape }}
			</div>
			<a href="{{ post.url | relative_url }}">
				<span class="title h3">{{ post.title | escape }}</span>
			</a>
				<p style="font-size:1.1em">{{ post.content | strip_html | truncatewords: 28 }}</p>
				<span>
					{{ post.author | escape }}</span>, <span>{{ post.date | date: "%b %-d, %Y" }}
				</span>
			<hr>
		</div>
	</div>
	{% endfor %}
	<div class="team-member col-md-4 col-md-offset-4 text-center" style="margin-top:50px"> <!-- TODO: put this into stylesheet properly -->
		{% include social_buttons.html %}
		<div class="text-muted" style="margin-top: 20px">
		Subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a>
		</div>
	</div>
</div>
	




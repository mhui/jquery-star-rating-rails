jQuery Star Rating plugin for Rails
===

Simple integration of jQuery Star Rating plugin into the asset pipeline.

The original jQuery plugin is [http://www.fyneworks.com/jquery/star-rating/](http://www.fyneworks.com/jquery/star-rating/)

Install
---
Install with

	gem install jquery-star-rating-rails

or in your Gemfile

	gem 'jquery-star-rating-rails'

Requirements
---

Requires Rails 3.1 and higher

Usage
---

In your application.js javascript file include the following

//= require jquery-star-rating

//= require jquery.MetaData (If you want support for split/partial star ratings)

and in your application.css stylesheet

*= require jquery-star-rating

In your view (e.g. new.html.erb) add the "star" class to your radio buttons:
<%= f.label :rating, "Rating" %>

<%= f.radio_button :rating, "1", :class => "star" %>
<%= f.radio_button :rating, "2", :class => "star" %>
<%= f.radio_button :rating, "3", :class => "star" %>
<%= f.radio_button :rating, "4", :class => "star" %>
<%= f.radio_button :rating, "5", :class => "star" %>

or like this:

 <% (1..5).each do |i| %>
  	 <%= radio_button_tag(name, value, checked?, :class => "star") %>
 <% end %>

 <% (1..5).each do |i| %>
  	 <%= f.radio_button :rating, i, :class => "star" %>
 <% end %>

Changelog
---
#### v0.0.1

* NEW: added jquery star rating plugin, use `require jquery-star-rating` to require javascript and `require jquery-star-rating` to require stylesheet.

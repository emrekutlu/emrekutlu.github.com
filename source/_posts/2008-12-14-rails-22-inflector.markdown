---
layout: post
title: !binary |-
  UmFpbHMgMi4yICZhbXA7IEluZmxlY3Rvcg==
wordpress_id: 92
wordpress_url: !binary |-
  aHR0cDovL2l6emV0ZW1yZWt1dGx1LmNvbS9ibG9nLz9wPTky
date: 2008-12-14 22:14:52.000000000 +02:00
comments: true
---
If you have recently updated to Rails 2.2.2, you may encounter this error when you want to start your application:
<pre lang="bash">/.gem/ruby/1.8/gems/activesupport-2.2.2/lib/active_support/dependencies.rb:445:in
`load_missing_constant': uninitialized constant Inflector (NameError)</pre>
As I learned from <a href="http://paulsturgess.co.uk/articles/show/76-load_missing_constant-uninitialized-constant-inflector-when-upgrading-to-ruby-on-rails-222" target="_blank">Paul's post</a> usage of <code>Inflector</code> class is changed a bit. You can see the difference when you compare the inflections.rb files. Path of the file is <em>yourApp/config/initializers/inflections.rb</em>

inflections.rb (Rails 2.1.0)
<pre lang="ruby"> Inflector.inflections do |inflect|
  .
  .
  .
 end</pre>

inflections.rb (Rails 2.2.2)
<pre lang="ruby"> ActiveSupport::Inflector.inflections do |inflect|
  .
  .
  .
 end</pre>
In my situation changing <code>Inflector</code> to <code>ActiveSupport::Inflector</code> was enough to solve the problem.

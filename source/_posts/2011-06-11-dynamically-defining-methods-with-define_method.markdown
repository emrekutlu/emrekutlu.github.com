---
layout: post
title: !binary |-
  RHluYW1pY2FsbHkgRGVmaW5pbmcgTWV0aG9kcyB3aXRoIGRlZmluZV9tZXRo
  b2Q=
wordpress_id: 190
wordpress_url: !binary |-
  aHR0cDovL3JhaWxzdGljLmNvbS8/cD0xOTA=
date: 2011-06-11 02:08:08.000000000 +03:00
comments: true
---
If you have been hacking ruby for a while you should have heard that "Everything is an object". To understand this concept knowing what a <strong>singleton class</strong> is important. <a href="http://yehudakatz.com/2009/11/15/metaprogramming-in-ruby-its-all-about-the-self/" target="_blank">Yehuda Katz's post</a> is a good source for it.

My ruby version 1.9.2.

<script src="https://gist.github.com/1009449.js?file=ruby_version.bash"></script>

First I'm going to show you how to add methods to instances by using <code><strong>define_method</strong></code>.

<script src="https://gist.github.com/1009449.js?file=add_instance_methods.rb"></script>

You can also write an instance method to create instance methods. <code><strong>send</strong></code> must be used because <code><strong>define_method</strong></code> is private.

<script src="https://gist.github.com/1009449.js?file=add_instance_methods_by_instance_method.rb"></script>

Write a singleton method to create instance methods.

<script src="https://gist.github.com/1009449.js?file=add_instance_methods_by_singleton_method.rb"></script>

Now it is time to add singleton methods. When we call <code><strong>define_method</strong></code>, it creates an instance method. What we have to do is call <code><strong>define_method</strong></code> on class' singleton class.

Getting singleton class of a class:

<script src="https://gist.github.com/1009449.js?file=get_singleton_class.rb"></script>

First defining singleton method to create singleton methods.

<script src="https://gist.github.com/1009449.js?file=add_singleton_methods_by_singleton_method.rb"></script>

Then defining instance method to create singleton methods.

<script src="https://gist.github.com/1009449.js?file=add_singleton_methods_by_instance_method.rb"></script>

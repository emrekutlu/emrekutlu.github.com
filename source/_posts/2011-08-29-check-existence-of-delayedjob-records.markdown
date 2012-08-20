---
layout: post
title: !binary |-
  Q2hlY2sgRXhpc3RlbmNlIG9mIERlbGF5ZWRKb2IgUmVjb3Jkcw==
wordpress_id: 217
wordpress_url: !binary |-
  aHR0cDovL3JhaWxzdGljLmNvbS8/cD0yMTc=
date: 2011-08-29 03:23:19.000000000 +03:00
---
I'm using the collectiveidea fork of <a href="http://github.com/collectiveidea/delayed_job" target="_blank">DelayedJob</a>. There are two ways to create a DelayedJob record. First you can use the <code>delay</code> method.

<script src="https://gist.github.com/1177431.js?file=dj_delay.rb"></script>

Second way to create DelayedJob records is custom jobs.

<script src="https://gist.github.com/1177431.js?file=dj_custom_job.rb"></script>

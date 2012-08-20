---
layout: post
title: !binary |-
  VGlkYml0OiBDb252ZXJ0aW5nIFN0cmluZ3Mgd2l0aCBMaW5lIEZlZWQgdG8g
  QXJyYXk=
wordpress_id: 126
wordpress_url: !binary |-
  aHR0cDovL3JhaWxzdGljLmNvbS8/cD0xMjY=
date: 2009-01-21 10:08:02.000000000 +02:00
---
If you have trouble when converting string to array, check if your string includes any line feed (\n). Check how <code>Array("string")</code> behaves:
<pre lang="bash">irb(main):001:0> Array("izzet emre \nkutlu")
=> ["izzet emre \n", "kutlu"]
</pre>

This output is not what most of the people expected. Be careful!

---
layout: post
title: !binary |-
  TmVzdGVkIE9iamVjdCBGb3JtcyB3aXRoIGhhc19vbmUgUmVsYXRpb24=
wordpress_id: 138
wordpress_url: !binary |-
  aHR0cDovL3JhaWxzdGljLmNvbS8/cD0xMzg=
date: 2009-06-15 15:40:30.000000000 +03:00
---
Rails 2.3 has a good solution for multi model forms. But there is not much examples of  how to use<code> <strong>accepts_nested_attributes_for</strong></code> with <code><strong>has_one</strong></code> relation.

Assume that we have a Book model which has one Author.
<script src="http://snipt.net/embed/821f03288846297c2cf43c34766a38f7" type="text/javascript"><!--mce:0--></script><br />
<script src="http://snipt.net/embed/02bd92faa38aaa6cc0ea75e59937a1ef" type="text/javascript"><!--mce:1--></script>
<br />
Controller :<script src="http://snipt.net/embed/f0ef6bf2d1b0bc59796999ff717bf149" type="text/javascript"><!--mce:2--></script>
<br />
View:
<script src="http://snipt.net/embed/2b2d98bcfa219f53623aa6c1f1301a01" type="text/javascript"><!--mce:3--></script>
<br />
No special action is needed for <strong><code>create</code></strong> method of BooksController,  <strong>attr_accessible</strong> is not necessary for Book model. Just don't forget to add the second parameter (<strong><code>@book</code></strong>) of <strong><code>form_for</code></strong> and build your nested object (@book.build_author).

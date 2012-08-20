---
layout: post
title: !binary |-
  SG93IHRvIGNoZWNrIGlmIGEgZGl2IGV4aXN0cyBpbiByanM/
wordpress_id: 172
wordpress_url: !binary |-
  aHR0cDovL2l6emV0ZW1yZWt1dGx1LmNvbS9ibG9nLz9wPTM=
date: 2008-08-24 17:52:36.000000000 +03:00
---
<br />
<pre lang="html4strict" colla="+">
&lt;body&gt;
   &lt;div id='main'&gt;
      Main Div
   &lt;/div&gt;
&lt;/body&gt;
</pre>
<br />
<pre lang="ruby" colla="+">
render :update do |page|
   page << "if ($('main')){"
   page.replace_html 'main', :inline => 'Here it is'
   page << "}"
end
</pre>
This ruby code checks if there is a DOM object that its id = "main".
If there is then changes its content to "Here it is", if there is not do nothing.

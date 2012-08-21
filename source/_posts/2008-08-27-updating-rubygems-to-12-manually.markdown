---
layout: post
title: !binary |-
  VXBkYXRpbmcgUnVieUdlbXMgdG8gMS4yIChNYW51YWxseSk=
wordpress_id: 45
wordpress_url: !binary |-
  aHR0cDovL2l6emV0ZW1yZWt1dGx1LmNvbS9ibG9nLz9wPTQ1
date: 2008-08-27 12:34:50.000000000 +03:00
comments: true
---
<br />
This is what happened when I want to install rmagick gem.
<br />
<pre lang="bash" colla="+">
username@username-desktop:~$ sudo gem install rmagick
Bulk updating Gem source index for: http://gems.rubyforge.org/
ERROR:  could not find rmagick locally or in a repository
</pre>
<br />
What the hell...
After some googling I found that RubGems 1.1.x is buggy and and update to RubyGems 1.2 is necessary.
To learn your RubyGems version:
<br />
<pre lang="bash" colla="+">
username@username-desktop:~$ gem -v
1.1.0
</pre>
<!--more-->
 I try to update RubyGems :
<br />
<pre lang="bash" colla="+">
username@username-desktop:~$ sudo gem update --system
Updating RubyGems
Bulk updating Gem source index for: http://gems.rubyforge.org/
Nothing to update
</pre>
<br />
After this failed attempt, I realized that RubyGems 1.1.x is really buggy. So I must go on manually to update RubyGems.
<br />
<strong>Now the solution:</strong>
<br />
<ol>
<li>
Download <a href="http://rubyforge.org/frs/download.php/38844/rubygems-update-1.2.0.gem">rubygems-update-1.2.0.gem</a>
</li>
<li>
Change your directory where your downloaded gem is. In these example my gem is at Desktop.
Now you must install <em>rubygems-update-1.2.0.gem</em>.
<pre lang="bash" colla="+">
username@username-desktop:~$ cd Desktop/
username@username-desktop:~/Desktop$ sudo gem install rubygems-update-1.2.0.gem
</pre>
</li>
<li>
<pre lang="bash" colla="+">
username@username-desktop:~$sudo update_rubygems
</pre>
</li>
</ol>
<br />
To check if our process is successful :
<br />
<pre lang="bash" colla="+">
username@username-desktop:~$gem -v
1.2.0
</pre>
<br />
If you see <em>1.2.0</em>, you did it.

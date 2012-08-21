---
layout: post
title: !binary |-
  UmVjdXJzaXZlIG1ldGhvZHMgd2l0aCBibG9jayBpbiBSdWJ5
wordpress_id: 20
wordpress_url: !binary |-
  aHR0cDovL2l6emV0ZW1yZWt1dGx1LmNvbS9ibG9nLz9wPTIw
date: 2008-08-26 10:46:17.000000000 +03:00
comments: true
---
<br />
<pre lang="ruby" colla="+">
def comic(cast)
   cast.each do |character|
      unless character.is_a?(Array)
         yield(character)
      else
	 comic(character) {|x| yield x}
      end
   end
end
</pre>
<br />
This method takes an array as argument and checks each element if it is an <em>Array</em>.
If the element is not an <em>Array</em> then the block is called.
If the element is an <em>Array</em> then the same method is called with that element as an argument and with the same block.
<br />
Now let's look how we can call this method.
<pre lang="ruby" colla="+">
names = ['lucky luke', 'jolly jumper', 'rin tin tin', ['joe', 'william','jack', 'averell']]
comic(names) {|c| puts c}
</pre>
<br />
<strong>Output :</strong>
<pre lang="bash">
lucky luke
jolly jumper
rin tin tin
joe
william
jack
averell
</pre>

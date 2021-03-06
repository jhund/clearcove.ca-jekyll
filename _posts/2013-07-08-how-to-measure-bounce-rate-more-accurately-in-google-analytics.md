---
title: How to measure Bounce Rate more accurately in Google Analytics
author: jhund
layout: post
permalink: /2013/07/how-to-measure-bounce-rate-more-accurately-in-google-analytics/
categories:
  - Blog
---
<p class="iii-article-excerpt">
  This Google article explains how to measure Bounce Rate more accurately by adding an event that gets fired after, e.g., 15 seconds on page. Any visit during which this event gets fired is not considered a bounce. No additional setup required.
</p>

<p class="iii-article-excerpt">
  Here is the code (setTimeout):
</p>

<pre>&lt;script type="text/javascript"&gt;
&nbsp; var _gaq = _gaq || [];
&nbsp; _gaq.push(['_setAccount', 'UA-XXXXXXX-1']);
&nbsp; _gaq.push(['_trackPageview']);
&nbsp; setTimeout("_gaq.push(['_trackEvent', '15_seconds', 'read'])",15000);
&nbsp;
&nbsp; (function() {
&nbsp; &nbsp; var ga = document.createElement('script'); 
&nbsp; &nbsp; ga.type = 'text/javascript'; ga.async = true;
&nbsp; &nbsp; ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
&nbsp; &nbsp; var s = document.getElementsByTagName('script')[0]; 
&nbsp; &nbsp; s.parentNode.insertBefore(ga, s);
&nbsp; })();
&lt;/script&gt;</pre>

<p class="iii-article-source">
  Link: <a href="http://analytics.blogspot.ca/2012/07/tracking-adjusted-bounce-rate-in-google.html">Tracking Adjusted Bounce Rate In Google Analytics &#8211; Analytics Blog</a> via analytics.blogspot.ca
</p>
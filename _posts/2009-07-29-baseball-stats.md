---
id: 143
title: Baseball Stats
date: 2009-07-29T13:40:29+00:00
author: tom_schenk
layout: post
guid: http://tomschenkjr.net/?p=143
permalink: /blog/baseball-stats/
tagazine-media:
  - 'a:7:{s:7:"primary";s:42:"http://a.espncdn.com/i/mlb/start_pitch.jpg";s:6:"images";a:2:{s:42:"http://a.espncdn.com/i/mlb/start_pitch.jpg";a:6:{s:8:"file_url";s:42:"http://a.espncdn.com/i/mlb/start_pitch.jpg";s:5:"width";s:3:"576";s:6:"height";s:3:"324";s:4:"type";s:5:"image";s:4:"area";s:6:"186624";s:9:"file_path";s:0:"";}s:44:"http://a.espncdn.com/i/mlb/highest_pitch.jpg";a:6:{s:8:"file_url";s:44:"http://a.espncdn.com/i/mlb/highest_pitch.jpg";s:5:"width";s:3:"576";s:6:"height";s:3:"324";s:4:"type";s:5:"image";s:4:"area";s:6:"186624";s:9:"file_path";s:0:"";}}s:6:"videos";a:0:{}s:11:"image_count";s:1:"2";s:6:"author";s:6:"176156";s:7:"blog_id";s:7:"8375094";s:9:"mod_stamp";s:19:"2009-07-29 18:40:29";}'
categories:
  - Data Visualization
tags:
  - baseball
  - Data Visualization
---
<a href="http://sports.espn.go.com/mlb/columns/story?columnist=kurkjian_tim&amp;id=4359938" target="_blank">ESPN's interesting article on pitch count</a> also contained some ugly graphs. The articles thesis is on starting pitchers now regularly pitching fewer than 100 pitches.

<strong>Exhibit 1: Transparency and Area Charts</strong>
<p style="text-align:left;"><strong><a href="http://a.espncdn.com/i/mlb/start_pitch.jpg"><img class="aligncenter" title="Starters Pitch Count" src="http://a.espncdn.com/i/mlb/start_pitch.jpg" alt="" width="576" height="324" /></a></strong></p>
<p style="text-align:left;">Area plots don't work well when they overlap. The above chart had to use transparency, which makes it difficult to associate colors with the key.</p>
<p style="text-align:left;">Also, ESPN appears to have plotted everything available instead of focusing on their argument. The overall point is to show how the number of pitches for starters--especially those with more than 100 pitches--has declined. It would be cleaner if they plotted what they wanted to show: the percentage of starts that ended up with more than 100 pitches.</p>
<p style="text-align:left;"><strong>Exhibit 2: The Descending Axis</strong></p>
<p style="text-align:left;"><strong><a href="http://a.espncdn.com/i/mlb/highest_pitch.jpg"><img class="aligncenter" title="Highest Pitch Count: 1988 - July 29, 2009" src="http://a.espncdn.com/i/mlb/highest_pitch.jpg" alt="" width="576" height="324" /></a></strong></p>
<p style="text-align:left;"></p>
<p style="text-align:left;">Two errors were made on exhibit 2. First, the x-axis (horizontal) starts at 2009 and goes back to 1988. It caught me by surprise since the slope was opposite of the argument of the article (positive instead of negative). Instead of glancing to get the idea, it wasn't until I read the axis that I understood the odd plotting behavior. In the end a simple rule: the x- and y-axis should always start at the lowest number and continue to ascend.</p>
<p style="text-align:left;">Second, the <a href="http://junkcharts.typepad.com/junk_charts/axis/" target="_blank">oft-made</a> mistake by not starting the axis at the appropriate spot (either 0 or 100 in this case). While 100 would make sense as the beginning of the y-axis (vertical), I would still prefer zero to maintain the appropriate scale. Using a scale greater than zero will over-emphasize the movement and make troughs or peaks appear significant while they usually are not.</p>
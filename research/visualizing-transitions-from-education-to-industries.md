---
id: 98
title: Visualizing Transitions from Education to Industries
date: 2009-07-05T20:48:35+00:00
author: Tom
layout: page
guid: http://tomschenkjr.net/?page_id=98
superawesome:
  - 'false'
---
<a href="http://tomschenkjr.net/workforcetransitions/"><img class="aligncenter size-full wp-image-1619" title="Interactive Transitions Preview" src="http://tomschenkjr.net/wordpress/wp-content/uploads/2009/07/Interactive-Transitions-Preview.png" alt="Visualization Transitions into the Workforce" width="600" height="278" /></a>

A common question is whether college graduates are employed in sectors related to their major. The poster (click on the image) shows the transitions from community college "career clusters" to one of the 20 industrial sectors.

<strong>Posts &amp; Publications</strong>
<ul>
	<li>Schenk, T. (2011, November) <a href="http://www3.airweb.org/images/irapps32.pdf">Measuring Transitions Into the Workforce as a Form of Accountability</a>. <em>IR Applications </em>32(18)</li>
	<li>Working Paper: <em><a href="http://tomschenkjr.net/wordpress/wp-content/uploads/2011/02/measuring-transitions-into-the-workforce-as-a-form-of-accountability.pdf">Measuring Transitions into the Workforce as a Form of Accountability</a> </em>(2.17.11)<em></em></li>
	<li><a href="http://tomschenkjr.net/workforcetransitions/">Interactive Webpage</a> (9.9.2012)</li>
	<li><em><a href="http://tomschenkjr.net/2009/10/21/visualizing-transitions-into-the-workforce/">Poster on tomschenkjr.net</a> (8.16.09)</em></li>
	<li><em>Annual Condition of Iowa's Community Colleges 2009</em> Special Supplement (1.15.10)</li>
	<li><a href="http://tomschenkjr.net/2010/01/03/preview-from-major-to-targeted-clusters/">Transitions into Iowa's Targeted Clusters</a> (1.3.10)</li>
	<li><a href="http://tomschenkjr.net/2009/11/25/visualizing-transitions-into-the-workforce-presentation/">Presentation to MidAIR</a> (11.25.09)</li>
</ul>
<strong>Creating the Diagram - Source Code</strong>

Some source materials related to the visualization of Iowa's community college graduates from majors to industries. This project uses <a href="http://mkweb.bcgsc.ca/circos/">Circos</a>, however, we <em>do not</em> use Circos' tableviewer. Instead, we transform the data from tables into appropriate "karyotype" files. I wrote a script in R to rotate the data from a pivot table to a karyotype file. Below is the the script, but the most-recent version can always be grabbed from its <a href="https://github.com/tomschenkjr/circosRearrange">github page</a>.

[sourcecode language="R"]
#CIRCOS REARRANGE
#REARRANGES A CROSS TABULATION OF CIP-TO-NAICS CODES INTO AN APPROPRIATE SEGDUP FILE FOR CIRCOS.
#LAST MODIFIED: 1/3/09 BY TOM SCHENK JR.
#DISTRIBUTED UNDER GNU-GPL 2.0, see http://creativecommons.org/licenses/GPL/2.0/
#REPOSITORY: https://github.com/tomschenkjr/circosRearrange
xtab &amp;lt;- read.csv(file.choose())
circosRearrange(xtab)
xtab &amp;lt;- matrix(1:12, ncol=4)
xtab &amp;lt;- matrix(1:8, ncol=4)

circosRearrange &amp;lt;- function(xtab){
#CAREER CLUSTERS - START POINTS
segdup.start.cc &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]-1
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(i in 1:height){
if(xtab[i,1] == 0)
1
else
{segdup.start.cc[stop_j] &amp;lt;- 1; stop_j &amp;lt;- stop_j + 1}

for(j in 1:width){
if(xtab[i,j+1] == 0)
next
else
{segdup.start.cc[stop_j] &amp;lt;- sum(xtab[i,1:j]) + 1; stop_j &amp;lt;- stop_j + 1}
}
}
#CAREER CLUSTERS - END POINTS
segdup.end.cc &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(i in 1:height){
for(j in 1:width){
if(xtab[i,j] == 0)
next
else
{segdup.end.cc[stop_j] &amp;lt;- sum(xtab[i,1:j]); stop_j &amp;lt;- stop_j + 1}
}
}
#NAIC CODES - START POINTS
segdup.start.ic &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(k in 1:width){
if(xtab[1,k] == 0)
1
else
{segdup.start.ic[stop_j] &amp;lt;- 1; stop_j &amp;lt;- stop_j + 1}
}
stop_j &amp;lt;- length(segdup.start.ic) + 1
for(i in 2:height){
for(j in 1:width){
if(xtab[i,j] == 0)
1
else
{segdup.start.ic[stop_j] &amp;lt;- sum(xtab[1:i-1,j]) + 1; stop_j &amp;lt;- stop_j + 1}
}
}
#NAIC CODES - END POINTS
segdup.end.ic &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(i in 1:height){
for(j in 1:width){
if(xtab[i,j] == 0)
1
else
{segdup.end.ic[stop_j] &amp;lt;- sum(xtab[1:i,j]); stop_j &amp;lt;- stop_j + 1}
}
}
#CREATE CAREER CLUSTER ID'S
career.clusters &amp;lt;- c(&quot;cc1&quot;, &quot;cc2&quot;, &quot;cc3&quot;, &quot;cc4&quot;, &quot;cc5&quot;, &quot;cc6&quot;, &quot;cc7&quot;, &quot;cc8&quot;, &quot;cc9&quot;, &quot;cc10&quot;, &quot;cc11&quot;, &quot;cc12&quot;, &quot;cc13&quot;, &quot;cc14&quot;, &quot;cc15&quot;, &quot;cc16&quot;, &quot;cc99&quot;)
cc.col &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]-1
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(i in 1:height){
if(xtab[i,1] == 0)
1
else
{cc.col[stop_j] &amp;lt;- career.clusters[i]; stop_j &amp;lt;- stop_j + 1}

for(j in 1:width){
if(xtab[i,j+1] == 0)
next
else
{cc.col[stop_j] &amp;lt;- career.clusters[i]; stop_j &amp;lt;- stop_j + 1}
}
}

#CREATE NAICS ID'S
twodigit.naics &amp;lt;- c(&quot;ic1&quot;, &quot;ic2&quot;, &quot;ic3&quot;)
ic.col &amp;lt;- 0
width &amp;lt;- dim(xtab)[2]
height &amp;lt;- dim(xtab)[1]
stop_j &amp;lt;- 1
for(i in 1:height){
for(j in 1:width){
if(xtab[i,j] == 0)
1
else
{ic.col[stop_j] &amp;lt;- twodigit.naics[j]; stop_j &amp;lt;- stop_j + 1}
}
}

segdup.start.cc &amp;lt;- matrix(segdup.start.cc, ncol=1)
segdup.end.cc &amp;lt;- matrix(segdup.end.cc, ncol=1)
segdup.start.ic &amp;lt;- matrix(segdup.start.ic, ncol=1)
segdup.end.ic &amp;lt;- matrix(segdup.end.ic, ncol=1)

segdup.cc &amp;lt;- cbind(1:dim(segdup.start.cc)[1], cc.col, segdup.start.cc, segdup.end.cc)
segdup.ic &amp;lt;- cbind(1:dim(segdup.start.ic)[1], ic.col, segdup.start.ic, segdup.end.ic)
segdup &amp;lt;- cbind(segdup.cc, segdup.ic)
write.csv(segdup)
}
[/sourcecode]
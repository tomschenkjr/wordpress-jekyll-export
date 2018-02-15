---
id: 61
title: Indexes
date: 2009-06-30T00:34:26+00:00
author: Tom
layout: page
guid: http://tomschenkjr.net/?page_id=61
---
<strong>Slide Show:</strong> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/index.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/index.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/index.tex">Source File (.tex)</a>
<strong>Lecture Notes:</strong> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/indexnote.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/indexNote.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/intermediate/indexing/index/indexnote.tex">Source File (.tex)</a>
<strong>Supplemental Docs</strong>
<ul>
	<li><em>Not So Short Introduction to L<sup>A</sup>T<sub>E</sub>X</em> § 4.3: 70-71 <a href="http://dl.dropbox.com/u/3194367/lshort.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/lshort.dvi">DVI</a> <a href="http://dl.dropbox.com/u/3194367/lshort.ps">PostScript</a></li>
	<li><a href="http://ils.lib.drake.edu/uhtbin/cgisirsi/YAWOIhLcH9/COWLES/184510008/5/0"><em>Digital Typography Using L<sup>A</sup>T<sub>E</sub>X</em></a> (Access to Drake's ebrary required)</li>
</ul>
Topics covered in this slide:
<ul>
	<li> Introducting the <span style="font-family:courier;">makeidx</span> package.</li>
	<li> Creating index points and the index.</li>
	<li> Parent-child index entries.</li>
</ul>
Along with the table of contents and bibliographies, creating indexes is simple. Normally indexing would require the author to keep track of certain words and pages they are written. To create an index in L<sup>A</sup>T<sub>E</sub>X we need to use the <span style="font-family:courier;">makeidx</span> package. Also, we need to place <span style="font-family:courier;">\makeindex</span> in the preamble. To create actual points we want in the index, we use <span style="font-family:courier;">\index{<em>key</em>}</span> immediately after the word we're referencing, where <em>key</em> is the word or phrase we want to use in the index. We can create parent-child relationships using <span style="font-family:courier;">\index{<em>key</em>!<em>sub-key</em>}</span>.

This slide show should take 5 to 15 minutes.
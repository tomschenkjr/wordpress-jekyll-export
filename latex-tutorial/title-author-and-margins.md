---
id: 37
title: Title, Author, and Margins
date: 2009-06-30T00:24:13+00:00
author: Tom
layout: page
guid: http://tomschenkjr.net/?page_id=37
---
<strong>Slide Show:</strong> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/title.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/title.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/title.tex">Source File (.tex)</a>
<strong>Lecture Notes:</strong> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/titlenote.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/titlenote.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/create/preamble/title/titlenote.tex">Source File (.tex)</a>
<strong>Supplemental Docs</strong>
<ul>
	<li> <em>Not So Short Introduction to L<sup>A</sup>T<sub>E</sub>X</em> § 6.4-6.5: pp. 112-114 <a href="http://dl.dropbox.com/u/3194367/lshort.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/lshort.dvi">DVI</a> <a href="http://dl.dropbox.com/u/3194367/lshort.ps">PostScript</a></li>
	<li> CTAN documentation on <span style="font-family:courier new;">fullpage</span> package: <a href="ftp://tug.ctan.org/pub/tex-archive/macros/latex/contrib/preprint/fullpage.pdf">PDF</a> <a href="ftp://tug.ctan.org/pub/tex-archive/macros/latex/contrib/preprint/fullpage.ps">PostScript</a></li>
</ul>
Topics covered in this slide:
<ul>
	<li> Title, Author, and Institution commands.</li>
	<li> Adjusting margins manually.</li>
	<li> Using <span style="font-family:courier new;">fullpage</span> package.</li>
	<li> Making headers with the <span style="font-family:courier new;">fancyhdr</span> package.</li>
</ul>
Besides the document class and package, the preamble also contains other commands that apply to the formatting of the document. For instance <span style="font-family:courier new;">\title{...}</span>, <span style="font-family:courier new;">\author{...}</span>, and <span style="font-family:courier new;">\institution{...}</span> allows the author to fill in these fields and create a title header with <span style="font-family:courier new;">\maketitle</span> command.

Furthermore, the margins of the paper are also set in the preamble. It is somewhat complicated, however, most students need a document with one-inch margins. The <span style="font-family:courier new;">fullpage</span> will automatically format the paper to meet those specifications. Lastly, headers are also made in the preamble. The <span style="font-family:courier new;">fancyhdr</span> package allows the author to create sophisticated headers. If the document is two-sided, the author may assign different headers to even and odd pages (like those in a book). By default, the headers will consist of the section's name and number.

This slide show should take 15 to 25 minutes.
---
id: 42
title: Linebreaking, Paragraphs, and Sections
date: 2009-06-30T00:26:08+00:00
author: Tom
layout: page
guid: http://tomschenkjr.net/?page_id=42
---
<strong>Slide Show:</strong> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sect.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sect.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sect.tex">Source File (.tex)</a>
<strong>Lecture Notes:</strong> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sectnote.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sectnote.ps">PostScript</a> <a href="http://dl.dropbox.com/u/3194367/create/body/sect/sectnote.tex">Source File (.tex)</a> <strong></strong>

<strong>Supplemental Docs:</strong>
<ul>
	<li> <a href="http://www.ctan.org/">ctan.org</a> is the best central source for all package information.</li>
	<li> <em>Not So Short Introduction to L<sup>A</sup>T<sub>E</sub>X</em> § 2.7: pp. 34-36 <a href="http://dl.dropbox.com/u/3194367/lshort.pdf">PDF</a> <a href="http://dl.dropbox.com/u/3194367/lshort.dvi">DVI</a> <a href="http://dl.dropbox.com/u/3194367/lshort.ps">PostScript</a></li>
	<li> <a href="http://www.tug.org.in/tutorial/chap03-scr.pdf">India T<sub>E</sub>X User Group: Introduction to L<sup>A</sup>T<sub>E</sub>X (PDF)</a> (a good review for material covered to this point).</li>
</ul>
Topics covered in this slide:
<ul>
	<li> Creating linebreaks.</li>
	<li> Creating paragraphs.</li>
	<li> Preventing or forcing indentation.</li>
	<li> Creating chapters, sections, and subsections.</li>
</ul>
Creating spaces, new lines, and paragraphs seem like a trivial matter. There are a couple of ways to do each. LaTeX also ignores when there are multiple spaces, instead, it will insert a single space. For linebreaks, a simple return usually works; however, sometimes it is necessary to force a linebreak with a command (it will become obvious later when this is needed). Since LaTeX ignores multiple spacing, we cannot tab to create an indentation for a paragraph. Instead, after creating two linebreaks, LaTeX will assume it's a new paragraph and insert it's own indentation. We are able to control when LaTeX indents and when it does not through commands.

Another important command in LaTeX is its <em>chapter</em> and <em>section</em> command. With this command we can break our document into named and numbered sections. These sections will be automatically formatted (slightly larger and bolder text) and included in a table of contents if we deceide to include one. Section commands are very helpful for large documents and for creating a table of contents.
This slide show should take 10 to 20 minutes.
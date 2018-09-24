# Xi personal wiki language

"Xi" is a markdown-like language designed for a personal knowledge base.
Color and indentation is used to highlight headings, paragraphs, links,
source code examples and definitions. You can read and write Xi from
within a VSCode without a need to "render" it into a "visual" web page
or PDF. This makes Xi a very **fast** tool to keep records: you grep
someting, skim through Xi pages, add or change some text from within a same
editor, without a need to switch between 'edit' and 'previes' modes. An
example of Xi page from my personal knowledge base with "Memory" color theme:

<img src="https://raw.githubusercontent.com/grigoryvp/vscode-language-xi/master/doc/xi_illustration.png" height="256">

Example below shows a simple markdown syntax with nested headings and
paragraphs. With Xi, heading is marked with indentation and tail space-dot
instead of indentation. So, heading 2 in markdown that is '## Heading 2'
becomes '  Heading 2 .' in Xi (tail space-dot defines that it's a heading
and leading two spaces defines second level. Third level will be 4 spaces
and up to 10 spaces for a maximum nesting level 5). Paragraphs are marked
with dot-space, effectively saving one empty line used in markdown:

<img src="https://raw.githubusercontent.com/grigoryvp/vscode-language-xi/master/doc/md_to_xi_src.png" width="256">
<img src="https://raw.githubusercontent.com/grigoryvp/vscode-language-xi/master/doc/md_to_xi_dst.png" width="256">

## Paragraph

Simplest building block of a knowledge base, first paragraph line is prefixed
with dot-and-space, while each next line is prefixed with two spaces.
Paragraph itself can be indented with increments of two spaces in order to
nest under different heading or other paragraphs. Compared to markdown
notion of separating paragraphs with empty line, such layout saves a lot
of vertical space, which is vital for documenting software-related things
like programming lanugae syntax, APIs, frameworks etc. We tend to have
short paragraphs that do not tend to follow each other, but tend to form
a really complex nested strucure with lots of headings, meta information,
code samples etc. Such paragrpah layout, used alongside colored headings and
proper indentation, proved it's worth during my 10 years of using Xi as a
personal knowledge base.

<img src="https://raw.githubusercontent.com/grigoryvp/vscode-language-xi/master/doc/paragraph_1.png" width="256">

## Heading

Alongside paragraph, heading is a second most used building block for a
knowledge base. Heading type is denoted by space-dot suffix, while heading
nesting level is denoted by increments of two spaces. In most cases headings
are combined with paragraphs in order to create hierarchical structures
that are easy to read **and modify**.

<img src="https://raw.githubusercontent.com/grigoryvp/vscode-language-xi/master/doc/heading_1.png" width="256">

## Todo

* Anchors like [#1] => [1#] support.
* Correctly catch links within special marks, ex |https://foo|.
* Need to somehow implement deep links like "ruby api#Kernel#system" where
  "system" is a nested heading under "Kernel".
* Outline API support.

## License

The following licensing applies to Xi personal wiki language:
Attribution-NonCommercial-NoDerivatives 4.0 International
(CC BY-NC-ND 4.0). For more information go to
https://creativecommons.org/licenses/by-nc-nd/4.0/

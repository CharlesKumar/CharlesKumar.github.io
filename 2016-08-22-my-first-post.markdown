---
layout: post
title:  "My first Post"
date:   2016-08-22 10:25:36 +0530
categories: blog introduction
--- 
 I just now started a blog with the help of jekyll features. I'm excited about what else i can do next.


 I'm looking for the different formatting options available in jekyll.


   two spaces or two backslashes breaks the line in a paragraph

# Headers 
  as you markup in html
# h1 header
## h2 header
### h3 header
#### h4 header
##### h5 header
###### h6 header


# Blockqoutes 
  
  starts with > optional space
  you can add any block level element in a blockqoute. 

> simple blockquote
>
> >it is also possible
> ## h2 header


# codeblocks

    code blocked
    does this code block terminated    

now its gone based on indentation and new line

~~~python
tilde as delimiters in code blocks

if x=1
  do  x+1

~~
ending must have as many as starting tildes
~~~~

# Horizontal rule 

Three or more asteriks,dashes or underscores

***

# Ordered and Unordered lists

ordered lists are followed by numeral and period

1. first-item
2. second-item
3. last-item

unordered lists are followed by astersik,dash or plus sign

* lazy item
* maybe nav
* item with 
  > blockquote and 
  # header


nested lists can be created by
1. first-item
    1. nested in first
    2. nested in first

2.second-item

# Definition Lists

A definition list works similar to a normal list and is used to associate definitions with terms. Definition lists are started when a normal paragraph is followed by a line starting with a colon and then the definition text. One term can have many definitions and multiple terms can have the same definition. Each line of the preceding paragraph is assumed to contain one term, for example:

term
: first
: second

Each term can be styled using span-level elements and each definition is parsed as block-level elements, i.e. you can use any block-level in a definition. Just use the same indent for the lines following the definition line:

another-term
and another-term
: same definition 
> blockquote note that title  (by IAL) placed at the top
{:title="The blockquote title"}

: *wrapped* in paragraph (1 new line)
# header

# Tables

kramdown supports a syntax for creating simple tables. A line starting with a pipe character (\|) starts a table row. However, if the pipe characters is immediately followed by a dash (-), a separator line is created. Separator lines are used to split the table header from the table body (and optionally align the table columns) and to split the table body into multiple parts. If the pipe character is followed by an equal sign (=), the tables rows below it are part of the table footer.
{: #kramdowntable}

   

|table row |
^

 
|another row |--+--| cell2|


|table row |! cell2|optional pipe at end
-|
|seperators are pipe and dash|any plus,asterisk can be used|to get a nice visual|
|------|----|----|

| Header1| Header2| Header3 |
|:-------|:------:|-------:| <!-- this acts as a align left,right and center -->
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}


# HTML elements

parse_block_html option. If this options is set to true, then the content of a block-level HTML tag is parsed by kramdown either as block level or span-level text, depending on the tag

<div style="float:right">
	This element is parsed as HTML element and wrapped in p tag.
</div>

{::options parse_block_html = "true" /}

<div>
    this is wrapped in p tag by default in kramdown
</div>
---
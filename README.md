<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
- [General File Style](#general-file-style)
  - [Indentation](#indentation)
  - [Line Length](#line-length)
  - [File Names](#file-names)
  - [Line Breaks](#line-breaks)
  - [charset](#charset)
  - [Enforcement](#enforcement)
    - [editorconfig plugin](#editorconfig-plugin)
    - [linting](#linting)
- [HTML](#html)
  - [Quotation Marks](#quotation-marks)
  - [File Names](#file-names-1)
    - [Pages](#pages)
    - [Templates](#templates)
  - [Page Sections](#page-sections)
  - [Comments](#comments)
  - [Line Lengths](#line-lengths)
- [CSS](#css)
  - [File Names](#file-names-2)
- [Javascript](#javascript)
  - [File Names](#file-names-3)
- [Angular](#angular)
  - [File Names](#file-names-4)
- [PHP](#php)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# General File Style

## Indentation

Soft Tabs, 2 spaces

## Line Length

80 characters max

## File Names

dashes for separating long file names

e.g.
	long-file-name.html

## Line Breaks

unix style carriage return line endings (i.e. \r)

## charset

utf-8

## Enforcement

In many cases, maintaining proper code style is a function of the developer
and code reviewer. However, where possible, automated processes should manage 
enforcement

### editorconfig plugin

we use the editorconfig plugin project to support many browsers. Please
install [the plugin](http://editorconfig.org/#download "the editorconfig
project") to the supported editor of your choice

and then install the sdicg editorconfig file 

### linting

where possible, code requirements should be managed by a linting project

it should not be possible to submit code to a repository that does not conform
to any lint-checked formatting requirement

# HTML

## Quotation Marks

All quotation marks used in attribute definitions should be double quotes

e.g.

	<a href="http://example.org">example link</a>

## Attribute Ordering

The order is as follows:

* required tags (e.g. the anchor tag's "href" or img tag's "src")
* id
* class
* standard html attributes (e.g. 

## Inline Styles

Inline styles should be avoided except where absolutely necessary

## Line Lengths

Element definitions that exceed the 80 character line length should be broken
up by stacking the element's attributes

e.g.

	<input
		id    = "test-id"
		class = "test-class"
		type  = "text" />

## Page Sections

Page sections should be delimited by comments. What is a "section" is left to
the discression of the developer. 

Section comments should abide by the following formaty

## Comments

Comments should be used reasonably liberally to describe the purpose of any 
non-obvious design or functionality. Comments should exist on their own lines.

e.g.
	
Bad:

	<div> <!-- here is a comment about this div -->
		...
	</div>

Good

	<!-- here is a comment about this div -->
	<div> 
		...
	</div>

Multiline comments should be formatted as follows

	<!--
		this is a multiline comment

		note the tab indentation after the comment's start
	-->

## File Names

file names should abide by the general naming principle, except that template
or included files have a special naming requirements 

### Pages

a "page" is defined as any html file that has a `<head></head>` section. Should
be named as normal

e.g. `file-name.html`

### Templates

a "template" is defined as any html file that does not have a `<head></head>`
section. Should be named starting with an underscore.

e.g. `_file-name.html`

# CSS

## Rule Names

Long names should be delmited with dashes

e.g.

	.long-style-name {
		...
	}

## Semantic Naming

Class and ID names should have an obvious meaning that applies to their place,
function, or position on the page, as the item's use case dictates

## Rule Definition Format

### Multiline only

There should be no one line rule definitions, no matter how simple

e.g.

Bad: 

	.style-name { color: '#ffffff'; }

Good:

	.style-name {
		color: '#ffffff';
	}

### One expression per line

e.g.

Bad:

	.style-name {
		color: #333333; background: #ffffff;
	}

Good:

	.style-name {
		color: #333333;
		background: #ffffff;
	}

### All lines end with semicolon

e.g.

Bad:

	.style-name {
		color: #333333
	}

Good:

	.style-name {
		color: #333333;
	}

### Space after rule name

A space should exist between the rule name and the opening bracket, which
should be on the same line as the rule name

e.g.

Bad:

	.style-name{
		...
	}

Bad
	
	.style-name
	{
		...
	}

Good

	.style-name {
		...
	}

## Quotation Marks

All attributes should be defined with single quotes where quotes are required

## Class and ID naming conventions

Classes and IDs should be named with dashes for long items

e.g. `.my-custom-class` or `#my-custom-id`

## Color Definitions

All HEX definitions should be 6 characters long. 

If rgba definitions are required, a HEX definition should preceed it

## Combination Attributes

Combination attributes should be used where possible (border, background,
margin, padding). Single margin/padding definitions should be used only 
to override predefined rules

do not use combo attributes with font-related rules

# Javascript

## File Names

# Angular

## File Names

# PHP

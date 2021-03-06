# Markdown to Docs

[![license](https://img.shields.io/github/license/dlvoy/markdown-to-docs.svg)](https://github.com/dlvoy/markdown-to-docs/blob/master/LICENSE)
[![NPM version](http://img.shields.io/npm/v/markdown-to-docs.svg?style=flat)](https://www.npmjs.com/package/markdown-to-docs)
[![Dependencies Status](http://img.shields.io/david/dlvoy/markdown-to-docs.svg?style=flat)](https://david-dm.org/dlvoy/markdown-to-docs)

**markdown-to-docs** is command line tool to convert Markdown files to HTML and PDF documents, embedding local images and replacing PNGs with SVGs if provided.


## Setup

* install [Node.JS](https://nodejs.org) (if not already installed)
* from command line execute:

```sh
$ npm install -g markdown-to-docs 
``` 

## Usage

```sh
$ markdown-to-docs [options] [path_to_markdown_file]
``` 

or

```sh
$ markdown-to-docs --convert [options] [path_to_html_file]
``` 


For full list of supported options execute:
```sh
$ markdown-to-docs -h
``` 

## Options

All options are *optional*. When not specified, they are *ignored* or have *default value*.
Boolean options are *true* if flag is present, *false* otherwise.

Option                                   | Type        
---                                      | :---:              
[`-p`, `--pdf`](#option-pdf)             | `File Path`  
[`-w`, `--html`](#option-html)           | `File Path`  
[`-f`, `--fit`](#option-fit)             | `Boolean` 
[`-r`, `--relink`](#option-relink)       | `Boolean`    
[`-c`, `--convert`](#option-convert)     | `Boolean`    
[`-v`, `--verbose`](#option-verbose)     | `Boolean`    
[`-h`, `--help`](#option-help)           | `Boolean`   
[`-V`, `--version`](#option-version)     | `Boolean`   

### Option pdf

Specifies output path for PDF file.

All local images are embedded. If it is only possible, SVG are used instead of raster files
(if provided).

### Option html

Specifies output path for HTML file.

All local images are embedded. If it is only possible, SVG are used instead of raster files
(if provided).

### Option fit

Works for PDF output only. Is set, images are fit to page width.

### Option relink

When turned on, changes all link to .md or .markdown files into links to .html or .pdf with same file name.

### Option convert

When turned on, input file should be HTML instead of markdown. Resulting HTML output does not have embedded images.

### Option verbose

If set, details of processing is logged into console.

### Option help

Displays all options with short description.

### Option version

Displays version of application (match NPM/Git version number).

# Testing

After install, run: 
    
    npm test


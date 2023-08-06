# obsidian-bibtex-tools
 Tools to manage Bibtex entries in Obsidian

## Set up
I use Obsidian to manage notes on what I read. Each source that I read has its own page in my Obsidian vault. These pages are marked with a #source hashtag. These pages also contain frontmatter; specifically a "cite" key that contains the metadata used to generate BibTeX entries both within Obsidian and on the command line. 

To use these files, one should be familiar with Obsidian and the Templater plugin. 

## Example

Source pages should include a few important frontmatter entries. These are the `source` tag, and the `cite` array with additional keys. This is included at the top of every source file.

```
---
tags:
  - source
  - topic/animals
alias:
  - "@2023denny"
cite:
  key: "2022denny"
  type: "book"
  title: "My Favorite Animals"
  author: "Will Denny"
  year: 2022
  publisher: "Denny Books"
  address: "Boston, MA"
---
```

Within the source file, you can insert the "Generate Bibtex from Metadata (Script)" template. The resulting BibTeX entry will be inserted into the document at the cursor location wrapped in a code block with the tag "bibtex".
# Oxygen XML Editor

> The Complete Solution for XML Editing, Authoring, Development & Collaboration

https://www.oxygenxml.com/

## What is it?

* well, it is an XML Editor
* nice **TEI integration** (framework)
* ships with software ([Saxon](https://www.saxonica.com/products/why-saxon.xml) and [Java](https://www.java.com/en/)) to process (transform, query) XML documents


> [!WARNING]  
> Oxygen is not free, you need to buy a license, starting from [$137 (academic)](https://www.oxygenxml.com/buy-academic.html) or [$240 (personal)](https://www.oxygenxml.com/buy-personal.html)


> [!TIP]
> You can try it for free for 30 days

## Download and install

https://www.oxygenxml.com/xml_editor/download_oxygenxml_editor.html

## Why should I use it?

* People say it is the **de facto standard tool** in the context of digital editions; at least here at the ACDH-CH used in many projects.
* **TEI-Support**
* **WYSIWYG View** (Author-Mode)
* especially useful for **developing** XSL stylesheets for e.g. the conversion from XML to HTML files
* especially useful for **querying/analyzing** XML-Documents

> [!TIP]
> If you are mainly interested in encoding XML-Documents you can use free, general Code-Editors like e.g. VS-Code with additional XML Plug-Ins

## Useful things in Oxygen

### Oxygen-Project
* having a file browser in Oxygen

demonstrate with [this repo](https://github.com/acdh-oeaw/mtr-tei-oxygen)

### Transformation Scenarios
* Oxygen ships with stylesheets to convert TEI/XML Documents into e.g. Word, HTML, PDF
* You can create your own stylesheets and transformation scenarios

demonstrate with [`wkfm-static`](https://github.com/donauhandel/wkfm-static)

### Batch Validation
* Check files in batches if they are well-formed and valid

demonstrate with [`tillich-briefe-data`](https://github.com/TillichCorrespondence/tillich-briefe-data)

### Git-Plugin
* interact with GIT directly from Oxygen
  * check diffs, commit, pull, ...

### Author mode
* customizable WYSIWYG Editor

demonstrate with [`tillich-briefe-data`](https://github.com/TillichCorrespondence/tillich-briefe-data)

### Xpath-Builder
* Query one or many files using Xpath

demonstrate with [`tillich-briefe-data`](https://github.com/TillichCorrespondence/tillich-briefe-data)

"find all letters written by Gustav Dürselen"
```xpath
//correspAction[@type="sent"]/persName[@ref="#tillich_person_id__2237"]
```

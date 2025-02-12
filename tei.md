# Text Encoding Initiative - TEI

The TEI combines several aspects:
1. it is a **community** (or consortium) [go to](#consortium)
1. this community develops a set of **human readable rules** how to encode text, the **Guidelines** [go to](#guidelines)
1. these guidelines are materialized in form of a **schema to validate TEI/XML documents** [go to](#tei-schema)
1. **tools and services** helping to create, validate and transform TEI/XML documents [go to](#tools-and-services)


## consortium

* [Mailing-List](https://tei-c.org/support/)
* [Meetings](https://members.tei-c.org/Events/meetings)
* [GitHub-Organisation](https://github.com/TEIC)
  * e.g. [Issues](https://github.com/TEIC/TEI/issues/2382)

## Guidelines

* A human readable but formalized description of all tags and attributes the TEI provides for the encoding of texts. [Link to the Guidelines](https://tei-c.org/release/doc/tei-p5-doc/en/html/index.html). 
* The [PDF](https://tei-c.org/release/doc/tei-p5-doc/en/Guidelines.pdf) has about 2600 Pages!

### Navigating the TEI

You want to mark up some textual phenomenon; let's say you have an abbreviation like `e.g.` in your text and you want to:
* express that this is an abbreviation
* tell what this abbreviation stands for

#### Google it
* https://www.google.com/search?q=tei+abbreviation
* should lead you to the [TEI-guidelines page of some tag/element](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-abbr.html)
* Read the description! Does it fit your needs?
* Look at the example!

> [!TIP]
> Ask some LLM

#### ChatGPT-Example

You are encoding a text using TEI. You want to mark up some textual phenomenon; let's say you have an abbreviation like `e.g.` in your text and you want to:
* express that this is an abbreviation
* tell what this abbreviation stands for

two solutions provided:

> [!WARNING]
> The first example does not validate against the TEI-Schema, therefore it is wrong!
```xml
<abbr expan="exempli gratia">e.g.</abbr>
```

```xml
<choice>
  <abbr>e.g.</abbr>
  <expan>exempli gratia</expan>
</choice>
```

#### Follow examples you like

https://kaiserin-eleonora.oeaw.ac.at/kasten_blau_45_9_0278.html -> [download TEI/XML](https://kaiserin-eleonora.oeaw.ac.at/kasten_blau_45_9_0278.xml)

## TEI-Schema

* can be downloaded [here somewhere](https://www.tei-c.org/guidelines/customization/)
* TEI-ALL as XML Schema Definition: https://www.tei-c.org/release/xml/tei/custom/schema/xsd/tei_all.xsd
* needs to be linked to your TEI/XML Document
* or in Oxygen, File -> New (ctrl+n) -> All [TEI] -> creates following Document

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?xml-model href="http://www.tei-c.org/release/xml/tei/custom/schema/relaxng/tei_all.rng" type="application/xml" schematypens="http://relaxng.org/ns/structure/1.0"?>
<?xml-model href="http://www.tei-c.org/release/xml/tei/custom/schema/relaxng/tei_all.rng" type="application/xml"
    schematypens="http://purl.oclc.org/dsdl/schematron"?>
<TEI xmlns="http://www.tei-c.org/ns/1.0">
  <teiHeader>
      <fileDesc>
         <titleStmt>
            <title>Title</title>
         </titleStmt>
         <publicationStmt>
            <p>Publication Information</p>
         </publicationStmt>
         <sourceDesc>
            <p>Information about the source</p>
         </sourceDesc>
      </fileDesc>
  </teiHeader>
  <text>
      <body>
         <p>Some text here.</p>
      </body>
  </text>
</TEI>
```

* Now any **violations** should be picked up by your editor and marked, in Oxygen with a **red underline**
* Schema-aware code editors should provide you with **code completion / autocompletes**, suggesting allowed tags/attributes
* Schema-aware code editors should **explain the tags**

## Tools and Services
### [ROMA](https://roma.tei-c.org/)
> Roma is an ODD Editor, using the TEI ODD (One Document Does-it-all) format for meta-schema documentation and local encoding guidelines as created by the Text Encoding Initiative.

### [TEIGarage](https://teigarage.tei-c.org/)
> TEIGarage is a web service and RESTful service to transform, convert and validate various formats, focusing on the TEI format. TEIGarage is based on the proven OxGarage.

### [TEI XSLT Stylesheets](https://github.com/TEIC/Stylesheets)
> This is a family of XSLT 3.0 stylesheets to transform TEI XML documents to various formats, including XHTML, LaTeX, XSL Formatting Objects, ePub, plain text, RDF, JSON; and to/from Word OOXML (docx) and OpenOffice (odt). 

* (partly) included in Oxygen
* used by TEIGarage
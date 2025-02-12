# Text Encoding Initiative - TEI

The TEI combines several aspects:
1. it is a **community** (or consortium)
1. this community develops a set of **human readable rules** how to encode text, the **Guidelines**
1. these guidelines are materialized in form of a **schema to validate TEI/XML documents**
1. **tools and services** helping to create, validate and transform TEI/XML documents


## consortium

* [Mailing-List](https://tei-c.org/support/)
* [Meetings](https://members.tei-c.org/Events/meetings)
* [GitHub-Organisation](https://github.com/TEIC)
  * e.g. [Issues](https://github.com/TEIC/TEI/issues/1861)

## Guidelines

* A human readable but formalized description of all tags and attributes the TEI provides for the encoding of texts. [Link to the Guidelines](https://tei-c.org/release/doc/tei-p5-doc/en/html/index.html). 
* The [PDF](https://tei-c.org/release/doc/tei-p5-doc/en/Guidelines.pdf) has about 2600 Pages!

### Navigating the TEI

You want to mark up some textual phenomenon; let's say you have an abbreviation like `e.g.` in your text and you want to:
* express that this is an abbreviation
* tell what this abbreviation stands for

> [!TIP]
> Google it! https://www.google.com/search?q=tei+abbreviation

> [!TIP]
> Ask some LLM

#### ChatGPT

You are encoding a text using TEI. You want to mark up some textual phenomenon; let's say you have an abbreviation like `e.g.` in your text and you want to:
* express that this is an abbreviation
* tell what this abbreviation stands for

two solutions provided:

> [!WARNING]
> This is not valid TEI
```xml
<abbr expan="exempli gratia">e.g.</abbr>
```

```xml
<choice>
  <abbr>e.g.</abbr>
  <expan>exempli gratia</expan>
</choice>
```
# factsheets_sshoc_services

This is the Gitlab repository for the factsheets created within SSHOC WP3.6 for the Virtual Collection Registry and the Language Resource Switchboard.

In case of questions write to sbudden@gwdg.de

The files in this repository are Markdown files which contain - one service per file - the factsheets. All factsheets follow the same pattern and describe the service, its possible use case, point to other services in the SSHOC environment and illustrate all of this with examples.

# Documentation

This folder contains all static pages belonging to the factsheets_sshoc_services. They are all written in [Markdown](https://daringfireball.net/projects/markdown/).

## Naming schema

The files in the <_posts> directory follow the naming scheme

        [date][pagename].md

Where `pagename` is the identifier used for the page. The `.md` extension identifies the file as Markdown file.

The markdown files are later rendered as html within the SSHOC static docs site <https://buddenbohm.pages.gwdg.de/factsheets_sshoc_services> identified as `pagename.html`.

## Index

The index is autogenerated and lists all docs found in <_posts/>. Description and page title are changed in <_config.yaml>.

### Linking between pages

Linking between pages is possible. Refer to the 2020-01-01-syntax.md document as to `syntax.html`. Example: 

```markdown
Find more info on the [syntax](syntax.html) page.
```

### Linking within pages / Heading anchors


IDs are genereted for heading elements. Which could be used as anchors, this means that you can link to them.

An Example:

A Marddown snippet

        # A headline

        ## A subsection

will be rendered as HTML Elements

        <h1 id="a headline">A headline</h1>
 
        <h2 id="a-subsection">A subsection</h2>

which means the ID will be lowercase with hyphens (`-`) instead of spaces. So you can link to them in Markdown like

        See [chapter 1](#a-headline) and [chapter 1.1](#a-subsection)

Which allwos creation of a TOC for example. You can also reference headings or subheadings on other pages

        see the [voyant-example](voyant.html#example)

If you are unsure which ID was generated for a heading inspect the element with the developer tool of your web browser. In Firefox for example you can do this with a click on the heading and the context menu entry "Inspect Element"("Element untersuchen"), which will reveal the id:

![inspecting the anchor id](images/inspect-anchor.png)


### Images

Own images can be placed in the `images` subfolder of this directory. They are referenced by their relative path like this:

```
  ![SSHOC logo](/sshoc-docs/images/sshoc-logo.png)
```

This will be rendered as:

![SSHOC logo](images/sshoc-logo.png)


## Running locally / development

This site could be viewed locally with docker-compose

        docker-compose up

Afterwards the website is visible at http://localhost:4000/sshoc-docs/

# Credits

Theme is derived from https://gitlab.com/jekyll-themes/carte-noire


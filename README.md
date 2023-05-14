<div align="center">
	<h1>
		<img src="assets/icon.png" width="170" height="170" align='right'></br>
    <i>µ</i>Bib | MicroBib</br>
    <a href="https://github.com/zeitlings/ubib/releases"><img src="https://img.shields.io/github/v/release/zeitlings/ubib.svg" alt="GitHub Release"></a>
	</h1>
<i>Citations, BibTeX, and Research</i> 
</div>

---

The project combines the APIs of Crossref, Semantic Scholar, OpenAlex, OpenLibrary, Wikipedia, Google Books, and doi.org. Reference metadata is highly inconsistent, incomplete, erroneous or otherwise flawed across different sources. *µ*Bib tries to remedy this by heuristically aggregating information from different sources into one best possible result.


## Core Functions

- Reference lookup using `DOI`, `ISBN`, `PMID`, `PMCID`, `MAG`, `arXiv`, `ACL` identifiers, and URLs (e.g. jstor)
- CSL formatted citations from identifiers and BibTeX
- Free-text search for publication discovery
- Author lookup and publication retrieval
- Ad hoc citation graph traversal
- Lightweight BibTeX reference management and citation picker

## Cheat Sheet

- `ubib <identifier>`
- `ubib <URL>`
- `ubib <free-text>`
- `ubib @article{citekey,...`
- `ubib pmid:<identifier>`
- `ubib pmcid:<identifier>`
- `ubib mag:<identifier>`
- `ubib arxiv:<identifier>`
- `ubib acl:<identifier>`
- `ubib :`
- `ubib ::`
- `ubib :::`, `ubib :c`
- `ubib :b`, `ubib cit`, `ubib lib`
  - bangs: `!a[rticle]`, `!b[ooks]`, `!c[hapter]`, `!o[ther]`

## Documentation

### Metadata retrieval

<img src="assets/img/ubib.prev.1.gif" width="564px" />

- __⇧__ to Quicklook preview the formatted citations

<details>
  <summary>Example</summary>
  <img src="assets/img/preview.rendered.png" width="564px" />
</details>

### Publication Discovery

Search is available through Crossref, Semantic Scholar, and OpenAlex. Where available, 
- Crossref allows for traversal of *referenced works* ⌃,
- Semantic Scholar allows for traversal of referenced works and *citing works* ⌥,
- OpenAlex allows for traversal of referenced works, citing works and *related works* ⌥⇧.


| Service          	| Landing-page Preview 	| Abstract 	| TL;DR Digest 	| Open Access 	| Concepts 	| Citation Intent & Context 	|
|------------------	|:--------------------:	|:--------:	|:------------:	|:---------------------:	|:--------:	|:-------------------------:	|
| Crossref         	|           ✔︎          	|     ✔︎    	|              	|                       	|          	|                           	|
| Semantic Scholar 	|           ✔︎          	|     ✔︎    	|       ✔︎      	|           ✔︎           	|          	|             ✔︎             	|
| Open Alex        	|           ✔︎          	|          	|              	|           ✔︎           	|     ✔︎    	|                           	|
|                  	|           ⇧          	|    ⌘+L   	|      ⌘+L     	|           ⌘⇧          	|    ⌘+L   	|            ⌘+L            	|

<img src="assets/img/ubib.prev.2.gif" width="564px" />

<img src="assets/img/preview.search.author.png" width="564px" />

### Reference Management & Citation Picker

You can link your existing bibliography document in the workflow configuration, or select a location where you want to create a new one. New BibTeX references can be quickly added to the library, and managed using the built-in reference manager and citation picker.

While searching the library, you can use `!bangs` to filter by publication type:
- `!a[rticle]`
- `!b[ooks]`
- `!c[hapter]`
- `!o[ther]`

<img src="assets/img/ubib.prev.3.gif" width="564px" />

> __Note__  
> 1. The citation style corresponding to the pasted *CSL formatted bibliographic reference* can be freely configured.  
> 2. The BibTeX entries may include a key `dvn`, which is intended to contain the DEVONthink item link to the corresponding document. 

<img src="assets/img/ubib.prev.3.dvn.png" width="564px" />


To configure a citation, action the entry while holding down the __⌘__ modifier. Multiple citations can be chained using the __⌥__ modifier. Citations can be configured in either __LaTeX__ or __Pandoc Markdown__.

<img src="assets/img/preview.cite.latex.png" width="564px" />
<img src="assets/img/preview.cite.markdown.png" width="564px" />


### CSL Management & Maintenance

<img src="assets/img/preview.csl.png" width="564px" />
<img src="assets/img/preview.config.png" width="564px" />


<!--

## Icon Legend

- !todo

-->

<!--

## Static Previews

<details>

### Metadata retrieval

<img src="assets/img/preview.doi.png" width="564px" />
<img src="assets/img/preview.rendered.png" width="564px" />

### Publication Discovery

<img src="assets/img/preview.search.png" width="564px" />
<img src="assets/img/preview.search2.png" width="564px" />
<img src="assets/img/preview.search.author.png" width="564px" />

### Reference Management & Citation Picker

<img src="assets/img/preview.bibtex.png" width="564px" />
<img src="assets/img/preview.cite.latex.png" width="564px" />
<img src="assets/img/preview.cite.markdown.png" width="564px" />

### CSL Management & Maintenance

<img src="assets/img/preview.csl.png" width="564px" />
<img src="assets/img/preview.config.png" width="564px" />


</details>

-->

## Thanks

- Cormac Relf for [CiteprocRsKit](https://github.com/cormacrelf/CiteprocRsKit) | CSL processing
- Max Haertwig for [SwiftyBibtex](https://github.com/MaxHaertwig/SwiftyBibtex) | BibTeX parsing


---

Created by [Patrick Sy](https://github.com/zeitlings/ubib) |  [Report Issues](https://github.com/zeitlings/ubib) | [Support the Project](https://ko-fi.com/zeitlings) ❤️
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

<details>

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

</details>

## Documentation

### Metadata retrieval

<img src="assets/img/ubib.prev.1.gif" width="564px" />

- Press __⇧__ to Quicklook preview the formatted citations

<details>
  <summary>Quicklook Example</summary>

  Citation Styles can be configured [within the workflow](https://github.com/zeitlings/ubib#csl-management--maintenance) or the workflow configuration by providing their identifiers. Those can be retrieved via (a) [Zotero](https://www.zotero.org/styles/), or (b) the Citation Style Language [repository](https://github.com/citation-style-language/styles) (alternative: [Github search](https://github.com/search?q=path%3Achicago+repo%3Acitation-style-language%2Fstyles+path%3A*csl+&type=code)).

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


### Author Discovery & Filtered Search

Besides discovering publications through free-text searches, it's also possible to retrieve works that have been registered under an author's name by looking up the author first (Semantic Scholar and OpenAlex). 


<img src="assets/img/preview.search.author.png" width="564px" />

You can refine a Crossref search by filtering the query by the author's name.

<img src="assets/img/preview.search.author.cr.png" width="564px" />

The different search modes are accessible through the `ubib :` entry point.

<img src="assets/img/preview.search2.png" width="564px" />


### Reference Management & Citation Picker

You can link your existing bibliography document in the workflow configuration, or select a location where you want to create a new one. New BibTeX references can be quickly added to the library, and managed using the built-in reference manager and citation picker.

While searching the library, you can use `!bangs` to filter by publication type: `!a[rticle]`, `!b[ooks]`, `!c[hapter]`, `!o[ther]`

<img src="assets/img/ubib.prev.3.gif" width="564px" />

The subtitle field provides cues about extracted information, such as the presence of an associated abstract, keywords, or document links. These cues are represented using symbols, which may not be visible if the [SF Pro](https://developer.apple.com/fonts/) font is not installed on your device. The information can be viewed in Alfred's large type utility by pressing __⌘+L__.

The citation style corresponding to the pasted *CSL formatted bibliographic reference* can be freely configured.  

> __Note__  
> The BibTeX entries may include a key `dvn`, which is intended to contain the DEVONthink item link to the corresponding document. 

<img src="assets/img/ubib.prev.3.dvn.png" width="564px" />


To configure a citation, action the entry while holding down the __⌘__ modifier. To chain multiple citations, use the __⌥__ modifier. The citation picker supports two flavours - __LaTeX__ and __Pandoc Markdown__ - to accomodate various writing scenarios.

<img src="assets/img/preview.cite.latex.png" width="564px" />
<img src="assets/img/preview.cite.markdown.png" width="564px" />


### CSL Management & Maintenance

New citation styles are retrieved from the [Zotero](https://www.zotero.org/styles/) repository. When configuring styles manually, the identifier is the last path component of the Zotero URL that resolves to a valid CSL-XML document. For example, the identifier for APA 6th edition is `apa-6th-edition` as in `https://www.zotero.org/styles/apa-6th-edition`.

The display name of a CSL used in the workflow is taken from the short title of the corresponding style sheet. The short title should be declared like this: `<title-short>Display Name</title-short>`. By editing or adding this field, you can influence the appearance. The style sheets can be found in *Data Folder > csl*.

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

Created by [Patrick Sy](https://github.com/zeitlings/ubib) |  [Make Suggestions](https://github.com/zeitlings/ubib/issues/new/choose) | [Report Issues](https://github.com/zeitlings/ubib/issues/new/choose) | [Support the Project](https://ko-fi.com/zeitlings) ❤️
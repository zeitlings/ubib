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
- Lightweight BibTeX reference management and citation picker

## Cheat Sheet

- `ubib <identifier>`
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
- `ubib :b`, `ubib cit`, `ubib bib`
  - bangs: `!a[rticle]`, `!b[ooks]`, `!c[hapter]`, `!na`

## Previews

<img src="assets/img/preview.doi.png" width="564px" />
<img src="assets/img/preview.rendered.png" width="564px" />
<img src="assets/img/preview.search.png" width="564px" />
<img src="assets/img/preview.search2.png" width="564px" />
<img src="assets/img/preview.csl.png" width="564px" />
<img src="assets/img/preview.config.png" width="564px" />
<img src="assets/img/preview.bibtex.png" width="564px" />
<img src="assets/img/preview.cite.latex.png" width="564px" />
<img src="assets/img/preview.cite.markdown.png" width="564px" />


## Thanks

- Cormac Relf for [CiteprocRsKit](https://github.com/cormacrelf/CiteprocRsKit) | CSL processing
- Max Haertwig for [SwiftyBibtex](https://github.com/MaxHaertwig/SwiftyBibtex) | BibTeX parsing
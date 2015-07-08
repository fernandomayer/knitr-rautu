# Citações bibliográficas com knitr



Citações bibliográficas podem ser feitas em documentos Markdown através
do pacote knitcitations, usando arquivos no formato BibTeX (`.bib`), o
mesmo utilizado em documentos LaTeX.

Instalar o pacote:


```r
library(devtools)
install_github("cboettig/knitcitations")
```

Ler um arquivo `.bib` do LaTeX


```r
library(knitcitations)
bib <- read.bibtex("walmes.bib")
```

Confere os nomes das referências neste arquivo:


```r
names(bib)
```

```
##     Bonat2011   Zeviani2014 
##   "Bonat2011" "Zeviani2014"
```

Para citar, por exemplo, as referências com as tags `Zeviani2014` e
`Bonat2011`, usamos a função `citep()` dessa forma:
`citep(bib[["Zeviani2014"]])` que gera (<a href='#bib-Zeviani2014'>Zeviani, Ribeiro
Jr, Bonat, Shimakura, et al., 2014</a>) e
`citep(bib[["Bonat2011"]])` que gera (<a href='#bib-Bonat2011'>Bonat, Ribeiro
Jr, and Zeviani, 2011</a>).

O formato das referências pode ser controlado pela função
`cite_options()`, que neste documento foi configurado da seguinte forma:


```r
cite_options(citation_format = "text",
             style = "html",
             hyperlink = TRUE)
```

## Referências

A lista de referências citadas pode ser incluida no final do texto com a
função `bibliography()`, que permite também modificar o estilo de
apresentação da lista e a ordem da lista. Mais detalhes em
`?bibliography`.


```r
bibliography()
```

<p><a id='bib-Bonat2011'></a><a href="#cite-Bonat2011">[1]</a><cite>
W. H. Bonat, P. J. Ribeiro
Jr and W. M. Zeviani.
&ldquo;Comparando predições por modelos geoestatístico e
aditivo generalizado para reconstituição de
superfícies contínuas gaussianas&rdquo;.
Pt.
In: <em>Energia na Agricultura</em> 26.2 (Apr. 2011), pp. 119&ndash;128.
ISSN: 1808-8759.
URL: <a href="http://200.145.140.50/index.php/energia/article/view/214">http://200.145.140.50/index.php/energia/article/view/214</a>.</cite></p>

<p><a id='bib-Zeviani2014'></a><a href="#cite-Zeviani2014">[2]</a><cite>
W. M. Zeviani, P. J. Ribeiro
Jr, W. H. Bonat, S. E. Shimakura, et al.
&ldquo;The Gamma-count distribution in the analysis of experimental underdispersed data&rdquo;.
In: <em>Journal of Applied Statistics</em> 41.12 (Jun. 2014), pp. 1&ndash;11.
ISSN: 0266-4763.
DOI: <a href="http://dx.doi.org/10.1080/02664763.2014.922168">10.1080/02664763.2014.922168</a>.
URL: <a href="http://dx.doi.org/10.1080/02664763.2014.922168">http://dx.doi.org/10.1080/02664763.2014.922168</a>.</cite></p>

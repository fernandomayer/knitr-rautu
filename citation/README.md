# Citações bibliográficas com knitr



Citações bibliográficas podem ser feitas em documentos Markdown através
do pacote knitcitations, usando arquivos no formato BibTeX (`.bib`), o
mesmo utilizado em documentos LaTeX.

Instalar o pacote:


```r
library(devtools)
install_github("cboettig/knitcitations")
```

Ler um arquivo `.bib`


```r
library(knitcitations)
bib <- read.bibtex("walmes.bib")
```

Confere os nomes das referências neste arquivo:


```r
names(bib)
```

```
##     RODRIGUES2010         Bonat2011      Carducci2011      Carneiro2011 
##   "RODRIGUES2010"       "Bonat2011"    "Carducci2011"    "Carneiro2011" 
##      Clemente2011       Barbosa2012         Bonat2012         Bruhn2012 
##    "Clemente2011"     "Barbosa2012"       "Bonat2012"       "Bruhn2012" 
##      Carducci2012         Hoyos2012       Machado2012         Paula2012 
##    "Carducci2012"       "Hoyos2012"     "Machado2012"       "Paula2012" 
##      Serafim2012a       Serafim2012        Silva2012a         Souza2012 
##    "Serafim2012a"     "Serafim2012"      "Silva2012a"       "Souza2012" 
##       Zeviani2012      Carducci2013       Serafim2013     Centurion2014 
##     "Zeviani2012"    "Carducci2013"     "Serafim2013"   "Centurion2014" 
##       DaSilva2014   Lichtemberg2014   Lichtemberg2014      Rozwalka2014 
##     "DaSilva2014" "Lichtemberg2014" "Lichtemberg2014"    "Rozwalka2014" 
##       Zeviani2014 
##     "Zeviani2014"
```

Para citar, por exemplo, [@Zeviani2014] e [@Bonat2011].

## Referências


```r
bibliography()
```

```
## Warning in parse_Rd(Rd, encoding = encoding, fragment = fragment, ...):
## <connection>:3: unknown macro '\i'
```

```
## Warning in parse_Rd(Rd, encoding = encoding, fragment = fragment, ...):
## <connection>:3: unknown macro '\i'
```

```
## Warning in parse_Rd(Rd, encoding = encoding, fragment = fragment, ...):
## <connection>:3: unknown macro '\i'
```

```
## <a name=bib-Bonat2011></a>[[1]](#cite-Bonat2011) W. H. Bonat, P.
## J. R. Junior and W. M. Zeviani. "Comparando predições por modelos
## geoestat\'\istico e aditivo generalizado para reconstituição de
## superf\'\icies cont\'\inuas gaussianas". Pt. In: _Energia na
## Agricultura_ 26.2 (Apr. 2011), pp. 119-128. ISSN: 1808-8759. URL:
## [http://200.145.140.50/index.php/energia/article/view/214](http://200.145.140.50/index.php/energia/article/view/214).
## 
## <a name=bib-Zeviani2014></a>[[2]](#cite-Zeviani2014) W. M.
## Zeviani, P. J. Ribeiro, W. H. Bonat, S. E. Shimakura, et al. "The
## Gamma-count distribution in the analysis of experimental
## underdispersed data". In: _Journal of Applied Statistics_ 41.12
## (Jun. 2014), pp. 1-11. ISSN: 0266-4763. DOI:
## [10.1080/02664763.2014.922168](http://dx.doi.org/10.1080/02664763.2014.922168).
## URL:
## [http://dx.doi.org/10.1080/02664763.2014.922168](http://dx.doi.org/10.1080/02664763.2014.922168).
```

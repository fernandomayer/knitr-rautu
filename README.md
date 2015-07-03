# knitr-rautu

Utilização básica do knitr.

O [knitr][] é um pacote do R desenvolvido para produzir relatórios
dinâmicos, onde é possível misturar texto (LaTeX, Markdown, ...) e
códigos do R. Ao ser interpretado, um arquivo do knitr (com extensão
`.Rnw` para LaTeX, e `.Rmd` para Markdown) gera um arquivo PDF ou
Markdown com as saídas dos comando do R já interpretadas. O knitr
aprimora e estende o antigo pacote Sweave do R.

Os arquivos `knitr-rautu.{Rnw, tex, pdf}` contém uma introdução geral ao
uso do knitr, e fazem parte de um mini-curso apresentado dentro do curso
"Introdução ao LaTeX", na ESALQ/USP, 23/09 a 04/10, 2013.

O arquivo [knitr-rautu.Rnw][] possui texto em LaTeX e códigos do R
"entrelaçados". Este é o arquivo que usamos para edição. O arquivo
[knitr-rautu.tex][] é o arquivo processado pelo knitr, e contém diversos
ambientes gerados automaticamente, os quais você não precisa se
preocupar. Qualquer alteração deve ser feita no arquivo `.Rnw`. O
arquivo [knitr-rautu.pdf][] é o resultado final após ser processado com
o LaTeX (`pdflatex`). A partir do arquivo `knitr-rautu.Rnw` você pode
reproduzir estes slides usando:

```r
## Carrega o pacote knitr
library(knitr)
## Converte Rnw em tex
knit("knitr-rautu.Rnw")
## Converte tex em pdf
system("pdflatex knitr-rautu.tex")
```

Se você procura por um template básico para dar o primeiro passo com o
knitr, use o arquivo [knitr-template.Rnw](template/knitr-template.Rnw),
e veja os demais arquivos gerados dentro do diretório
[`template/`](template/).


## Licença

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/deed.pt_BR"><img alt="Licença Creative Commons" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />Esta obra foi licenciada sob uma Licença <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/deed.pt_BR">Creative Commons Atribuição-CompartilhaIgual 3.0 Não Adaptada</a>.

[knitr]: http://yihui.name/knitr/

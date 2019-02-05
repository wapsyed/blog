<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello, woRld</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#hello-world---code-with-pizza-1">“Hello, woRld - Code with Pizza! #1”</a></li>
<li><a href="#programação-em-r-com-swirl">Programação em R com swiRl</a>
<ul>
<li><a href="#instalação---r-e-r-studio">Instalação - R e R Studio</a></li>
<li><a href="#instalação---swirl">Instalação - swirl</a></li>
</ul>
</li>
<li><a href="#guia-de-estudos">Guia de estudos</a>
<ul>
<li><a href="#instalação-dos-pacotes-usados-no-curso">Instalação dos pacotes usados no curso</a></li>
</ul>
</li>
<li><a href="#links-úteis">Links úteis</a></li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="hello-world---code-with-pizza-1">“Hello, woRld - Code with Pizza! #1”</h1>
<h1 id="programação-em-r-com-swirl">Programação em R com swiRl</h1>
<p>O evento “Hello, woRld - Code with Pizza” será realizado em sua primeira edição pela Liga de Ômicas da FCFRP-USP. O curso terá duração de, no máximo, 6h, e seguirá um método de autoaprendizagem, explorando todos os tópicos sugeridos no ritmo de cada participante. Como o curso será extenso, faremos coffee breaks com pizzas com carne e vegetarianas, refrigerantes e sucos, ao longo da programação.</p>
<p>O evento, todavia, terá um número limitado de vagas, mas, ainda que não consiga participar, o presente guia de instalação ainda será útil para sua aprendizagem.</p>
<blockquote>
<p>Faça sua inscrição em: _________.</p>
</blockquote>
<h2 id="instalação---r-e-r-studio">Instalação - R e R Studio</h2>
<h3 id="usuários-windows">Usuários Windows</h3>
<p>Se você estiver usando o Windows, siga os seguintes passos:</p>
<p>1 - Instação do R: <a href="https://cran.rstudio.com/bin/windows/base/R-3.5.2-win.exe">https://cran.rstudio.com/bin/windows/base/R-3.5.2-win.exe</a> e salve na pasta de “Downloads”</p>
<p>2 - Instalação do R Studio: <a href="https://download1.rstudio.org/RStudio-1.1.463.exe">https://download1.rstudio.org/RStudio-1.1.463.exe</a></p>
<h3 id="usuários-mac">Usuários Mac</h3>
<p>Se você estiver usando o Mac, siga os seguintes passos:</p>
<p>1 - Instação do R: <a href="https://cran.rstudio.com/bin/macosx/R-3.5.2.pkg">https://cran.rstudio.com/bin/macosx/R-3.5.2.pkg</a> e salve na pasta de “Downloads”</p>
<p>2 - Instalação do R Studio: <a href="https://download1.rstudio.org/RStudio-1.1.463.dmg">https://download1.rstudio.org/RStudio-1.1.463.dmg</a></p>
<h3 id="usuários-linux">Usuários Linux</h3>
<p>Se você estiver usando o Linux Ubuntu ou Mint, siga os seguintes passos:</p>
<p>1- Abra o terminal e copie (ctrl+c) e cole (ctrl+shift+v) cada linha de código, sem o $.</p>
<p>(Troque “precise/”" pela versão do ubuntu atual. Para saber a sua versão, digite, no terminal, $ cat /etc/*release.)</p>
<pre class=" language-undefined"><code class="prism language-{bash} language-undefined">$ sudo sh -c 'echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" &gt;&gt; /etc/apt/sources.list'
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E084DAB9
$ sudo apt-get update
$ sudo apt-get install r-base-dev
$ sudo sh -c 'echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" &gt;&gt; /etc/apt/sources.list.d/cran.list'
</code></pre>
<p>Confirme a sua versão do R (3.1.0 ou mais recente)</p>
<pre class=" language-undefined"><code class="prism language-{bash} language-undefined">$ R --version
</code></pre>
<p>3 - Baixe o RStudio em <a href="https://www.rstudio.com/products/rstudio/download/#download">https://www.rstudio.com/products/rstudio/download/#download</a></p>
<p>4 - Instale libcurl</p>
<p>No ubuntu:</p>
<pre class=" language-undefined"><code class="prism language-{bash} language-undefined">$ sudo apt-get install libcurl4-openssl-dev
</code></pre>
<p>No Linux Mint 17:</p>
<pre class=" language-undefined"><code class="prism language-{bash} language-undefined">$ sudo apt-get install libcurl4-openssl-dev r-base-dev libxml2-dev
</code></pre>
<h2 id="instalação---swirl">Instalação - swirl</h2>
<p>Ao instalarmos o swirl no R, devemos instalar também todos os cursos disponiveis no repositório deles no GitHub. Faça o download da pasta completa do curso Hello, woRld pelo link (<a href="https://tinyurl.com/ycacarh9">https://tinyurl.com/ycacarh9</a>) e salve em “Meus Documentos”. A pasta será baixada como .zip, então vá na pasta onde foi salvo o .zip, clique com o botão direito do mouse no arquivo e escolha para descompactar/unzip na mesma pasta. Quando a pasta estiver completamente descompactada, exclua o arquivo .zip, pois não será mais necessário.</p>
<p>Abra o RStudio e digite no Console:</p>
<pre class=" language-undefined"><code class="prism language-{r} language-undefined">install.packages("swirl")
library(swirl)
</code></pre>
<p>Após instalar o swirl com install.packages() e importar a sua biblioteca com library() instale todos os cursos da pasta baixada digitando o comando abaixo:</p>
<pre class=" language-undefined"><code class="prism language-{r} language-undefined">install_course_zip("Documentos/Hello, woRld/Swirl/swirl_courses-master.zip", multi=TRUE)
</code></pre>
<p>Abra o Swirl com o comando abaixo:</p>
<pre class=" language-undefined"><code class="prism language-{r} language-undefined">swirl()
</code></pre>
<p><strong>Pronto, você já pode acessar todos os cursos interativos disponíveis do swirl!</strong></p>
<hr>
<h1 id="guia-de-estudos">Guia de estudos</h1>
<p>Ao longo do code with pizza, você deverá aprender os seguintes tópicos, apresentados em dois cursos. Siga os tópicos traduzidos abaixo:</p>
<blockquote>
<ol>
<li>R programming (#7)</li>
</ol>
</blockquote>
<ul>
<li>Básico do R</li>
<li>Diretórios e arquivos</li>
<li>Álgebra</li>
<li>Formatos de arquivos</li>
<li>Vetores</li>
<li>Matrizes e Data Frames</li>
<li>Lógica de programação</li>
<li>Funções</li>
<li>lapply, saplly, vapply e tapply</li>
<li>Análise de dados</li>
<li>Simulação</li>
<li>Datas e horários</li>
</ul>
<blockquote>
<ol start="2">
<li>Exploratory Data Analysis (#3)</li>
</ol>
</blockquote>
<ul>
<li>Princípios de análise de gráficos</li>
<li>Gráficos exploratórios</li>
<li>Sistemas de plotagem de dados</li>
<li>Sistema de plotagem Base</li>
<li>Sistema de plotagem Lattice</li>
<li>Trabalhando com cores</li>
<li>GGPlot2 (partes 1, 2 e extras)</li>
<li>Clusterização hierárquica</li>
<li>Clusterização K Means</li>
<li>Redução de dimensionalidade</li>
<li>Exemplo de clusterização</li>
<li>Estudo de caso</li>
</ul>
<h2 id="instalação-dos-pacotes-usados-no-curso">Instalação dos pacotes usados no curso</h2>
<p>Antes de participar do evento, indico que instalem os seguintes pacotes em casa, uma vez que a conexão wi-fi da faculdade pode não funcionar na hora (lei de Murphy, people).</p>
<blockquote>
<p>São muitos tópicos a serem estudados. Mas, não se preocupem, teremos muita pizza e refrigerante para animarmos nossa noite de programação! &lt;3</p>
</blockquote>
<blockquote>
<p>##<strong>Para dar uma ajuda durante o curso e no futuro, use os Cheatsheets presentes na pasta “Cheatsheets” da pasta do curso.</strong></p>
</blockquote>
<h1 id="links-úteis">Links úteis</h1>
<ul>
<li><a href="https://rseek.org/:">https://rseek.org/:</a> Ajuda sobre qualquer dúvida relacionada à linguagem, pacotes/bibliotecas, funções, etc.</li>
<li><a href="https://www.r-graph-gallery.com">https://www.r-graph-gallery.com</a>: Galeria de exemplos de gráficos feitos no R, com código aberto. Gostou de um gráfico? Copie e cole o código e adapte seus dados a ele.</li>
<li><a href="https://www.rdocumentation.org/:">https://www.rdocumentation.org/:</a> Documentação do R.</li>
</ul>

    </div>
  </div>
</body>

</html>

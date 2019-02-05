<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Reprodução da estrutura 3D de proteínas usando o PyMol</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#reprodução-da-estrutura-3d-de-proteínas-usando-o-pymol">Reprodução da estrutura 3D de proteínas usando o PyMol</a>
<ul>
<li><a href="#buscando-estruturas-no-pdb">Buscando estruturas no PDB</a></li>
<li><a href="#buscando-informações-sobre-a-proteína-no-proteopedia">Buscando informações sobre a proteína no Proteopedia</a></li>
<li><a href="#visualizando-a-estrutura-no-pymol">Visualizando a estrutura no PyMol</a></li>
<li><a href="#converta-as-imagens-em-vídeo-com-gifmaker">Converta as imagens em vídeo com Gifmaker</a></li>
<li><a href="#edite-o-vídeo.">Edite o vídeo.</a></li>
</ul>
</li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="reprodução-da-estrutura-3d-de-proteínas-usando-o-pymol">Reprodução da estrutura 3D de proteínas usando o PyMol</h1>
<p>Neste manual, iremos fazer a representação da proteína Insulina. Precisaremos de acesso à internet e do software <a href="https://pymol.org/2/">PyMol</a></p>
<h2 id="buscando-estruturas-no-pdb">Buscando estruturas no PDB</h2>
<ol>
<li>
<p>Crie um diretório/pasta no seu computador com o nome da molécula. Lembre-se, no fim deste tutorial, de fazer o upload da pasta para o Google Drive da Liga;</p>
</li>
<li>
<p>Entre no <a href="https://www.rcsb.org/">site do PDB</a> e pesquise pelo nome genérico da proteína (Insulin).</p>
</li>
<li>
<p>Faça o refinamento da busca quando as estruturas forem listadas. Neste caso, queremos só <strong>insulina humana</strong> (<strong>Organism: Homo sapiens only</strong>), somente a Insulin, <strong>não Insulin-receptor ou Insulin-degrading enzyme</strong>, tem de ser <strong>100% Representativa</strong> e a <strong>Resolução</strong> tem de ser alta (no caso, &lt;1.499A). O texto de busca deve parecer com este:</p>
</li>
</ol>
<pre><code>Text Search for: insulin and TAXONOMY is just Homo sapiens (human) and TAXONOMY is only just Homo sapiens (human) and Molecule : Insulin [P01308, P01315, P01317, P01318, P30410, P67974] 
</code></pre>
<ol start="4">
<li>Escolha uma estrutura. Aqui, escolheremos a <strong>5E7W</strong>.</li>
<li>Faça o Download da molécula em <strong>PDB Format</strong>. É possível também baixar em <strong>Biological Assembly .gz</strong> - neste formato, é baixada estrutura da proteína + ligantes. No caso, somente usaremos o arquivo .pdb.</li>
<li>Abra um bloco de notas e copie as informações da página. Elas serão úteis para quando formos apresentá-la no post dela.</li>
</ol>
<blockquote>
<p><strong>Nome</strong>: 5E7W<br>
<strong>O que é</strong>: X-ray Structure of Human Recombinant 2Zn insulin at 0.92 Angstrom<br>
<strong>DOI</strong>: 10.2210/pdb5E7W/pdb<br>
<strong>Classification</strong>: IMMUNE SYSTEM<br>
<strong>Organism(s)</strong>: Homo sapiens<br>
<strong>Expression System</strong>: Komagataella pastoris<br>
<strong>Deposited</strong>: 2015-10-13 <strong>Released</strong>: 2016-10-12<br>
<strong>Deposition Author(s)</strong>: Lisgarten, D.R., Naylor, C.E., Palmer, R.A., Lobley, C.M.C.<br>
<strong>Macromolecule Content</strong><br>
Total Structure Weight: 11885.26<br>
Atom Count: 904<br>
Residue Count: 102<br>
Unique protein chains: 2<br>
<strong>PubMed Abstract</strong>: The crystal structure of a commercially available form of human recombinant (HR) insulin, Insugen (I), used in the treatment of diabetes has been determined to 0.92 Å resolution using low temperature, 100 K, synchrotron X-ray data collected at 16,000 keV (λ = 0.77 Å). Refinement carried out with anisotropic displacement parameters, removal of main-chain stereochemical restraints, inclusion of H atoms in calculated positions, and 220 water molecules, converged to a final value of R = 0.1112 and Rfree = 0.1466. The structure includes what is thought to be an ordered propanol molecule (POL) only in chain D(4) and a solvated acetate molecule (ACT) coordinated to the Zn atom only in chain B(2). Possible origins and consequences of the propanol and acetate molecules are discussed(…)</p>
</blockquote>
<h2 id="buscando-informações-sobre-a-proteína-no-proteopedia">Buscando informações sobre a proteína no Proteopedia</h2>
<ol>
<li>Acesse a <a href="https://proteopedia.org/wiki/index.php/Molecular_Playground/Insulin">Proteopedia</a> da proteína e copie o texto e cole no mesmo arquivo aberto no bloco de notas. Traduza as informações mais importantes, como <strong>Função</strong>, <strong>Onde é expressa</strong>, <strong>Importância biológica e terapêutica (se houver)</strong>, <strong>Estrutura</strong>, <strong>Como funciona</strong> e sua <strong>Farmacodinâmica</strong>:</li>
</ol>
<blockquote>
<p><strong>Função e como funciona</strong>: Insulin is a hormone that controls carbohydrate metabolism and storage in the human body. &gt; <strong>Como funciona</strong>: This is the form that binds the insulin receptor on fat or muscle cells in the body, singling them to take up glucose, or sugar, from the blood and save it for later.<br>
<strong>Importância e Onde é expressa</strong>: The body is able to sense the concentration of glucose in the blood and respond by secreting insulin, which is produced by beta cells in the pancreas .<br>
<strong>Importância Médica</strong>: Synthesis of human insulin in E. coli is important to producing insulin for the treatment of type 1 diabetes.<br>
<strong>Estrutura</strong>: Insulin is made up of two pieces called the A- and B-chain, shown in grey and green respectively. These two chains are joined by disulfide bonds, which are shown in yellow. This single piece made up of the A- and B-chains is the active form of the insulin hormone.</p>
</blockquote>
<h2 id="visualizando-a-estrutura-no-pymol">Visualizando a estrutura no PyMol</h2>
<ol>
<li>Abra o Pymol.</li>
<li>Abra o arquivo .pdb.</li>
</ol>
<pre><code>File &gt; Open &gt; Pasta &gt; "5E7W.pdb"
</code></pre>
<ol start="3">
<li>Altere a representação. No canto direito, clique no “S” (Show) ao lado do item da lista “5e7w” &gt; “as” &gt; “cartoon”.</li>
<li>Cadeias laterais e principais e pontes dissulfeto.</li>
</ol>
<pre><code>Show &gt; main chain &gt; sticks.
Show &gt; disulfides &gt; lines
</code></pre>
<ol start="5">
<li>Coloração ©.</li>
</ol>
<pre><code>Color &gt; By rep &gt; sticks &gt; oranges &gt; orange 
Color &gt; By rep &gt; cartoon &gt; grays &gt; white
</code></pre>
<ol start="6">
<li>Video. Digite os comandos abaixo na linha de comando do pymol (PyMOL&gt;):</li>
</ol>
<pre><code>mset 1 x90
util.mroll(1,90,1)
mplay 
</code></pre>
<ol start="7">
<li>Salve o vídeo. O vídeo será salvo como múltiplas imagens/frames.</li>
</ol>
<pre><code>File &gt; Save movie as &gt; PNG Images &gt; Pasta da molécula
</code></pre>
<h2 id="converta-as-imagens-em-vídeo-com-gifmaker">Converta as imagens em vídeo com <a href="https://giphy.com/create/">Gifmaker</a></h2>
<ul>
<li>Faça o upload dos frames e defina o tempo para 0.1s.</li>
<li>Adicione uma legenda com o nome da proteína. Escolha a opção de fonte pixelada e o efeito wavy.</li>
<li>Adicione um filtro. Escolha o rainbow.</li>
<li>Dê um nome ao gif, assim como tags.</li>
<li>Quando estiver concluído, clique com o botão direito no gif gerado e salve o arquivo na pasta.</li>
</ul>
<h2 id="edite-o-vídeo.">Edite o vídeo.</h2>
<p>Adicione as informações extraídas do proteopedia traduzidas no vídeo, utilizando seu editor de vídeo favorito.</p>
<p><strong>Função e como funciona</strong>: A Insulina é um peptídeo hormonal que controla o metabolismo e estoque de carboidratos no corpo humano</p>
<blockquote>
<p><strong>Como funciona</strong>: O gif mostra a forma ativa, que se liga no receptor de insulina expresso nos adipócitos ou nas células musculares, ativando uma cascata de sinalização para o transporte de glucose do sangue para dentro da célula.<br>
<strong>Importância e Onde é expressa</strong>: A insulina é expressa pelas células beta-pancreáticas.<br>
<strong>Importância Médica</strong>: A síntese de insulina humana em E. coli é importante para o tratamento de diabetes.<br>
<strong>Estrutura</strong>: O peptídeo é composto de duas cadeias, A e B. Ambas são unidas por ligações dissulfeto.</p>
</blockquote>

    </div>
  </div>
</body>

</html>

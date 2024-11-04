Original file line number	Diff line number	Diff line change
@@ -1 +1,17 @@
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AluraBooks</title>
    <link rel="stylesheet" href="reset.css">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Alurabook</h1>
</body>
</html>
‎reset.css
+135
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,135 @@
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/
html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
    display: block;
}
body {
    line-height: 1;
}
ol,
ul {
    list-style: none;
}
blockquote,
q {
    quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
    content: '';
    content: none;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
}
‎styles.css
+11
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,11 @@
:root {
    --cor-de-fundo: #EBECEE;
}
body {
    background-color: var(--cor-de-fundo);
}
h1 {
    background-color: white;
}
</head>

<body>
    <h1>Alurabook</h1>
    <header class="cabeçalho">
        <span class="cabeçalho__menu-hamburguer"></span>
        <img src="img/Logo.svg" alt="Logo da AluraBooks">
        <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos"></a>
        <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras"></a>
        <a href="#"><img src="img/Usuario.svg" alt="Meu perfil"></a>
    </header>
</body>

</html>
</html>
‎styles.css
+3
-4
Original file line number	Diff line number	Diff line change
@@ -1,11 +1,10 @@
@import url("styles/header.css");
:root {
    --cor-de-fundo: #EBECEE;
    --branco: #FFFFFF;
}

body {
    background-color: var(--cor-de-fundo);
}
h1 {
    background-color: white;
}
‎styles/header.css
+21
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,21 @@
.cabeçalho_menu-hamburguer {
    width: 24px;
    height: 24px;
    display: inline-block;
    background-image: url("../img/Menu.svg");
    background-repeat: no-repeat;
    background-position: center;
}
.cabeçalho {
    background-color: var(--branco);
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
}
.container {
    display: flex;
    align-items: center;
}<body>
    <header class="cabeçalho">
        <span class="cabeçalho__menu-hamburguer"></span>
        <img src="img/Logo.svg" alt="Logo da AluraBooks">
        <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos"></a>
        <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras"></a>
        <a href="#"><img src="img/Usuario.svg" alt="Meu perfil"></a>
        <div class="container">
            <span class="cabeçalho__menu-hamburguer container__imagem"></span>
            <img src="img/Logo.svg" alt="Logo da AluraBooks" class="container__imagem">
        </div>
        <div class="container">
            <input type="checkbox" id="menu" class="container__botao">
            <label for="menu">
                    <span class="cabeçalho__menu-hamburguer container__imagem"></span>
            </label>
            <ul class="lista-menu">
                <li class="lista-menu_titulo">Categorias</li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Programação</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Front-end</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Infraestrutura</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Business</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Design & UX</a>
                </li>
              </ul>
            <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos" class="container__imagem"></a>
            <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras" class="container__imagem"></a>
            <a href="#"><img src="img/Usuario.svg" alt="Meu perfil" class="container__imagem"></a>
        </div>
    </header>
</body>

‎styles/header.css
+15
-1
Original file line number	Diff line number	Diff line change
@@ -18,4 +18,18 @@
.container {
    display: flex;
    align-items: center;
}
}
.container__imagem {
    padding: 1em;
}
.lista-menu {
    display: none;
    position: absolute;
    top:100%;
}
.container__botao:checked ~ .lista-menu {
    display: block;
}
:root {
    --cor-de-fundo: #EBECEE;
    --branco: #FFFFFF;
    --laranja: #EB9B00;
    --azul-degrade: linear-gradient(97.54deg, #002F52 35.49%, #326589 165.37%);
}

body {
‎styles/header.css
+21
-1
Original file line number	Diff line number	Diff line change
@@ -27,9 +27,29 @@
.lista-menu {
    display: none;
    position: absolute;
    top:100%;
    top: 100%;
    width: 60vw;
}

.container__botao:checked ~ .lista-menu {
    display: block;
}
.lista-menu__titulo,
.lista-menu__item {
    padding: 1em;
    background-color: var(--branco);
}
.lista-menu__titulo {
    color: var(--laranja);
    font-weight: 700;
}
.lista-menu__link {
    background: var(--azul-degrade);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
}
<html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AluraBooks</title>
    <link rel="stylesheet" href="reset.css">
    <link rel="stylesheet" href="styles.css">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AluraBooks</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="styles.css">
</head>

<body>
    <header class="cabeçalho">
        <div class="container">
            <span class="cabeçalho__menu-hamburguer container__imagem"></span>
            <img src="img/Logo.svg" alt="Logo da AluraBooks" class="container__imagem">
        </div>
        <div class="container">
            <input type="checkbox" id="menu" class="container__botao">
            <label for="menu">
                    <span class="cabeçalho__menu-hamburguer container__imagem"></span>
            </label>
            <ul class="lista-menu">
                <li class="lista-menu_titulo">Categorias</li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Programação</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Front-end</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Infraestrutura</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Business</a>
                </li>
                <li class="lista-menu_item">
                  <a href="#" class="lista-menu_link">Design & UX</a>
                </li>
              </ul>
            <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos" class="container__imagem"></a>
            <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras" class="container__imagem"></a>
            <a href="#"><img src="img/Usuario.svg" alt="Meu perfil" class="container__imagem"></a>
        </div>
    </header>
  <header class="cabeçalho">
    <div class="container">
      <span class="cabeçalho__menu-hamburguer container__imagem"></span>
      <img src="img/Logo.svg" alt="Logo da AluraBooks" class="container__imagem">
    </div>
    <div class="container">
      <input type="checkbox" id="menu" class="container__botao">
      <label for="menu">
        <span class="cabeçalho__menu-hamburguer container__imagem"></span>
      </label>
      <ul class="lista-menu">
        <li class="lista-menu_titulo">Categorias</li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Programação</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Front-end</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Infraestrutura</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Business</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Design & UX</a>
        </li>
      </ul>
      <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos" class="container__imagem"></a>
      <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras" class="container__imagem"></a>
      <a href="#"><img src="img/Usuario.svg" alt="Meu perfil" class="container__imagem"></a>
    </div>
  </header>
  <section class="banner">
    <h2 class="banner__titulo">Já sabe por onde começar?</h2>
    <p class="banner__texto">Encontre em nossa estante o que precisa para seu desenvolvimento!
    <p>
      <input type="search" class="banner_pesquisa" placeholder="Qual será sua próxima leitura?">
  </section>
</body>

</html>
‎styles.css
+4
Original file line number	Diff line number	Diff line change
@@ -1,4 +1,8 @@
@import url("styles/header.css");
@import url("styles/banner.css");
/* código omitido */

:root {
    --cor-de-fundo: #EBECEE;
‎styles/banner.css
+35
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,35 @@
.banner {
    background: var(--azul-degrade);
    color: var(--branco);
    text-align: center;
    padding: 2.5em 2em;
}
.banner__titulo {
    font-size: 18px;
    font-weight: 700;
}
.banner__texto {
    font-weight: 500;
    margin: 1em0;
}
.banner__pesquisa {
    background-color: transparent;
    border: 1px solid var(--branco);
    color: var(--branco);
    border-radius: 24px;
    padding: 1em;
    width: 100%;
}
.banner__pesquisa::placeholder {
    font-family: var(--fonte-principal);
    font-size: 14px;
    font-weight: 400;
    text-align: center;
    color: var(--branco);
    background: url("../img/Lupa.svg") no-repeat;
    background-position: 1em;
}
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AluraBooks</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://unpkg.com/swiper@8/swiper-bundle.min.css" />
  <link rel="stylesheet" href="styles.css">
</head>

@@ -50,6 +54,41 @@ <h2 class="banner__titulo">Já sabe por onde começar?</h2>
    <p>
      <input type="search" class="banner_pesquisa" placeholder="Qual será sua próxima leitura?">
  </section>
  <section class="carrossel">
    <h2 class="carrossel__titulo">Novos lançamentos</h2>
    <!-- Slider main container -->
    <div class="swiper">
      <!-- Additional required wrapper -->
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="img/ApacheKafka.svg"
            alt="Livro sobre apache kafka e spring boot da alura books"></div>
        <div class="swiper-slide"><img src="img/Liderança.svg" alt="Livro sobre liderança em design da alura books">
        </div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alurabooks">
        </div>
        <div class="swiper-slide"><img src="img/Guia Front-end.svg" alt="Livro Guia front end"></div>
        <div class="swiper-slide"><img src="img/Portugol.svg" alt="Livro sobre portugol"></div>
        <div class="swiper-slide"><img src="img/Acessibilidade.svg" alt="livro sobre acessibilidade"></div>
      </div>
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
      <!-- If we need scrollbar -->
      <div class="swiper-scrollbar"></div>
    </div>
  </section>
  <script src="https://unpkg.com/swiper@8/swiper-bundle.min.js"></script>
</body>

</html>
‎styles.css
+1
Original file line number	Diff line number	Diff line change
@@ -1,5 +1,6 @@
@import url("styles/header.css");
@import url("styles/banner.css");
@import url("styles/carrossel.css");

/* código omitido */

‎styles/carrossel.css
+9
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,9 @@
.carrossel__titulo {
    color: var(--laranja);
    background-color: var(--branco);
    text-align: center;
    text-transform: uppercase;
    font-size: 18px;
    font-weight: 700;
    padding: 2em 0 1em 0;
}
 <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://unpkg.com/swiper@8/swiper-bundle.min.css" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <header class="cabeçalho">
    <div class="container">
      <span class="cabeçalho__menu-hamburguer container__imagem"></span>
      <img src="img/Logo.svg" alt="Logo da AluraBooks" class="container__imagem">
    </div>
    <div class="container">
      <input type="checkbox" id="menu" class="container__botao">
      <label for="menu">
        <span class="cabeçalho__menu-hamburguer container__imagem"></span>
      </label>
      <ul class="lista-menu">
        <li class="lista-menu_titulo">Categorias</li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Programação</a>
        <li class="lista-menu__titulo">Categorias</li>
        <li class="lista-menu__item">
          <a href="#" class="lista-menu__link">Programação</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Front-end</a>
        <li class="lista-menu__item">
          <a href="#" class="lista-menu__link">Front-end</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Infraestrutura</a>
        <li class="lista-menu__item">
          <a href="#" class="lista-menu__link">Infraestrutura</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Business</a>
        <li class="lista-menu__item">
          <a href="#" class="lista-menu__link">Business</a>
        </li>
        <li class="lista-menu_item">
          <a href="#" class="lista-menu_link">Design & UX</a>
        <li class="lista-menu__item">
          <a href="#" class="lista-menu__link">Design & UX</a>
        </li>
      </ul>
      <img src="img/Logo.svg" alt="Logo da Alurabooks" class="container__imagem">
    </div>
    <div class="container">
      <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos" class="container__imagem"></a>
      <a href="#"><img src="img/Compras.svg" alt="Carrinho de compras" class="container__imagem"></a>
      <a href="#"><img src="img/Usuario.svg" alt="Meu perfil" class="container__imagem"></a>
@@ -50,45 +49,58 @@

  <section class="banner">
    <h2 class="banner__titulo">Já sabe por onde começar?</h2>
    <p class="banner__texto">Encontre em nossa estante o que precisa para seu desenvolvimento!
    <p>
      <input type="search" class="banner_pesquisa" placeholder="Qual será sua próxima leitura?">
    <p class="banner__texto">Encontre em nossa estante o que precisa para seu desenvolvimento!</p>
    <input type="search" class="banner__pesquisa" placeholder="Qual será sua próxima leitura?">
  </section>

  <section class="carrossel">
    <h2 class="carrossel__titulo">Novos lançamentos</h2>
    <!-- Slider main container -->
    <div class="swiper">
      <!-- Additional required wrapper -->
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="img/ApacheKafka.svg"
        <div class="swiper-slide"><img src="img/Apachekafka.svg"
            alt="Livro sobre apache kafka e spring boot da alura books"></div>
        <div class="swiper-slide"><img src="img/Liderança.svg" alt="Livro sobre liderança em design da alura books">
        <div class="swiper-slide"><img src="img/Liderança.svg"
            alt="Livro sobre liderança em design design da alura books"></div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alura books">
        </div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alurabooks">
        <div class="swiper-slide">
          <img src="img/Guia Front-end.svg" alt="Livro Guia front end" />
        </div>
        <div class="swiper-slide">
          <img src="img/Portugol.svg" alt="Livro sobre portugol" />
        </div>
        <div class="swiper-slide">
          <img src="img/Acessibilidade.svg" alt="Livro sobre acessibilidade" />
        </div>
        <div class="swiper-slide"><img src="img/Guia Front-end.svg" alt="Livro Guia front end"></div>
        <div class="swiper-slide"><img src="img/Portugol.svg" alt="Livro sobre portugol"></div>
        <div class="swiper-slide"><img src="img/Acessibilidade.svg" alt="livro sobre acessibilidade"></div>
      </div>
    </div>
    <!-- If we need pagination -->
    <div class="swiper-pagination"></div>

      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    <!-- If we need navigation buttons -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>

      <!-- If we need scrollbar -->
      <div class="swiper-scrollbar"></div>
    <!-- If we need scrollbar -->
    <div class="swiper-scrollbar"></div>
    </div>
  </section>

  <script src="https://unpkg.com/swiper@8/swiper-bundle.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <script>
    const swiper = new Swiper(".swiper", {
      spaceBetween: 10,
      slidesPerView: 3,
      pagination: {
        el: ".swiper-pagination",
        type: "bullets",
      },
    });
  </script>
</body>

</html>
‎styles.css
+4
Original file line number	Diff line number	Diff line change
@@ -10,8 +10,12 @@
    --branco: #FFFFFF;
    --laranja: #EB9B00;
    --azul-degrade: linear-gradient(97.54deg, #002F52 35.49%, #326589 165.37%);
    --fonte-principal: "Poppins";
}

body {
    background-color: var(--cor-de-fundo);
    font-family: var(--fonte-principal);
    font-size: 16px;
    font-weight: 400;
}
‎styles/carrossel.css
+17
-1
Original file line number	Diff line number	Diff line change
@@ -5,5 +5,21 @@
    text-transform: uppercase;
    font-size: 18px;
    font-weight: 700;
    padding: 2em 0 1em 0;
    padding: 1em 0 0.5em 0;
}
.swiper-slide img {
    width: 100%;
}
.swiper-button-prev,
.swiper-button-next {
    display: none;
}
.swiper-pagination {
    position: initial;
    margin: .5em 0;
}
    <div class="swiper-slide">
          <img src="img/Acessibilidade.svg" alt="Livro sobre acessibilidade" />
        </div>
        <!-- If we need navigation buttons -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>

      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
    <div class="card">
      <div class="card__descrição">
        <div class="descrição">
          <h3 class="descrição__titulo">Talvez você também se interesse por...</h3>
          <h2 class="descrição__titulo-livro">Angular 11 e Firebase</h2>
          <p class="descrição__texto">
            Construindo uma aplicação integrada com a plataforma do Google.
          </p>
        </div>
        <img src="img/Angular.svg" class="descrição__imagem" />
      </div>
      <div class="card__botões">
        <ul class="botões">
          <li class="botões__item">
            <img src="img/Favoritos.svg" alt="Favoritar livro" />
          </li>
          <li class="botões__item">
            <img src="img/Compras.svg" alt="Adicionar no carrinho de compras" />
          </li>
        </ul>
        <a href="#" class="botões__ancora">Saiba mais</a>
      </div>
    </div>

  </section>
‎styles.css
+3
-5
Original file line number	Diff line number	Diff line change
@@ -2,20 +2,18 @@
@import url("styles/banner.css");
@import url("styles/carrossel.css");

/* código omitido */
:root {
    --cor-de-fundo: #EBECEE;
    --branco: #FFFFFF;
    --laranja: #EB9B00;
    --azul-degrade: linear-gradient(97.54deg, #002F52 35.49%, #326589 165.37%);
    --azul-degrade: linear-gradient(97.54deg, #002f52 35.49%, #326589 165.37%);
    --fonte-principal: "Poppins";
    --azul: #002F52;
}

body {
    background-color: var(--cor-de-fundo);
    font-family: var(--fonte-principal);
    font-size: 16px;
    font-weight: 400;
}
}
‎styles/carrossel.css
+53
Original file line number	Diff line number	Diff line change
@@ -22,4 +22,57 @@
.swiper-pagination {
    position: initial;
    margin: .5em 0;
}
.card {
    background: var(--branco);
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
    margin: 1em;
    padding: 1em;
}
.card__descrição {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.5em;
}
.card__botões {
    display: flex;
    justify-content: space-between;
}
.botões {
    display: flex;
}
.descrição__titulo {
    color: var(--laranja);
    font-weight: 700;
}
.descrição__titulo-livro {
    color: var(--azul);
    font-size: 18px;
    font-weight: 700;
    margin: 0.5em 0;
}
.descrição__texto {
    font-size: 14px;
}
.botões__ancora {
    background-color: var(--laranja);
    padding: 1em 2.2em;
    color: var(--branco);
    font-weight: 700;
    text-decoration: none;
}
.botões__item {
    margin: 0 0.5em;
}
  </section>

  <section class=”carrossel”>
    <h2 class="carrossel__titulo">Mais vendidos</h2>
    <div class="swiper">
      <!-- Additional required wrapper -->
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="img/ApacheKafka.svg"
            alt="Livro sobre apache kafka e spring boot da alura books"></div>
        <div class="swiper-slide"><img src="img/Liderança.svg" alt="Livro sobre liderança em design da alura books">
        </div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alurabooks">
        </div>
        <div class="swiper-slide"><img src="img/Guia Front-end.svg" alt="Livro Guia front end"></div>
        <div class="swiper-slide"><img src="img/Portugol.svg" alt="Livro sobre portugol"></div>
        <div class="swiper-slide"><img src="img/Acessibilidade.svg" alt="livro sobre acessibilidade"></div>
      </div>
      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
    <div class="card">
      <!-- 1º linha -->
      <div class="card__descrição">
        <!-- 1º coluna -->
        <div class="descrição">
          <img src="img/Estrelinhas.svg" alt="Avaliação 5 estrelas">
          <h3 class="descrição__titulo">Autora do Mês</h3>
          <h2 class="descrição__titulo-livro">Juliana Agarikov</h2>
          <p class="descrição__texto">Analista de sistemas e escritora, Juliana é especialista em Front-End.
          </p>
        </div>
        <!-- 2º coluna -->
        <img src="img/Escritora.svg" class="descrição__imagem">
      </div>
      <!-- 2º linha -->
      <div class="card__botões">
        <!-- 1º coluna -->
        <ul class="botões">
          <li class="botões__item"><img src="img/Favoritos.svg" alt="Favoritar livro"></li>
          <li class="botões__item"><img src="img/Compras.svg" alt="Adicionar no carrinho de compras"></li>
        </ul>
        <!-- 2º coluna -->
        <a href="#" class="botões__ancora">Saiba mais</a>
      </div>
    </div>
  </section>
  <section class="tópicos">
    <h2 class="tópicos__titulo">TÓPICOS VISITADOS RECENTEMENTE</h2>
    <ul class="tópicos__lista">
      <li class="tópicos__item"><a href="#" class="tópicos__link">Android</a></li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">Marketing Digital</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">Agile</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">Startups</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">HTML & CSS</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">Python</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">OO</a>
      </li>
      <li class="tópicos__item">
        <a href="#" class="tópicos__link">Java</a>
      </li>
    </ul>
  </section>
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <script>
    const swiper = new Swiper(".swiper", {
‎styles.css
+1
Original file line number	Diff line number	Diff line change
@@ -1,6 +1,7 @@
@import url("styles/header.css");
@import url("styles/banner.css");
@import url("styles/carrossel.css");
@import url("styles/topicos.css");

:root {
    --cor-de-fundo: #EBECEE;
‎styles/topicos.css
+30
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,30 @@
.tópicos {
    background: var(--azul-degrade);
    text-align: center;
    padding: 1em 0;
}
.tópicos__titulo {
    color: var(--branco);
    font-weight: 300;
    margin-bottom: 1em;
}
.tópicos__lista {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.tópicos__item {
    margin: 2em 0.5em;
}
.tópicos__link {
    color: var(--branco);
    padding: 1em;
    background-color: var(--laranja);
    text-decoration: none;
    font-size: 14px;
    font-weight: 700;
}
    </ul>
  </section>

  <section class="contato">
    <h2 class="contato__titulo">Fique por dentro das novidades!</h2>
    <p class="contato__texto">
      Atualizações de e-books, novos livros, promoções e outros.
    </p>
    <input type="email" placeholder="Cadastre seu e-mail" class="contato__email" />
  </section>
  <hr />
  <footer class="rodapé">
    <h2 class="rodapé__titulo">Grupo Alura</h2>
  </footer>
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <script>
    const swiper = new Swiper(".swiper", {
‎styles.css
+2
Original file line number	Diff line number	Diff line change
@@ -2,6 +2,8 @@
@import url("styles/banner.css");
@import url("styles/carrossel.css");
@import url("styles/topicos.css");
@import url("styles/contato.css");
@import url("styles/rodapé.css");

:root {
    --cor-de-fundo: #EBECEE;
‎styles/contato.css
+37
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,37 @@
.contato {
    background-color: var(--branco);
    padding: 1em;
}
.contato__titulo,
.contato__texto {
    background: var(--azul-degrade);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
.contato__titulo {
    font-size: 18px;
    font-weight: 500;
}
.contato__texto {
    font-weight: 300;
    margin: 1em 0;
}
.contato__email {
    padding: 1em;
    border: 1px solid var(--azul);
    border-radius: 24px;
    width: 90%;
    color: var(--azul);
}
.contato__email::placeholder {
    font-family: var(--fonte-principal);
    color: var(--azul);
    background: url("../img/Email.svg") no-repeat;
    padding-left: 2em;
}
   </ul>
  </section>

  <section class="contato">
    <h2 class="contato__titulo">Fique por dentro das novidades!</h2>
    <p class="contato__texto">
      Atualizações de e-books, novos livros, promoções e outros.
    </p>
    <input type="email" placeholder="Cadastre seu e-mail" class="contato__email" />
  </section>
  <hr />
  <footer class="rodapé">
    <h2 class="rodapé__titulo">Grupo Alura</h2>
  </footer>
  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
  <script>
    const swiper = new Swiper(".swiper", {
‎styles.css
+2
Original file line number	Diff line number	Diff line change
@@ -2,6 +2,8 @@
@import url("styles/banner.css");
@import url("styles/carrossel.css");
@import url("styles/topicos.css");
@import url("styles/contato.css");
@import url("styles/rodapé.css");

:root {
    --cor-de-fundo: #EBECEE;
‎styles/contato.css
+37
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,37 @@
.contato {
    background-color: var(--branco);
    padding: 1em;
}
.contato__titulo,
.contato__texto {
    background: var(--azul-degrade);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
.contato__titulo {
    font-size: 18px;
    font-weight: 500;
}
.contato__texto {
    font-weight: 300;
    margin: 1em 0;
}
.contato__email {
    padding: 1em;
    border: 1px solid var(--azul);
    border-radius: 24px;
    width: 90%;
    color: var(--azul);
}
.contato__email::placeholder {
    font-family: var(--fonte-principal);
    color: var(--azul);
    background: url("../img/Email.svg") no-repeat;
    padding-left: 2em;
}
‎styles/rodapé.css
+8
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,8 @@
hr {
    margin: 0;
}
.rodapé {
    background-color: var(--branco);
    padding: 1em;
}
  -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
}
@media screen and (min-width: 1024px) {
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css?family=Josefin+Sans:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
  <link rel="stylesheet" href="styles.css">
</head>
@@ -39,9 +40,39 @@
        </li>
      </ul>
      <img src="img/Logo.svg" alt="Logo da Alurabooks" class="container__imagem">
      <h1 class="container__titulo"><b class="container__titulo--negrito">Alura</b>Books</h1>
      <ul class="opções">
        <input type="checkbox" id="opções-menu" class="opções__botão" />
        <label for="opções-menu">
          <li class="opções__item">Categorias</li>
        </label>
        <ul class="lista-menu">
          <li class="lista-menu__item">
            <a href="#" class="lista-menu__link">Programação</a>
          </li>
          <li class="lista-menu__item">
            <a href="#" class="lista-menu__link">Front-end</a>
          </li>
          <li class="lista-menu__item">
            <a href="#" class="lista-menu__link">Infraestrutura</a>
          </li>
          <li class="lista-menu__item">
            <a href="#" class="lista-menu__link">Business</a>
          </li>
          <li class="lista-menu__item">
            <a href="#" class="lista-menu__link">Design & UX</a>
          </li>
        </ul>
        <li class="opções__item"><a href="#" class="opções__link">Favoritos</a></li>
        <li class="opções__item"><a href="#" class="opções__link">Minha estante</a></li>
      </ul>
    </div>
    <div class="container">
      <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos" class="container__imagem"></a>
      <a href="#"><img src="img/Favoritos.svg" alt="Meus favoritos"
          class="container__imagem container__imagem-transparente"></a>
      <a href="#"><img src="img/Compras.svg" alt="Carrinhos de compras" class="container__imagem"></a>
      <a href="#"><img src="img/Usuario.svg" alt="Meu perfil" class="container__imagem"></a>
    </div>
‎styles.css
+3
Original file line number	Diff line number	Diff line change
@@ -5,13 +5,16 @@
@import url("styles/contato.css");
@import url("styles/rodapé.css");

:root {
    --cor-de-fundo: #EBECEE;
    --branco: #FFFFFF;
    --laranja: #EB9B00;
    --azul-degrade: linear-gradient(97.54deg, #002f52 35.49%, #326589 165.37%);
    --fonte-principal: "Poppins";
    --azul: #002F52;
    --fonte-secundario: "Josefin Sans";
    --preto: #000000;
}

body {
‎styles/header.css
+61
-2
Original file line number	Diff line number	Diff line change
@@ -1,4 +1,4 @@
.cabeçalho_menu-hamburguer {
.cabeçalho__menu-hamburguer {
    width: 24px;
    height: 24px;
    display: inline-block;
@@ -24,14 +24,15 @@
    padding: 1em;
}

.lista-menu {
    display: none;
    position: absolute;
    top: 100%;
    width: 60vw;
}

.container__botao:checked ~ .lista-menu {
.container__botao:checked~.lista-menu {
    display: block;
}

@@ -54,6 +55,64 @@
    text-transform: uppercase;
}

.container__botao {
    display: none;
}
.container__titulo {
    display: none;
}
.opções {
    display: none
}
@media screen and (min-width: 1024px) {

    .container__titulo,
    .container__titulo--negrito {
        font-family: var(--fonte-secundario);
        font-size: 30px;
    }
    .container__titulo {
        font-weight: 400;
        display: block;
    }
    .container__titulo--negrito {
        font-weight: 700;
    }
    .opções {
        display: flex;
    }
    .opções__item {
        padding: 0 1em;
        text-transform: uppercase;
    }
    .opções__link {
        text-decoration: none;
        color: var(--preto);
    }
    .container__imagem-transparente {
        display: none;
    }
    .cabeçalho__menu-hamburguer {
        display: none;
    }
    .opções__botão:checked~.lista-menu {
        display: block;
        width: auto;
    }
    .opções__botão {
        display: none;
    }
}
   <h2 class="carrossel__titulo">Novos lançamentos</h2>
    <!-- Slider main container -->
    <div class="swiper">
      <div class="swiper-pagination"></div>
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
@@ -225,10 +227,12 @@ <h2 class="tópicos__titulo">TÓPICOS VISITADOS RECENTEMENTE</h2>
  </section>

  <section class="contato">
    <h2 class="contato__titulo">Fique por dentro das novidades!</h2>
    <p class="contato__texto">
      Atualizações de e-books, novos livros, promoções e outros.
    </p>
    <div class="contato__descrição">
      <h2 class="contato__titulo">Fique por dentro das novidades!</h2>
      <p class="contato__texto">
        Atualizações de e-books, novos livros, promoções e outros.
      </p>
    </div>
    <input type="email" placeholder="Cadastre seu e-mail" class="contato__email" />
  </section>

‎styles/banner.css
+14
Original file line number	Diff line number	Diff line change
@@ -32,4 +32,18 @@
    color: var(--branco);
    background: url("../img/Lupa.svg") no-repeat;
    background-position: 1em;
}
@media screen and (min-width: 1024px) {
    .banner__titulo {
        font-size: 36px;
    }
    .banner__pesquisa {
        width: 50%;
    }
    .banner__pesquisa::placeholder {
        background-position: 7em;
    }
}
‎styles/carrossel.css
+22
-3
Original file line number	Diff line number	Diff line change
@@ -12,16 +12,14 @@
    width: 100%;
}

.swiper-button-prev,
.swiper-button-next {
    display: none;
}

.swiper-pagination {
    position: initial;
    margin: .5em 0;
    margin: 0.5em 0;
}

.card {
@@ -75,4 +73,25 @@

.botões__item {
    margin: 0 0.5em;
}
@media screen and (min-width: 1024px) {
    .carrossel__titulo {
        font-size: 26px;
    }
    .swiper-pagination {
        margin: 2em 0 3em 0;
    }
    .swiper {
        width: 60%;
    }
    .swiper-button-prev,
    .swiper-button-next {
        display: block;
        top: 60%;
    }
}
‎styles/contato.css
+24
-2
Original file line number	Diff line number	Diff line change
@@ -32,6 +32,28 @@
.contato__email::placeholder {
    font-family: var(--fonte-principal);
    color: var(--azul);
    background: url("../img/Email.svg") no-repeat;
    padding-left: 2em;
    background: url("../img/email.svg") no-repeat 5%;
    padding-left: 5em;
}
@media screen and (min-width: 1024px) {
    .contato {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .contato__titulo {
        font-size: 24px;
    }
    .contato__descrição {
        margin-right: 1em;
        width: 30%;
    }
    .contato__email {
        width: 30%;
    }
}
‎styles/topicos.css
+10
Original file line number	Diff line number	Diff line change
@@ -27,4 +27,14 @@
    text-decoration: none;
    font-size: 14px;
    font-weight: 700;
}
@media screen and (min-width: 1024px) {
    .tópicos__titulo {
        font-size: 24px;
    }
    .tópicos__link {
        font-size: 24px;
    }
}

  <footer class="rodapé">
    <h2 class="rodapé__titulo">Grupo Alura</h2>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Educação</li>
      <li class="lista-rodapé__item">
        <img src="img/Caelum.svg" alt="Logo da Caelum" />
        <a href="#" class="lista-rodapé__link">Caelum</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/CasaDoCodigo.svg" alt="Logo da Casa do Código" />
        <a href="#" class="lista-rodapé__link">Casa do Código</a>
      </li>
    </ul>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Educação online</li>
      <li class="lista-rodapé__item">
        <img src="img/Alura.svg" alt="Logo da Alura" />
        <a href="#" class="lista-rodapé__link">Alura</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraEmpresas.svg" alt="Logo da AluraParaEmpresas" />
        <a href="#" class="lista-rodapé__link">Alura para Empresas</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraLATAM.svg" alt="Logo da Alura Latam" />
        <a href="#" class="lista-rodapé__link">Alura LATAM</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraStart.svg" alt="Logo da Alura START" />
        <a href="#" class="lista-rodapé__link">Alura Start</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/MusicDot.svg" alt="Logo da Music Dot" />
        <a href="#" class="lista-rodapé__link">Music Dot</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraLingua.svg" alt="Logo da Alura Lingua" />
        <a href="#" class="lista-rodapé__link">Alura Língua</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/PM3.svg" alt="Logo da PM3" />
        <a href="#" class="lista-rodapé__link">PM3</a>
      </li>
    </ul>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Comunidade</li>
      <li class="lista-rodapé__item">
        <img src="img/HipstersTech.svg" alt="Logo do Hipsters ponto Tech" />
        <a href="#" class="lista-rodapé__link">Hipsters ponto Tech</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/ScubaDev.svg" alt="Logo do Scuba Dev" />
        <a href="#" class="lista-rodapé__link">Scuba Dev</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/LayersTech.svg" alt="Logo do Layers ponto Tech" />
        <a href="#" class="lista-rodapé__link">Layers ponto Tech</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/LikeABoss.svg" alt="Logo do Like a Boss" />
        <a href="#" class="lista-rodapé__link">Like a Boss</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/CarreiraSemFronteira.svg" alt="Logo do Carreira sem fronteiras" />
        <a href="#" class="lista-rodapé__link">Carreira sem fronteiras</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/HipstersJobs.svg" alt="Logo do Hipsters ponto jobs" />
        <a href="#" class="lista-rodapé__link">Hipsters ponto jobs</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/GUJ.svg" alt="Logo do GUJ" />
        <a href="#" class="lista-rodapé__link">GUJ</a>
      </li>
    </ul>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
‎styles.css
+2
Original file line number	Diff line number	Diff line change
@@ -15,6 +15,8 @@
    --azul: #002F52;
    --fonte-secundario: "Josefin Sans";
    --preto: #000000;
    --cinza: #474646;
    --cinza-claro: #858585;
}

body {
‎styles/rodapé.css
+37
Original file line number	Diff line number	Diff line change
@@ -5,4 +5,41 @@ hr {
.rodapé {
    background-color: var(--branco);
    padding: 1em;
}
.lista-rodapé {
    display: none;
}
@media screen and (min-width: 1024px) {
    .rodapé {
        display: flex;
        justify-content: space-around;
    }
    .lista-rodapé {
        display: block;
    }
    .lista-rodapé__item {
        display: flex;
        align-items: center;
        margin: 0.6em 0;
    }
    .lista-rodapé__link {
        color: var(--cinza);
        text-decoration: none;
        margin-left: 0.6em;
    }
    .lista-rodapé__titulo {
        font-size: 14px;
        color: var(--cinza-claro);
    }
    .rodapé__titulo {
        font-size: 24px;
    }
}

  <footer class="rodapé">
    <h2 class="rodapé__titulo">Grupo Alura</h2>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Educação</li>
      <li class="lista-rodapé__item">
        <img src="img/Caelum.svg" alt="Logo da Caelum" />
        <a href="#" class="lista-rodapé__link">Caelum</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/CasaDoCodigo.svg" alt="Logo da Casa do Código" />
        <a href="#" class="lista-rodapé__link">Casa do Código</a>
      </li>
    </ul>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Educação online</li>
      <li class="lista-rodapé__item">
        <img src="img/Alura.svg" alt="Logo da Alura" />
        <a href="#" class="lista-rodapé__link">Alura</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraEmpresas.svg" alt="Logo da AluraParaEmpresas" />
        <a href="#" class="lista-rodapé__link">Alura para Empresas</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraLATAM.svg" alt="Logo da Alura Latam" />
        <a href="#" class="lista-rodapé__link">Alura LATAM</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraStart.svg" alt="Logo da Alura START" />
        <a href="#" class="lista-rodapé__link">Alura Start</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/MusicDot.svg" alt="Logo da Music Dot" />
        <a href="#" class="lista-rodapé__link">Music Dot</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/AluraLingua.svg" alt="Logo da Alura Lingua" />
        <a href="#" class="lista-rodapé__link">Alura Língua</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/PM3.svg" alt="Logo da PM3" />
        <a href="#" class="lista-rodapé__link">PM3</a>
      </li>
    </ul>
    <ul class="lista-rodapé">
      <li class="lista-rodapé__titulo">Comunidade</li>
      <li class="lista-rodapé__item">
        <img src="img/HipstersTech.svg" alt="Logo do Hipsters ponto Tech" />
        <a href="#" class="lista-rodapé__link">Hipsters ponto Tech</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/ScubaDev.svg" alt="Logo do Scuba Dev" />
        <a href="#" class="lista-rodapé__link">Scuba Dev</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/LayersTech.svg" alt="Logo do Layers ponto Tech" />
        <a href="#" class="lista-rodapé__link">Layers ponto Tech</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/LikeABoss.svg" alt="Logo do Like a Boss" />
        <a href="#" class="lista-rodapé__link">Like a Boss</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/CarreiraSemFronteira.svg" alt="Logo do Carreira sem fronteiras" />
        <a href="#" class="lista-rodapé__link">Carreira sem fronteiras</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/HipstersJobs.svg" alt="Logo do Hipsters ponto jobs" />
        <a href="#" class="lista-rodapé__link">Hipsters ponto jobs</a>
      </li>
      <li class="lista-rodapé__item">
        <img src="img/GUJ.svg" alt="Logo do GUJ" />
        <a href="#" class="lista-rodapé__link">GUJ</a>
      </li>
    </ul>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
‎styles.css
+2
Original file line number	Diff line number	Diff line change
@@ -15,6 +15,8 @@
    --azul: #002F52;
    --fonte-secundario: "Josefin Sans";
    --preto: #000000;
    --cinza: #474646;
    --cinza-claro: #858585;
}

body {
‎styles/rodapé.css
+37
Original file line number	Diff line number	Diff line change
@@ -5,4 +5,41 @@ hr {
.rodapé {
    background-color: var(--branco);
    padding: 1em;
}
.lista-rodapé {
    display: none;
}
@media screen and (min-width: 1024px) {
    .rodapé {
        display: flex;
        justify-content: space-around;
    }
    .lista-rodapé {
        display: block;
    }
    .lista-rodapé__item {
        display: flex;
        align-items: center;
        margin: 0.6em 0;
    }
    .lista-rodapé__link {
        color: var(--cinza);
        text-decoration: none;
        margin-left: 0.6em;
    }
    .lista-rodapé__titulo {
        font-size: 14px;
        color: var(--cinza-claro);
    }
    .rodapé__titulo {
        font-size: 24px;
    }
}
  <section class="carrossel">
    <h2 class="carrossel__titulo">Novos lançamentos</h2>
    <!-- Slider main container -->
    <div class="swiper">

      <div class="swiper-pagination"></div>
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="img/Apachekafka.svg"
            alt="Livro sobre apache kafka e spring boot da alura books"></div>
        <div class="swiper-slide"><img src="img/Liderança.svg"
            alt="Livro sobre liderança em design design da alura books"></div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alura books">
        </div>
        <div class="swiper-slide">
          <img src="img/Guia Front-end.svg" alt="Livro Guia front end" />
        </div>
        <div class="swiper-slide">
          <img src="img/Portugol.svg" alt="Livro sobre portugol" />
        </div>
        <div class="swiper-slide">
          <img src="img/Acessibilidade.svg" alt="Livro sobre acessibilidade" />
    <div class="carrossel__container">
      <!-- Slider main container -->
      <div class="swiper">
        <div class="swiper-pagination"></div>
        <!-- Additional required wrapper -->
        <div class="swiper-wrapper">
          <!-- Slides -->
          <div class="swiper-slide"><img src="img/Apachekafka.svg"
              alt="Livro sobre apache kafka e spring boot da alura books"></div>
          <div class="swiper-slide"><img src="img/Liderança.svg"
              alt="Livro sobre liderança em design design da alura books"></div>
          <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alura books">
          </div>
          <div class="swiper-slide">
            <img src="img/Guia Front-end.svg" alt="Livro Guia front end" />
          </div>
          <div class="swiper-slide">
            <img src="img/Portugol.svg" alt="Livro sobre portugol" />
          </div>
          <div class="swiper-slide">
            <img src="img/Acessibilidade.svg" alt="Livro sobre acessibilidade" />
          </div>
        </div>
      </div>

      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
        <!-- If we need navigation buttons -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>

    </div>
      </div>

    <div class="card">
      <div class="card__descrição">
        <div class="descrição">
          <h3 class="descrição__titulo">Talvez você também se interesse por...</h3>
          <h2 class="descrição__titulo-livro">Angular 11 e Firebase</h2>
          <p class="descrição__texto">
            Construindo uma aplicação integrada com a plataforma do Google.
          </p>
      <div class="card">
        <div class="card__descrição">
          <div class="descrição">
            <h3 class="descrição__titulo">Talvez você também se interesse por...</h3>
            <h2 class="descrição__titulo-livro">Angular 11 e Firebase</h2>
            <p class="descrição__texto">
              Construindo uma aplicação integrada com a plataforma do Google.
            </p>
          </div>
          <img src="img/Angular.svg" class="descrição__imagem" />
        </div>
        <div class="card__botões">
          <ul class="botões">
            <li class="botões__item">
              <img src="img/Favoritos.svg" alt="Favoritar livro" />
            </li>
            <li class="botões__item">
              <img src="img/Compras.svg" alt="Adicionar no carrinho de compras" />
            </li>
          </ul>
          <a href="#" class="botões__ancora">Saiba mais</a>
        </div>
        <img src="img/Angular.svg" class="descrição__imagem" />
      </div>
      <div class="card__botões">
        <ul class="botões">
          <li class="botões__item">
            <img src="img/Favoritos.svg" alt="Favoritar livro" />
          </li>
          <li class="botões__item">
            <img src="img/Compras.svg" alt="Adicionar no carrinho de compras" />
          </li>
        </ul>
        <a href="#" class="botões__ancora">Saiba mais</a>
      </div>
    </div>

  </section>

  <section class=”carrossel”>
    <h2 class="carrossel__titulo">Mais vendidos</h2>
    <div class="swiper">
      <!-- Additional required wrapper -->
      <!-- If we need pagination -->
      <div class="swiper-pagination"></div>

      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="img/ApacheKafka.svg"
            alt="Livro sobre apache kafka e spring boot da alura books"></div>
        <div class="swiper-slide"><img src="img/Liderança.svg" alt="Livro sobre liderança em design da alura books">
        </div>
        <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alurabooks">
    <div class="carrossel__container">
      <div class="swiper">
        <!-- Additional required wrapper -->
        <!-- If we need pagination -->
        <div class="swiper-pagination"></div>
        <div class="swiper-wrapper">
          <!-- Slides -->
          <div class="swiper-slide"><img src="img/ApacheKafka.svg"
              alt="Livro sobre apache kafka e spring boot da alura books"></div>
          <div class="swiper-slide"><img src="img/Liderança.svg" alt="Livro sobre liderança em design da alura books">
          </div>
          <div class="swiper-slide"><img src="img/Javascript.svg" alt="Livro sobre javascript assertivo da alurabooks">
          </div>
          <div class="swiper-slide"><img src="img/Guia Front-end.svg" alt="Livro Guia front end"></div>
          <div class="swiper-slide"><img src="img/Portugol.svg" alt="Livro sobre portugol"></div>
          <div class="swiper-slide"><img src="img/Acessibilidade.svg" alt="livro sobre acessibilidade"></div>
        </div>
        <div class="swiper-slide"><img src="img/Guia Front-end.svg" alt="Livro Guia front end"></div>
        <div class="swiper-slide"><img src="img/Portugol.svg" alt="Livro sobre portugol"></div>
        <div class="swiper-slide"><img src="img/Acessibilidade.svg" alt="livro sobre acessibilidade"></div>
      </div>

      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
        <!-- If we need navigation buttons -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>

    <div class="card">
      <!-- 1º linha -->
      <div class="card__descrição">
        <!-- 1º coluna -->
        <div class="descrição">
          <img src="img/Estrelinhas.svg" alt="Avaliação 5 estrelas">
          <h3 class="descrição__titulo">Autora do Mês</h3>
          <h2 class="descrição__titulo-livro">Juliana Agarikov</h2>
          <p class="descrição__texto">Analista de sistemas e escritora, Juliana é especialista em Front-End.
          </p>
      <div class="card">
        <!-- 1º linha -->
        <div class="card__descrição">
          <!-- 1º coluna -->
          <div class="descrição">
            <img src="img/Estrelinhas.svg" alt="Avaliação 5 estrelas">
            <h3 class="descrição__titulo">Autora do Mês</h3>
            <h2 class="descrição__titulo-livro">Juliana Agarikov</h2>
            <p class="descrição__texto">Analista de sistemas e escritora, Juliana é especialista em
              Front-End.
            </p>
          </div>
          <!-- 2º coluna -->
          <img src="img/Escritora.svg" class="descrição__imagem">
        </div>
        <!-- 2º coluna -->
        <img src="img/Escritora.svg" class="descrição__imagem">
      </div>

      <!-- 2º linha -->
      <div class="card__botões">
        <!-- 1º coluna -->
        <ul class="botões">
          <li class="botões__item"><img src="img/Favoritos.svg" alt="Favoritar livro"></li>
          <li class="botões__item"><img src="img/Compras.svg" alt="Adicionar no carrinho de compras"></li>
        </ul>
        <!-- 2º coluna -->
        <a href="#" class="botões__ancora">Saiba mais</a>
        <!-- 2º linha -->
        <div class="card__botões">
          <!-- 1º coluna -->
          <ul class="botões">
            <li class="botões__item"><img src="img/Favoritos.svg" alt="Favoritar livro"></li>
            <li class="botões__item"><img src="img/Compras.svg" alt="Adicionar no carrinho de compras"></li>
          </ul>
          <!-- 2º coluna -->
          <a href="#" class="botões__ancora">Saiba mais</a>
        </div>
      </div>
    </div>


  </section>

  <section class="tópicos">
‎styles/banner.css
+18
Original file line number	Diff line number	Diff line change
@@ -46,4 +46,22 @@
    .banner__pesquisa::placeholder {
        background-position: 7em;
    }
}
@media screen and (min-width: 1728px) {
    .banner__pesquisa {
        width: 35%;
    }
    .banner {
        padding: 6em 0;
    }
    .banner__pesquisa::placeholder {
        background-position: 12em;
    }
}
‎styles/carrossel.css
+40
Original file line number	Diff line number	Diff line change
@@ -94,4 +94,44 @@
        display: block;
        top: 60%;
    }
    .card {
        width: 60%;
        margin-left: 3em;
    }
}
@media screen and (min-width: 1728px) {
    .carrossel__container {
        display: flex;
        margin: 0 20vw 3em 20vw;
        align-items: center;
    }
    .swiper-pagination {
        margin: 1em 0;
    }
    .swiper {
        width: 50%;
    }
    .descrição__titulo {
        font-size: 32px;
    }
    .descrição__texto {
        font-size: 16px;
    }
    .descrição {
        margin-right: 2em;
    }
    .card {
        width: 60%;
        margin-left: 3em;
    }
}
‎styles/contato.css
+7
Original file line number	Diff line number	Diff line change
@@ -56,4 +56,11 @@
    .contato__email {
        width: 30%;
    }
}
@media screen and (min-width: 1728px) {
    .contato {
        padding: 3em 20vw;
    }
}
‎styles/rodapé.css
+7
Original file line number	Diff line number	Diff line change
@@ -42,4 +42,11 @@ hr {
    .rodapé__titulo {
        font-size: 24px;
    }
}
@media screen and (min-width: 1728px) {
    .lista-rodapé {
        border-left: 1px solid var(--cinza-claro);
        padding-left: 1em;
    }
}
‎styles/topicos.css
+7
Original file line number	Diff line number	Diff line change
@@ -37,4 +37,11 @@
    .tópicos__link {
        font-size: 24px;
    }
}
@media screen and (min-width: 1728px) {
    .tópicos {
        padding: 3em 30vw;
    }
}
  <header class="cabeçalho">
    <div class="container">
      <input type="checkbox" id="menu" class="container__botao">
      <label for="menu">
      <label for="menu" class="container__rotulo">
        <span class="cabeçalho__menu-hamburguer container__imagem"></span>
      </label>
      <ul class="lista-menu">
@@ -44,7 +44,7 @@ <h1 class="container__titulo"><b class="container__titulo--negrito">Alura</b>Boo

      <ul class="opções">
        <input type="checkbox" id="opções-menu" class="opções__botão" />
        <label for="opções-menu">
        <label for="opções-menu" class="opções__rotulo">
          <li class="opções__item">Categorias</li>
        </label>

‎styles/header.css
+29
-3
Original file line number	Diff line number	Diff line change
@@ -7,6 +7,14 @@
    background-position: center;
}

.container__botao:checked~.container__rotulo>.cabeçalho__menu-hamburguer {
    background-image: url("../img/MenuAberto.svg");
}
.container__botao:checked~.container__rotulo {
    background: var(--azul-degrade);
}
.cabeçalho {
    background-color: var(--branco);
    display: flex;
@@ -63,6 +71,10 @@
    display: none;
}

.container__texto {
    display: none;
}
.opções {
    display: none
}
@@ -115,10 +127,24 @@
        display: none;
    }

}
    .opções__botão:checked~.opções__rotulo>.opções__item {
        background: var(--azul-degrade);
        color: var(--branco);
    }
    .opções__item {
        padding: 2em 1em;
    }
    .lista-menu__item:hover {
        background: var(--azul-degrade);
    }
    .lista-menu__item:hover>.lista-menu__link {
        -webkit-text-fill-color: var(--branco);
        text-decoration: none;
    }

.container__texto {
    display: none;
}

@media screen and (min-width: 1728px) {
  </p>
    </div>
    <input type="email" placeholder="Cadastre seu e-mail" class="contato__email" />
    <input type="email" placeholder="         Cadastre seu e-mail" class="contato__email" />
  </section>

  <hr />

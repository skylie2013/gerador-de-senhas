# Segurança digital: utilizando matemática para programar senhas seguras

# *`Aula 01`*

## ### Primeiros passos
### crie dois arquivos:
* index.html
* stye.css

Seu explorador ficará dessa forma:
![img1](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-03.png)

Agora, no arquivo HTML, digite `html:5` e aperte a tecla **Enter**, para adicionar uma estrutura inicial, ou copie o codigo abaixo. Seu código deve aparecer assim:

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

```

Feito isso, vamos realizar algumas alterações no código criado.

Altere o  **idioma**  de  `en`  para  `pt-BR`  (que significa o idioma Português-Brasil):

```xml
<html lang="pt-BR">

```

Em seguida, altere o **título** de `Document` para `Gerador de senhas`, desta forma:

```xml
<title>Gerador de senhas</title>

```

Agora vamos **linkar** o arquivo HTML com o CSS. Para isso, adicione a tag `link rel="stylesheet" href="style.css"` abaixo da tag `title`, como mostra o código abaixo:
`OBS:(Preste atenção pois iremos adicionar apenas o link do CSS)`

```xml
<title>Gerador de senhas</title>
<link rel="stylesheet" href="style.css">

```


Codigo para comparação se acaso seu codigo está errado pode usar esse trecho como exemplo ou copiar inteiro e subistituir o que voce estava fazndo antes. 
Seu código com as alterações ficará assim:
```xml
<!DOCTYPE html>
<html lang="pt-BR">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>Gerador de senhas</title>
	    <link rel="stylesheet" href="style.css">
	</head>
	<body>
	
	</body>
</html>

```

Pronto! Agora já temos a estrutura inicial do nosso projeto e podemos prosseguir na criação do código.

### Cabeçalho

Vamos criar a primeira parte do projeto:  **o Cabeçalho**. Observe como ele está no protótipo do Figma:

![Captura de tela do protótipo no figma com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-04.png)

Note que o cabeçalho possui  **3 partes**:

-   Imagem (cadeado)
-   Título principal
-   Título secundário

Sendo assim, no arquivo HTML, adicione dentro do  `body`  a tag  `img`  com a descrição  `alt="cadeado fechado"`, como mostra o código abaixo:

Obs: as tags body já existe no seu codigo então não a nescecidade de faze-lá novamente

```xml
<body>
    <img src="" alt="cadeado fechado">
</body>

```

> Aqui você estará adicionando um  **campo de imagem**.

Agora, insira uma tag  `h2`  de classe  `titulo-principal`  e texto  **Gerador de senhas**:

obs: abaixo do codigo `<img src="" alt="cadeado fechado">`  
```xml
<body>
    <img src="" alt="cadeado fechado">
    <h2 class="titulo-principal">Gerador de senhas</h2>
</body>

```

Por fim, adicione a tag  `h3`  de classe  `titulo-secundario`  e texto  **Gere instantaneamente uma senha aleatória e segura**:
obs: abaixo do codigo `<img src="" alt="cadeado fechado">`  e abaixo do codigo `<h2 class="titulo-principal">Gerador de senhas</h2>` 
```xml
<body>
    <img src="" alt="cadeado fechado">
    <h2 class="titulo-principal">Gerador de senhas</h2>
    <h3 class="titulo-secundario">Gere instantaneamente uma senha aleatória e segura</h3>
</body>

```

Você pode perceber que a  **estrutura do cabeçalho**  já foi criada, no entanto falta adicionar a imagem e alguns detalhes.

![Captura de tela do projeto no navegador com um campo de imagem e a escrita “cadeado fechado”, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-04.2.png)

Vamos explorar em breve alguns estilos!

### Cadeado

A imagen do cadeado já está no seu repositorio basta chama-la no projeto.

Agora no HTML, insira o caminho  `"unlock.svg"`  dentro da tag  `img`, desta forma:

```xml
<img src="unlock.svg" alt="cadeado fechado">

```

Já temos nossa imagem adicionada ao código!

![Captura de tela do projeto no navegador com uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-06.png)

### Cores personalizadas

Precisamos inserir as cores do protótipo, mas antes vamos  **reconhecer um padrão**, o que irá agilizar na criação do projeto.

Para isso, insira no arquivo CSS a tag  `root`, atribuindo as seguintes cores:

-   --branco: white;
-   --cor-de-fundo: #00162E;
-   --fundo-senha: #00244D;
-   --fundo-texto: #001E40;
-   --borda: #0075FF;

Seu código ficará da seguinte forma:
obs: esse codigo ficará no arquivo style.css
```css
:root{
    --branco: white;
    --cor-de-fundo: #00162E;
    --fundo-senha: #00244D;
    --fundo-texto: #001E40;
    --borda: #0075FF;
}

```

Feito isso, vamos incluir as cores no projeto! Adicione a tag  `body`  no CSS e insira a propriedade  `color`, para definir a  **cor da fonte**. Insira nela a cor  `var(--branco)`:

obs: na linha de baixo aonde termina o `:root` 
```css
body{
    color: var(--branco);
}

```

Adicione também a propriedade  `background-color`  para definir a  **cor de fundo**, inserindo nela a cor  `var(--cor-de-fundo)`:

```css
body{
    color: var(--branco);
    background-color: var(--cor-de-fundo);
}

```

Após adicionar as cores, seu projeto ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-07.png)

### Importando fontes externas

Vamos agora importar fontes externas ao nosso projeto. Para isso, abra o site  [Google Fonts](https://fonts.google.com/)  e pesquise a fonte  **"Roboto"**.

Clique na opção  `Roboto`  e selecione a fonte  **Regular 400**:

![Captura de tela do site “google fonts” com a opção “select regular 400” selecionada.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-08.png)

Faça o mesmo pesquisando  `Roboto Mono`  e selecionando a fonte  **Regular 400**:

![Captura de tela do site “google fonts” com os dados da fonte “roboto” e “roboto mono”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-09.png)

Feito isso, selecione a opção  `@import`  e copie o código que está dentro da tag  `style`  no navegador:

![Captura de tela do site “google fonts”  com o campo “Use on the web”, a opção “import” selecionada e o texto “@import url('https://fonts.googleapis.com/css2?family=Roboto&family=Roboto+Mono&display=swap');” selecionado.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-10.png)

Clique no ícone inferior direito da seção  **"CSS rules to specify families"**  ("Regras CSS para especificar famílias", traduzindo para português), copiando assim as informações:

![Captura de tela do site “google fonts”  com o campo “CSS rules to specify families”, o texto “font-family: 'Roboto', sans-serif; font-family: 'Roboto Mono', monospace;” e o ícone de “copiar”, destacado por um retângulo vermelho.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-11.png)

Agora, no seu arquivo CSS,  **cole as regras**  dentro da tag  `root`, alterando os nomes  `font-family`  para  `--roboto`  e  `--roboto-mono`, respectivamente. Sua tag ficará assim:

```css
:root{
    --branco: white;
    --cor-de-fundo: #00162E;
    --fundo-senha: #00244D;
    --fundo-texto: #001E40;
    --borda: #0075FF;
    --roboto: 'Roboto', sans-serif;
    --roboto-mono: 'Roboto Mono', monospace;
}

```

### Fontes e tamanhos

Nosso projeto ja está tomando forma, no entanto precisamos determinar a  **tipografia**, isto é: adicionar  **fontes**  e  **tamanhos de letras**  nas partes de texto.

No arquivo CSS, adicione na tag  `body`  a propriedade  `font-family`  com o valor  `var(--roboto)`:
Observe que já existe esse trecho de codigo então vamos adicionar o que falta.
```css
body{
    color: var(--branco);
    background-color: var(--cor-de-fundo);
    font-family: var(--roboto);
}

```

Em seguida, crie a classe  `.titulo-principal`, inserindo nela as propriedades  `font-family`  de valor  `var(--roboto-mono)`  e  `font-size`  com tamanho  `32px`:

```css
.titulo-principal{
    font-family: var(--roboto-mono);
    font-size: 32px;
}

```

Após isso, crie a classe  `.titulo-secundario`  no CSS e adicione a propriedade  `font-size`  com tamanho  `24px`:

```css
.titulo-secundario{
    font-size: 24px;
}

```

Pronto, já adicionamos as fontes escolhidas da internet! Seu projeto ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula01_FCF-final.png)

Fim aula 01-

# *`Aula 02`*

Nessa aula, aprendemos a organizar os conteúdos da página e criar o campo de senha. Vamos revisar nosso código com os conceitos abaixo!

### Alinhando itens ao centro

Para alinhar os itens ao centro da página, vamos criar uma nova divisão de conteúdo.

No código HTML, adicione uma  `div`  de classe  `conteudo-titulo`  e inclua nela as tags  `img`,  `h2`  e  `h3`, desta forma:
Observe que iremos colocar envolta do conteudo que criamos na aula 01.
```html
<div class="conteudo-titulo">    <!-- adicionar conteudo dessa linha -->
    <img src="unlock.svg" alt="cadeado fechado">
    <h2 class="titulo-principal">Gerador de senhas</h2>
    <h3 class="titulo-secundario">Gere instantaneamente uma senha aleatória e segura</h3>
</div> 							<!-- adicionar conteudo dessa linha -->	

```

Em seguida, no arquivo CSS, adicione na classe  `.conteudo-titulo`  as propriedades  `text-align: center;`  e  `margin-top: 80px;`, como mostra o código abaixo:
Obs: sempre leia o codigo para não duplicar trechos existentes.

```css
.conteudo-titulo{
    text-align: center;
    margin-top: 80px;
}

```

> `text-align: center;`  é responsável por  **alinhar o texto ao centro**;  `margin-top: 80px;`  dará um  **espaçamento superior**  de 80 px.

Pronto, todos os itens dessa  `div`  já estão alinhados corretamente ao centro!

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-00.png)

### Corrigindo o peso da fonte

Podemos notar no protótipo do Figma um padrão de  **peso (espessura)**  nas fontes:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas” e o título secundário “Gere instantaneamente uma senha aleatória e segura”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-01.png)

Para obter o mesmo padrão ao código CSS, adicione abaixo da classe  `root`  o  **seletor universal**  `*`, que irá englobar todos os demais seletores do código.

Insira nele a propriedade  `font-weight: 400;`:

Crie esse seletor nas primeiras linhas do style.css.
```css
*{
    font-weight: 400
}

```

> Com essa definição, todas as fontes da página terão  **peso 400**.

### Campo de senha

Agora, vamos criar o campo de senha no nosso projeto. Observe como ele aparece no protótipo do Figma:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, um campo de texto com o título “Senha” e o texto “zcBLsNGXabce”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-02.png)

Para isso, adicione dentro do  `body`  no arquivo HTML, uma nova  `div`  de classe  `conteudo-senha`:
Obs: pule uma linha do anterior e começe a escrever esse codigo.
```html
<div class="conteudo-senha">

</div>

```

Dentro dela, adicione a tag  `label for="senha"`, atribuindo a ela o texto  **"Senha"**, da seguinte forma:

```html
<div class="conteudo-senha">
    <label for="senha">Senha</label>
</div>

```

Em seguida, insira a tag  `input`  com o  **nome**  `"senha"`, atribuindo o  **tipo**  `text`  e um  `id="campo-senha"`  :

```html
<div class="conteudo-senha">
    <label for="senha">Senha</label>
    <input name="senha" type="text" id="campo-senha">
</div>

```

> O valor  `name="senha"`  permitirá que o  `label`  localize o  `input`  no código.

Observe como o projeto está ficando:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura” e o campo de texto de cor branca com o título “Senha” e o texto “zcBLsNGXabce”. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-03.png)

Com o conteúdo HTML criado, vamos agora estilizar essa nova  `div`!

### Estilizando o campo de senha

No arquivo CSS, crie um seletor de classe  `.conteudo-senha`  e adicione nele a propriedade  `background-color`  com o valor  `var(--fundo-senha)`:

```css
.conteudo-senha{
    background: var(--fundo-senha);
}

```

Agora, adicione as propriedades:

-   `padding: 24px`  : que irá inserir um  **espaçamento**
-   `border-bottom: 6px solid var(--borda)`: para adicionar uma  **borda inferior**, determinando sua  _espessura, tipo e cor_.

Seu seletor  `.conteudo-senha`  no CSS deve ficar assim:

```css
.conteudo-senha{
    background: var(--fundo-senha);
    padding: 24px;
    border-bottom: 6px solid var(--borda);
}

```

Feito isso, agora precisamos estilizar o local do  `input`, ou seja, lugar onde será inserido o texto. Adicione um novo  **seletor**  no CSS, identificando pelo  `id`  `#campo-senha`:

```bash
#campo-senha{
   
}

```

Agora, para definir as propriedades de  **cor**, adicione  `background-color: var(--fundo-senha);`  e  `color: var(--branco);`

```css
#campo-senha{
    background-color: var(--fundo-senha);
    color: var(--branco);    
}

```

Em seguida, para  **remover a borda**, adicione a propriedade  `border:none`  abaixo de  `background-color`, desta forma:

```css
#campo-senha{
    background-color: var(--fundo-senha);
    border: none;
    color: var(--branco);    
}

```

Vamos definir as propriedades de  **texto**, adicionando  `font-family: var(--roboto-mono);`  e  `font-size: 40px;`:

```css
#campo-senha{
    background-color: var(--fundo-senha);
    border: none;
    color: var(--branco);  
    font-family: var(--roboto-mono);
    font-size: 40px;
}

```

Apesar de criado o estilo, note que ao clicar no  `input`  uma  **borda laranja**  aparece:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, um campo de texto com o título “Senha” e um retângulo de cor laranja.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-04.png)

Para resolver este problema, adicione um novo seletor de nome  `#campo-senha:focus`, inserindo nele a propriedade  `outline:none`:

```css
#campo-senha:focus{
    outline: none;
}

```

> Essa propriedade irá  **remover o contorno**  do campo, quando estiver em foco.

### Agrupando o conteúdo

Nosso projeto está quase pronto, no entanto observe que o  **campo de senha**  está ocupando quase 100% de  **largura**  da tela:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura” e o campo de texto de cor branca com o título “Senha”  destacado por um retângulo vermelho. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-05.png)

Vamos resolver este problema criando uma  **seção de conteúdo**  que irá agrupar as informações.

No HTML, crie uma tag  `section`  de classe  `conteúdo`  e agrupe nela as  `divs`  criadas anteriormente:

```javascript
<section class="conteudo">
        <div class="conteudo-titulo">
            <img src="unlock.svg" alt="cadeado fechado">
            <h2 class="titulo-principal">Gerador de senhas</h2>
            <h3 class="titulo-secundario">Gere instantaneamente uma senha aleatória e segura</h3>
        </div>
        <div class="conteudo-senha">
            <label for="senha">Senha</label>
            <input name="senha" type="text" id="campo-senha">
        </div>
    </section>

```

Agora, no arquivo CSS, crie um seletor para a classe  `.conteudo`  e adicione nele a propriedade  `max-width: 1200px;`  que irá definir um  **tamanho máximo de tela**:

```css
.conteudo{
    max-width: 1200px;
}

```

Em seguida, adicione a propriedade  `margin: 0 auto;`, para  **remover as margens**  de modo automático:

```css
.conteudo{
    max-width: 1200px;
    margin: 0 auto;
}

```

Está quase pronto! Para finalizar, vamos  **aumentar o espaçamento**  entre os elementos da  `div`  de classe  `conteudo-senha`:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha” e  um retângulo vermelho ilustrando o espaçamento entre texto e borda do campo de texto. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-06.png)

No arquivo CSS, adicione no seletor da classe  `.conteudo-senha`  a propriedade  `margin-top`  de valor  `80 px`:

```css
.conteudo-senha{
    margin-top: 80px; 
    background: var(--fundo-senha);
    padding: 24px;
    border-bottom: 6px solid var(--borda);
}

```

Pronto! Todas as propriedades do campo de senha foram criadas e estão de acordo com o protótipo do Figma. Seu projeto ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura” e  o campo de texto de cor branca com o título “Senha”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula02_FCF-07.png)

Fim aula 02

# *`Aula 03`*
Nessa aula aprendemos como adicionar uma nova divisão, aplicando o conceito de  _Mobile First_. Vamos revisar nosso código com o conteúdo abaixo!

### Entendendo o  _Mobile First_

Para iniciar o nosso projeto, precisamos ter em mente a aplicação do  _**Mobile First**_. Mas afinal, o que seria esse conceito?

> `Mobile First`: ou  **"Celular Primeiro"**  (traduzido para português) é uma abordagem de desenvolvimento que prioriza a criação da versão para  **dispositivos móveis**  (como smartphones).

Pensando nisso, podemos observar nosso projeto e entender a disposição do conteúdo:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linha e destacados por retângulos vermelhos. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-01.png)

> Na disposição de telas de celular, os três blocos que encontram-se alinhados horizontalmente passariam a ser alinhados por uma  **coluna**.

Tenha em mente as informações acima, pois vamos explorar esse conceito novamente em breve!

### Nova divisão:  `.parametro`

Vamos criar agora uma nova aba de conteúdo. Essa divisão será responsável por englobar todo o conteúdo que está destacado na figura abaixo:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo, destacada por um retângulo vermelho. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linhas. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-02.png)

Para isso, no arquivo HTML, crie dentro da tag  `section`  uma nova  `div`  de classe  `parametro`:

```xml
<div class="parametro">
            
</div>

```

Agora, dentro da  `div`  criada, precisamos adicionar os elementos. Observe que, no protótipo, há um  **título**  e um  **agrupamento**  de conteúdos:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, e uma nova seção de conteúdo. A nova seção está destacada em duas partes diferentes, o retângulo vermelho destaca o título “Personalize sua senha” e o retângulo amarelo destaca três blocos de texto agrupados em linhas. No primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-03.png)

Sendo assim, adicione uma tag  `h3`  de classe  `parametro-titulo`  com o texto  **"Personalize sua senha"**:

```xml
<div class="parametro">
    <h3 class="parametro-titulo">Personalize sua senha</h3>           
</div>

```

Em seguida, adicione dentro dela uma nova  `div`  de classe  `parametro-coluna__senha`:

```xml
<div class="parametro">
    <h3 class="parametro-titulo">Personalize sua senha</h3>   
    <div class="parametro-coluna__senha">

    </div>
</div>

```

Feito isso, vamos seguir criando o conteúdo. Observe abaixo a disposição dos elementos no protótipo do Figma:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro e uma nova seção de conteúdo. A nova seção está destacada em duas partes diferentes, o retângulo amarelo destaca o conjunto agrupado em linha de três blocos, já os retângulos vermelhos destacam cada bloco separadamente. No primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-04.png)

Perceba que, dentro da  `div`  que criamos, há uma  **subdivisão de 3 partes**.

Para criar essa subdivisão, adicione  **uma nova  `div`**  de classe  `parametro-senha`  e dentro dela, insira uma tag  `h4`  de classe  `parametro-senha__titulo`, para adicionar o título  **"Número de caracteres"**, desta forma:

```xml
<div class="parametro-coluna__senha">
    <div class="parametro-senha">
        <h4 class="parametro-senha__titulo">Número de caracteres</h4>
    </div>                
</div>

```

Feito isso,  **copie e cole 2x**  a  `div`  de classe  `parametro-senha`, adicionando assim 3 subdivisões, como mostra o código abaixo:

```xml
<div class="parametro-coluna__senha">
    <div class="parametro-senha">
        <h4 class="parametro-senha__titulo">Número de caracteres</h4>
    </div> 
    <div class="parametro-senha">
        <h4 class="parametro-senha__titulo">Características da senha</h4>
    </div>
    <div class="parametro-senha">
        <h4 class="parametro-senha__titulo">Força da senha</h4>
    </div>
</div>

```

> Não se esqueça de  **alterar os textos**  de acordo com os títulos do protótipo!

Observe como está ficando o seu projeto no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-05.png)

Agora vamos adicionar estilo aos textos criados!

### Estilizando com CSS

Para começar, insira no arquivo CSS um seletor da classe  `.parametro`, adicionando nele as propriedades  `background-color`  e  `border`, com os valores mostrados abaixo:

```css
.parametro{
    background-color: var(--fundo-texto);
    border: 2px solid var(--borda);
}

```

Observe que está faltando um  **espaçamento**  entre as  `divs`:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A ilustração enfatiza que as duas seções de conteúdo estão encostadas, sem espaçamento. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-06.png)

Para resolver este problema, adicione a propriedade  `margin-top`  com valor  **32px**:

```css
.parametro{
    background-color: var(--fundo-texto);
    border: 2px solid var(--borda);
    margin-top: 32px;
}

```

Pronto! As  `divs`  estão espaçadas corretamente.

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A ilustração enfatiza que as duas seções de conteúdo agora estão espaçadas corretamente. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-07.png)

Agora, vamos alterar a  **fonte**  e o  **tamanho**  de cada título inserido.

Para isso, crie um seletor da classe  `parametro-titulo`, adicionando nele as propriedades  `font-family`  e  `font-size`, com os valores mostrados abaixo:

```css
.parametro-titulo{
    font-family: var(--roboto-mono);
    font-size: 28px;
}

```

Nossos títulos já estão com fontes e tamanhos padrão. Agora, vamos corrigir o  **espaçamento interno**  e manter todos os textos alinhados:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. A ilustração enfatiza uma linha vermelha que visa alinhar todos os textos a fim de iniciarem sempre de um espaçamento determinado.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-08.png)

Adicione no seletor da classe  `.parametro`  a propriedade  `padding`  de valor  **24px**:

```css
.parametro{
    background-color: var(--fundo-texto);
    border: 2px solid var(--borda);
    margin-top: 32px;
    padding: 24px;
}

```

Pronto! Todos os textos encontram-se alinhados com o mesmo espaçamento.

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. A ilustração enfatiza que agora todos os títulos contém o mesmo espaçamento inicial.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-09.png)

Vamos prosseguir na estilização do projeto, determinando agora um padrão de estilo para a classe  `parametro-senha__titulo`.

Adicione no arquivo CSS um seletor para a classe  `parametro-senha__titulo`, inserindo nela a propriedade  `font-size`  de valor  **24px**:

```css
.parametro-senha__titulo{
    font-size:24px;
}

```

Observe como está ficando seu projeto no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. A ilustração enfatiza a alteração de fontes nos títulos da nova seção.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-10.png)

### Aplicando o conceito  _Mobile First_

Para aplicar o conceito de Mobile First, precisamos pensar inicialmente na configuração de tela de um  **celular**, onde temos uma  **tela pequena**  e uma  **disposição em colunas**  dos conteúdos.

Para aplicar isso ao código, adicione no CSS, um seletor da classe  `parametro-coluna__senha`  com as propriedades  `display`,  `flex-direction`  e  `justify-content`:

```css
.parametro-coluna__senha{
    display: flex;
    flex-direction: column;
    justify-content: center;
}

```

> `display: flex;`: torna os elementos-filhos da  `div`  **flexíveis**.  `flex-direction: column;`: determina a disposição dos elementos em  **coluna**.  `justify-content: center;`: alinha o conteúdo  **ao centro**.

Ao visualizar o projeto em telas menores, você vai perceber que ocorreu um  _bug_  (erro) no código:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”. A ilustração enfatiza o erro de layout no campo de senha.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-11.png)

Vamos resolvê-lo a seguir!

### Resolvendo o  _bug_  no campo de senha

Para solucionar este problema de exibição, adicione no seletor  `#campo-senha`  a propriedade  `width`  com valor  **70%**:

```css
#campo-senha{
    background-color: var(--fundo-senha);
    border: none;
    color: var(--branco);
    font-family: var(--roboto-mono);
    font-size: 40px;
    width: 70%;
}

```

> É essencial que o valor esteja em  **porcentagem**, para que possa se adequar de forma responsiva ao projeto.

### Layout responsivo

Por fim, vamos adicionar a responsividade ao nosso projeto, para que os elementos sejam  **alinhados de forma flexível**  de acordo com o tamanho da tela.

No final do arquivo CSS, adicione a regra  `@media screen and (min-width: 768px)`, desta forma:

```python
@media screen and (min-width: 768px) {

}

```

> Todas as propriedades dentro dessa regra serão aplicadas se a  **largura mínima**  da tela for equivalente a  **768px**.

Em seguida, adicione dentro dela o seletor  `.parametro-coluna__senha`, inserindo nele a propriedade  `flex-direction: row;`

```css
@media screen and (min-width: 768px) {
    .parametro-coluna__senha{
        flex-direction: row;
    }
}

```

> `flex-direction: row;`: determina a disposição dos elementos  **em linha**.

Observe agora o projeto no navegador:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. A ilustração enfatiza a disposição flexível dos elementos, onde ficam em linha para telas maiores, e em coluna para telas menores.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-12.gif)

Você pode perceber que a disposição dos elementos muda de acordo com o tamanho da tela. No entanto é necessário adicionar um  **espaçamento**  entre os títulos.

### Corrigindo o espaçamento externo

Para corrigir o espaçamento, adicione um seletor para a classe  `.parametro-senha`, inserindo nele as propriedades  `width`  e  `margin`  com os valores descritos abaixo:

```css
.parametro-senha{
    width: 50%;
    margin: 0 auto;
}

```

> `width: 50%;`: vai determinar a largura do elemento como  **metade**  da largura total;  `margin: 0 auto;`: remove as margens de modo automático.

Pronto! Finalizamos o código e o seu projeto ao final da aula ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui os títulos “Personalize sua senha”, “Número de caracteres”, “Características da senha”, “Força da senha”. A ilustração enfatiza a disposição dos três títulos em linha.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula03_FCF-13.png)

Na próxima aula vamos criar os demais elementos das  `divs`  `parametro-senha`. Te espero lá!
# *`Aula 04`*
Nessa aula aprendemos a programar o conteúdo da primeira  `div`  de classe  `parametro-senha`. Vamos revisar nosso código com os conceitos abaixo!

### Criando botões

Vamos criar o conteúdo da parte destacada no protótipo do Figma, como mostra abaixo:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +” e está destacado por um retângulo vermelho. O segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula04_FCF-01.png)

Para isso, no arquivo HTML, adicione dentro da  `div`  de classe  `parametro-senha`  duas tags  `button`  com a classe  `parametro-senha__botao`. Adicione neles o texto  `-`  e  `+`, respectivamente:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Número de caracteres</h4>
    <button class="parametro-senha__botao">-</button>
    <button class="parametro-senha__botao">+</button>
</div>  

```

Agora, entre as duas tags que foram criadas, insira uma nova tag ‘p’ com a classe parametro-senha__texto e o texto "12", como demonstrado abaixo:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Número de caracteres</h4>
    <button class="parametro-senha__botao">-</button>
    <p class="parametro-senha__texto">12</p>
    <button class="parametro-senha__botao">+</button>
</div>  

```

Para manter o mesmo padrão de estilo dos elementos criados, podemos adicioná-los a uma nova  `div`.

Crie então uma nova  `div`  com a classe  `parametro-senha-botoes`  e adicione nela as três tags criadas anteriormente:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Número de caracteres</h4>
    <div class="parametro-senha-botoes">
        <button class="parametro-senha__botao">-</button>
        <p class="parametro-senha__texto">12</p>
        <button class="parametro-senha__botao">+</button>
    </div>
</div>  

```

Observe como está ficando o nosso projeto no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A imagem enfatiza a criação dos botões, porém não estão estilizados de acordo com o padrão.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula04_FCF-02.png)

Agora, adicionaremos estilo ao conteúdo que acabamos de criar.

### Estilo dos botões

Vamos iniciar a criação do estilo determinando a  **disposição**  dos elementos-filhos na  `div`  principal.

Para isso, adicione no CSS um seletor para a classe  `.parametro-senha-botoes`, inserindo nele as propriedades  `display: flex;`  e  `justify-content: center;`:

```css
.parametro-senha-botoes{
    display: flex;
    justify-content: center;
}

```

Agora, vamos dar estilo aos  **botões**. Adicione um seletor para a classe  `.parametro-senha__botao`  e insira as propriedades de cor  `background-color`  e  `color`, para definir a  **cor de fundo**  e a  **cor do texto**:

```css
.parametro-senha__botao{
    background-color: var(--fundo-texto);
    color: var(--branco);
}

```

Em seguida, adicione a propriedade  `border`  para definir bordas de  **2px**,  **sólidas**  e de cor  `var(--borda)`, como mostra abaixo:

```css
.parametro-senha__botao{
    background-color: var(--fundo-texto);
    color: var(--branco);
    border: 2px solid var(--borda);
}

```

Feito isso, vamos alterar o  **espaçamento**  dos botões, adicionando um  `padding`  de valor  **"24px"**.

Inclua também a propriedade  `font-size`  de valor  **"24px"**, para definir o  **tamanho do texto**:

```css
.parametro-senha__botao{
    background-color: var(--fundo-texto);
    color: var(--branco);
    border: 2px solid var(--borda);
    padding: 24px;
    font-size: 24px;
}

```

Observe o resultado das mudanças de estilo no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A imagem enfatiza os botões “-” e “+” já estilizados de acordo com o padrão, com fundo azul marinho e contorno azul royal.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula04_FCF-03.png)

Note que falta adicionar estilo ao  **texto**  da tag  `p`.

Sendo assim, adicione no CSS um seletor da classe  `.parametro-senha__texto`, inserindo nele a propriedade  `padding: 24px;`  para adicionar um  **espaçamento**:

```css
.parametro-senha__texto{
    padding: 24px;
}

```

Agora, adicione as propriedades  `border-top`  e  `border-bottom`  para inserir uma borda  **no topo e em baixo**, ambas de valor  **"2 px"**,  **sólidas**  e de cor  `var(--borda)`.

Inclua também a propriedade  `margin`  de valor  **"0"**  para remover as margens:

```css
.parametro-senha__texto{
   padding: 24px;
   border-top: 2px solid var(--borda);
   border-bottom: 2px solid var(--borda);
   margin: 0;
}

```

Feito isso, adicione a propriedade  `font-size: 24px;`, para determinar o  **tamanho do texto**:

```css
.parametro-senha__texto{
    padding: 24px;
    border-top: 2px solid var(--borda);
    border-bottom: 2px solid var(--borda);
    margin: 0;
    font-size: 24px;
}

```

Após as alterações, seu projeto ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A imagem enfatiza os botões “-” e “+” e texto “12” já estilizados de acordo com o padrão, com fundo azul marinho e contorno azul royal.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula04_FCF-04.png)

### Aprimorando o resultado

Para finalizar, vamos adicionar um efeito onde, ao passar o mouse por cima dos botões  `-`  e  `+`, aparece a opção de  _clicar_. Observe a seguir:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza o cursor do mouse que muda de “seta” para “mão” quando passa pelos botões, indicando que podem ser clicados. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula04_FCF-05.gif)

Para isso, adicione no CSS, na classe  `.parametro-senha__botao`  a propriedade  `cursor: pointer;`:

```css
.parametro-senha__botao{
    background-color: var(--fundo-texto);
    color: var(--branco);
    border: 2px solid var(--borda);
    padding: 24px;
    font-size: 24px;
    cursor: pointer;
}

```

Pronto! A primeira divisão de conteúdo já foi criada e funciona corretamente!

Na próxima aula vamos adicionar os checkboxes da  **segunda divisão**. Te espero lá!
# *`Aula 05`*
Nessa aula aprendemos a criar a divisão “Características da Senha”, adicionando textos e classes correspondentes aos elementos checkbox. Vamos revisar nosso código com o conteúdo abaixo!

### Programando o checkbox

Vamos incluir no projeto o conteúdo mostrado a seguir:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco está destacado por um retângulo vermelho, contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-01.png)

Para criar o primeiro checkbox ou caixa de seleção, adicione dentro da  **segunda**  `div`  de classe  `parametro-senha`, uma tag  `input`  de  **nome**  `maiusculo`  e  **tipo**  `checkbox`, da seguinte forma:

```javascript
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <input name="maiusculo" type="checkbox">
 </div>

```

Em seguida adicione a tag  `label`  indicando o  **for**  `"maiusculo"`  e o conteúdo de texto  **"Letras maiúsculas"**:

```javascript
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <input name="maiusculo" type="checkbox">
    <label for="maiusculo">Letras maiúsculas</label>
 </div>

```

> O atributo  `name`, da tag  `input`  necessariamente terá o  **mesmo valor**  do atributo  `for`, da tag  `label`, para que sejam conectados entre si.

Seu projeto ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Características da senha e um checklist com o texto: “Letras maiúsculas”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-02.png)

Feito isso, podemos  **copiar e colar**  as duas tags criadas acima, alterando os atributos para  `minusculo`  e o texto para  **"Letras minúsculas"**:

```javascript
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <input name="maiusculo" type="checkbox">
    <label for="maiusculo">Letras maiúsculas</label>
    <input name="minusculo" type="checkbox">
    <label for="minusculo">Letras minúsculas</label>
 </div>

```

Observe o resultado no navegador:![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Características da senha e dois checklists. O primeiro com o texto: “Letras maiúsculas” e o segundo com o texto “Letras minúsculas”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-adicional.png)

### Organizando em  `divs`

O conteúdo está sendo criado, mas precisamos ter em mente a organização dele no código, para que seja possível aplicar os padrões de estilo.

Para isso, adicione dentro da  `div`  `parametro-senha`  uma nova  `div`  de classe  `parametro-senha-checkbox`, incluindo nela as duas tags referentes ao  **primeiro checkbox**:

```javascript
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <div class="parametro-senha-checkbox">
        <input name="maiusculo" type="checkbox">
        <label for="maiusculo">Letras maiúsculas</label>
    </div>
</div>

```

Agora, crie uma nova  `div`  com a mesma classe  `parametro-senha-checkbox`, adicionando as tags do  **segundo checkbox**:

```javascript
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <div class="parametro-senha-checkbox">
        <input name="maiusculo" type="checkbox">
        <label for="maiusculo">Letras maiúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="minusculo" type="checkbox">
        <label for="minusculo">Letras minúsculas</label>
    </div>
</div>

```

Pronto! Agora seu código já está organizado em divisões de conteúdo, isso irá facilitar a estilização com CSS.

### Replicando padrões

Podemos observar que o padrão da  `div`  `parametro-senha-checkbox`  se repete no código, então vamos reutilizá-lo para os próximos checkboxes.

Adicione mais uma  `div`  de classe  `parametro-senha-checkbox`, incluindo as tags  `input name="numero"`  e  `label for="numero"`  com o texto do  **terceiro checkbox**:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <div class="parametro-senha-checkbox">
        <input name="maiusculo" type="checkbox">
        <label for="maiusculo">Letras maiúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="minusculo" type="checkbox">
        <label for="minusculo">Letras minúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="numero" type="checkbox">
        <label for="numero">Números</label>
    </div>
</div>

```

Por último, vamos adicionar a quarta  `div`  de classe  `parametro-senha-checkbox`, com as tags e atributos do  **quarto checkbox**.

Insira também o atributo  `checked`  no  `input`  do  **primeiro checkbox**, para exibi-lo sempre como  _checado_:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <div class="parametro-senha-checkbox">
        <input name="maiusculo" type="checkbox" checked>
        <label for="maiusculo">Letras maiúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="minusculo" type="checkbox">
        <label for="minusculo">Letras minúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="numero" type="checkbox">
        <label for="numero">Números</label>
    </div>
    <div class="parametro-senha-checkbox">
    <input name="simbolo" type="checkbox">
        <label for="simbolo">Símbolos</label>
    </div>
</div>

```

Observe como está ficando seu projeto no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. A primeira opção do checklist está selecionada.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-03.png)

### Padrão de estilo para  `label`

Vamos agora determinar um tamanho de texto para os checkboxes! Para isso, podemos criar um padrão de estilo específico para as tags  `label`, ou seja, os textos que aparecem ao lado de checkboxes.

Para isso, adicione no arquivo CSS um seletor da tag  `label`, incluindo nele a propriedade  `font-size`  de valor  **"20px"**:

```css
label{
    font-size: 20px;
}

```

> LEMBRE-SE! Para selecionar  **tags**  no CSS não utilizamos caracteres como  `.`  ou  `#`.

Observe o resultado da mudança de estilo:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. A primeira opção do checklist está selecionada. A imagem enfatiza o aumento de tamanho dos textos.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-04.png)

### Estilizando o checkbox

O texto já está no tamanho desejado, vamos agora aumentar o tamanho do checkbox.

Para inserir um estilo, adicione dentro de todas as tags  `input`  a classe  `checkbox`.

Seu código HTML ficará assim:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Características da senha</h4>
    <div class="parametro-senha-checkbox">
        <input name="maiusculo" type="checkbox" class="checkbox" checked>
        <label for="maiusculo">Letras maiúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="minusculo" type="checkbox" class="checkbox">
        <label for="minusculo">Letras minúsculas</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="numero" type="checkbox" class="checkbox">
        <label for="numero">Números</label>
    </div>
    <div class="parametro-senha-checkbox">
        <input name="simbolo" type="checkbox" class="checkbox">
        <label for="simbolo">Símbolos</label>
    </div>
</div>

```

Agora, selecione a classe  `.checkbox`  no CSS, adicionando as propriedades  `width`  e  `height`  de valor  **"20px"**:

```css
.checkbox{
    width: 20px;
    height: 20px;
}

```

Em seguida, adicione a propriedade  `cursor: pointer;`  para identificar os locais em que o projeto pode ser clicado:

```css
.checkbox{
    width: 20px;
    height: 20px;
    cursor: pointer;
}

```

Ao final da aula, essa divisão de conteúdo ficará da seguinte forma no projeto:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. A primeira opção do checklist está selecionada. A ilustração enfatiza o cursor do mouse que muda de “seta” para “mão” quando passa pelos checkboxes, e seleciona cada item. ](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula05_FCF-05.gif)

Na próxima aula vamos finalizar o CSS do projeto. Te espero lá!
# *`Aula 06`*
Nessa aula aprendemos a inserir a barra de força da senha. Vamos revisar nosso código com o conteúdo abaixo!

### Força da senha

Podemos observar no protótipo que existem  **três**  barras a serem adicionadas:

![Captura de tela do protótipo do Figma com a cor de fundo azul escuro, indicando três barras de força. A primeira barra possui a cor vermelha e está indicando a posição“fraca”. A segunda barra possui a cor amarelo e indica a posição “Média”. A terceira barra possui a cor verde e indica a posição “Forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula06_FCF-01.png)

Para isso, adicione dentro da  **terceira**  `div`  de classe  `parametro-senha`  e adicione mais três  `divs`  com as respectivas classes:

-   `barra`
-   `forca fraca`
-   `parametro-senha-textos`

> No segundo item, inserimos palavras separadas por um  **espaço**  (`space`) para determinar  **mais de uma classe**  ao mesmo elemento.

Seu código ficará assim:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Força da senha</h4>
    <div class="barra"></div>
    <div class="forca fraca"></div>
    <div class="parametro-senha-textos"></div>
</div>

```

Em seguida, adicione três tags  `p`  dentro da  `div`  de classe  `parametro-senha-textos`  com seus respectivos textos, como mostra abaixo:

```xml
<div class="parametro-senha">
    <h4 class="parametro-senha__titulo">Força da senha</h4>
    <div class="barra"></div>
    <div class="forca fraca"></div>
    <div class="parametro-senha-textos">
        <p>Fraca</p>
        <p>Média</p>
        <p>Forte</p>
    </div>
</div>

```

Observe o resultado do código no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Força da Senha e os textos: “Fraca”, “Média”  e “Forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula06_FCF-02.png)

### Determinando padrões

Antes de iniciar a criação das barras, vamos determinar um  **tamanho**  e  **cor de fundo**  para o espaço onde a barra irá ficar.

No arquivo CSS, selecione a classe  `.barra`  e insira as propriedades  `background-color`,  `height`  e  `width`, com os valores atribuídos abaixo:

```css
.barra{
    background-color: var(--fundo-senha);
    height: 30px;
    width: 100%;
}

```

Em seguida, adicione um seletor para a classe  `.forca`, inserindo nele as propriedades  `height`,  `position`  e  `bottom`, com os valores mostrados abaixo:

```css
.forca{
    height: 30px;
    position: relative;
    bottom: 30px;
}

```

> Este seletor irá determinar as propriedades de  **tamanho**  e  **posição**  de cada barra.

### Adicionando a barra "Fraca"

Para criar a primeira barra, selecione a classe  `.fraca`  no CSS e insira propriedades  `width: 25%;`  e  `background-color: #E71B32;`, para determinar seu  **tamanho**  e  **cor vermelha**:

```css
.fraca{
    width: 25%;
    background-color: #E71B32; 
}

```

Observe como ela irá ficar no projeto:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Força da Senha, uma barra de cor vermelha e os textos: “Fraca”, “Média”  e “Forte”, alinhados em coluna.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula06_FCF-03.png)

### Alterando o texto

Vamos alterar o texto de modo em que apareça com  **alinhamento horizontal**  em relação à barra.

Para isso, adicione um seletor da classe  `.parametro-senha-textos`  e insira as propriedades  `display`  e  `justify-content`, com os valores mostrados abaixo:

```css
.parametro-senha-textos{
    display: flex;
    justify-content: space-between;
}

```

Pronto, seu texto já está alinhado conforme o protótipo!

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título Força da Senha, uma barra de cor vermelha e os textos: “Fraca”, “Média”  e “Forte”, alinhados horizontalmente.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula06_FCF-04.png)

### Inserindo as outras barras

Vamos adicionar agora as demais barras:  **"Média"**  e  **"Forte"**.

No arquivo CSS, abaixo do seletor  `.fraca`  adicione um seletor de classe  `.media`, incluindo nele as propriedades  `background-color`  e  `width`, com os valores mostrados abaixo:

```css
.media{
    background-color: #FAF408;
    width: 50%;
}

```

Em seguida, adicione um seletor de classe  `.forte`, incluindo nele as propriedades  `background-color`  e  `width`, com seus respectivos valores:

```css
.forte{
    background-color: #00FF85;
    width: 100%;
}

```

No arquivo HTML, você pode substituir a classe  `fraca`  por  `media`  ou  `forte`  para observar o resultado das demais barras no navegador:

```xml
<div class="forca fraca"></div>

```

Este será o resultado da substituição:![Gif do projeto no navegador com a cor de fundo azul escuro, o título Força da Senha, uma barra e os textos: “Fraca”, “Média”  e “Forte”, alinhados horizontalmente. A ilustração mostra a barra mudando de cor e largura na ordem: vermelho, amarelo, verde, indicando as posições “Fraca”, “Média” e “forte”, respectivamente.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula06_FCF-05.gif)

Na próxima aula, vamos aprender a adicionar e remover essas classes com JavaScript. Te espero lá!
# *`Aula 07`*
Nessa aula começamos a implementar o arquivo JavaScript no nosso projeto. Vamos revisar nosso código com os conceitos abaixo.

### Primeiros passos

Vamos tornar os botões "-" e "+" do protótipo funcionais.

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-01.png)

Para isso, crie um arquivo de nome  `main.js`:

![Captura de tela do Visual Studio Code indicando os arquivos: index.html, main.js e style.css.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-02.1.png)

Adicione no HTML a tag  `script`  com  `src="main.js"`  no final da tag  `body`:

```xml
<script src="main.js"></script>

```

### Acessando elementos através do DOM

Para acessar a parte da  `div`  do HTML, adicione no arquivo JavaScript a  **constante**  `numeroSenha`, atribuindo-a ao DOM com  `querySelector('.parametro-senha__texto')`, desta forma:

```javascript
const numeroSenha = document.querySelector('.parametro-senha__texto');

```

Agora, vamos acessar o conteúdo de  **texto**  da tag  `p`. Para isso crie uma variável  `let`  de nome  `tamanhoSenha`  e valor  **12**:

```bash
let tamanhoSenha = 12;

```

Logo abaixo, atualize a variável  `numeroSenha`, com a propriedade  `textContent`  e o valor  `tamanhoSenha`:

```bash
let tamanhoSenha = 12;
numeroSenha.textContent = tamanhoSenha;

```

Para acessar a classe dos botões, adicione uma nova  **constante**  de nome  `botoes`  atribuindo-a ao DOM, através do  `querySelectorAll('.parametro-senha__botao')`:

```javascript
const botoes = document.querySelectorAll('.parametro-senha__botao');

```

> O  `querySelectorAll`  selecionará  **todos os elementos**  que possuem essa classe.

Agora vamos verificarvamos verificar se a constante  `botoes`  está funcionando, adicionando  `console.log(botoes)`  no final do código :

```javascript
const numeroSenha = document.querySelector('.parametro-senha__texto');
let tamanhoSenha = 12;
numeroSenha.textContent = tamanhoSenha;

const botoes = document.querySelectorAll('.parametro-senha__botao');

console.log(botoes)

```

Você verá que as tags ‘button’ do HTML aparecem no console do navegador.

![Captura de tela do console do navegador indicando a lista “Node List” com os botões 0 e 1, suas respectivas clases “parametro-senha__botao”e a escrita “length”, indicando o comprimento da lista.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-02.2.png)

### Clique no botão  `-`

Para dar funcionalidade ao botão  `-`, vamos adicionar à ele um evento de clique.

Indique o objeto  `botoes[0]`, e atribua a ele o evento  `.onclick`  com a função  `diminuiTamanho`, que criaremos em breve:

```undefined
botoes[0].onclick = diminuiTamanho;

```

> O objeto  `botoes[0]`  acessará o  **primeiro item**  da lista  `botoes`, ou seja, o botão  `-`.

Agora crie a função  `diminuiTamanho()`  e insira dentro dela o retorno  `tamanhoSenha = tamanhoSenha-1;`

```csharp
function diminuiTamanho(){
    tamanhoSenha = tamanhoSenha-1;
}

```

> A função irá retornar o valor  **subtraído em 1**  toda vez que o botão  `-`  for clicado.

No entanto, podemos observar que quando clicamos, o novo número não é exibido:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza que ao clicar no botão “-”, nada acontece no projeto.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-03.gif)

Vamos resolver este problema adicionando uma  **atualização**  ao código.

Para isso,  **copie**  a linha  `numeroSenha.textContent = tamanhoSenha;`  e  **cole**  dentro da função criada:

```csharp
function diminuiTamanho(){
    tamanhoSenha = tamanhoSenha-1;
    numeroSenha.textContent = tamanhoSenha;
}

```

Pronto, a interação do botão  `-`  foi criada e o código já funciona corretamente!

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza que ao clicar no botão “-”, o número do visor é atualizado, sempre subtraído em 1.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-04.gif)

### Clique no botão  `+`

Vamos agora adicionar a funcionalidade do botão  `+`. Podemos basear o código do botão  `-`  para isso.

Abaixo do objeto  `botoes[0]`  indique também  `botoes[1]`, e atribua a ele o evento  `.onclick`  com a função  `aumentaTamanho`:

```undefined
botoes[0].onclick = diminuiTamanho;
botoes[1].onclick = aumentaTamanho;

```

> O objeto  `botoes[1]`  acessará o  **segundo item**  da lista  `botoes`, ou seja, o botão  `+`.

Agora, crie a função  `aumentaTamanho()`, adicionando nela o retorno  `tamanhoSenha = tamanhoSenha+1;`

```csharp
function aumentaTamanho(){
    tamanhoSenha = tamanhoSenha+1;
}

```

> Este retorno irá  **adicionar 1**  a cada vez que o botão  `+`  for clicado.

Por fim, para  **atualizar o valor**  exibido na tela, adicione a linha  `numeroSenha.textContent = tamanhoSenha;`  dentro da função:

```csharp
function aumentaTamanho(){
    tamanhoSenha = tamanhoSenha+1;
    numeroSenha.textContent = tamanhoSenha;
}

```

Seu botão  `+`  deve funcionar da seguinte forma:![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza que ao clicar no botão “+”, o número do visor é atualizado, sempre adicionado em 1.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-05.gif)

### Restrição para números inválidos

Nossos botões já estão funcionando, no entanto precisamos criar uma regra para que o  **número de caracteres**  seja possível somente  **entre 1 a 20**.

Para isso, adicione uma  **condição**  `if`  na função  `diminuiTamanho()`, com o parâmetro  `(tamanhoSenha > 1)`  , inserindo dentro dela o retorno  `tamanhoSenha = tamanhoSenha-1;`:

```csharp
function diminuiTamanho(){
    if (tamanhoSenha > 1){
        tamanhoSenha = tamanhoSenha-1;
    }
    numeroSenha.textContent = tamanhoSenha;
}

```

Você pode perceber que agora, números  **menores que 1**  não aparecem no projeto:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza que números menores que 1 não aparecem no visor.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-06.gif)

Faça o mesmo para a função  `aumentaTamanho()`, adicionando uma  **condição**  de parâmetro  `(tamanhoSenha < 20)`, e dentro dela o retorno  `tamanhoSenha = tamanhoSenha+1;`  ficará da seguinte forma:

```csharp
function aumentaTamanho(){
    if (tamanhoSenha < 20){
       tamanhoSenha = tamanhoSenha+1;
    }
    numeroSenha.textContent = tamanhoSenha;
}

```

Observe que os números  **maiores que 20**  também não ficarão disponíveis no visor:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Número de caracteres”, seguido de um botão “-”, o texto “12” e o botão “+”. A ilustração enfatiza que números maiores que 20 não aparecem no visor.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula07_FCF-07.gif)

### Aprimorando o código

Para aprimorar o código JavaScript, na função  `diminuiTamanho()`, comente a linha  `tamanhoSenha = tamanhoSenha-1;`  adicionando  `//`  na frente dela para torná-la  **inativa**.

Em seguida adicione  `tamanhoSenha--;`, para inserir o comando de  **subtrair 1**:

```csharp
function diminuiTamanho(){
    if (tamanhoSenha > 1){
       // tamanhoSenha = tamanhoSenha-1;
        tamanhoSenha--;
    }
    numeroSenha.textContent = tamanhoSenha;
}

```

> A expressão  `tamanhoSenha--`  é equivalente a  `x = (x - 1)`.

Agora na função  `aumentaTamanho()`, comente a linha  `tamanhoSenha = tamanhoSenha+1;`  para torná-la inativa e adicione  `tamanhoSenha++;`:

```csharp
function aumentaTamanho(){
    if (tamanhoSenha < 20){
       // tamanhoSenha = tamanhoSenha+1;
       tamanhoSenha++;
    }
    numeroSenha.textContent = tamanhoSenha;
}

```

> A expressão  `tamanhoSenha++`  é equivalente a  `x = (x + 1)`.

Seu código já está otimizado e funciona corretamente!

Na próxima aula vamos aprender a gerar senhas com o número de caracteres selecionado nos botões. Te espero lá!
# *`Aula 08`*
Nessa aula você aprendeu como gerar uma senha de letras maiúsculas. Vamos revisar nosso código com o conteúdo abaixo!

### Bloqueando o input

Antes de criar o gerador de senhas, vamos adicionar uma propriedade que irá  **bloquear**  o  `input name="senha"`, ou seja, ele não poderá ser editado.

Dentro da  `div`  `conteudo-senha`, adicione a propriedade  `readonly`  no elemento  `input`:

```bash
<input name="senha" type="text" id="campo-senha" readonly>

```

Observe que agora ele não pode mais ser editado:![Gif do projeto no navegador com a cor de fundo azul escuro, o campo de senha, o texto “Senha”. A ilustração enfatiza que o campo não é editável, pois ao clicar nele, nada acontece.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-01.gif)

Agora, no arquivo JavaScript, adicione uma  **constante**  de nome  `campoSenha`, atribuindo-a ao DOM e selecionando o id  `#campo-senha`:

```javascript
const campoSenha = document.querySelector('#campo-senha');

```

Crie também uma nova  **constante**  de nome  `letrasMaiusculas`  e valor  `'ABCDEFGHIJKLMNOPQRSTUVXYWZ'`, para adicionar  **todas as letras do alfabeto**:

```csharp
const letrasMaiusculas = 'ABCDEFGHIJKLMNOPQRSTUVXYWZ';

```

Para exibir o resultado dentro do campo de senha, adicione  `campoSenha.value`  com retorno  `letrasMaiusculas`:

```csharp
const letrasMaiusculas = 'ABCDEFGHIJKLMNOPQRSTUVXYWZ';

campoSenha.value = letrasMaiusculas;

```

Observe o resultado no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o campo de senha, o texto “Senha” e o texto: “ABCDEFGHIJKLMNOPQRSTUVWXYZ”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-02.png)

### Criando números aleatórios

Agora vamos adicionar uma sequência de números aleatórios para testar o gerador.

Para isso, crie uma função  `geraSenha()`, inserindo nela a variável  `let numeroAleatorio`.

Adicione no valor da variável  `numeroAleatorio`  a função  `Math.random()`, multiplicada (`*`) pela constante  `letrasMaiusculas`  e atribuindo a propriedade  `.length`:

```javascript
function geraSenha(){
    let numeroAleatorio = Math.random()*letrasMaiusculas.length;
    console.log(numeroAleatorio);
}

```

> A função  `Math.random()`  gera um número aleatório. Ao multiplicar por  `letrasMaiusculas.length`, este número terá entre 0 e 26 casas decimais.

Para executar a função criada acima, adicione a chamada  `geraSenha();`  abaixo da constante  `letrasMaiusculas`:

```csharp
const letrasMaiusculas = 'ABCDEFGHIJKLMNOPQRSTUVXYWZ';
geraSenha();

```

Observe o resultado no console e perceba que os números estão com uma grande quantidade de casas decimais:![Captura de tela do console exibindo o valor “20.748839436561507”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-03.png)

### Arredondando os resultados

Vamos arredondar esses números usando a função  `Math.floor`.

Para isso, adicione uma nova linha para a variável  `numeroAleatorio`, atribuindo a ela a função  `Math.floor(numeroAleatorio)`, como mostra a seguir:

```javascript
function geraSenha(){
    let numeroAleatorio = Math.random()*letrasMaiusculas.length;
    numeroAleatorio = Math.floor(numeroAleatorio);
    console.log(numeroAleatorio);
}

```

Observe agora o novo resultado do console:

![Gif do console do navegador exibindo números aleatórios de 0 a 26.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-04.gif)

Agora, são exibidos números aleatórios  **sem casas decimais**.

### Obtendo letras

Feito isso, vamos mudar a chamada do console para que sejam exibidas  **letras**  ao invés de números.

Altere a saída do console de  `numeroAleatorio`  para  `letrasMaiusculas[numeroAleatorio]`, como mostra abaixo:

```javascript
function geraSenha(){
    let numeroAleatorio = Math.random()*letrasMaiusculas.length;
    numeroAleatorio = Math.floor(numeroAleatorio);
    console.log(letrasMaiusculas[numeroAleatorio]);
}

```

Observe que agora, a saída do console ocorre  **em letras**:

![Gif do console do navegador exibindo letras aleatórias de A a Z.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-05.gif)

### Adicionando uma sequência de letras aleatórias

Para adicionar uma  **sequência de letras**  é necessário uma  **repetição**.

Crie dentro da função  `geraSenha()`  um laço de repetição  `for`  de parâmetros  `(let i = 0; i < tamanhoSenha;i++)`  e adicione dentro dele as linhas criadas anteriormente:

```javascript
function geraSenha(){
    for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*letrasMaiusculas.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        console.log(letrasMaiusculas[numeroAleatorio]);
    }
}

```

Observe agora o que aparece no console do navegador:

![Captura de tela do console exibindo as letras em sequência: X, F, W, R, X, D, N, H, B, F, B, Z.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-06.png)

Neste caso, apareceram 12 letras pois o valor inicial do  **Número de caracteres**  é igual a  **12**.

### Corrigindo o erro nos botões

Observe o teste abaixo, perceba que quando atualizamos o número de caracteres a senha não é atualizada no console:

![Gif do console e do navegador. Na parte do navegador os botões “+” e “-” são clicados. Na parte do console nenhuma atualização acontece.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-07.gif)

Para corrigir este  _bug_  (erro), vamos adicionar a chamada  `geraSenha()`  nas funções  `diminuiTamanho()`  e  `aumentaTamanho()`, referente a cada um dos botões:

```csharp
function diminuiTamanho(){
    if (tamanhoSenha > 1){
       // tamanhoSenha = tamanhoSenha-1;
        tamanhoSenha--;
    }
    numeroSenha.textContent = tamanhoSenha;
    geraSenha();
}
function aumentaTamanho(){
    if (tamanhoSenha < 20){
       // tamanhoSenha = tamanhoSenha+1;
       tamanhoSenha++;
    }
    numeroSenha.textContent = tamanhoSenha;
    geraSenha();
}

```

Pronto, agora tudo funciona corretamente!

### Juntando as letras

Por fim, vamos  **concatenar**, ou seja,  **unir as letras**  para formar uma senha.

Adicione na função  `geraSenha()`  a variável  `let senha = '' ”;`, para que ela inicie vazia:

```javascript
function geraSenha(){
    let senha = '' ”;
    for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*letrasMaiusculas.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        console.log(letrasMaiusculas[numeroAleatorio]);
    }
}

```

Feito isso,  **apague a linha**  `console.log`, pois utilizamos apenas para verificar o funcionamento do código, então não será mais necessário mantê-la.

Em seguida, insira dentro da repetição  `for`  a variável  `senha`, atribuindo à ela o valor  `senha + letrasMaiusculas[numeroAleatorio];`:

```javascript
function geraSenha(){
    let senha = '' ”;
    for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*letrasMaiusculas.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + letrasMaiusculas[numeroAleatorio];
    }
}

```

Agora, vamos alterar a linha  `campoSenha.value = letrasMaiusculas;`, que está  **fora da função**. Substitua seu valor para  `senha`, desta forma:

```ini
campoSenha.value = senha;

```

Por último, mova esta linha para dentro da função  `geraSenha()`:

```javascript
function geraSenha(){
    let senha = '' ”;
    for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*letrasMaiusculas.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + letrasMaiusculas[numeroAleatorio];
    }
    campoSenha.value = senha;
}

```

Seu projeto ao final da aula ficará assim:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o campo de senha, o texto “Senha”, seguido da seção “Personalize sua senha”, o título “número de caracteres” e os botões “-” e “+”. A ilustração mostra que quando os botoes são clicados, uma nova senha é gerada de acordo com o número de carateres correspondente no visor.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula08_FCF-08.gif)

Na próxima aula vamos adicionar outras funcionalidades ao gerador! Te espero lá!
# *`Aula 09`*
Nessa aula aprendemos como adicionar regras aos campos de  _checkbox_  do nosso projeto. Vamos revisar nosso código com o conteúdo abaixo!

### Acessando os checkboxes

Para acessar as caixas de seleção, adicione uma  **constante**  de nome  `checkbox`, atribuindo-a ao DOM através do  `querySelectorAll`  e selecionando a classe  `.checkbox`:

```javascript
const checkbox = document.querySelectorAll('.checkbox');

```

Insira também uma saída  `console.log`  para observar se o primeiro checkbox está marcado:

```javascript
const campoSenha = document.querySelector('#campo-senha');
const checkbox = document.querySelectorAll('.checkbox');

console.log(checkbox[0].checked);

```

Observe o que aparece no console:

![Captura de tela do console exibindo o valor “True”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-01.png)

> Neste caso apareceu  `true`  pois o checbox está marcado.

Agora que já verificamos, você pode  **excluir a linha**  `console.log(checkbox[0].checked);`.

### Determinando novas características

Até agora, nosso gerador só exibe senhas com letras maiúsculas. Vamos então determinar novas características para as senhas.

Abaixo da  `const`  `letrasMaiusculas`, adicione uma nova  **constante**  de nome  `letrasMinusculas`  e valor  `'abcdefghijklmnopqrstuvxywz'`, para inserir  **o alfabeto de letras minúsculas.**

```csharp
const letrasMinusculas = 'abcdefghijklmnopqrstuvxywz';

```

Agora, adicione uma  **constante**  de nome  `numeros`  e valor  `'0123456789'`, para inserir  **todos os números.**

```csharp
const numeros = '0123456789';

```

Por último, adicione uma  **constante**  de nome  `simbolos`  e valor  `'!@%*?'`, para inserir  **todos os símbolos.**

```csharp
const simbolos = '!@%*?';

```

### Verificando checkboxes

Vamos criar agora uma  **verificação**, para saber se os seletores estão marcados ou não.

Começando pelas letras maiúsculas, no início da função  `geraSenha()`, adicione a variável  `let alfabeto`, de valor vazio:

```bash
let alfabeto = '';

```

Agora, insira uma condição  `if`  com o parâmetro  `(checkbox[0].checked)`, que irá verificar se o  **primeiro checkbox**  foi marcado.

```bash
let alfabeto = '';
if (checkbox[0].checked){
}

```

Adicione também uma nova declaração da variável  `alfabeto`, atribuindo agora o valor  `alfabeto + letrasMaiusculas`:

```bash
let alfabeto = '';
if (checkbox[0].checked){
    alfabeto = alfabeto + letrasMaiusculas;
}

```

Por último, adicione uma saída  `console.log`  de valor  `alfabeto`, para checar o novo valor da variável:

```javascript
let alfabeto = '';
if (checkbox[0].checked){
    alfabeto = alfabeto + letrasMaiusculas;
}
console.log(alfabeto);

```

Observe o resultado do console:

![Captura de tela do console exibindo o valor “ABCDEFGHIJKLMNOPQRSTUVWXYZ”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-02.png)

### Adicionando um novo comando

Perceba que, quando clicamos nos seletores a senha não é atualizada:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Personalize sua senha”,  e dois blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 5 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. A ilustração enfatiza as caixas de seleção sendo desmarcadas e nenhuma atualização acontece na senha.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-03.gif)

Vamos corrigir este problema adicionando um  **evento de clique**.

Abaixo das constantes  `campoSenha`  e  `checkbox`, adicione um laço de repetição  `for`  com parâmetro  `(i=0; i < checkbox.length;i++)`:

```scss
for (i=0; i < checkbox.length;i++){
 
}

```

Insira dentro dele o índice  `checkbox[i]`  com o evento  `.onclick`, atribuindo a função  `geraSenha`:

```markdown
for (i=0; i < checkbox.length;i++){
    checkbox[i].onclick = geraSenha;
}

```

Observe que, no console aparece uma atualização em azul, no canto direito, a cada vez que os checkboxes são clicados.

![Gif do console exibindo o valor “empty string”, que significa “string vazia” e a atualização numérica do lad direito em azul.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-04.gif)

### Continuando a verificação de checkboxes

Para continuar criando a verificação de cada seletor, copie o padrão da condição  `if`, alterando seu  **índice**  e o valor da constante, assim como mostra nos códigos abaixo.

Verificando letras minúsculas:

```markdown
if (checkbox[1].checked){
    alfabeto = alfabeto + letrasMinusculas;
}

```

Verificando números:

```markdown
if (checkbox[2].checked){
    alfabeto = alfabeto + numeros;
}

```

Verificando símbolos:

```markdown
if (checkbox[3].checked){
    alfabeto = alfabeto + simbolos;
}

```

Observe o resultado do projeto quando clicamos em cada uma das caixas de seleção:

![Gif do console exibindo o valor “ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz”. A ilustração enfatiza que o valor é atualizado três vezes, adicionando e removendo alfabetos.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-05.gif)

### Alteração no  `for`

Agora, vamos fazer uma pequena alteração no laço  `for`  da função  `geraSenha`, para que seja possível  **utilizar todos os alfabetos**  na senha.

Para isso, substitua a constante  `letrasMaiusculas`  por  `alfabeto`  nas linhas do  `for`. Seu  `for`  deve ficar assim:

```javascript
for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*alfabeto.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + alfabeto[numeroAleatorio];
    }

```

Você pode conferir o código completo da função  `geraSenha()`  abaixo:

```javascript
function geraSenha(){
    let alfabeto = '';
    if (checkbox[0].checked){
        alfabeto = alfabeto + letrasMaiusculas;
    }
    if (checkbox[1].checked){
        alfabeto = alfabeto + letrasMinusculas;
    }
    if (checkbox[2].checked){
        alfabeto = alfabeto + numeros;
    }
    if (checkbox[3].checked){
        alfabeto = alfabeto + simbolos;
    }
    console.log(alfabeto);
    let senha = '';
    for (let i = 0; i < tamanhoSenha;i++){
        let numeroAleatorio = Math.random()*alfabeto.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + alfabeto[numeroAleatorio];
    }
    campoSenha.value = senha;
}

```

Seu projeto ao final da aula ficará assim:![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Personalize sua senha”,  e dois blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 5 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. A ilustração enfatiza as caixas de seleção sendo marcadas e a senha sendo atualizada.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula09_FCF-06.gif)
# *`Aula 10`*
Nessa aula, aprendemos como criar a funcionalidade da divisão  **Força da Senha**. Vamos revisar nosso código com o conteúdo abaixo!

### Organizando o código

Antes de iniciar a criação do código, vamos organizar alguns elementos para facilitar a leitura.

Primeiro,  **reposicione**  todas as variáveis  `let`  e constantes  `const`  nas primeiras linhas do arquivo. Seu código deve ficar assim:

```javascript
const numeroSenha = document.querySelector('.parametro-senha__texto');
let tamanhoSenha = 12;
numeroSenha.textContent = tamanhoSenha;
const letrasMaiusculas = 'ABCDEFGHIJKLMNOPQRSTUVXYWZ';
const letrasMinusculas = 'abcdefghijklmnopqrstuvxywz';
const numeros = '0123456789';
const simbolos = '!@%*?';
const botoes = document.querySelectorAll('.parametro-senha__botao');
const campoSenha = document.querySelector('#campo-senha');
const checkbox = document.querySelectorAll('.checkbox');

```

### Classificando a senha

Vamos agora classificar nossa senha em  **fraca, média e forte**.

Para isso, adicione uma constante  `forcaSenha`, atribuindo-a ao DOM através do  `querySelector`, selecionando a classe  `.forca`

```javascript
const forcaSenha = document.querySelector('.forca');

```

Em seguida crie abaixo da função  `geraSenha()`  uma nova função de nome  `classificaSenha()`.

```csharp
function classificaSenha(){

}

```

Dentro dela acesse a constante  `forcaSenha`, inserindo o seletor  `classList`  com a propriedade  `add`  para adicionar a classe  `forte`:

```csharp
function classificaSenha(){
    forcaSenha.classList.add('forte');

}

```

Agora, insira a chamada da função  `classificaSenha()`  no final da função  `geraSenha()`, desta forma:

```javascript
function geraSenha() {
    let alfabeto = '';
    if (checkbox[0].checked) {
        alfabeto = alfabeto + letrasMaiusculas;
    }
    if (checkbox[1].checked) {
        alfabeto = alfabeto + letrasMinusculas;
    }
    if (checkbox[2].checked) {
        alfabeto = alfabeto + numeros;
    }
    if (checkbox[3].checked) {
        alfabeto = alfabeto + simbolos;
    }
    let senha = '';
    for (let i = 0; i < tamanhoSenha; i++) {
        let numeroAleatorio = Math.random() * alfabeto.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + alfabeto[numeroAleatorio];
    }
    campoSenha.value = senha;
    classificaSenha();
}

```

Observe o resultado no navegador:![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”. A barra possui cor verde e está indicando “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula10_FCF-01.png)

### Removendo classes

Ao clicar em  `inspecionar`  no console, é possível observar que a  `div`  de classe  `forca`  possui mais duas classes:  `fraca`  e  `forte`:

![Captura de tela do console exibindo o valor HTML: “<div class= “forca fraca forte”></div>”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula10_FCF-02.png)

Vamos resolver isso  **removendo**  inicialmente essas classes.

Acesse no início da função  `classificaSenha()`  a constante  `forcaSenha`, inserindo o seletor  `classList`  com propriedade  `remove`  para remover as classes  `fraca`,  `media`,  `forte`:

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    
    forcaSenha.classList.add('forte');
}

```

Agora, todas as classes foram removidas e a barra ficará vazia:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Personalize sua senha” e três blocos agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”. A ilustração enfatiza que a barra de força muda da cor amarelo para verde quando tem um número de caracteres maior que 11.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula10_FCF-03.gif)

### Regra das barras

Vamos agora inserir uma regra que irá determinar quando cada barra deve aparecer.

Adicione dentro da função  `classificaSenha()`  uma condição  `if`  de parâmetro  `(tamanhoSenha > 11)`.

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){

    }
}

```

Dentro dela, insira a linha que criamos para  **adicionar**  a classe  `forte`, desta forma:

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){
        forcaSenha.classList.add('forte');
    }
}

```

Em seguida, inclua após o  `if`  uma nova condição  `else`:

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){
        forcaSenha.classList.add('forte');
    } else {
        forcaSenha.classList.add('media');
    } 
}

```

Observe o resultado no navegador, perceba que a barra é atualizada de acordo com o tamanho de caracteres:

![Gif do projeto no navegador com a cor de fundo azul escuro, o título “Personalize sua senha” e três blocos agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”. A ilustração enfatiza a regra: para números menores que 5, a cor da barra será vermelho. Para números entre 6 e 11, a cor da barra será amarelo, para números entre 12 e 26, a barra será verde”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula10_FCF-04.gif)

Agora vamos criar uma nova regra para a classe  `fraca`  no mesmo  `if`, mas antes é necessário organizar a condição já criada.

Para isso, seguido do  `else`  adicione uma nova condição  `if`  com os parâmetros  `(tamanhoSenha > 5 && tamanhoSenha < 12 )`, e insira dentro dela a linha que  **adiciona**  a classe  `media`:

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){
        forcaSenha.classList.add('forte');
    } else if (tamanhoSenha > 5 && tamanhoSenha < 12 ) {
        forcaSenha.classList.add('media');
    }
}

```

> Na condição criada, a classe  `media`  será exibida se o  `tamanhoSenha`  for equivalente a um  **número entre 6 e 11**.

Agora, adicione uma terceira condição  `else if`  com parâmetro  `(tamanhoSenha <= 5)`  e retorno  `forcaSenha.classList.add('fraca');`:

```csharp
function classificaSenha(){
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){
        forcaSenha.classList.add('forte');
    } else if (tamanhoSenha > 5 && tamanhoSenha < 12 ) {
        forcaSenha.classList.add('media');
    } else if (tamanhoSenha <= 5){
        forcaSenha.classList.add('fraca');
    }
}

```

Pronto! Observe que a regra já funciona corretamente!

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, uma imagem de cadeado na cor azul royal, seguido do título “Gerador de senhas”, o título secundário “Gere instantaneamente uma senha aleatória e segura”, o campo de texto de cor branca com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiúsculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”. A ilustração enfatiza o funcionamento da regra, onde números maiores que 5 identificam a barra “ Fraca”, números entre 6 e 11 identificam a barra “Média” e números maiores que 12 identificam a barra “forte”.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula10_FCF-05.gif)
# *`Aula 11`*
Nessa aula, entendemos o conceito de entropia das senhas. Vamos revisar nosso código com os conceitos abaixo.

### Entropia

Em sua definição, a entropia é uma  **medida de incerteza**  e  **aleatoriedade**.

É uma forma de medir a força da sua senha, calculando o quão  **previsível ou imprevisível**  ela é, por exemplo, quanto maior for a entropia, mais imprevisível será a sua senha.

Para calculá-la utilizamos uma equação, observe abaixo:

![Captura de tela da equação: H = L X log2(n)](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_01.png)

Sendo:

-   H = Entropia
-   L = Comprimento da senha
-   N = Tamanho dos conjuntos de caracteres

Mas afinal, o que significa  `log2`?

O  `log`  é um registro inverso da equação exponencial, ou seja, ele irá calcular o  **número de possibilidades**  até encontrar seu resultado final. O log é como um “detetive matemático” que nos ajuda a descobrir o número de opções necessárias para chegar a um resultado específico. Observe o exemplo abaixo:

![Captura de tela do texto referente à operação matemática que relaciona a potência de 2 elevado a 'b' com o logaritmo na base 2 de 8. Nesse exemplo, b é igual a 3, demonstrando que 2 elevado a 3 resulta em 8, o que é o mesmo que multiplicar 2 por 2 três vezes, totalizando 8](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_02.png)

Nesse caso, o resultado dessa equação será  _3 bits_, pois o número 2 se multiplica  **três vezes**  para alcançar o resultado ‘8’.

### Implementando no código

Vamos agora utilizar a entropia no nosso projeto.

No arquivo JavaScript, adicione dentro da função  `classificaSenha()`  uma variável  `let entropia`, atribuindo o valor  `tamanhoSenha * Math.log2(alfabeto.length);`:

```javascript
let entropia = tamanhoSenha * Math.log2(alfabeto.length);

```

Em seguida adicione uma saída no console do navegador, para verificar o funcionamento da nova variável que criamos:

```cpp
console.log(entropia);

```

Perceba que, no console aparece um erro, pois o alfabeto não está definido.

![Captura de tela do console no navegador exibindo um erro, seguido do texto: Uncaught ReferenceError: alfabeto is not defined. A ilustração indica que há um erro no console pois “alfabeto” não está definido.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_03.png)

Para resolver este problema, adicione a referência  `alfabeto.length`  no parâmetro da função  `clasisficaSenha`, dentro da função  `geraSenha`:

```javascript
function geraSenha() {
    let alfabeto = '';
    if (checkbox[0].checked) {
        alfabeto = alfabeto + letrasMaiusculas;
    }
    if (checkbox[1].checked) {
        alfabeto = alfabeto + letrasMinusculas;
    }
    if (checkbox[2].checked) {
        alfabeto = alfabeto + numeros;
    }
    if (checkbox[3].checked) {
        alfabeto = alfabeto + simbolos;
    }
    let senha = '';
    for (let i = 0; i < tamanhoSenha; i++) {
        let numeroAleatorio = Math.random() * alfabeto.length;
        numeroAleatorio = Math.floor(numeroAleatorio);
        senha = senha + alfabeto[numeroAleatorio];
    }
    campoSenha.value = senha;
    classificaSenha(alfabeto.length);

}

```

Agora, adicione o parâmetro  `tamanhoAlfabeto`  na função  `classificaSenha`:

```csharp
function classificaSenha(tamanhoAlfabeto){
    let entropia = tamanhoSenha * Math.log2(alfabeto.length);
    console.log(entropia);
    forcaSenha.classList.remove('fraca','media','forte');
    if (tamanhoSenha > 11){
        forcaSenha.classList.add('forte');
    } else if (tamanhoSenha > 5 && tamanhoSenha < 12) {
        forcaSenha.classList.add('media');
    } else if (tamanhoSenha <= 5){
        forcaSenha.classList.add('fraca');
    }
}

```

Insira este mesmo parâmetro na função  `Math.log2();`, substituindo o valor  `alfabeto.length`, dentro da mesma função  `classificaSenha(tamanhoAlfabeto)`:

```javascript
let entropia = tamanhoSenha * Math.log2(tamanhoAlfabeto);

```

Observe agora no console que não apresenta mais erro:

![Captura de tela do console no navegador exibindo o valor: 69.9946801699769](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_04.png)

### Aumentando a entropia

Para aumentar a incerteza da senha, vamos adicionar o padrão de entropia nas condições.

Na primeira condição  `if`  dentro da função  `classificaSenha`, substitua o parâmetro  `(tamanhoSenha > 11)`  por  `(entropia > 57)`:

```csharp
if (entropia > 57){
    forcaSenha.classList.add('forte');
} else if (tamanhoSenha > 5 && tamanhoSenha < 12) {
    forcaSenha.classList.add('media');
} else if (tamanhoSenha <= 5){
    forcaSenha.classList.add('fraca');
}

```

Agora, na condição  `else if`  substitua o parâmetro  `(tamanhoSenha > 5 && tamanhoSenha < 12)`  por  `(entropia > 35 && entropia < 57)`:

```csharp
if (entropia > 57){
    forcaSenha.classList.add('forte');
} else if (entropia > 35 && entropia < 57) {
    forcaSenha.classList.add('media');
} else if (tamanhoSenha <= 5){
    forcaSenha.classList.add('fraca');
}

```

Por último, substitua na segunda condição  `else if`  o parâmetro  `(tamanhoSenha <= 5)`  por  `(entropia <= 35)`:

```csharp
function classificaSenha(tamanhoAlfabeto){
    let entropia = tamanhoSenha * Math.log2(tamanhoSenha);
    console.log(entropia);
    forcaSenha.classList.remove('fraca','media','forte');
    if (entropia > 57){
        forcaSenha.classList.add('forte');
    } else if (entropia > 35 && entropia < 57) {
        forcaSenha.classList.add('media');
    } else if (entropia <= 35){
        forcaSenha.classList.add('fraca');
    }
}

```

Observe o resultado no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o campo de texto de cor azul com o título “Senha”, seguido da nova seção de conteúdo. A nova seção possui o título “Personalize sua senha” e três blocos de texto agrupados em linha. O primeiro bloco contém o título “Número de caracteres” e um botão “- 12 +”, o segundo bloco contém o título Características da senha e um checklist com os textos: “Letras maiusculas”, “letras minúsculas”, “Números”, “símbolos”. O terceiro bloco contém o título “Força da senha” e uma barra de indicação dos valores “fraca”, “média”, “forte”. A ilustração enfatiza que ao selecionar as opções da caixa de seleção, a barra de força da senha muda de cor e tamanho e uma nova senha é atualizada.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_05.gif)

### Exibição do cálculo

Para exibir a entropia no projeto, adicione no arquivo HTML, na última  `div`  `parametro-senha`, uma tag  `p`  de classe  `entropia`:

```xml
<p class="entropia"></p>

```

Agora, no arquivo JavaScript, adicione dentro da função  `classificaSenha`  uma constante de nome  `valorEntropia`, atribuindo-a ao DOM e selecionando a classe  `.entropia`:

```javascript
const valorEntropia = document.querySelector('.entropia');

```

Em seguida, adicione uma chamada da constante que acabamos de criar, inserindo nela a propriedade  `textContent`  e atribuindo o valor  `2**Math.floor(entropia)`:

```javascript
const valorEntropia = document.querySelector('.entropia');
valorEntropia.textContent = 2**Math.floor(entropia);

```

Observe que é exibido um número muito extenso no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Força da senha”, uma barra de indicação dos valores “fraca”, “média”, “forte” e uma sequência de números. A ilustração enfatiza que a sequência de números está indicando a entropia da senha.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula11_FCF_06.png)

Para  **reduzir**  este número, adicione a divisão pelo número  `100e6*60*60*24`:

```javascript
const valorEntropia = document.querySelector('.entropia');
valorEntropia.textContent = 2**Math.floor(entropia)/(100e6*60*60*24);

```

Interpretando este valor, temos:

-   `100e6`: 1.000.000, ou seja, a quantidade em  **milissegundos**;
-   `*60`: 60  **segundos**;
-   `*60`: 60  **minutos**;
-   `*24`: 24  **horas**.

Pronto, agora seu projeto já está considerando o conceito de entropia na classificação das senhas!
# *`Aula 12`*
Nessa aula aprendemos como aprimorar a exibição da entropia no projeto. Vamos revisar nosso código com os conceitos a seguir

### Corrigindo a exibição

Observe que no projeto, a exibição do número de entropia continua de uma forma muito extensa:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Força da senha”, uma barra de indicação dos valores “fraca”, “média”, “forte” e uma sequência de números. A ilustração enfatiza o extenso número da sequência que está indicando a entropia da senha.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula12_FCF-01.png)

Para exibir a resposta em  **dias**. Corrija o código da função  `classificaSenha`, inserindo toda a operação do  `Math.floor`  entre os parênteses, desta forma:

Antes

```ini
valorEntropia.textContent = 2**Math.floor(entropia)/(100e6*60*60*24);

```

Depois

```ini
valorEntropia.textContent = Math.floor(2**entropia/(100e6*60*60*24));

```

Agora o valor será exibido em  **dias**:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Força da senha”, uma barra de indicação dos valores “fraca”, “média”, “forte” e uma sequência de números. A ilustração enfatiza a sequência de números: 11045.](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula12_FCF-02.png)

### Concatenando textos e números

Vamos criar um contexto de exibição, para que a aparição deste número faça sentido no projeto.

Para isso, na mesma linha da constante  `valorEntropia`, adicione logo após o sinal  `=`  o texto  `"Um computador pode levar até "`  e o símbolo  `+`  para  **concatenar**  os elementos:

```ini
valorEntropia.textContent = "Um computador pode levar até " + Math.floor(2**entropia/(100e6*60*60*24));

```

Em seguida, após a expressão da função  `Math.floor`, adicione novamente o sinal  `+`  e o texto  `" dias para descobrir essa senha."`:

```ini
valorEntropia.textContent = "Um computador pode levar até " + Math.floor(2**entropia/(100e6*60*60*24)) + " dias para descobrir essa senha.";

```

Observe como aparece agora no navegador:

![Captura de tela do projeto no navegador com a cor de fundo azul escuro, o título “Força da senha”, uma barra de indicação dos valores “fraca”, “média”, “forte”, seguido do texto: “Um computador pode levar até 11045 dias para descobrir essa senha.”](https://cdn3.gnarususercontent.com.br/3416+-+JavaScript%3A+senhas+seguras+com+matem%C3%A1tica+e+programa%C3%A7%C3%A3o/aula12_FCF-03.png)

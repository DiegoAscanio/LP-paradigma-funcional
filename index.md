<style>
  section {
    background: #fff url(./img/background.png) no-repeat center center;
    background-size: cover;
  }

  section.center img {
    display: block;
    margin: auto;
  }

  img[alt=small-img] {
    display: block;
    margin: auto;
    width: 45%;
  }

  .transparent {
    background-color: transparent!important;
  }

  section.transparent img {
    background-color: transparent!important;
  }

  section.ttable table {
    margin: auto;
  }

  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }

  .conteudo {
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }

  .conteudo-absoluto {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
  
  .large {
    font-size: 36px;
  }

  .normal {
    font-size: 22px;
  }
  .regular {
    font-size: 18px;
  }
  .small {
    font-size: 16px;
  }
  .footnotesize {
    font-size: 14px;
  }
  .scriptsize {
    font-size: 12px;
  }
  .tiny {
    font-size: 10px;
  }
  .bold {
    font-weight: bold;
  }
  .center {
    text-align: center;
  }
  section.lead p {
    text-align: justify;
  }
  section.lead h1 {
    text-align: center;
  }
  section.lead h2 {
    text-align: center;
  }
  section.lead h3 {
    text-align: center;
  }
  section.lead h4 {
    text-align: center;
  }

  
  .grid-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: justify;
  }

  .grid-25-25-25-25 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    text-align: justify;
  }

  .grid-33-33-33 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    text-align: justify;
  }


  .grid-66-33 {
    display: grid;
    grid-template-columns: 2fr 1fr;
    text-align: justify;
  }

  .grid-33-66 {
    display: grid;
    grid-template-columns: 1fr 2fr;
    text-align: justify;
  }

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
  }
  img[alt=grid-img] {
    width: 100%;
  }
  img[alt=slide-img] {
    width: 75%;
  }
  img[alt=reduced-img] {
    width: 40%;
  }

  .dashedmargin {
    border-style: dashed;
  }

  .solidmargin {
    padding: 9px;
    border-style: solid;
  }

  .tooltip {
    position: relative;
    display: inline-block;
    cursor: pointer;
    border-bottom: 1px dotted #7851a9;
    color: #7851a9;
  }

  .tooltip .tooltiptext {
    visibility: hidden;
    width: 300px;
    top: 100%;
    left: 50%;
    margin-left: -150px;
    background-color: #7851a9;
    color: #fff;
    text-align: justify;
    border-radius: 6px;
    padding: 5px 5px;
    opacity: 0;

    position: absolute;
    z-index: 1;
  }

  .tooltip:hover .tooltiptext {
    visibility: visible;
    opacity: 1;
  }

</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>


# Linguagens de Programação
## Paradigma Funcional
 
Prof. [M.Sc. Diego Ascânio Santos](mailto:ascanio@cefetmg.br)

Aula baseada sobre os materiais do professor [Dr. Andrei Rimsa Alvares](mailto:andrei@cefetmg.br) e da bibliografia padrão da disciplina.

CEFET-MG DIGDDV - Divinópolis, 2023.


---

## Roteiro

1. Introdução
2. Programação Funcional
3. Programação Funcional em Python


---

## Introdução

<div class="grid-66-33 normal">

<div class="grid-element">

- Programação funcional é baseada no conceito de funções matemáticas;
- Uma função matemática é um mapeamento entre um conjunto de valores de entrada (**domínio**) e um conjunto de valores de saída (**imagem**);

</div>
<div class="grid-element">

<!-- _class: transparent center -->
![](https://i.imgur.com/KUo0c20.png)

</div>
</div>
<div class="normal">

- Recursões (chamadas às próprias funções) e expressões condicionais controlam o fluxo da execução em vez de sequenciamentos de instruções e iterações.
- Idealmente não possuem efeitos colaterais, ou seja, produzem sempre a mesma saída para a mesma entrada.

</div>


---

## Introdução
### Exemplo de Função

<div class="grid-66-33 regular">

<div class="grid-element">

- Função Círculo (retorna a área de um círculo de diâmetro \\(d\\))

\\[
    \text{circulo}(d) = \pi (\frac{d}{2})^2
\\]

- Domínio: \\(d \in \Re^{+}\\)
- **=**: símbolo de atribuição, que neste caso significa símbolo de definição, ou seja, que a função é definida como.
- \\(\textbf{d}\\): representa qualquer elemento do domínio (da entrada) da função.
- Imagem: \\(\text{circulo}(d) \in \Re^{+}, d \in \Re^{+}\\)

- As variáveis de funções nos paradigmas funcionais são diferentes de variáveis no paradigma imperativo porque são imutáveis (não podem ser alteradas após a sua definição). Por isso, o símbolo de atribuição é usado para definir uma função, e não para atribuir um valor a uma variável.
    - A imutabilidade das variáveis colabora para mitigar efeitos colaterais nas funções.

</div>

<div class="grid-element">

<!-- _class: transparent center -->
![small-img](https://i.imgur.com/eSmboyr.png)

</div>

</div>


---

## Introdução
### Formas Funcionais

<div class="normal">

**Formas Funcionais** ou **funções de ordem superior** são funções que recebem outras funções como parâmetro ou retornam funções como resultado.

São essenciais para a programação funcional e possuem inspiração nas funções matemáticas de ordem superior, onde verificamos a existência de funções compostas. Exemplo de função matemática (e computacional) composta:

\\[
\begin{align}
    f(x) &= x + 2 \\\\
    g(x) &= 3x \\\\
    h(x) &= (f \circ g)(x) \therefore \\\\
    h(x) &= f(g(x)) = f(3x) = 3x + 2
\end{align}
\\]

O que diferem as funções matemáticas compostas das formas funcionais do paradigma funcional é que as primeiras não retornam outras funções como resultado, apenas valores numéricos. Já as segundas, sim.

</div>


---

## Introdução
### Exemplo de Formas Funcionais que Recebem Funções Como Argumentos

<div class="normal">

```python
square = lambda x: x * x
numeros = range(1, 10)
# a função map em python é uma forma funcional, pois recebe uma função 
# e uma lista como argumentos, aplica esta função a cada elemento da
# lista e retorna uma nova lista com os resultados.
# Assim, map é uma função de ordem superior que recebe funções
# e iteradores como argumentos.

numeros_quadrados = map(square, numeros)
print(list(numeros_quadrados))
```

</div>


---

## Introdução
### Exemplo de Quasi-Formas Funcionais que Retornam Funções

<div class="small">

```python
# Exemplo de Quasi-Forma Funcional que retorna funções em python
# Aqui coloquei quasi-forma funcional porque o acesso a valores
# em dicionários em python não ocorre através de funções, mas,
# sim, por meio de hash tables. Porém, o comportamento que
# esperamos — que a partir de determinado parâmetro, nesse caso
# uma chave que representa um dos estados possíveis do AFD —
# seja retornada uma função responsável por processar o estado
# da chave, é o mesmo que ocorre com as formas funcionais.

# Aqui encontra-se descrito o AFD do analisador léxico da
# linguagem tiny
AFD = {
    estados.inicial: processar_estado_1,
    estados.ler_comentarios: processar_estado_2,
    estados.ler_atribuicao_comparacao_ou_igualdade: processar_estado_3,
    estados.ler_nao_igual: processar_estado_4,
    estados.ler_variavel: processar_estado_5,
    estados.ler_digito: processar_estado_6,
    estados.criar_token_reservado_ou_variavel: processar_estado_7,
    estados.criar_token_numerico: processar_estado_8,
    estados.criar_token_fim_de_arquivo_nao_esperado: processar_estado_9,
    estados.criar_token_invalido: processar_estado_10,
    estados.criar_token_fim_de_arquivo: processar_estado_11
}

```

</div>


---

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=exemplo_formas_funcionais.ipynb" width="100%" height="100%"></iframe>


---

<!-- _class: lead -->
# Programação Funcional


---

## Programação Funcional

<div class="normal">

- [A programação funcional] quebra um problema em um conjunto — uma composição — de funções que, idealmente, apenas recebem entradas e produzem saídas sem ter quaisquer tipos de estados internos — variáveis como endereços de memória — que afetem as saídas produzidas para uma dada entrada, ou seja, sem efeitos colaterais.

- Tem por objetivo imitar uma função matemática e até as notações são parecidas, como a seguir:
\\[
\begin{align}
    P & \equiv f (x_{1}, x_{2}, \ldots, x_{n}) \\\\
      & \equiv f_{1} \circ f_{2} \circ \ldots \circ f_{n} (x_{1}, x_{2}, \ldots, x_{n}) \\\\
\end{align}
\\]

- Baseada no modelo computacional *Lambda Calculus* (Church, 1941)

</div>


---

## Paradigma Funcional vs Paradigma Imperativo

<div class="regular">

- Exemplo de avaliação de \\((x + y) / (a - b)\\)

<div class="grid-33-66">
<div class="grid-element">
    <figure>
        <img src="https://i.imgur.com/cdI13Z4.png">
        <figcaption>Alan Turing</figcaption>
    </figure>
</div>
<div class="grid-element">

**Programação Imperativa**
- Avalia \\((x + y)\\) e armazena resultado na memória
- Avalia \\((a - b)\\) e armazena resultado na memória
- Carrega ambos valores da memória e faz a divisão

</div>
</div>

<div class="grid-33-66">
<div class="grid-element">
    <figure>
        <img src="https://i.imgur.com/aZgUYTB.png">
        <figcaption>Alonzo Church</figcaption>
    </figure>
</div>
<div class="grid-element">

**Programação Funcional**
- Não usa variáveis como endereços de memória
- Usa recursão em vez de iterações
- Não possui efeitos colaterais — dados as mesmas entradas (parâmetros) sempre serão produzidas as mesmas saídas — também conhecido como **transparência referencial**

</div>
</div>


</div>


---

<iframe src="https://diegoascanio.github.io/jupyterlite/lab?path=algoritmo_euclides_mdc.ipynb" width="100%" height="100%"></iframe>

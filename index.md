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


---

## Paradigma Funcional — Exemplos de Linguagens Funcionais

- [Haskell](https://www.haskell.org/)
- [Lisp](https://pt.wikipedia.org/wiki/Lisp) (multiparadigma)
- [ML](https://pt.wikipedia.org/wiki/ML_(linguagem_de_programa%C3%A7%C3%A3o))
- [Python](https://www.python.org/) (multiparadigma)
- [C++](https://pt.wikipedia.org/wiki/C%2B%2B) (multiparadigma)


---

<!-- _class: lead -->
# Programação Funcional em Python


---

## Programação Funcional em Python

<div class="regular">

- Por ser multiparadigma, Python não é uma linguagem puramente funcional, pois, armazena na memória os valores de variáveis locais, permite fazer alterações dos valores destas variáveis e não proíbe operações de entrada e saída, mas, a implementação de uma função em Python não vai fazer (se não for explicitamente instruída) alterações em variáveis globais nem tampouco ter outros tipos de efeitos colaterais.

- Porém, os recursos que Python oferece permitem a implementação de funções puras, ou seja, funções que não alteram o estado do programa e não têm efeitos colaterais.

- Como vimos, na nossa disciplina não aprenderemos Haskell devido ao nosso tempo exíguo. Python é suficiente para o nosso propósito por ser uma linguagem de fácil aprendizado, onde muitos estamos familiarizados, bem como, por possuir os principais recursos fundamentais que Haskell possui — de acordo com o material do prof. Dr. Andrei Rimsa Álvares — que são:

    - *Pattern Matching* (casamento de padrões)
    - Funções de Ordem Superior
    - *Lazy Evaluation* (avaliação preguiçosa)

</div>


---

## Programação Funcional em Python — Casamento de Padrões

<div class="small">

- Em linguagens exclusivamente funcionais, como Haskell, Scala e Erlang, é comum o uso de casamento de padrões (pattern matching) para definir funções.
- Nestas linguagens, o casamento de padrões é uma forma de definir funções recursivas, com várias equações, cada uma com um padrão no seu lado esquerdo, de forma concisa e elegante, como neste exemplo em Haskell:

```haskell
fib :: Int -> Int
fib 0 = 0 -- equação aplicada ao caso 0
fib 1 = 1 -- equação aplicada ao caso 1
fib n = fib (n-1) + fib (n-2) -- equação aplicada aos demais casos
```

- Em Python, desde a versão 3.10 é possível realizar o casamento de padrões usando a palavra reservada `match` como abaixo:
```python
def fib(n):
    match n:
        case 0:
            return 0
        case 1:
            return 1
        case _: # caso geral, pois, _ é o default de match case em python
            return fib(n-1) + fib(n-2)
```

Infelizmente não fica tão elegante quanto Haskell, mas, é um recurso que amplia o leque de ferramentas funcionais da linguagem.
</div>


---

## Programação Funcional em Python — Casamento de Padrões

<div class="small">

- Outro exemplo de casamento de padrões, em Haskell e em Python

```haskell
soma :: Int > Int
soma n
    | n <= 0 = 0
    | n > 0 = n + soma (n-1)
```

- Em Python, você deve submeter os padrões das comparações matemáticas que deseja fazer (no match) e só depois casá-las com os valores lógicos de retorno de tais comparações:
```python
def soma(n):
    match [n <= 0, n > 0]: # aqui submeti os dois padrões de comparacao que desejo verificar
        case [True, False]: # aqui verifico, se n <= 0 e ¬(n > 0) então, retorno 0
            return 0
        case [False, True]: # aqui verifico, se ¬(n <= 0) e n > 0 então, retorno n + soma(n-1)
            return n + soma(n-1)
```

Infelizmente não fica tão elegante quanto Haskell, mas, é um recurso que amplia o leque de ferramentas funcionais da linguagem.
</div>


---

## Programação Funcional em Python — Casamento de Padrões, Opção Padrão

<div class="regular">

- Em Haskell a opção padrão é caracterizada pela palavra reservada `otherwise`:

```haskell
fun :: Int -> Int
fun n
    | n < 10 = 0
    | n > 10 = 2
    | otherwise = 1
```

- Em Python, no match case a opção padrão é o underscore `_`:

```python
def fun(n):
    match n:
        case n < 10:
            return 0
        case n > 10:
            return 2
        case _: # opcao padrao
            return 1
```

</div>


---

## Programação Funcional em Python — Composição de Funções

- Cálculo das raízes de uma equação do segundo grau por composição de funções:

\\[
    x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\\]

- Implementação em Python:

```python
menos_b_sobre_2a = lambda a, b: -b / (2 * a)
raiz_delta_sobre_2_a = lambda a, b, c: ((b ** 2 - 4 * a * c) ** 0.5) / (2 * a)
raizes = lambda a, b, c: menos_b_sobre_2a(a, b) + raiz_delta_sobre_2_a(a, b, c),
                         menos_b_sobre_2a(a, b) - raiz_delta_sobre_2_a(a, b, c)
```


---

## Programação Funcional em Python
### Iteradores

<div class="small">

- Fundamentais para escrever programas funcionais em Python;
- Um iterador é um objeto que representa um fluxo de dados e que retorna um elemento de dado por vez, a cada vez;
- Todo iterador em Python deve implementar o método `__next__`, que retorna o próximo elemento do fluxo de dados;
    - Este método não possui argumentos e sempre retorna o próximo elemento no fluxo de dados (ou lança uma exceção `StopIteration` se não houver mais elementos);

```python
iterador = iter([1, 2, 3])
print(iterador.__next__()) # 1
print(iterador.__next__()) # 2
print(iterador.__next__()) # 3
print(iterador.__next__()) # StopIteration
```

- Iteradores não precisam ser finitos, de fato, é perfeitamente razoável escrever um iterador que seja capaz de produzir um fluxo infinito de dados.
- Listas, Tuplas, Strings e Dicionários são iteráveis, mas não são iteradores. Porém, todos eles possuem um método `__iter__` que retorna um iterador que produz um fluxo de dados.
- O iterador por si só é como se fosse uma lista encadeada, onde sabemos apenas que existe um ponteiro para o próximo elemento (next).
- Podemos materializar um iterador em uma lista usando as funções construtoras `list()` ou `tuple()`.

</div>


---

## Programação Funcional — Iteradores

<div class="regular">

- Porquê iteradores são fundamentais para a programação funcional?

    1. **Promovem tratamento eficaz de sequências de dados**: programação funcional frequentemente lida com transformação de dados em sequências (listas, tuplas, etc) e iteradores são a forma mais eficiente de lidar com isso, permitindo percorrer, filtrar, mapear e reduzir dados de maneira expressiva e concisa.
    2. **Lazy Evaluation (Avaliação Preguiçosa)**: as execuções de funções só são realizadas quando estritamente necessário, ou seja, quando um dado estiver disponível. Iteradores respeitam este princípio, pois, seus elementos são obtidos sob demanda (**__next__**) um de cada vez. Isto economiza memória e tempo de processamento, sendo muito útil para lidar com grandes volumes de dados ou fluxos infinitos.
    3. **Imutabilidade e sem Estado**: Iteradores não armazenam estados (exceto pela sua posição atual) e são imutáveis — não alteram a esturuta dos dados ao serem percorridos. Tudo isto fortalece os princípios de **transparência referencial**.
    4. **Composição de Funções e Encadeamento**: Iteradores podem ser facilmente combindos com funções de ordem superior (como **map**, **filter** e **reduce**) permitindo a composição e o encadeamento de operações de maneira clara e lógica.

</div>


---

## Iteradores - Geradores (generators)

<div class="footnotesize">

Geradores em Python são uma maneira eficiente de criar iteradores que permitem a iteração sobre sequências de dados sem a necessidade de carregar toda a sequência na memória, o que é benéfico para manipular grandes conjuntos de dados ou fluxos contínuos. Eles são implementados como funções que usam a palavra-chave **yield** para retornar elementos um de cada vez. Quando um gerador é invocado, ele retorna um objeto gerador que pausa a execução da função após cada **yield** e retoma de onde parou na próxima iteração, mantendo o estado interno e proporcionando uma maneira de processar sequências de dados de forma eficaz e com economia de memória.

Aqui temos um exemplo simples de um gerador:

<div class="tiny">

```python
def contador(maximo):
    n = 0
    while n < maximo:
        yield n
        n += 1

# Usando o gerador
for i in contador(3000):
    print(i)
```

<div class="regular" style="text-align: center;">

**Características dos geradores que são benéficas para a programação funcional:**

</div>

</div>

</div>
<div class="footnotesize grid-50-50">

<div class="grid-element">

1. **Lazy evaluation:** os elementos são gerados sob demanda, o que garante que a execução de um trecho de código só será realizada até que seu resultado seja estritamente necessário.
2. **Eficiência de Memória:** Ao evitar a criação de uma sequência completa de elementos, os geradores permitem que grandes conjuntos (quiçá infinitos) de dados sejam processados de forma eficiente, sem sobrecarregar a memória.

</div>
<div class="grid-element">

3. **Composição:** Os geradores podem ser combinados para criar novos geradores, permitindo a criação de sequências complexas de dados de forma eficiente e com economia de memória.
4. **Melhor Fluxo de Controle:** Os geradores permitem que o fluxo de controle seja alterado de forma eficiente, permitindo que o código seja escrito de forma mais clara e concisa.

</div>


</div>


---

## Compreensão de Listas (List Comprehension)

<div class="small">

- Compreensão de listas é uma forma concisa e eficiente de criar listas.
- Um conceito tomado emprestado da linguagem de programação funcional Haskell, permite:
    1. Executar uma operação (exemplo: inversão) para cada item oriundo de um iterador (por exemplo, uma lista);
    2. Criar um subconjunto de elementos que atendam a um determinado critério (por exemplo, números pares) também oriundos de um iterador.
    3. Criar listas de forma concisa e elegante.

Exemplos:

1. Criar uma lista dos quadrados dos números de 0 a 9:

```python
quadrados = [x**2 for x in range(10)]
```

2. Filtrar os números ímpares oriundos de um iterador:
```python
impares = [x for x in range(10) if x % 2 != 0]
```

3. Transformar uma lista de strings em maiúsculas:
```python
strings = ['abc', 'def', 'ghi']
maiusculas = [s.upper() for s in strings]
```


</div>


---

## Aplicando funções em iteradores e retornando iteradores
### Funções Map e Filter

<div class="footnotesize">

**Map**

- A função map aplica uma função a cada elemento de um iterador e retorna um iterador com os resultados aplicados.

Exemplo:

```python
def inverte_caracteres(palavra: str):
    return palavra[::-1]

lista_palavras = ['ovo', 'bola', 'casa', 'moto', 'mundo']
palavras_invertidas = map(inverte_caracteres, lista_palavras)
print(palavras_invertidas) # <map object at 0x7f9b1c0b6a90> (pois o map é um iterador)
print(list(palavras_invertidas)) # ['ovo', 'alob', 'asac', 'otom', 'odnum'], agora sim, pois a lista desenvolve o iterador
```

**Filter**

- A função filter retorna um iterador que contenha todos os elementos (de um iterador já existente) que atendam determinados critérios, por exemplo: palavras com mais de 3 caracteres.

Exemplo:
```python
def maior_que_3_caracteres(palavra: str):
    return len(palavra) > 3
palavras_invertidas_maior_que_3_caracteres = filter(maior_que_3_caracteres, palavras_invertidas) # ['alob', 'asac', 'otom', 'odnum']
print(list(palavras_invertidas_maior_que_3_caracteres)) # ['alob', 'asac', 'otom', 'odnum']
```

</div>


---

## Operações Acumulativas Sobre Iteradores (reduce)

<div class="small">

Quando queremos realizar operações acumulativas sobre elementos de um iterador, queremos aplicar uma função ao primeiro elemento, acumular seu resultado, aplicar a função ao segundo elemento e acumular seu resultado, e assim por diante. Esta operação acumulativa é chamada de `reduce` (redução) e fica fácil entender o seu nome ao verificar que todos os elementos do iterador são **reduzidos** a um único valor.

Python não oferece uma função nativa (como `map` ou `filter`) para realizar esta redução, porém, oferece um módulo de ferramentas para funções de ordem superior chamado `functools` que contém a função `reduce`. Para utilizá-la, precisamos importar o módulo `functools` e, em seguida, chamar a função `reduce` passando como argumentos uma função e um iterador.

Verifiquemos o exemplo do produtório sobre um iterador:

```python
from functools import reduce

def produto(a, b):
    return a * b

iteravel = range(1, 10)
resultado = reduce(produto, iteravel)
print(resultado) # 362880
```

</div>


---

## Programação Funcional em Python — Funções Lambda (anônimas)

<div class="small">

Em muitos casos precisamos de funções pequenas (1 ou 2 linhas) que são usadas apenas uma vez, como para realizar um filtro ou uma conversão de unidade por exemplo. Nesses casos, podemos usar funções lambda (anônimas).

```python
# lista de temperaturas em graus Celsius
celsius = [39.2, 36.5, 37.3, 37.8]
fahrenheit = map(lambda x: (float(9)/5)*x + 32, celsius)
print(list(fahrenheit))
```

Podemos atribuir as funções lambda a variáveis, como fizemos no cálculo de raízes de uma equação do segundo grau e, a partir destas variáveis, é possível chamar tais funções.

Porém, por, ser difícil expressar todos os casos de retorno que uma função típica pode apresentar, bem como, por não lidar adequadamente com exceções, na [documentação oficial de python](https://docs.python.org/3/howto/functional.html#small-functions-and-the-lambda-expression) é recomendado que se use funções nomeadas ao invés de funções lambda.

</div>


---

## Simplicidade do Paradigma Funcional

<div class="small">

**Implementação Puramente Funcional em Python do Algoritmo Quick Sort:**

```python
def quicksort(array):
    if len(array) <= 1:
        return array
    else:
        # retorna compreensão de elementos menores que o pivo a esquerda
        # mais o pivo mais a compreensão de elementos maiores que o pivo
        # a direita, onde o pivô é o primeiro elemento do array
        return quicksort([x for x in array[1:] if x < array[0]]) + [array[0]] + quicksort([x for x in array[1:] if x >= array[0]])

array = [5, 6, 7, 8, 1, 2, 12, 14]
print(quicksort(array)) # [1, 2, 5, 6, 7, 8, 12, 14]
```

**Em uma linha de codigo:**
```python
quicksort = lambda array: array if len(array) <= 1 else quicksort([x for x in array[1:] if x < array[0]]) + [array[0]] + quicksort([x for x in array[1:] if x >= array[0]])
```

</div>


---

## Resumo Comparativo Entre o Paradigma Imperativo e o Paradigma Funcional

- Linguagens imperativas são mais eficientes
    - Porque são mais próximas da máquina de von Neumann (o modelo padrão para as atuais arquiteturas de computadores)

- Linguagens funcionais possuem construções com um nível de abstração maior
    - Úteis para prototipação

- Linguagens funcionais viabilizam provas formais das propriedades de um programa


---

## Referências Bibliográficas

- [Slides do professor Andrei Rimsa Álvares](http://rimsa.com.br/documents/lectures/decom009/lessons/Aula10.pdf)
- [Tutorial da programação funcional em Python](https://docs.python.org/3/howto/functional.html#small-functions-and-the-lambda-expression)


---

## Trabalho e Lista de Exercício

Os enunciados do trabalho e da lista de exercícios serão disponibilizados neste slide até o final da semana.

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

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

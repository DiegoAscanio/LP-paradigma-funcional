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

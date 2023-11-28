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

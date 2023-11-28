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

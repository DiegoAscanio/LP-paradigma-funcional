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

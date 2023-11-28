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

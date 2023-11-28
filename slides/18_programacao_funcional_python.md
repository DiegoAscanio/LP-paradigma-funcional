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

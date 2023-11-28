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

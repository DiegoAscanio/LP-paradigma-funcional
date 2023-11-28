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

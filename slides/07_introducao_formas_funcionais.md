## Introdução
### Exemplo de Quasi-Formas Funcionais que Retornam Funções

<div class="small">

```python
# Exemplo de Quasi-Forma Funcional que retorna funções em python
# Aqui coloquei quasi-forma funcional porque o acesso a valores
# em dicionários em python não ocorre através de funções, mas,
# sim, por meio de hash tables. Porém, o comportamento que
# esperamos — que a partir de determinado parâmetro, nesse caso
# uma chave que representa um dos estados possíveis do AFD —
# seja retornada uma função responsável por processar o estado
# da chave, é o mesmo que ocorre com as formas funcionais.

# Aqui encontra-se descrito o AFD do analisador léxico da
# linguagem tiny
AFD = {
    estados.inicial: processar_estado_1,
    estados.ler_comentarios: processar_estado_2,
    estados.ler_atribuicao_comparacao_ou_igualdade: processar_estado_3,
    estados.ler_nao_igual: processar_estado_4,
    estados.ler_variavel: processar_estado_5,
    estados.ler_digito: processar_estado_6,
    estados.criar_token_reservado_ou_variavel: processar_estado_7,
    estados.criar_token_numerico: processar_estado_8,
    estados.criar_token_fim_de_arquivo_nao_esperado: processar_estado_9,
    estados.criar_token_invalido: processar_estado_10,
    estados.criar_token_fim_de_arquivo: processar_estado_11
}

```

</div>

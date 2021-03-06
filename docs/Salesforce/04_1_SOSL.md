# :back: [README](../../../README.md#programming-languages)

<h1 align="center">
    SOSL - Salesforce Object Search Language
</h1>

<br>

# Introdução
O acesso aos dados dentro do Salesforce é feita através do SOSL, é considerado um **Search Engine** dentro da plataforma Salesforce.

> O SOSL é bastante útil quando sabemos o valor que estamos procurando mas não sabemos em qual campo está.

<br>

Abaixo a sintáxe de um SOSL:

```sql
FIND {SearchQuery} 
[ IN SearchGroup ]
[ RETURNING FieldSpec [[ toLabel(fields)] [convertCurrency(Amount)] [FORMAT()]] ]
[ WITH DivisionFilter ]
[ WITH DATA CATEGORY DataCategorySpec ]
[ WITH SNIPPET[(target_length=n)] ]
[ WITH NETWORK NetworkIdSpec ]
[ WITH PricebookId ]
[ WITH METADATA ]
[ LIMIT n ]

[ UPDATE [TRACKING], [VIEWSTAT] ]
```

<br>
<br>

# Boas práticas

> Nunca devemos colocar uma chamada SOSL dentro de um loop, seja ele qual for. Ou seja, nunca coloque uma chamada SOSL dentro de um `for` por exemplo.

<br>
<br>

# SOSL Limits

| Description | Synchronous limit | Asynchonous limit |
|:-|:-|:-|
| Total number of SOSL queries ussued (Total de chamadas SOSL que podemos fazer por vez) | 20 | 20 |
| Total number of records retrieved by a single SOSL query (Total de registros que podem ser retornados em uma SOSL) | 2000 | 2000 |

<br>

> Sincrono são os métodos que nós sabemos quando vamos chamar, ou seja quando chamamos uma classe efetivamente e quando acaba ela espera que nós a chamemos novamente pra que ela possa rodar de novo.

> Assincrono é quando não sabemos quando um método será chamado, por exemplo no caso de uma Trigger de Update onde não sabemos quando o registro será atualizado e assim chamar o método.

> O salesforce funciona por chamada (ciclo transacional) que nada mais é do que o tempo de CPU que nosso programa tem para executar dentro do Salesforce.

> Os limite insdependem de liceça. Para todas vale igual.

<br>

Exemplos:












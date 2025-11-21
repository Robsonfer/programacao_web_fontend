# Seção 5 - Flexbox

## O que é o flexbox?

Por muito tempo, as únicas ferramentas disponíveis para criar leiautes em CSS e posicionar elementos com boa compatibilidade entre browsers eram float e position. Porém, essas ferramentas possuem algumas limitações muito frustrantes, especialmente no que diz respeito à responsividade. Algumas tarefas que consideramos básicas em um leiaute, como centralização vertical de um elemento-filho com relação a um elemento-pai ou fazer com que elementos-filhos ocupem a mesma quantidade de espaço, ou colunas terem o mesmo tamanho independente da quantidade de conteúdo interno, eram impossíveis ou muito difíceis de serem manejadas com floats ou position, ao menos de forma prática e flexível.

A ferramenta Flexbox (de Flexible Box) foi criada para tornar essas tarefas mais simples e funcionais: os filhos de um elemento com Flexbox podem se posicionar em qualquer direção e pode ter dimensões flexíveis para se adaptar.

## Elemento pai

Quando utilizamos o Flexbox, é muito importante saber quais propriedades são declaradas no elemento-pai (por exemplo, uma div que irá conter os elementos a serem alinhados) e quais serão declaradas nos elementos-filhos. Abaixo, seguem propriedades que devem ser declaradas utilizando o elemento-pai como seletor (para alinhar elementos-filhos):

**display:**

Esta propriedade define um flex container; inline ou block dependendo dos valores passados. Coloca todos os elementos-filhos diretos num contexto Flex.

```css
.container {
    display: flex; /* or inline-flex*/
}
```

## display: flex;

Devemos usar a propriedade display flex sempre no container pai, pois desta forma indicamos que tudo o que está dentro daquele container é flex. Somente então poderemos utilizar as propriedades do flexbox para os elementos filhos deste container.

**OBS IMPORTANTE:** O uso do display flex indica os elementos filhos daquele container, se houverem elementos dentro de um dos elementos filhos deste container, vale lembrar que o display flex não vai funcionar para o este outro elemento, pois os elementos dos containers filhos não herdam o display flex do container pai. Resumindo: a propriedade display flex só funciona para um grau, se quiser atingir mais um grau para dentro, deve-se repetir a propriedade display flex novamente.

``` css
.container {
    width: 300px;
    display: flex;
}
```

O display flex adiciona em seu container pai a propriedade de dividir por igual as propriedades como width e height igualmente por padrão, exceto se ele for maior do que a soma do tamanho dos elementos dentro dele.

Se a soma dos elementos forem maior do que o container, ele vai dividir em tamnahos iguais, exceto se usarmos a propriedade flex-wrap. Por padrão essa propriedade já vem como nowrap, mas podemos informar wrap e assim teremos os elementos divididos em duas linhas obedecendo assim o seu tamanho padrão já determinado.

```css
.container {
    width: 300px;
    display: flex;
    flex-wrap: wrap;
}
```

## justify-content



## align-itens



## align-content

__base para consulta:__ https://www.alura.com.br/artigos/css-guia-do-flexbox?utm_term=&utm_campaign=&utm_source=google&utm_medium=cpc&campaign_id=23137788902__&utm_id=23137788902__&hsa_acc=7964138385&hsa_cam=&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=google&hsa_ver=3&gad_source=1&gad_campaignid=23132128725&gbraid=0AAAAADpqZIBRx_5bSNEriep7lBDzYBpxz&gclid=CjwKCAiAlfvIBhA6EiwAcErpyfGYX6yTrYKFpxCrjEmUeTUww9DVPeWOJJZ-dYRO4AIzuLPMnNKN0BoCa0IQAvD_BwE
# Seção 5 - Flexbox

## O que é o flexbox?

A ferramenta Flexbox (de Flexible Box) foi criada para tornar a tarefa de criar layouts mais simples e funcionais. Funciona fácil para tarefas como centralizar elementos, ajustar à esquerda ou à direita, em cima ou embaixo, acima ou abaixo, dentro ou fora. Por isso o nome flexbox, ou seja, caixa flexível. Os filhos de um elemento com Flexbox podem se posicionar em qualquer direção e pode ter dimensões flexíveis para se adaptar.

## Estruturas do flexbox

Basicamente o flexbox se divide em duas partes, sendo a primeira o Elemento pai e a segunda o Elemento filho. Dentro de um elemento pai, podemos ter quantos elementos filhos quisermos e dentro de um elemento filho podem haver outros elementos, o que torna este elemento filho também um elemnto pai.

```html
<div class="elemento1">
    <div class="elemento2">
        <div class="elemento3">
            <div class="elemento4">
                <p class="elemento5">Lorem Ipsum</div>
            </div>
        </div>
    </div>
</div>
```

Conforme mostrado no exemplo acima, o elemento1 é o pai do elemento2 que por sua vez é pai do elemento3 que por sua vez é pai do elemento4 que por sua vez é pai do elemento5.

O importante a compreender dentro desta estrutura é que o flexbox trabalha o relacionamento de somente uma etapa por vez, ou seja, cada filho só obedece ao seu pai, o elemento "neto" por assim dizer, não obedece ao seu avô, somente ao seu pai. Portanto, cada elemento só respeita as propriedades determinadas pelo elemento diretamente acima dele.

**Mas nós podemos ter dois ou mais elementos filhos do mesmo pai?**

Sim, é completamente possível um elemento ter mais de um filho por vez, desta forma o exemplo ficaria assim:

```html
<div class="elemento1">
    <div class="elemento-a">
        <p>Lorem Ipsum</div>
    </div>
    <div class="elemento-b">
        <p>Lorem Ipsum</div>
    </div>
    <div class="elemento-c">
        <p>Lorem Ipsum</div>
    </div>
</div>

<div class="elemento2">
    <div class="elemento-d">
        <p>Lorem Ipsum</div>
    </div>
    <div class="elemento-e">
        <p>Lorem Ipsum</div>
    </div>
    <div class="elemento-f">
        <p>Lorem Ipsum</div>
    </div>
</div>
```

Note que no exemplo acima o elemento1 que é o elemento pai tem abaixo de si como elementos filhos três elementos: elemento-a, elemento-b e elemento-c e cada um deles tem seus elementos filhos que são parágrafos. O mesmo foi feito para o elemento2 que é o pai do elemento-d, elemento-e e elemento-f.

## Elemento pai

Antes definir então o que é o elemento pai, precisamos entender que todo elemento pode ser um container, pois pode conter muitos elementos dentro de si.

Portanto elemento pai nada mais é do que um container que abriga dentro de si mais elementos independente do tipo.

## Elemento filho

Antes de definir o que é o elemento filho, precisamos entender que todo elemento filho é um item dentro de um elemento pai, ou seja, um container.

Resumindo: Um elemento filho dentro de um elemento pai = Um item dentro de um container. Seguir o mesmo raciocíno para o elemento filho que também tem filhos.

Elemento filho é todo aquele elemento que tem outro elemento acima de si que é responsável por guardá-lo dentro de si.

## O que são propriedades em CSS?

Ao determinar elementos pai e elementos filhos ou containers e itens, estamos criando a hierarquia dos containers, entretanto não passa disso. O que realmente determina como os elementos e itens são estrutuados dentro de cada container são as propriedades.

São as propriedades que manipulam os espaços e características que temos da forma que precisamos. Tamanho, largura, altura, posicionamento, tudo é determinado por aí.

## A relação entre a estrutura de container e as propriedades

Quando utilizamos o Flexbox, é muito importante saber quais propriedades são declaradas no elemento-pai e quais serão declaradas nos elementos-filhos.

Abaixo, seguem propriedades que devem ser declaradas utilizando o elemento-pai como seletor (para alinhar elementos-filhos):

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
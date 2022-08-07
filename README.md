
# CSS FLEXBOX

Criei este repositório para guardar minhas anotações e arquivos de práticas que produzi durante o curso **Posicionando elementos com Flexbox em CSS** Ministrado por Karen Santos e disponível na plataforma da [Digital Inovation One](https:
web.dio.me/ "DIO")

## Referências

https:
css-tricks.com/snippets/css/a-guide-to-flexbox/

https:
origamid.com/projetos/flexbox-guia-completo/

https:
desenvolvimentoparaweb.com/css/unidades-css-rem-vh-vw-vmin-vmax-ex-ch/

## Propriedades do Flex Container

## Propriedades dos Flex Items

### flex-basis

Indica o tamanho inicial do flex item antes da distribuição do espaço restante.

Quando definimos o flex-grow: 1; e possuímos auto no basis, o valor restante para ocupar o container é distribuído ao redor do conteúdo do flex-item.

```css
flex-basis: auto;
/* Esse é o padrão, ele faz com que a largura da base seja igual a do item. Se o item não tiver tamanho especificado, o tamanho será de acordo com o conteúdo. */
```

```css
flex-basis: unidade;
/* Pode ser em %, em, px e etc. */
```

```css
flex-basis: 0;
/* Se o grow for igual ou maior que 1, ele irá tentar manter todos os elementos com a mesma largura, independente do conteúdo (por isso 0 é o valor mais comum do flex-basis). Caso contrário o item terá a largura do seu conteúdo. */
```

### flex-shrink

É a propriedade que estabelece a capacidade de redução ou compressão do tamanho de um item.

```css
flex-shrink: 1;
/* Valor padrão, permite que os itens tenham os seus tamanhos (seja esse tamanho definido a partir de width ou flex-basis) reduzidos para caber no container. */
```

```css
flex-shrink: 0;
/* Não permite a diminuição dos itens, assim um item com flex-basis: 300px; nunca diminuirá menos do que 300px, mesmo que o conteúdo não ocupe todo esse espaço. */
```

```css
flex-shrink: número;
/* Um item com shrink: 3 diminuirá 3 vezes mais que um item com 1. */
```

### flex

É um *shorthand* para as propriedades flex-grow, flex-shrink e flex-basis. Comumente mais utilizado.
Fortemente recomendado para melhor compatibilidade entre os browsers.

```css
flex: 1;
/* Define flex-grow: 1; flex-shrink: 1; e flex-basis: 0; (em alguns browsers define como 0%, pois estes ignoram valores sem unidades, porém a função de 0 e 0% é a mesma.) */
```

```css
flex: 0 1 auto;
/* Esse é o padrão, se você não definir nenhum valor de flex ou para as outras propriedades separadas, o normal será flex-grow: 0, flex-shrink: 1 e flex-basis: auto. */
```

```css
flex: 2;
/* Define exatamente da mesma forma que o flex: 1; porém neste caso o flex-grow será de 2, o flex-shrink continuará 1 e o flex-basis 0.*/
```

```css
flex: 3 2 300px;
/* flex-grow: 3, flex-shrink: 2 e flex-basis: 300px; */
```

### order

Altera a ordem dos flex itens. Sempre do menor para o maior, assim order: 1, aparece na frente de order: 5.

```css
order: número;
/* Número para modificar a ordem padrão. Pode ser negativo. */
```

```css
order: 0;
/* 0 é o valor padrão e isso significa que a ordem dos itens será a ordem apresentada no HTML. Se você quiser colocar um item do meio da lista no início da mesma, sem modificar os demais, o ideal é utilizar um valor negativo para este item, já que todos os outros são 0. */
```

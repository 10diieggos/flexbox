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
```

Esse é o padrão, ele faz com que a largura da base seja igual a do item. Se o item não tiver tamanho especificado, o tamanho será de acordo com o conteúdo.

```css
flex-basis: unidade;
```

Pode ser em %, em, px e etc.

```css
flex-basis: 0;
```

Se o grow for igual ou maior que 1, ele irá tentar manter todos os elementos com a mesma largura, independente do conteúdo (por isso 0 é o valor mais comum do flex-basis). Caso contrário o item terá a largura do seu conteúdo.

### flex-shrink

É a propriedade que estabelece a capacidade de redução ou compressão do tamanho de um item.

```css
flex-shrink: 1;
```

 Valor padrão, permite que os itens tenham os seus tamanhos (seja esse tamanho definido a partir de width ou flex-basis) reduzidos para caber no container.
```css
flex-shrink: 0;
```

 Não permite a diminuição dos itens, assim um item com flex-basis: 300px; nunca diminuirá menos do que 300px, mesmo que o conteúdo não ocupe todo esse espaço.
```css
flex-shrink: número;
```

 Um item com shrink: 3 diminuirá 3 vezes mais que um item com 1.
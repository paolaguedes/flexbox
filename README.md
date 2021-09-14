## Conceitos do FlexBox

Se você reparar bem nos sites que você entra, verá que todas as informações dos layouts é dividida de alguma forma. Seja em colunas ou em linhas.

O legal do css é que você pode brincar de organizar os elementos da sua página da forma que quiser. E o flexbox é nosso grande aliado nisso pois com ele podemos juntar um bloco com outro deixando todos eles enfileirados, ou um do lado do outro, ou também um na esquerda e outro laaa na direita, enfim... muitas formas!!

E é por isso que eu decidi criar esse repositório, porque apesar de ser uma ferramenta muito boa, as vezes é difícil de entender o conceito, e eu espero poder te ajudar nisso (e claro, me ajudar a enraizar na minha mente também rs)

- Podemos usar o flexbox pelo eixo principal (horizontalmente) e no eixo transversal (vertical)

# Eixo principal
<div style="display: flex;">
<img width="300px" src="https://user-images.githubusercontent.com/53832972/133309926-61d67a13-ba44-43f3-9912-683d92be0c7e.png" alt="">
<img width="300px" src="https://user-images.githubusercontent.com/53832972/133310833-3ec048c2-8bdc-4568-ac26-745278d6f8fc.png" alt="">
</div>


É importante saber que o padrão é o row, que foi o mesmo que eu sei para deixar essas duas imagens uma do lado da outra, é só você olhar o código desse README :)


- Enquanto row seus elementos vão se mover "inlinemente", assim você pode por todos os elementos no centro, ou alinhados com uma margem entre eles, ou um de um lado e outro do outro kkkk e vou mostrar como fazer isso usando:

# Justify-content

Para poder exemplificar vou usar essas três div que atualmente estão grudadas uma do lado da outra.
```html
  ...
  <style>
    
    section {
      display: flex;
    }
    
    section div {
      background-color: rgb(0,0,0);
      width: 100px;
      height: 100px;
    }
    
<!-- usei para adicionar cor a div do meio -->
    section div:not(:first-child):not(:last-child) {
      background-color: rgb(23, 25, 122);       
    }

  </style>
...
  <section>
    <div></div>
      <div></div>
    <div></div>
  </section>

  ...

```

![divgit](https://user-images.githubusercontent.com/53832972/133316155-f63564ce-7bce-4ace-81bc-3160d2d550b7.png)

#

Para não ficar informações repetidas vou deixar apenas a section que é onde vou mostrar a aplicação do justify-content. No caso debaixo usei center para alinhar nossas três divs no meio do elemento pai que no caso é o body.

```html
  ...

  <style>
    
    section {
      display: flex;
      justify-content: center;
    }

  ...

```

Ficou assim :

![center](https://user-images.githubusercontent.com/53832972/133316836-c2b74185-4eef-4214-9f6a-9b93cb812f10.png)

Agora usando start e end:

```html
  ...
Exemplo com start:

  <style>
    
    section {
      display: flex;
      justify-content: start;
    }
</style>
  ...

Exemplo com end:

  <style>
    
    section {
      display: flex;
      justify-content: end;
    }
</style>
  ...

```

<div style="display: flex">
  <img src="https://user-images.githubusercontent.com/53832972/133317386-749e30d1-5b01-47c5-98c4-56b9483f75e6.png">
  <img src="https://user-images.githubusercontent.com/53832972/133317398-34e6e2c1-4a0b-46f8-90af-3fef9253e660.png">
</div>

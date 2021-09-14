## Conceitos do FlexBox

Se você reparar bem nos sites que você entra, verá que todas as informações dos layouts é dividida de alguma forma. Seja em colunas ou em linhas.

O legal do css é que você pode brincar de organizar os elementos da sua página da forma que quiser. E o flexbox é nosso grande aliado nisso pois com ele podemos juntar um bloco com outro deixando todos eles enfileirados, ou um do lado do outro, ou também um na esquerda e outro laaa na direita, enfim... muitas formas!!

E é por isso que eu decidi criar esse repositório, porque apesar de ser uma ferramenta muito boa, as vezes é difícil de entender o conceito, e eu espero poder te ajudar nisso (e claro, me ajudar a enraizar na minha mente também rs)

- Podemos usar o flexbox pelo eixo principal (horizontalmente) e no eixo transversal (vertical)
- Para definir isso usamos FLEX-DIRECTION, que possui 4 componentes:
     - row
     - row-reverse
     - column
     - column-reverse

# Eixo horizontal
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
    
//usei para adicionar cor na div do meio
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

Para não ficar informações repetidas vou deixar apenas a section que é onde vou mostrar a aplicação do justify-content. No caso debaixo usei center para alinhar nossas três divs no meio do elemento pai que no caso é a section.

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

#

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

Então ele alinhará os itens a esquerda ou a direita.

#

Agora com space-evenly, around e between:

```html
  ...
Exemplo com space-evenly:

  <style>
    
    section {
      display: flex;
      justify-content: space-evenly;
    }
</style>
  ...

Exemplo com space-between:

  <style>
    
    section {
      display: flex;
      justify-content: space-between;
    }
</style>
  ...

 ...

Exemplo com space-around:

  <style>
    
    section {
      display: flex;
      justify-content: space-around;
    }
</style>
  ...

```

<div style="display:flex; flex-direction: column;">
<p>Space-evenly divide o espaço do elemento igualmente ENTRE E FORA das divs</p>
<img src="https://user-images.githubusercontent.com/53832972/133322969-0ed799d2-69f4-4e74-80bd-06110b941c91.png">
  
<p>Space-between divide o espaço entre as divs para fazer o alinhamento</p>
<img src="https://user-images.githubusercontent.com/53832972/133322999-1c9ca35c-4dcc-4167-9532-fe29494d18ab.png">
  
<p>Space-around pega todo o espaço da linha e divide igualmente ENTRE os elementos</p>
<img src="https://user-images.githubusercontent.com/53832972/133323014-30f2aa8d-11db-41a9-a4bf-45fbff7c2e95.png">
</div>
  
  - Esses são os mais usados do justify-content agora vamos estudar sobre o :

## Eixo vertical

Para alinhar elementos usando como base o eixo vertical usamos outra propriedade do flexbox que é :

# Align-items

- Possui como valores:
    - center
    - flex-end
    - flex-start
    
E modifica nossos elementos verticalmente!

Recomendo fortemente que ao acompanhar esse 'tutorial' você vá fazendo, sério, observa o que acontece e também o que não acontece kkkkkkkkk vai te ajudar a saber o que usar em cada situação. A prática é o melhor professor!

E é por isso que vou deixar com vocês para modificar suas divs que estão em row com align-items, e partir para mostrar como funciona quando elas estão com flex-direction: column..

# Flex-direction: column
Aqui temos as mesmas divs, mas seu direcionamento é em coluna:

![column](https://user-images.githubusercontent.com/53832972/133328624-48894479-2668-43be-ab64-2f6807874fa6.png)

Queria que você testasse o justify-content nelas e ver o que acontece. Não funciona horizontalmente né? Doido isso mas quando você coloca seus elementos em coluna meio que as coisas invertem.

- se nada acontece veja se tem height suficiente para elas se mexerem... (sim, ja me estressei muito com isso)

Vamos ao código e sua visualização:


```html
  ...
Exemplo com align-items: flex-end e justify-content: space-between

<style>
    
    section {
      display: flex;
      flex-direction: column; 
      align-items: flex-end;
      justify-content: space-between;
      height: 100vh; --> Para poder aumentar a altura da minha section e ver o comportamento do justify-content
    }
</style>
```
<img src="https://user-images.githubusercontent.com/53832972/133336762-49a1c2a1-b93e-4ce2-861a-b7638237f727.png">


```html
  ...

Exemplo com align-items: flex-start e justify-content: space-around

<style>
    
    section {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: center;
          height: 70vh; --> Para poder aumentar a altura da minha section e ver o comportamento do justify-content
    }
</style>
```
<img src="https://user-images.githubusercontent.com/53832972/133336966-9acc70f4-ce65-44e7-8002-50b4ce6f5f76.png">

```html
 ...
Exemplo com align-items: center e justify-content: center

<style>
    
    section {
      display: flex;
      flex-direction: column; 
      align-items: center;
      justify-content: center;
      height: 100vh; --> Para poder aumentar a altura da minha section e ver o comportamento do justify-content
    }
</style>

```

<img src="https://user-images.githubusercontent.com/53832972/133337140-ecd44ff0-a524-45ed-a006-7fc84117b1c3.png">


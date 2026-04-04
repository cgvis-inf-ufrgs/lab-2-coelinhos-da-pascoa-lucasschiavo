# Relatório - Coelinhos da Páscoa

> [!CAUTION]
>
> - Lembre-se que você <ins>**não pode utilizar ferramentas de IA para
>   escrever este relatório**</ins>

## Dados do aluno

- **Cartão UFRGS**: 00578225
- **Nome**: Lucas Slongo Schiavo

## Passos que eu segui para resolver o problema especificado (em formato de _"prompt"_)

Primeiro, altere a parte de desenho do código para utilizar um loop que repete um número `BUNNY_COUNT` de vezes.
Cada iteração do loop deve desenhar um coelho e duas esferas. Para isso, calcula-se um ângulo `angle`, para cada iteração, que definirá a posição do coelho e dos ovos no círculo.
Agora, aplique no coelho:

- Uma matriz de translação de modo que cada coelho fique a um ângulo único do centro, formando um círculo de coelhos ao final. Isso pode ser feito usando o seno e cosseno do ângulo `angle`;
- Uma matriz de escalamento, que diminui o tamanho dos coelhos;
- Uma matriz de rotação no eixo y para que os coelhos apontem no sentido da tangente do círculo formado.
- Uma matriz de rotação no eixo z para um a cada quatro coelhos do loop.

Para as esferas, aplique:

- Em uma das esferas, uma translação positiva em y e, em outra uma negativa.
- Uma matriz de rotação no eixo X, baseada na váriavel `angle`.
- Uma matriz de escalamento, que deve ser menor nos eixos X e Z, e levemente maior no eixo Y, para as esferas ficarem em formato elipsóide.
- Uma matriz de translação para colocar as duas esferas centradas no seu respectivo coelho (mesma matriz de translação do coelho)

Depois, vamos adicionar variações com o tempo, do seguinte modo

- Crie uma váriavel `movement` que é o tempo (obtido através da função do `glfw`) multiplicado por um fator.
- Para cada matriz aplicada na primeira etapa, substituir todos lugares que utilizam `angle` por `angle + movement`, isso gera movimento em todas as operações.

## Principais dificuldades encontradas durante o desenvolvimento (formato livre)

A maior dificuldade foi aplicar os conhecimentos de matemática e trigonometria para replicar a disposição e movimentação dos objetos no vídeo do resultado esperado.
Outra dificuldade foi encontrar valores que se aproximassem de forma satisfatória do resultado esperado.

## Você acha que conseguiu resolver o problema de forma adequada?

Sim, o resultado ficou bastante semelhante com o do vídeo, com exceção de que alguns valores diferentes foram usados, o que causa uma pequena diferença em alguns detalhes.

## Se você quiser compartilhar mais alguma coisa, coloque aqui:

<mark>`<preencher>`</mark>

## Se você possui alguma sugestão para o professor sobre esta atividade, coloque aqui:

<mark>`<preencher>`</mark>

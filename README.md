# DirectxRidePrice
Minha resolução do kaggle proposto pelo projeto Cidamo
https://www.kaggle.com/competitions/4-desafio-cidamo-2022/overview

O nome dado é em função a uma brincadeira feita com o primeiro desafio do projeto, chamado "TaxiRidePrice"  \
e pelos outros desafios serem chamados somente como "nº desafio cidamo" resolvi chamar os outros desafios como "TemaRidePrice" 

O estudo é sobre a versão do DirectX suportada por uma GPU, com os valores variando de 8 a 12. <!-- Deixo bem claro os possíveis valores para a versão do DirectX Por que eu consegui errar a previsão por causa disso -->

As features a serem estudadas estavam entre valores de resolução adequada da GPU, taxa de pixeis e TMU. Que são apresentadas de forma bem crua.
Então o tratamento de dados foi bem trabalhado no notebook e espero ter feito um bom estudo para concluir as ações que eu fiz.

## Tratamento de Dados

Para tratar os dados do Dataset, utilizei o máximo que eu pude das informações das colunas, principalmente das que são numéricas por natureza.
Isso se da por que eu sinceramente estava mais animado para estudar esses dados no inicio do trabalho. Então primeiramente é notavel a diferneça no tratamento dos dados iniciais para os finais. \
Então passei boa parte do notebook simplesmente trabalhando com os dados que continham unidades de medidas nas células. O que por ser minha primeira vez fazendo isso. Obtive um pouco de trabalho. \
Mas antes disso, fiz um pequeno estudo sobre os valores nulos de cada coluna, e conclui-se que o fato do valor não existir em uma coluna é relevante para a predição do DirectX \
Então criei colunas binárias correspondendo às colunas mais importantes em relação a nulidade do valor. Estas features houveram uma ocorrencia significativa no DirectX. \
Também acredito que nas colunas de entradas (como HDMI por exemplo) seja melhor e mais facil para o modelo ler a existencia ou não de entradas. 
Verifiquei então em quais colunas fazia diferença o existir mais de uma entrada, e tratei estes casos. <!-- Ainda pretendo realizar estes testes -->

## Redes neurais

Como o tema do módulo era sobre redes neurais, não há muito aonde eu escapar para a montagem do modelo.  <!-- Btw é bom realizar testes com outros modelos mais simples --> 
Estarei usando o Keras como ensinado e proposto pelo projeto.

Primeiramente eu gostaria de testar um modelo pequeno e simples para ver a eficiencia do meu tratamento de dados. Consegui um score de 0.92 no kaggle (Ver markdown com os scores) \

~Atualmente me encontro aqui~ Agora o passo é entender melhor o funcionamento de redes neurais e principalmente a aplicação delas para aprimorar a acurácia do modelo. Considerando que com um modelo pouco planejado e com falta de estudo o score foi de .92 acredito conseguir montar um com pelo menos .96 de acurácia. Para isso pretendo estudar métodos para evitar overfitting, escolha de funções de ativação (Atualmente pretendo utilizar Elu e Tanh) e por fim estudar um pouco melhor implementações do treino do modelo.

~Futuramente~ Pelo meu interesse e ansiedade por redes neurais gostaria de implementar uma minha, simples e provavelmente ineficaz, e estudar como otimizar ao máximo as redes neurais que eu ja tenho. Possívelmente utilizar random forest para estudar importância de variaveis, e comparar com alguns outros modelos mais complexos com um tratamento de dados parecido.




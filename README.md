# PLN-Word2vec
Estudo de Caso - Previsão de Palavras com Base no Contexto e Visualização com PCA

![nuvem_palavras](https://user-images.githubusercontent.com/72530507/139607686-c3121831-dec8-4dff-aeca-51ed93cd5d82.png)


Teste do Modelo e Redução de Dimensionalidade com PCA

Para testar o modelo, tudo que precisamos é dos pesos, em nosso exemplo W1 e W2. Mas visualizar os dados é desafiador, pois a dimensionalidade é alta e quanto maior o número de palavras do vocabulário, mais complicado.

Uma alternativa, é reduzir a diemensionalidade dos dados. Convertemos todos os atributos em 2 componentes principais usando PCA (Principal Component Analysis) e com 2 componentes podemos visualizar os dados.

Cada componentes principal nada mais é do que a junção matemática da informação em outras variáveis. O PCA é um algoritmo de Machine Learning por si mesmo, da categoria de aprendizagem não supervisionada.

Vamos aplicar o PCA para visualizar os dados.

Definição dos pesos da rede neural.

W1 é uma matriz de pesos de dimensões embedding_dims x tamanho_vocab
W2 é uma matriz de pesos de dimensões tamanho_vocab x embedding_dims
Os pesos (ou coeficientes ou parâmetros) é aquilo que a rede aprende durante o treinamento. Como no início não sabemos qual o valor ideal de pesos (isso é o que queremos descobrir) iniciamos com valores randômicos usando torch.randn().

Ao final do aprendizado, o modelo em si nada mais é do que os valores ideais de W1 e W2.

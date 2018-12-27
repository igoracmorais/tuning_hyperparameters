# Tuning_hyperparameters

Uma das técnicas muito úteis para encontrar bons resultados em modelos de Machine Learning é a determinação dos parâmetros ótimos que minimizam um função perda. Há diferentes formas de se fazer isso, em especial o GridSearchCV e o RandomSearch, ambos disponíveis no pacote scikit-learn. Além desses, também podemos usar o metodo bayesiano para otimizar os hyperparâmetros de um modelo, um procedimento que é extremamente útil para reduzir o tempo de computação no processo de minimizar a função objetivo. 
Para quem conhece da técnica bayesiana o entendimento de como funciona esse método fica mais fácil. Aqui fazemos uso de observações passadas e resultados para escolher quais seriam os valores futuros, descartando aqueles que não produziram bons resultados. Isso reduz o tempo de avaliação de diferentes parâmetros que não irão performar bem e representa uma diferença com os tradicionais métodos utilizados para esse processo como o GridSearchCV e o RandomSearch. Esses dois métodos usam uma função, normalmente o próprio estimador, como um SVM, Random Forest dentre outros, para encontrar os hyperparâmetros ótimos, o que resulta em testar todas as possíveis combinações. De outra forma, o ajuste feito via método Bayesiano faz um update das probabilidades e acaba se concentrando nos hyperparâmetros que performaram melhor. O processo bayesiano pode ser entendido a partir de quatro passos: <br>
1. Determinar a função objetivo
2. Especificar o intervalo dos valores dos hyperparâmetros
3. Escolher o algoritmo de otimização
4. Avaliar os resultados

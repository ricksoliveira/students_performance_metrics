# 1 - Métricas utilizadas

##### Como visto anteriormente, dar uma olhada mais afundo nas métricas, o que elas significam, saber qual algoritmo conseguiu performar melhor e fazer as melhores previsões, assim como o oposto.

##### As métricas que vamos utilizar são:

- MSE - Erro quadrático médio
- RMSE - Raiz do erro quadrático médio
- R² - Coeficiente de determinação
- MAE - Erro médio absoluto

### 1.1 - MSE - Erro quadrático médio

##### Avalia o tamanho dos erros que o algoritmo está cometendo e os eleva ao quadrado, a fim de tornar os erros grandes ainda maiores.

##### Este modelo nos ajuda a ver se o modelo está cometendo muitos erros grandes.

### 1.2 - RMSE - Raiz do erro quadrático médio

##### Avalia o tamanho dos erros que o algoritmo está cometendo mas não os eleva ao quadrado.

##### Este modelo nos ajuda a ver se o modelo está cometendo erros como o MSE porém estes erros estarão na mesma unidade da medição.

### 1.3 - R² - Coeficiente de determinação (Regressão Linear)

##### Avalia o quão bem a Regressão Linear consegue explicar alguma coisa baseado em outras. Varia de 0 a 1, correspondendo à 0% e 100%

##### Um R² de 0 significa que o modelo de Regressão Linear não explica nada e essencialmente é como se estivesse adivinhando.

### 1.4 - MAE - Erro médio absoluto

##### O quão longe, em média, as previsões do modelo estão dos valores reais, ignorando se o valor é negativo ou positivo.

### 2 - Tabela de métricas

> | Matéria     | Modelo             | Features                                           | Variávael Alvo | MSE    | R²    | MAE   | RMSE  |
> | ----------- | ------------------ | -------------------------------------------------- | -------------- | ------ | ----- | ----- | ----- |
> | Matemática  | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 12.64	| 0.08  | 3.00  | 3.56  |
> | Português   | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 7.14	  | 0.17  | 2.07  | 2.67  |
> | Matemática  | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 12.26	| 0.14  | 2.95  | 3.50  |
> | Português   | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 7.43	  | 0.17  | 2.03  | 2.72  |
> | Matemática  | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 12.45	| 0.11  | 2.97  | 3.53  |
> | Português   | Regressao Linear   | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 7.28	  | 0.17  | 2.05  | 2.70  |
> | Matemática  | Regressao Linear   | ['G1', 'G2']                                       | G3             | 4.21	  | 0.79  | 1.26  | 2.05  |
> | Português   | Regressao Linear   | ['G1', 'G2']                                       | G3             | 1.37	  | 0.86  | 0.73  | 1.17  |
> | Matemática  | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 17.56	| -     | 3.41  | 4.19  |
> | Português   | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 8.85	  | -     | 2.41  | 2.98  |
> | Matemática  | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 22.97	| -     | 3.74  | 4.79  |
> | Português   | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 10.27	| -     | 2.39  | 3.21  |
> | Matemática  | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 19.47	| -     | 3.53  | 4.41  |
> | Português   | Arvore de Decisao  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 9.00	  | -     | 2.35  | 3.00  |
> | Matemática  | Arvore de Decisao  | ['G1', 'G2']                                       | G3             | 4.76  	| -     | 1.39  | 2.18  |
> | Português   | Arvore de Decisao  | ['G1', 'G2']                                       | G3             | 2.10	  | -     | 0.82  | 1.45  |
> | Matemática  | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 13.92	| -     | 3.13  | 3.72  |
> | Português   | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 7.71	  | -     | 2.07  | 2.70  |
> | Matemática  | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 13.92	| -     | 3.12  | 3.79  |
> | Português   | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 7.71	  | -     | 2.09  | 2.75  |
> | Matemática  | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 15.15	| -     | 1.34  | 2.17  |
> | Português   | KNN                | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | ['G1', 'G2']   | 7.60	  | -     | 0.78  | 1.37  |
> | Matemática  | KNN                | ['G1', 'G2']                                       | G3             | 5.04	  | -     | 3.09  | 3.73  |
> | Português   | KNN                | ['G1', 'G2']                                       | G3             | 1.79	  | -     | 2.20  | 2.78  |
> | Matemática  | Gradient Boosting  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 13.80	| -     | 3.09  | 3.73  |
> | Português   | Gradient Boosting  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 7.31	  | -     | 2.20  | 2.78  |
> | Matemática  | Gradient Boosting  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 14.34	| -     | 3.18  | 3.89  |
> | Português   | Gradient Boosting  | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 7.59	  | -     | 2.11  | 2.76  |
> | Matemática  | Gradient Boosting  | ['G1', 'G2']                                       | G3             | 4.76	  | -     | 1.50  | 2.24  |
> | Português   | Gradient Boosting  | ['G1', 'G2']                                       | G3             | 2.10	  | -     | 0.84  | 1.34  |
> | Matemática  | Light GBM          | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 12.12	| -     | 2.93  | 3.48  |
> | Português   | Light GBM          | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G1             | 7.32	  | -     | 2.07  | 2.71  |
> | Matemática  | Light GBM          | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 13.25	| -     | 2.99  | 3.64  |
> | Português   | Light GBM          | ['failures', 'studytime', 'Medu', 'Fedu', 'sch...  | G2             | 7.55   | -     | 2.04  | 2.75  |
> | Matemática  | Light GBM          | ['G1', 'G2']                                       | G3             | 5.39   | -     | 1.46  | 2.32  |
> | Português   | Light GBM          | ['G1', 'G2']                                       | G3             | 1.90   | -     | 0.83  | 1.38  |

##### A tabela acima nos mostra o seguinte:

##### Para todos os modelos utilizados, quando utilizamos as variáveis: repetições / tempo de estudo / escola / educação mãe / educação pai / interesse em ensino superior / acesso à internet, para prever as notas G1 e G2. Vemos que o algoritmo comete muitos erros, e erros grandes.

##### O MSE varia entre 7 para Português e 15 (chegando até 19) para Matemática. Porém considerando que a variável alvo varia entre 0 e 20. Um erro de MSE de 7 é bastante considerável.

##### A Regressão Linear consegue prever aproximadamente 15 a 20% das notas dos alunos baseada nessas informações, e o acerto da previsão da nota final baseado nas outras notas é de aproximadamente 80%

##### Por outro lado, considerando valores absolutos do MAE, observamos que a média dos erros do modelo não está tão longe dos valores reais. Eem média os maiores erros foram entre 2 e 3,5. Considerando a escala da variável entre 0 e 20, esta métrica mostrou que os modelos, quando não erraram bastante, tiveram uma taxa de acerto relativamente boa.

# 3- Conclusões Finais

##### Com tudo o que vimos nos dados dos estudantes, podemos tirar algumas conclusões:

##### Quanto mais tempo o aluno passa estudando, maior é a nota. Essa correlação é quase o dobro em Português do que em Matemática.

##### Isso explica o aumento de notas baixas durante o ano, significando que esta matéria fique bastante difícil com relação ao tempo, de maneira que nem um aluno que passa muito tempo estudando consiga um bom desempenho.

##### Há um menor tempo de dedicação aos estudos em matemática, por causa da crescente complexidade na matéria ao longo do ano, isso pode fazer com que os alunos acabem se "desmotivando" para estudar.

##### Alunos da escola Gabriel Pereira tem uma nota em português maior do que os alunos da escola Mousinho da Silveira.

##### A estrutura familiar do aluno não se relaciona tanto com a quantidade de horas que o aluno estuda e suas notas.

##### Alunos da zona urbana tem uma média de notas superior à alunos que moram em área rual. Assim como os que estudam mais longe de casa tem uma nota menor dos que estudam mais perto de casa.

##### Alunos com suporte educacional extra tendem a concentrar suas notas entre 7.5 e 10, alunos sem suporte adquirem uma frequência maior de notas 0.

# 4 Propostas

##### Propomos, então, a implementação dos seguintes modelos de modo a mitigar os principais problemas apresentados acima:

### 1 - Aumentar interesse do aluno.

##### Aumentar o interesse do aluno em estudar matemática ao diminuir o foco em decorar fórmulas onde isso ocorre, ao invés, trazer problemas mais palpáveis do ambiente do aluno para a sala de aula, mostrando onde tais numeros, fórmulas e metodologias se aplicam ao cotidiano do contexto em que o aluno está inserido, fazendo-o perceber como a matemática se aplica ao seu próprio dia a dia.

##### Exemplo: como alunos em um contexto rural tem notas menores, podemos ensinar matemática num contexto rural e de campo, mostrando como a matemática se aplica em diferentes áreas e ciclos de plantio, como a matemática foi usada na construção de casas na época dos grandes latifúndios, conceitos de matemática e física que se aplicam à GPS, ferramenta muito usada no controle de máquinas agrícolas.

### 2 - Recompensar esforço.

##### Ao diminuir um pouco a quantidade e complexidade do conteúdo, ao decorar menos fórmulas e entender mais, o aluno se sente mais recompensado, e consequentemente mais motivado à estudar mais, quando vê que seu entendimento foi convertido em uma nota maior.

##### Exemplo: Compor parte da média final com várias lições de casa e trabalhos, pode estimular o aluno à se dedicar apenas um pouco mais todos os dias, aumentando o número de horas que passa estudando sem nem perceber que está estudando, e não apenas motivar o aluno à estudar somente em vésperas de provas.

### 3 - Estudo da escola Gabriel Pereira.

##### Realizar um estudo mais aprofundado e detalhado sobre as diferenças das didáticas e planos estudantis das duas escolas:

##### - Como são as aulas dos professores ? E suas formações ?
##### - O quão atualizado é o material didático ? Há diferença entre eles ?
##### - Há diferenças nos valores da escola ?
##### - Como estão estruturados os horários e intervalos ?
##### - Há diferença entre aplicabilidade de provas ?

##### Estes questionamentos devem ser feitos a fim de entender melhor a causa das notas da escola Gabriel Pereira serem melhores, e, partir destes pontos, traçar um plano para a analisar as possíveis implementações e mudanças a serem feitas na escola Mousinho da Silveira.

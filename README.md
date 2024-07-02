# Detecção de linguagem ofensiva PLN_BERT.ipynb

<p>Trabalho da disciplina de Redes Neurais (UFOP), no qual foi proposta a criação de uma rede neural para identificação de linguagem ofensiva ou discurso de ódio em textos de redes sociais, mesmo com o treinamento sendo realizado em uma rede social diferente. </p>

Este trabalho explora a aplicação do modelo BERT para a detecção de linguagem ofensiva e discurso de ódio em textos em português brasileiro. A metodologia abrange a seleção das bases de dados, o processamento dos dados, a definição das arquiteturas dos modelos, o treinamento e a validação dos modelos, e a análise dos resultados.<p>

<h2>Base de Dados</h2>
<p>Foram utilizadas duas bases de dados principais, sendo que foi testado de forma binária, é ou não é discurso de ódio ou linguagem ofensiva:<p>

[`HateBR`](https://aclanthology.org/2022.lrec-1.777/): Composta por 7.000 documentos anotados em três camadas: classificação binária (comentários ofensivos vs. não ofensivos), nível de ofensividade (altamente, moderadamente, ligeiramente ofensivos) e nove grupos de discurso de ódio (xenofobia, racismo, homofobia, sexismo, intolerância religiosa, partidário, apologia à ditadura, antissemitismo e gordofobia).<p>
[`Offensive Language and Hate Speech Dataset in Brazilian Portuguese`](https://www.kaggle.com/datasets/hrmello/brazilian-portuguese-hatespeech-dataset): Contém 5.668 tweets anotados por não especialistas com rótulos binários (ódio vs. não-ódio) e por especialistas com um esquema hierárquico de 81 categorias de discurso de ódio.<p>

<h2>Metodologia</h2>
Preparação dos Dados<p>
Os dados foram inicialmente processados e divididos em conjuntos de treino e teste, com 80% dos dados destinados ao treinamento e 20% para o teste. Esse procedimento foi realizado para ambas as bases de dados.

<h2>Modelos e Arquiteturas</h2>
Foram testados dois modelos principais:

DistilBERT<p>
BERTimbau-base<p>

<h2>Resultados</h2>
Desempenho dos Modelos:<p>
  
<h3>DistilBERT</h3>

 <!-- jose --> 
Treinado com HateBR| Testado com Brazilian Portuguese Hatespeech dataset|
|------------------|----------------------------------------------------| 
|Acurácia: <!-- 0.89857 -->|Acurácia: <!--0.66843-->|
|Precisão: <!--0.91867-->|Precisão: <!--0.48084-->|
|Recall: <!--0.87392-->|Recall: <!--0.64597-->|
|F1-Score: <!--0.89574-->|F1-Score: <!--0.55131-->|

<h3>BERTimbau-base</h3>

Treinado com HateBR |Testado com Brazilian Portuguese Hatespeech dataset
|------------------|----------------------------------------------------| 
|Acurácia: <!--0.89357-->|Acurácia: <!--0.60176-->|
|Precisão: <!--0.87245-->|Precisão: <!--0.42539-->|
|Recall: <!--0.92120-->|Recall: <!--0.74944-->|
|F1-Score: <!--0.89616-->|F1-Score: <!--0.54272-->|


<h2>Conclusão</h2>
Os resultados indicam que o treinamento dos modelos utilizando dados do Twitter tende a produzir resultados mais eficazes na detecção de linguagem ofensiva e discurso de ódio. Isso sugere que a natureza diversificada e dinâmica das interações no Twitter fornece uma representação mais abrangente da linguagem tóxica em plataformas sociais.<p>

Este estudo confirma a relevância e eficácia do uso de modelos pré-treinados como o BERT no processamento de linguagem natural, especialmente para a tarefa de identificação de discurso de ódio e linguagem ofensiva em português brasileiro.

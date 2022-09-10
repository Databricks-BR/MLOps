## Arquitetura MLOps Databricks

O Databricks Machine Learning é uma solução colaborativa e nativa de dados para todo o ciclo de vida de ML.

Ele fornece todos os recursos necessários para que as equipes de dados treinem e implantem com sucesso modelos de Machine Learning e se concentrem em suas necessidades de negócios, em vez de jogar como integradores de sistemas.
</BR> </BR>

<img src='https://raw.githubusercontent.com/Databricks-BR/MLOps/main/images/mlops_arquitetura.png'></img>




## Data Science Workspace

Espaço de trabalho de ciência de dados, que facilita a colaboração entre os Times de Dados (Engenheiros e Cientistas de dados), suportando notebooks Multilanguage (Scala, SQL, Python ou R, tudo no mesmo notebook). Assim, os notebooks também fornecem recursos de colaboração nativos da nuvem, como co-edição, versionamentos (Git/REPOS) e comentários. Podendo também gerenciar melhor os "Experimentos", que mostram parâmetros, métricas e modelos rastreados, diretamente no contexto do seu trabalho.

## Data Lake Foundation

O Databricks Machine Learning é construído sobre uma base de data lakehouse aberta (DELTA), potencializando a integração com diversas soluções.


## Feature Store (Loja de Recursos)

Feature Store é um repositório centralizado que permite que os cientistas de dados encontrem e compartilhem recursos e também garante que o mesmo código usado para calcular os valores dos recursos seja usado para treinamento e inferência de modelos.
O aprendizado de máquina usa dados existentes para criar um modelo para prever resultados futuros. Em quase todos os casos, os dados brutos requerem pré-processamento e transformação antes que possam ser usados ​​para construir um modelo. Esse processo é chamado de featurização ou engenharia de recursos, e as saídas desse processo são chamadas de recursos - os blocos de construção do modelo.

## Databricks AutoML

O Databricks AutoML ajuda você a aplicar automaticamente o aprendizado de máquina a um conjunto de dados. Ele prepara o conjunto de dados para treinamento de modelo e, em seguida, executa e registra um conjunto de testes, criando, ajustando e avaliando vários modelos. Ele exibe os resultados e fornece um notebook Python com o código-fonte para cada execução de teste para que você possa revisar, reproduzir e modificar o código. O AutoML também calcula estatísticas resumidas em seu conjunto de dados e salva essas informações em um bloco de anotações que você pode revisar posteriormente.

O AutoML distribui automaticamente testes de ajuste de hiperparâmetros entre os nós do trabalhador de um cluster.

Cada modelo é construído a partir de componentes de código aberto e pode ser facilmente editado e integrado aos seus pipelines de aprendizado de máquina. Você pode usar o Databricks AutoML para problemas de regressão, classificação e previsão. 

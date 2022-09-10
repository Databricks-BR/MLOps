## MLflow: uma plataforma aberta de aprendizado de máquina
O MLflow é inspirado em plataformas de ML existentes, mas foi projetado para ser aberto em dois sentidos:

* **Interface aberta**: o MLflow foi projetado para funcionar com qualquer biblioteca, algoritmo, ferramenta de implantação ou linguagem de ML. Ele é construído em torno de APIs REST e formatos de dados simples (por exemplo, um modelo pode ser visto como uma função lambda) que pode ser usado a partir de uma variedade de ferramentas, em vez de fornecer apenas um pequeno conjunto de funcionalidades internas. Isso também facilita a adição de MLflow ao seu código de ML existente para que você possa se beneficiar dele imediatamente e compartilhar código usando qualquer biblioteca de ML que outras pessoas em sua organização possam executar.

* **Código aberto**: estamos lançando o MLflow como um projeto de código aberto que usuários e desenvolvedores de bibliotecas podem estender. Além disso, o formato aberto do MLflow facilita muito o compartilhamento de etapas e modelos de fluxo de trabalho entre organizações, caso você deseje abrir o código-fonte do seu código.


## Conceito
O MLflow é organizado em quatro componentes: Tracking , Projects , Models e Model Registry . Você pode usar cada um desses componentes por conta própria — por exemplo, talvez você queira exportar modelos no formato de modelo do MLflow sem usar Rastreamento ou Projetos — mas eles também foram projetados para funcionar bem juntos.

A filosofia principal do MLflow é colocar o mínimo possível de restrições em seu fluxo de trabalho: ele foi projetado para funcionar com qualquer biblioteca de aprendizado de máquina, determinar a maioria das coisas sobre seu código por convenção e exigir alterações mínimas para integrar a uma base de código existente. Ao mesmo tempo, o MLflow visa pegar qualquer base de código escrita em seu formato e torná-la reproduzível e reutilizável por vários cientistas de dados. Nesta página, descrevemos um fluxo de trabalho de ML típico e onde o MLflow se encaixa.

## Fluxo de trabalho 
O aprendizado de máquina requer experimentar uma ampla variedade de conjuntos de dados, etapas de preparação de dados e algoritmos para criar um modelo que maximize algumas métricas de destino. Depois de criar um modelo, você também precisa implantá-lo em um sistema de produção, monitorar seu desempenho e retreiná-lo continuamente em novos dados e comparar com modelos alternativos.

## Componentes do MLflow
O MLflow fornece quatro componentes para ajudar a gerenciar o fluxo de trabalho de ML:


## MLflow Tracking
O MLflow Tracking é uma API e interface do usuário para registrar parâmetros, versões de código, métricas e artefatos ao executar seu código de aprendizado de máquina e para visualizar os resultados posteriormente. Você pode usar o MLflow Tracking em qualquer ambiente (por exemplo, um script autônomo ou um notebook) para registrar resultados em arquivos locais ou em um servidor e comparar várias execuções. As equipes também podem usá-lo para comparar resultados de diferentes usuários.

## MLFlow Project
Projetos MLflow são um formato padrão para empacotar código de ciência de dados reutilizável. Cada projeto é simplesmente um diretório com código ou um repositório Git, e usa um arquivo descritor ou simplesmente convenção para especificar suas dependências e como executar o código. Por exemplo, os projetos podem conter um conda.yamlarquivo para especificar um ambiente Python Conda . Quando você usa a API MLflow Tracking em um projeto, o MLflow lembra automaticamente a versão do projeto (por exemplo, Git commit) e quaisquer parâmetros. Você pode executar facilmente projetos MLflow existentes no GitHub ou em seu próprio repositório Git e encadeá-los em fluxos de trabalho de várias etapas.

## MLFlow Models
Modelos de MLflow oferecem uma convenção para empacotar modelos de aprendizado de máquina em vários sabores e uma variedade de ferramentas para ajudá-lo a implantá-los. Cada modelo é salvo como um diretório contendo arquivos arbitrários e um arquivo descritor que lista vários “sabores” nos quais o modelo pode ser usado. Por exemplo, um modelo do TensorFlow pode ser carregado como um DAG do TensorFlow ou como uma função Python para aplicar à entrada dados. O MLflow fornece ferramentas para implantar muitos tipos de modelos comuns em diversas plataformas: por exemplo, qualquer modelo que suporte o sabor "função Python" pode ser implantado em um servidor REST baseado em Docker, em plataformas de nuvem como Azure ML e AWS SageMaker e como um função definida pelo usuário no Apache Spark para inferência em lote e streaming. Se você gerar modelos do MLflow usando a API de rastreamento, o MLflow também lembrará automaticamente de qual projeto e execução eles vieram.

## MLflow Registry
O MLflow Registry oferece um armazenamento de modelo centralizado, conjunto de APIs e interface do usuário para gerenciar de forma colaborativa o ciclo de vida completo de um modelo MLflow. Ele fornece linhagem de modelo (que o MLflow experimentou e executou produziu o modelo), versão de modelo, transições de estágio (por exemplo, de preparação para produção ou arquivamento) e anotações.


## Referências:

* https://mlflow.org/docs/latest/concepts.html

* https://pypi.org/project/mlflow

* https://mlflow.org

* https://www.databricks.com/blog/2018/06/05/introducing-mlflow-an-open-source-machine-learning-platform.html

* https://docs.microsoft.com/pt-br/azure/databricks/applications/mlflow/quick-start

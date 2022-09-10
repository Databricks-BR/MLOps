## MLflow: uma plataforma aberta de aprendizado de máquina
O MLflow é inspirado em plataformas de ML existentes, mas foi projetado para ser aberto em dois sentidos:

* **Interface aberta**: o MLflow foi projetado para funcionar com qualquer biblioteca, algoritmo, ferramenta de implantação ou linguagem de ML. Ele é construído em torno de APIs REST e formatos de dados simples (por exemplo, um modelo pode ser visto como uma função lambda) que pode ser usado a partir de uma variedade de ferramentas, em vez de fornecer apenas um pequeno conjunto de funcionalidades internas. Isso também facilita a adição de MLflow ao seu código de ML existente para que você possa se beneficiar dele imediatamente e compartilhar código usando qualquer biblioteca de ML que outras pessoas em sua organização possam executar.

* **Código aberto**: estamos lançando o MLflow como um projeto de código aberto que usuários e desenvolvedores de bibliotecas podem estender. Além disso, o formato aberto do MLflow facilita muito o compartilhamento de etapas e modelos de fluxo de trabalho entre organizações, caso você deseje abrir o código-fonte do seu código.


## Conceito
O MLflow é organizado em quatro componentes: Tracking , Projects , Models e Model Registry . Você pode usar cada um desses componentes por conta própria — por exemplo, talvez você queira exportar modelos no formato de modelo do MLflow sem usar Rastreamento ou Projetos — mas eles também foram projetados para funcionar bem juntos.

A filosofia principal do MLflow é colocar o mínimo possível de restrições em seu fluxo de trabalho: ele foi projetado para funcionar com qualquer biblioteca de aprendizado de máquina, determinar a maioria das coisas sobre seu código por convenção e exigir alterações mínimas para integrar a uma base de código existente. Ao mesmo tempo, o MLflow visa pegar qualquer base de código escrita em seu formato e torná-la reproduzível e reutilizável por vários cientistas de dados. Nesta página, descrevemos um fluxo de trabalho de ML típico e onde o MLflow se encaixa.

## Fluxo de trabalho 
O aprendizado de máquina requer experimentar uma ampla variedade de conjuntos de dados, etapas de preparação de dados e algoritmos para criar um modelo que maximize algumas métricas de destino. Depois de criar um modelo, você também precisa implantá-lo em um sistema de produção, monitorar seu desempenho e retreiná-lo continuamente em novos dados e comparar com modelos alternativos.


## Referências:

* https://mlflow.org/docs/latest/concepts.html

* https://pypi.org/project/mlflow

* https://mlflow.org

* https://www.databricks.com/blog/2018/06/05/introducing-mlflow-an-open-source-machine-learning-platform.html

* https://docs.microsoft.com/pt-br/azure/databricks/applications/mlflow/quick-start

## Quais são as melhores práticas para MLOps?

As melhores práticas para MLOps podem ser delineadas pelo estágio em que os princípios de MLOps estão sendo aplicados.

* **Análise exploratória de dados (EDA)** – explore, compartilhe e prepare dados de forma iterativa para o ciclo de vida do aprendizado de máquina criando conjuntos de dados, tabelas e visualizações reproduzíveis, editáveis ​​e compartilháveis.

* **Preparação de dados e engenharia de recursos** - Transforme, agregue e desduplicar iterativamente dados para criar recursos refinados. Mais importante ainda, torne os recursos visíveis e compartilháveis ​​entre as equipes de dados, aproveitando um repositório de recursos.

* **Treinamento e ajuste de modelo** - Use bibliotecas populares de software livre, como scikit-learn e hyperopt, para treinar e melhorar o desempenho do modelo. Como alternativa mais simples, use ferramentas automatizadas de aprendizado de máquina, como o AutoML, para realizar execuções de teste automaticamente e criar código revisável e implantável.

* **Revisão e governança do modelo** - Rastreie a linhagem do modelo, as versões do modelo e gerencie os artefatos e as transições do modelo ao longo de seu ciclo de vida. Descubra, compartilhe e colabore em modelos de ML com a ajuda de uma plataforma MLOps de código aberto, como o MLflow.

* **Inferência e veiculação de modelos** - Gerencie a frequência de atualização do modelo, tempos de solicitação de inferência e especificações de produção semelhantes em testes e controle de qualidade. Use ferramentas de CI/CD, como repositórios e orquestradores (princípios de devops emprestados) para automatizar o pipeline de pré-produção.

* **Implantação e monitoramento de modelos** - Automatize permissões e criação de clusters para produzir modelos registrados. Ative os endpoints do modelo da API REST.

* **Retreino automatizado do modelo** - Crie alertas e automação para tomar ações corretivas Em caso de desvio do modelo devido a diferenças nos dados de treinamento e inferência.



## Referências:

* https://www.databricks.com/glossary/mlops
* https://www.databricks.com/blog/2022/06/22/architecting-mlops-on-the-lakehouse.html

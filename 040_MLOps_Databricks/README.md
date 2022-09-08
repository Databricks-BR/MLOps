
## MLOps na plataforma Databricks

Na Databricks, ajudamos milhares de clientes a colocar o Machine Learning (ML) em produção. A Shell tem mais de 160 projetos ativos de IA economizando milhões de dólares; A Comcast gerencia centenas de modelos de aprendizado de máquina com facilidade com o MLflow; e muitos outros criaram soluções de ML bem-sucedidas.
</BR> </BR>

Antes de trabalhar conosco, muitos clientes lutavam para colocar o ML em produção – por um bom motivo: as operações de aprendizado de máquina (MLOps) são um desafio. O MLOps envolve o gerenciamento conjunto de código (**DevOps**), dados (**DataOps**) e modelos (**ModelOps**) em sua jornada para a produção. O desafio mais comum e doloroso que vimos é uma lacuna entre dados e ML, muitas vezes dividida em ferramentas e equipes mal conectadas.
</BR> </BR>
Para resolver esse desafio, o Databricks Machine Learning se baseia na arquitetura Lakehouse para estender seus principais benefícios – simplicidade e abertura – para MLOps.
</BR> </BR>
<img src='https://raw.githubusercontent.com/Databricks-BR/MLOps/main/images/mlops_databricks.png' width='500px'></img>

Nossa plataforma simplifica o ML definindo um fluxo de trabalho centrado em dados que unifica as melhores práticas de DevOps, DataOps e ModelOps. Os pipelines de aprendizado de máquina são, em última análise, pipelines de dados, nos quais os dados fluem pelas mãos de várias pessoas. Engenheiros de dados ingerem e preparam dados; cientistas de dados constroem modelos a partir de dados; Os engenheiros de ML monitoram as métricas do modelo; e analistas de negócios examinam as previsões. O Databricks simplifica o aprendizado de máquina de produção, permitindo que essas equipes de dados colaborem e gerenciem essa abundância de dados em uma única plataforma, em vez de silos. 
</BR> </BR>
Por exemplo, nossa Loja de Recursos (Feature Store) permite que você produza seus modelos e recursos em conjunto: os cientistas de dados criam modelos que estão "conscientes" de quais recursos eles precisam para que os engenheiros de ML possam implantar modelos com processos mais simples.

## Gerenciamento conjunto de código, dados e modelos

MLOps é um conjunto de processos e automação para gerenciar código, dados e modelos para atender às duas metas de desempenho estável e eficiência de longo prazo em sistemas de ML. Resumindo, MLOps = DevOps + DataOps + ModelOps.

Em sua jornada em direção a aplicativos voltados para negócios ou clientes, os ativos de ML (código, dados e modelos) passam por uma série de estágios. Eles precisam ser desenvolvidos (estágio de "desenvolvimento"), testados (estágio de "ensaio") e implantados (estágio de "produção"). Esse trabalho é feito em ambientes de execução, como espaços de trabalho do Databricks.

Todos os acima - ambientes de execução, código, dados e modelos - são divididos em dev, staging e prod. Essas divisões podem ser entendidas em termos de garantias de qualidade e controle de acesso. Os ativos em desenvolvimento podem ser mais amplamente acessíveis, mas não têm garantias de qualidade. Os ativos em produção são geralmente críticos para os negócios, com as mais altas garantias de teste e qualidade, mas com controles rígidos sobre quem pode modificá-los.

## MLOps de colaboração e gerenciamento

Devemos equilibrar as necessidades dos cientistas de dados para terem flexibilidade e visibilidade para desenvolver e manter modelos com a necessidade conflitante de engenheiros de ML de ter controle sobre os sistemas de produção. Os cientistas de dados precisam executar seu código em dados de produção e ver logs, modelos e outros resultados de sistemas de produção. Os engenheiros de ML precisam limitar o acesso aos sistemas de produção para manter a estabilidade e, às vezes, preservar a privacidade dos dados. Resolver essas necessidades torna-se ainda mais desafiador quando a plataforma é unida a partir de várias tecnologias desarticuladas que não compartilham um único modelo de controle de acesso.

## Integração e personalização

Muitas ferramentas para ML não foram projetadas para serem abertas; por exemplo, algumas ferramentas de ML exportam modelos apenas em formatos de caixa preta, como arquivos JAR. Muitas ferramentas de dados não são projetadas para ML; por exemplo, data warehouses exigem a exportação de dados para ferramentas de ML, aumentando os custos de armazenamento e as dores de cabeça de governança. Quando essas ferramentas componentes não são baseadas em formatos abertos e APIs, é impossível integrá-los em uma plataforma unificada.

## Simplificando MLOps com o LAKEHOUSE

Para atender aos requisitos do MLOps, a Databricks construiu sua abordagem em cima da arquitetura Lakehouse, que unificam os recursos de data lakes e data warehouses em uma única arquitetura, onde essa simplificação é possível usando formatos abertos e APIs que alimentam os dois tipos de cargas de trabalho de dados. Analogamente, para MLOps, oferecemos uma arquitetura mais simples porque construímos MLOps em torno de padrões de dados abertos.

## Principais benefícios do MLOps com o LAKEHOUSE

* **Processos operacionais**  - Nossa abordagem estende as ideias de DevOps ao ML, definindo uma semântica clara para o que significa "mover para produção" para código, dados e modelos. As ferramentas de DevOps e os processos de CI/CD existentes podem ser reutilizados para gerenciar o código para pipelines de ML. Computação de recursos, inferência e outros pipelines de dados seguem o mesmo processo de implantação do código de treinamento do modelo, simplificando as operações. Um serviço designado — o MLflow Model Registry — permite que o código e os modelos sejam atualizados independentemente, resolvendo o principal desafio de adaptar os métodos DevOps ao ML.

* **Colaboração e gerenciamento** - Nossa abordagem é baseada em uma plataforma unificada que oferece suporte a engenharia de dados, ciência de dados exploratória, ML de produção e análise de negócios, todos sustentados por uma camada de dados compartilhada. Os dados de ML são gerenciados sob a mesma arquitetura lakehouse usada para outros pipelines de dados, simplificando as transferências. Os controles de acesso em ambientes de execução, código, dados e modelos permitem que as equipes certas obtenham os níveis certos de acesso, simplificando o gerenciamento.

* **Integração e personalização** - Nossa abordagem é baseada em formatos abertos e APIs: Git e ferramentas CI/CD relacionadas, Delta Lake e a arquitetura Lakehouse e MLflow. Código, dados e modelos são armazenados em sua conta na nuvem (assinatura) em formatos abertos, apoiados por serviços com APIs abertas. Embora a arquitetura de referência descrita abaixo possa ser totalmente implementada no Databricks, cada módulo pode ser integrado à sua infraestrutura existente e personalizado. Por exemplo, o retreinamento do modelo pode ser totalmente automatizado, parcialmente automatizado ou manual.

## Referências:

* https://www.databricks.com/blog/2022/06/22/architecting-mlops-on-the-lakehouse.html

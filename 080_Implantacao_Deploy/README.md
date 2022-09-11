
## Padrões de implantação de modelo (Deploy Models)

A natureza assíncrona das alterações em modelos e código significa 
que há vários padrões possíveis que um processo de desenvolvimento de ML pode seguir.

Os modelos são criados pelo código, mas os artefatos de modelo resultantes e 
o código que os criou podem operar de modo assíncrono. 
Ou seja, novas versões de modelo e alterações de código podem não acontecer ao mesmo tempo. 

## Implantar código - Deploy Code (recomendado)

Na maioria das situações, o Databricks recomenda a abordagem de "implantar código". 
Essa abordagem é incorporada ao fluxo de trabalho de MLOps recomendado.

Nesse padrão, o código para treinar modelos é desenvolvido no ambiente de desenvolvimento. 
O mesmo código passa para o preparo e a produção. 
O modelo é treinado em cada ambiente: 
inicialmente, no ambiente de desenvolvimento como parte do desenvolvimento do modelo, 
no preparo (em um subconjunto limitado de dados) como parte de testes de integração e no ambiente de produção 
(em dados de produção completos) para produzir o modelo final.

### Vantagens:

Em organizações em que o acesso aos dados de produção é restrito, 
esse padrão permite que o modelo seja treinado em dados de produção no ambiente de produção.
A repetição de treinamentos automatizada é mais segura, pois o código de treinamento é revisado, 
testado e aprovado para produção.
O código de suporte segue o mesmo padrão que o código de treinamento do modelo. 
Ambos passam por testes de integração no preparo.

### As desvantagens:

A curva de aprendizado para os cientistas de dados entregarem código aos colaboradores pode ser íngreme. Modelos de projeto e fluxos de trabalho predefinidos são úteis.
Também nesse padrão, cientistas de dados devem ser capazes de examinar os resultados do treinamento do ambiente de produção, pois eles têm conhecimento para identificar e corrigir problemas específicos de ML.

Se sua situação exigir que o modelo seja treinado no preparo do conjunto de dados de produção completo, você poderá usar uma abordagem híbrida implantando código para preparo, treinando o modelo e implantando o modelo em produção. Essa abordagem economiza custos de treinamento na produção, mas adiciona custo de operação no preparo.

## Implantar modelos (Deploy Model)

Nesse padrão, o artefato do modelo é gerado pelo código de treinamento no ambiente de desenvolvimento. 
O artefato é testado no ambiente de preparo antes de ser implantado em produção.

Essa opção poderá ser considerada se uma ou mais das seguintes situações se aplicar:

* O treinamento do modelo é muito caro ou difícil de reproduzir.
* Todo o trabalho é feito em um só workspace do Azure Databricks.
* Você não está trabalhando com repositórios externos ou um processo de CI/CD.

### Vantagens:

Uma entrega mais simples para cientistas de dados.
Em casos em que o treinamento do modelo é caro, só é necessário treinar o modelo uma vez.

### As desvantagens:

Se os dados de produção não estiverem acessíveis do ambiente de desenvolvimento (o que pode ser verdadeiro por motivos de segurança), essa arquitetura poderá não ser viável.
O retreinamento automatizado de modelos é complicado nesse padrão. Você pode automatizar o retreinamento no ambiente de desenvolvimento, mas a equipe responsável por implantar o modelo em produção pode não aceitar o modelo resultante como pronto para produção.
O código de suporte, como pipelines usados para definição de recursos, inferência e monitoramento, precisa ser implantado na produção separadamente.


## Referência

* https://docs.microsoft.com/pt-br/azure/databricks/applications/machine-learning/mlops/deployment-patterns


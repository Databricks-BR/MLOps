
## Modelo de Maturidade em MLOps

Modelo baseado na documentação da Microsoft Azure (MLOps Maturity Model).
</BR>
A finalidade desse modelo de maturidade é ajudar a esclarecer os princípios e as práticas de MLOps (Operações de Machine Learning). O modelo de maturidade mostra a melhoria contínua na criação e operação de um ambiente de aplicativo de machine learning em nível de produção. Você pode usá-lo como uma métrica para estabelecer os requisitos progressivos necessários para medir a maturidade de um ambiente de produção de machine learning e seus processos associados.

## Níveis de Maturidade

|Nível|Descrição|Destaques|Tecnologia|
|-----|-----|-----|-----|
|0|	**Sem MLOps**|Difícil gerenciar o ciclo de vida completo do modelo de machine learning;  </BR> As equipes são diferentes e as versões são dolorosas;  </BR> A maioria dos sistemas existem como "caixas pretas", poucos comentários durante/pós-implantação;|	Builds e implantações manuais;   </BR>  Teste manual de modelo e aplicativo;   </BR>  Sem acompanhamento centralizado do desempenho do modelo;   </BR>  O treinamento do modelo é manual.|
|1|	**Com DevOps mas sem MLOps**|As versões são menos dolorosas que Nenhuma MLOps, mas dependem da Equipe de Dados para cada novo modelo;   </BR>  Comentários ainda limitados sobre o desempenho de um modelo na produção;   </BR>  Difícil rastrear/reproduzir resultados.|	Builds automatizados;   </BR>  Testes automatizados para código do aplicativo.|
|2|	**Treinamento automatizado**|O ambiente de treinamento é totalmente gerenciado e rastreável;   </BR>  Modelo fácil de reproduzir;   </BR>  As versões são manuais, mas com baixo atrito;|	Treinamento de modelo automatizado;   </BR>  Acompanhamento centralizado do desempenho do treinamento de modelo;   </BR>  Gerenciamento de modelos.|
|3|	**Implantação de modelo automatizado**|As versões são de baixo atrito e automáticas;   </BR>  Rastreabilidade completa da implantação de volta aos dados originais;  </BR>  Ambiente inteiro gerenciado: treinar > produção.|	Teste A/B integrado do desempenho do modelo para implantação;   </BR>  Testes automatizados para todos os códigos;   </BR>  Acompanhamento centralizado do desempenho do treinamento de modelo.|
|4|	**Operações automatizadas completas do MLOps**|Sistema completo automatizado e monitorado facilmente;  </BR>  Os sistemas de produção estão fornecendo informações sobre como melhorar e, em alguns casos, melhorar automaticamente com novos modelos;   </BR>  Aproximando-se de um sistema de tempo de inatividade zero.|	Treinamento e teste de modelo automatizado;   </BR>  Métricas detalhadas e centralizadas do modelo implantado.|

</BR>

## Referência:

https://docs.microsoft.com/pt-br/azure/architecture/example-scenario/mlops/mlops-maturity-model

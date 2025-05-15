# dotnet9-semantickernel-postgres-otel-azureappinsights_consultaprodutos
Exemplo em .NET 9 de Console Application que faz uso do projeto Semantic Kernel, com integração com soluções de IA como Azure Open AI e Ollama na consulta de informações de produtos em uma base PostgreSQL. Inclui Docker Compose para criação do ambiente de testes com os dados + monitoramento com Application Insights/Azure Monitor.

Referências:
* [Enable Azure Monitor OpenTelemetry for .NET, Node.js, Python, and Java applications](https://learn.microsoft.com/en-us/azure/azure-monitor/app/opentelemetry-enable?tabs=net)

---

## Resultados da Telemetria

Acesse a partir do recurso do Application Insights as opções Investigate > Performance > Dependencies:

![Application Insights](img/otel-appinsights-00.png)

Selecionar a operação correspondente ao Trace em Dependencies e acionar a opção Drill into...:

![Application Insights - Dependencies](img/otel-appinsights-01.png)

Selecionar um dos traces (PerguntaChatIAProdutos) em All:

![Traces disponíveis](img/otel-appinsights-02.png)

Trace gerado, com a consulta à base de dados:

![Trace gerado + consulta à base](img/otel-appinsights-03.png)

E exibindo o detalhamento do consumo de tokens (em testes com o Azure OpenAI):

![Trace gerado + consumo de tokens](img/otel-appinsights-04.png)
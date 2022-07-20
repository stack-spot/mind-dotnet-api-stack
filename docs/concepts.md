### Capacidades de Template base

Confira abaixo as capacidades disponíveis para serem adicionadas em um Template base. 

- **Logging**  
Se você possui vários projetos, microsserviços e ou rotinas, com este Plugin você conseguirá manter a qualidade e padrão de informações de log para todas elas, considerando diferentes níveis de log. 

Isso permite definir Tags para que você consiga quantificar e/ou classificar erros, trazendo uma visão de falhas recorrentes ou permitindo a prevenção de problemas futuros. 

Além disso, é fácil fazer a integração com ferramentas como **Splunk** ou **AWS Cloud Watch** para monitorar e visualizar os dados, garantindo a observabilidade das suas aplicações.

- **Metrics**    
O Plugin de Metrics facilita a medição da quantidade de requisições em um endpoint crítico ou o monitoramento do tamanho de payloads que são enviados para sua API.

- **Trace**    
Já o Plugin de Trace facilita a instrumentação de telemetria da sua API, através do **Opentelemetry**, com exporter para **Jaeger** e **AWS X-Ray**.  

- **Queue**    
O Plugin Queue simplifica toda a configuração e implementação de um ambiente descentralizado, voltado à microsserviços e que se comunicam entre si, utilizando filas de mensagens. 

Comparado a criar uma classe, o Plugin Queue consegue abstrair toda a complexidade para a comunicação com a sua fila **AWS SQS**.

- **Notification**    
O plugin Notification provê os recursos do **AWS SNS (Simple Notification Service)** para que sua aplicação possa enviar mensagens para tópicos que serão consumidos por seus Inscritos, enviando de forma simultânea dados, informações e mensagem para diferentes plataformas de uma única vez.

- **Secrets**    
O plugin Secrets facilita o gerenciamento de informações sensíveis de sistemas com chaves de APIs, tokens de autenticação ou conexões com bases de dados. 

Pensando na utilização de um **Secret Manager** como o da AWS, essa gestão ficará mais fácil, já que o Plugin simplifica o consumo dessas informações. 

Utilize o plugin Secrets em qualquer momento em que você desejar dentro da sua aplicação. 

- **Bucket**    
Manipule arquivos utilizando o Plugin Bucket. Este Plugin elimina a complexidade e facilita a instrumentação com a **Amazon Simple Storage Service (S3)**.

- **Repository**    
Armazene dados ou documentos de forma trivial. O Plugin Repository reúne todas as capacidades do **AWS DynamoDB** de forma simples e rápida.

- **Authentication**    
Usando o Plugin Authentication você tem mais segurança ao verificar facilmente os acessos de um usuário ou uma API a recursos restritos da sua API. 

- **ErrorHandler**  
Manipule, padronize e personalize os retornos de erro em sua API REST.

- **gRPC**  
Através do Plugin gRPC é possível adicionar a capacidade de expor serviços `gRPC` e suas configurações, bem como prover a criação de um `gRPC Client`, que permite a distribuição e consumo desse serviço em outras aplicações.

Veja mais detalhes de cada Plugin, Caso e formas de uso disponíveis através do menu lateral esquerdo. 

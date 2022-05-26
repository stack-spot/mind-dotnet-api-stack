No processo de conectar softwares de uma empresa através de uma API, a Stack oferece velocidade e confiança para times de desenvolvimento.

Ao iniciar o seu produto através desse template base oferecido, é possível compilar e executar o projeto localmente. É importante lembrar que a Stack não é intrusiva. Os códigos são criados para ajudar times de desenvolvimento, mas cada desenvolvedor opta pelo que prefere usar. 

Para começar sua jornada de desenvolvimento utilizando os recursos disponibilizados pelo Estúdio Carbon, aplique o template base para iniciar o desenvolvimento de uma API completa usando **C#**, **.NET** e **REST**, rodando em um cluster de contêiner.  

### Visão Geral
O template **dotnet-api-template** adiciona em uma stack a capacidade de provisionar serviços REST.

### Pré-requisitos
Para utilizar esse template você precisa utilizar o `CLI` do `StackSpot` que você pode baixar [**aqui**](https://stackspot.com.br/).
- .NET 5 e/ou 6 instalados.

### Inputs
Os inputs necessários para utilizar o template são:  

| **Campo** | **Valor** | **Descrição** |
| :--- | :--- | :--- |
| Project Name| ex.: MyApp | Nome da aplicação  |
| Target Framework| 5 ou 6 | Framework em que a API será criada  |

## Execução do projeto criado

Após criar o projeto, acesse o diretório onde se encontra a **`Solution`** e os demais arquivos do projeto. Depois disso, execute o seguinte comando:

```bash
    dotnet restore <MyApp>.Api.sln
```

Realize também a compilação do projeto, através do comando abaixo:

```bash
    dotnet build <MyApp>.Api.sln
```

Realize a execução dos testes unitários e de integração. Execute o seguinte comando:

```bash
dotnet test <MyApp>.Api.sln
```

Para testar a aplicação, ainda no mesmo diretório da `Solution`. Execute o seguinte comando:

```bash
    dotnet run --project ./src/<MyApp>.Api/<MyApp>.Api.csproj
```

### Configuração do Docker

Para que o Docker funcione, você precisará adicionar um certificado SSL temporário e montar um volume para manter esse certificado.
Você pode encontrar as informações de como configurar o certificado no site [**Microsoft Docs**](https://docs.microsoft.com/en-us/aspnet/core/security/docker-https?view=aspnetcore-6.0), que descreve as etapas necessárias para **Windows**, **macOS** e **Linux**.

- Para Windows:
O comando seguinte precisará ser executado a partir do seu terminal para criar um certificado:

```bash
dotnet dev-certs https -ep %USERPROFILE%\.aspnet\https\aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

NOTA: Ao usar o PowerShell, substitua **%USERPROFILE% **por **$env:USERPROFILE**.

- Para macOS:
```bash
dotnet dev-certs https -ep ${HOME}/.aspnet/https/aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

- Para Linux:
```bash
dotnet dev-certs https -ep ${HOME}/.aspnet/https/aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

1. Para construir e executar os containers Docker, execute o seguinte comando na raiz da solução onde você encontra o arquivo **`docker-compose.yml`**:

 ```bash
 docker-compose -f 'docker-compose.yml' up --build
 ```

2. Em seguida, abra http://localhost:5000 no seu navegador.

> Dica: Você também pode utilizar uma IDE (VSCode, Visual Studio) de sua preferência para realizar os passos acima.

Com a aplicação em execução, acesse a url https://localhost:5001/swagger, acesse os detalhes da aplicação e clique em "Ir para localhost (não seguro)" no Chrome. Ao acessar o endereço acima, você poderá ver a documentação (*Swagger*) da sua aplicação.

> Dica: Neste caso, a estrutura de projeto com exemplo foi criada automaticamente. 

Aplicando este projeto base, é possível adicionar as seguintes capacidades ao seu template base:

#### Logging  
 Se você possui vários projetos, micro serviços e ou rotinas, com esse plugin você conseguirá manter a qualidade e padrão de informações de log para todas elas, considerando diferentes níveis de log.  Isso permite definir Tags para que você consiga quantificar e/ou classificar erros, trazendo uma visão de falhas recorrentes ou permitindo a prevenção de problemas futuros. 
 Além disso, é fácil fazer a integração com ferramentas como Splunk ou AWS Cloud Watch para monitorar e visualizar os dados, garantindo observabilidade de suas aplicações.

#### Metrics  
O plugin de Metrics facilita a medição da quantidade de requisições em um endpoint crítico ou o monitoramento do tamanho de payloads que são enviados para sua API.

#### Trace  
Já o plugin de Trace facilita a instrumentação de telemetria da sua API, através do Opentelemetry com exporter para Jaeger e AWS X-Ray. 

#### Queue  
O plugin Queue simplifica toda a configuração e implementação de um ambiente descentralizado, voltado à micro serviços e que se comunicam entre si, utilizando filas de mensagens. Comparado a criar uma classe, o plugin Queue consegue abstrair toda a complexidade para a comunicação com a sua fila AWS SQS.

#### Notification  
O plugin Notification provê os recursos do AWS SNS (Simple Notification Service) para que sua aplicação possa enviar mensagens para tópicos que serão consumidos por seus Inscritos, enviando de forma simultânea dados, informações e mensagem para diferentes plataformas de uma única vez.

#### Secrets  
O plugin Secrets facilita o gerenciamento de informações sensíveis de sistemas com chaves de APIs, tokens de autenticação ou conexões com bases de dados. Tendo em vista a utilização de um Secret Manager como o da AWS, essa gestão ficará mais fácil, pois o plugin simplifica o consumo dessas informações. Utilize o plugin Secrets a qualquer momento em que você desejar dentro da sua aplicação. 

#### Bucket  
Manipule arquivos utilizando o plugin Bucket, esse plugin elimina a complexidade e facilita a instrumentação com a Amazon Simple Storage Service (S3).

#### Repository  
Armazene dados ou documentos de forma trivial, o plugin Repository reúne todas as capacidades do AWS DynamoDB de forma simples e rápida.

#### Authentication  
Através do plugin Authentication, tenha mais segurança ao verificar facilmente os acessos de um usuário ou API a recursos restritos da sua API. 

#### ErrorHandler  
Manipule, padronize e personalize os retornos de erro em sua API REST.

#### gRPC  
Através do plugin gRPC é possível adicionar a capacidade de expor serviços `gRPC` e suas configurações, bem como prover a criação de um `gRPC Client` que permite a distribuição e consumo desse serviço em outras aplicações.

Veja mais detalhes de cada plugin, casos e formas de uso disponíveis através do menu lateral esquerdo. 

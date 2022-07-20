### Visão Geral  
A Stack de API não é intrusiva. Os códigos são criados para ajudar os times de desenvolvimento, mas cada desenvolvedor opta pelo que prefere usar. 

Ao iniciar o seu produto através do **template base** oferecido como exemplo, é possível compilar e executar o projeto localmente. 

O template **dotnet-api-template** adiciona em uma Stack a capacidade de provisionar serviços `REST`.

Para começar a sua jornada de desenvolvimento utilizando os recursos disponibilizados pelo **Estúdio Mind**, use este template base como exemplo para iniciar o desenvolvimento de uma API completa usando **C#**, **.NET** e **REST**, e rodando em um cluster de containers.  

### Pré-requisitos
Para utilizar o template **dotnet-api-template** você precisa instalar a tanto a [**`STK CLI`**](https://stackspot.com/) quanto o **.NET 5 e/ou 6**. 

### Inputs
Os inputs necessários para utilizar o template são:   

| **Campo** | **Valor** | **Descrição** |
| :--- | :--- | :--- |
| Project Name| ex.: MyApp | Nome da aplicação.  |
| Target Framework| 5 ou 6 | Framework em que a API será criada.  |

### Exemplo de execução do projeto criado  

1. Depois de criar o projeto, acesse o diretório em que estão a **`Solution`** e os demais arquivos do projeto. Depois disso, execute o comando abaixo:

```bash
    dotnet restore <MyApp>.Api.sln
```

2. Compile o projeto, executando o comando abaixo:

```bash
    dotnet build <MyApp>.Api.sln
```

3. Execute os testes unitários e de integração, com o comando abaixo:  

```bash
dotnet test <MyApp>.Api.sln
```

4. Para testar a aplicação, ainda no mesmo diretório da `Solution`, execute o comando abaixo:  

```bash
    dotnet run --project ./src/<MyApp>.Api/<MyApp>.Api.csproj
```

### **Configuração do Docker**

Para que o Docker funcione, você precisará adicionar um certificado SSL temporário e montar um volume para manter esse certificado.

Você pode encontrar as informações de como configurar o certificado no site [**Microsoft Docs**](https://docs.microsoft.com/en-us/aspnet/core/security/docker-https?view=aspnetcore-6.0), que descreve as etapas necessárias para **Windows**, **macOS** e **Linux**.

- **Para Windows**  
Para criar um certificado, execute o comando abaixo a partir do seu terminal:  

```bash
dotnet dev-certs https -ep %USERPROFILE%\.aspnet\https\aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

> Ao usar o PowerShell, substitua **%USERPROFILE%** por **$env:USERPROFILE**.

- **Para macOS**  
Para criar um certificado, execute o comando abaixo a partir do seu terminal:    

```bash
dotnet dev-certs https -ep ${HOME}/.aspnet/https/aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

- **Para Linux**  
Para criar um certificado, execute o comando abaixo a partir do seu terminal:  

```bash
dotnet dev-certs https -ep ${HOME}/.aspnet/https/aspnetapp.pfx -p Your_password123
dotnet dev-certs https --trust
```

####  **Execução de contêiners Docker**  

1. Para construir e executar os contêiners Docker, execute o comando abaixo na raiz da solução onde você encontra o arquivo **`docker-compose.yml`**:

 ```bash
 docker-compose -f 'docker-compose.yml' up --build
 ```

2. Em seguida, abra http://localhost:5000 no seu navegador.

> Você também pode utilizar uma **IDE** (VSCode, Visual Studio) de sua preferência para realizar os passos acima.

Com a aplicação em execução, siga os passos abaixo:  

1. Acesse a url https://localhost:5001/swagger;
2. Acesse os detalhes da aplicação e clique em **"Ir para localhost (não seguro)"** no Chrome. Ao acessar o endereço acima, você poderá ver a documentação (*Swagger*) da sua aplicação.

> Dica: Neste caso, a estrutura de projeto com exemplo foi criada automaticamente. 

Aplicando este projeto base, é possível adicionar ao seu template base as capacidades disponíveis na próxima página. 


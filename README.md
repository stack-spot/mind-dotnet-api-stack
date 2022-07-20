# mind-dotnet-api-stack

Desenvolva e publique APIs para conectar softwares da empresa no seu produto com a **Stack Cloud Native .NET**. A Stack inclui suporte ao protocolo REST, gRPC, Clean Arch, observabilidade, conexão com filas, além de rodar sobre containers Docker na AWS.  

A Stack facilita o desenvolvimento, publicação e conexão de softwares da sua empresa no seu produto, ajudando os times de desenvolvimento a entregar software com mais velocidade e confiança. Isso traz o benefício do que realmente importa: foco em **business features**. 

### **Estrutura da Stack**  

A **Stack API** foi desenvolvida seguindo todas boas práticas de arquitetura de software:  
- Clean Architecture;
- Atualização constante de Plugins e Templates, focando em acompanhar a modernização tecnológica do mercado, além de garantir a compatibilidade com versões anteriores;
- Código facilmente testável;
- Componentes desacoplados;
- Novas funcionalidades que podem ser adicionadas rapidamente pelo time de desenvolvedores.

A Stack apresenta uma estrutura básica onde o Template inicia todo o ciclo do desenvolvimento, definindo a linguagem, o framework e arquitetura. Isso garante que a aplicação seja compilada e executada localmente.  

Ao usar a Stack, é possível adicionar “superpoderes” ao seu Template utilizando os Plugins da StackSpot, como a capacidade de logs centralizados, publicação de métricas no [Prometheus](https://prometheus.io/) ou a conexão com um banco de dados, por exemplo.  

Na prática, um Plugin pode adicionar dependências ao seu projeto, criar alguns arquivos e, se necessário, executar alguns comandos. Além disso, a Stack possibilita que times de desenvolvimento apliquem Plugins de acordo com próprias necessidades. 

É possível listar todos os Plugins disponibilizados pelo [**Estúdio Mind**](https://stackspot.com/studios/b10fbf6e-cdde-4a8c-a156-da64a53df803) através de um canal próprio do STK CLI.  

Com isso, a Stack disponibiliza um conjunto de soluções, sendo eles: **Templates** e **Plugins**. Este conjunto ajuda os times de desenvolvimento a resolver um problema específico do negócio. 
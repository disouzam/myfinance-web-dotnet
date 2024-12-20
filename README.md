# Sobre esse repositório

Repositório com o conteúdo do trabalho prático da disciplina **Práticas de Implementação e Evolução de Software** da Pós graduação em Engenharia de Software - Oferta 7 - Turma 1 - do Instituto de Educação Continuada da PUC Minas

# Sobre o projeto

Esse projeto didático teve o intuito de criar uma pequena aplicação financeira para uso pessoal. A aplicação foi criada em ASP.NET MVC (Model-View-Controller) com Razor pages e persistência de dados em Microsoft SQL Server 2022, Developer Edition. O mapeamento dos dados foi feito usando Entity Framework Core 9.

A proposta do projeto está disponível no arquivo [ConcepçãoMyFinanceWeb.pdf](./docs/ConcepçãoMyFinanceWeb.pdf)

## Modelo arquitetural resumido

O modelo arquitetural resumido é apresentado na imagem abaixo e a implementação contida nesse projeto satisfaz parcialmente esse desenho. Algumas mudanças são a atualização da versão do SDK do .NET e uma simplificação com respeito às camadas do projeto. O projeto presente contém todas as camadas em um único arquivo .csproj por questões de tempo reduzido para uma implementação mais detalhada.

![Modelagem Arquitetural por Filipe Tório](./docs/MyFinanceWeb-ModelagemArquitetural.png)
*Figura 1: Modelagem Arquitetural elaborada pelo Professor Filipe Tório*

## Como executar a aplicação em ambiente local

### Pré-requisitos
Para executar essa aplicação são necessários os seguintes requisitos:
- Ter o SDK do .NET instalado em versões iguais ou superiores ao **.NET 8**
  - Para essa versão, consulte o link [Download .NET 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0));
- Um **editor de código** como o `Visual Studio Code` ou uma **IDE** como `Visual Studio Community 2022`
  - Essas são apenas sugestões de uso mas outros editores e IDEs podem ser também usados;
- E uma versão do **Microsoft SQL Server 2022** instalada no seu computador (para criar o banco para o desenvolvimento e execução)
  - Ou ainda acesso a uma instância do **Azure SQL Server** com permissão para criar um novo banco de dados.
- Clonar esse repositório em seu computador usando os comandos abaixo:
```bash
# Escolher um diretório para clonar o repositório
cd {diretório de sua preferência}

# Comando para clonar o repositório
git clone https://github.com/dickson-souza-projects/myfinance-web-dotnet.git

# Acessar o conteúdo do repositório
cd myfinance-web-dotnet
```

### Criando o banco de dados

A criação do banco de dados é feita através do script [DB-Creation-And-Configuration.sql](./Scripts/DB-Creation-and-Configuration.sql): por meio dele é criado o banco de dados **MyFinance** contendo duas tabelas: **PlanoConta** e **Transacao**.

A tabela **PlanoConta** descreve os tipos de transação existente, tais como despesas com combustível, água, luz e recebíveis como salários, aluguéis e dividendos.

![Exemplo de Tabela de Plano de Contas](./docs/Exemplo_Tabela_Plano_Contas.png)
*Figura 2: Exemplo de Tabela de Plano de Contas (extraído do documento [ConcepçãoMyFinanceWeb.pdf](./docs/ConcepçãoMyFinanceWeb.pdf), elaborado pelo professor Filipe Tório)*

Já a tabela **Transacao** contém registros de transações individuais, categorizadas pelo **PlanoConta** correspondente.

![Exemplo de Tabela de Transações](./docs/Exemplo_Tabela_Transacao.png)
*Figura 3: Exemplo de Tabela de Transações (extraído do documento [ConcepçãoMyFinanceWeb.pdf](./docs/ConcepçãoMyFinanceWeb.pdf), elaborado pelo professor Filipe Tório)*


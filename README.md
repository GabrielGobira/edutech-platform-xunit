
# EduTechPlatform

Plataforma acadêmica desenvolvida em C# utilizando .NET 10, com foco na implementação de regras de negócio e na garantia da qualidade de software por meio de testes unitários com xUnit.

## Tecnologias utilizadas

- C#
- .NET 10
- xUnit
- Git e GitHub
- Visual Studio Code

## Funcionalidades

### NotaDesempenhoService

Responsável pelo desempenho acadêmico dos alunos.

- CalcularMediaPonderada: calcula a média das notas com pesos 3, 3 e 4.
- ObterSituacaoAcademica: classifica o aluno como APROVADO, RECUPERACAO ou REPROVADO.

### FrequenciaService

Responsável pelo controle de presença dos alunos.

- CalcularPorcentagemPresenca: calcula o percentual de presença.
- AprovadoPorFrequencia: verifica se o aluno possui pelo menos 75% de presença.

### MatriculaFinanceiraService

Responsável pelas regras financeiras e de rematrícula.

- CalcularValorMensalidade: aplica desconto de 50% para bolsistas ou 10% para não bolsistas que pagam até o dia 5.
- PodeRealizarRematricula: permite a rematrícula apenas para alunos sem pendências financeiras e que não estejam reprovados.

## Estrutura do projeto

EduTechPlatform/
- EduTechPlatform.App/
  - Program.cs
  - NotaDesempenhoService.cs
  - FrequenciaService.cs
  - MatriculaFinanceiraService.cs
- EduTechPlatform.Tests/
- EduTechPlatform.slnx
- .gitignore
- LICENSE
- README.md

## Requisitos

- .NET 10 SDK instalado
- Visual Studio Code ou outra IDE compatível
- Git instalado

## Como executar

Clone o repositório:

git clone https://github.com/GabrielGobira/edutech-platform-xunit.git

Entre na pasta:

cd edutech-platform-xunit

Restaure as dependências:

dotnet restore

Compile a solução:

dotnet build

Execute a aplicação:

dotnet run --project EduTechPlatform.App

Execute os testes unitários:

dotnet test

## Testes unitários

O projeto utiliza xUnit para verificar as regras de negócio.

Os testes parametrizados utilizam:

- [Theory]: permite executar o mesmo teste com diferentes conjuntos de dados.
- [InlineData]: fornece os valores de entrada e os resultados esperados.

Os testes abrangem:

- Cálculo de média ponderada.
- Classificação da situação acadêmica.
- Cálculo do percentual de presença.
- Aprovação por frequência.
- Cálculo de mensalidades e descontos.
- Elegibilidade para rematrícula.

Os testes são implementados no projeto EduTechPlatform.Tests.

## Organização da equipe

- Desenvolvedor 1: implementação das regras de negócio.
- Desenvolvedor 2: desenvolvimento dos testes unitários.
- Desenvolvedor 3: documentação, GitHub e versionamento.

## Licença

Este projeto está licenciado sob a licença MIT.

## Objetivo acadêmico

Atividade desenvolvida para a disciplina de Garantia da Qualidade de Software, sob orientação do professor Daniel Henrique Matos de Paiva.

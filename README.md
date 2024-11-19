# Desafio Banco Carrefour

## Solução Atual

A descrição da arquitetura atual (hipotética) está disponível neste [documento](/arquitetura/arquitetura-atual.md).

## Solução Proposta

Solução proposta, considerando mapeamento de domínios funcionais e capacidades de negócio, o documento de requisitos funcionais e não funcionais, o  desenho da aolução está disponível no seguinte [documento](/arquitetura/solucao-proposta.md).

## Anexos

- Desenho da solução da Arquitetura de Transição (se necessária,
considerando uma migração de legado)
- Estimativa de custos com infraestrutura e licenças
Monitoramento e Observabilidade.
- Critérios de segurança para consumo (integração) de serviços.

## Para o desenvolvedor

### Ferramentas e tecnologias utilizadas

- Linguagens e Frameworks
  - Backend - Dotnet 8 com C Sharp.
  - Frontend - React com Typescript.

- Infraestrutura:
  - Backend - Opções em avaliação
    - Amazon EKS
    - Amazon Lambda functions
  - Frontend - Bucket S3
  - Banco de dados: Amazon DynamoDb

- Devops:
  - Git, via Github, para versionamento de código.
  - Github actions para pipelines
  - Github Secrets para credenciais da AWS.
  - Amazon ECR para deploy das imagens dos containers.
  - Amazon Systems Manager (Parameter Store) para configuração da aplicação.
  - Amazon Secrets Manager para armazenar credenciais utilizadas pela aplicação.

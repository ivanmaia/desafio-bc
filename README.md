# Desafio Banco Carrefour

## Solução Atual

A descrição da arquitetura atual (hipotética) está disponível neste [documento](/arquitetura/doc/arquitetura-atual.md).

## Solução Proposta

Solução proposta, considerando mapeamento de domínios funcionais e capacidades de negócio, o documento de requisitos funcionais e não funcionais, o  desenho da aolução está disponível no seguinte [documento](/arquitetura/doc/solucao-proposta.md).

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

### Estrutura de pastas

O repositorio está organizado da seguinte forma:

[Todo]

```text
../
  arquitetura
    doc [documentação de arquitetura]
      diagramas [diagramas e imagens utilizados nos docs de arquitetura]
    code [arquivos terraform infra as code]
        aws [específicos aws]
  pipeline
    local_dev
    aws
  backend [código do backend]
  frontend [código do frontend]
```


### Montando seu ambiente local

- Software necessário
  - Dotnet SDK Versão 8
  - Uma IDE à sua escolha
  - Git
  - Docker
  - AWS CLI
  
### Executando a aplicação localmente

Estando na pasta raiz do repositório.

``` bash
 $ cd devops/local_dev
 $ docker compose
```

Para acessar o banco de dados.

[Todo.]

Para acompanhar as mensagens na fila.

[Todo.]

## Devops

Os artefatos de devops encontram-se na pasta devops.

Artefatos relacionados às pipelines encontram-se na pasta ```devops/pipeline```.

Atualmente, esse projeto só possui a previsão de execução no ambiente aws. Caso seja necessário o deploy em outro provedor cloud, uma nova pasta (por exemplo, azure) em pipelines.

A pipeline para deploy na AWS fica na pasta ```devops/pipeline/aws```.
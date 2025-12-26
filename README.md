# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 25/12/2025
Empresa: Abstergo Industries (Divisão Farmacêutica)
Responsável: Mateus Montalvão Torres

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Shannon. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos através da migração de uma arquitetura legada (on-premise) para uma arquitetura Cloud Native (Serverless).

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos, focando na eliminação de provisionamento fixo de servidores. A seguir, serão descritas as etapas do projeto:

Etapa 1: 
- Amazon S3 (Simple Storage Service)
- Armazenamento de Objetos e Web Hosting Estático
- O S3 será utilizado para hospedar todo o front-end da farmácia virtual (HTML, CSS, JavaScript) e os assets estáticos (imagens dos medicamentos). Ao configurar o bucket como "Static Website Hosting", eliminamos a necessidade de instâncias EC2 rodando servidores web (Apache/Nginx) 24/7, reduzindo drasticamente o custo de computação ociosa e pagando apenas pelo armazenamento e transferência de dados (GB).

Etapa 2: 
- AWS Lambda
- Computação Serverless (FaaS - Function as a Service)
- Toda a lógica de backend (processamento de carrinho, cálculo de frete, validação de receitas médicas) será refatorada em funções Lambda. Diferente de um servidor tradicional que cobra por hora ligado, o Lambda cobra por milissegundo de execução e quantidade de requisições. Se não houver clientes na farmácia virtual durante a madrugada, o custo de computação será literalmente zero.

Etapa 3: 
- Amazon DynamoDB
- Banco de Dados NoSQL Gerenciado (Key-Value)
- Substituição do banco de dados relacional tradicional por uma tabela DynamoDB com capacidade sob demanda (On-Demand Capacity). Isso permite armazenar o catálogo de produtos e perfis de usuários com latência de milissegundos em qualquer escala, eliminando os custos fixos de gerenciamento de licenças e instâncias de banco de dados (RDS) superdimensionadas para suportar picos eventuais de tráfego.

## Conclusão
A implementação de ferramentas na empresa Abstergo Industries tem como esperado a redução do TCO (Total Cost of Ownership) e a eliminação de custos com capacidade ociosa, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias, como o Amazon API Gateway para orquestração das chamadas e o Amazon CloudFront para CDN e caching global.

## Anexos

- Diagrama de Arquitetura Serverless (Conceitual)
- Estimativa de Custos (AWS Calculator)
- Documentação da API de Pedidos

Assinatura do Responsável pelo Projeto:
Mateus Montalvão Torres

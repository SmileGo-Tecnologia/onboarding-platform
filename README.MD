# Onboarding Platform Challenge!

Para sua sorte temos um mega desafio para você, mas não se preocupe, não é tão complexo de implementar quanto parece ;)


# O problema...

Nossos clientes possuem uma operação de crédito, mas como você já deve saber, conceder crédito a portadores requer uma análise muito rígida dos critérios de avaliação para que se possa tomar uma decisão acerca de conceder ou não o crédito.

## O Desafio...

Precisamos que você monte uma plataforma utilizando arquitetura de microserviços e seja orientada a eventos, até porque uma proposta de crédito funciona exatamente por etapas, então já dando uma colher de chá, certifique-se de que microserviços distintos tomam conta de etapas distintas, mas tendo consciência que as vezes a mesma etapa se repete, apenas com detalhes diferentes.

A proposta deve acontecer de forma simples, seguindo o seguinte fluxo:

1. Captação Inicial
2. Motor (P1)
3. Captação Completa
4. Motor (P2)
5. Cadastro de Conta e Cartão (Processadora)
6. Envio de Aprovação/Reprovação por E-mail

![Fluxo de Proposta](./fluxo.png)

## Terminologias

### P1 e P2
São uma abreviação para Política 1 e 2. Isso porque a P1 se faz com dados resumidos podendo ser considerada uma pre-análise. Após aprovação nesta pre-análise é que a proposta pode ter mais dados captados e seguir para análise definitiva.

### Processadora
É a empresa responsável pela tecnologia de emissão e autorização de transações com cartão de crédito.

## Requisitos

Abaixo, alguns dados obrigatórios para cada proposta

### Captação Inicial

|Campo           |Tipo               |Descrição                                               |
|----------------|-------------------|--------------------------------------------------------|
|Nome			 |Texto              |Nome completo                                           |
|CPF			 |Texto              |Cadstro Pessoa Física                                   |
|E-mail			 |Texto              |Endereço eletrônico                                     |

### Captação Completa

|Campo           |Tipo               |Descrição                                               |
|----------------|-------------------|--------------------------------------------------------|
|Nome			 |Texto              |Nome completo                                           |
|CPF			 |Texto              |Cadstro Pessoa Física                                   |
|E-mail			 |Texto              |Endereço eletrônico                                     |
|Data Nascimento |Data               |Data de nascimento contido no RG                        |
|RG 			 |Texto              |Registro Geral                                          |
|CEP			 |Texto              |CEP do Endereço                                         |
|Endereço		 |Texto              |Endereço com logradouro, bairro e número                |
|Profissão		 |Texto              |Ocupação Profissional                                   |
|Renda			 |Numérico           |Renda total                                             |


## Desenvolvimento

1. Será obrigatório o uso de algum serviço de mensageria para a comunicação entre os microserviços, podendo ser Kafka, RabbitMQ ou Amazon SQS.

2. As integrações com processadora e motor de crédito devem ser mockados utilizando qualquer serviço de sua livre escolha.

3. Não deixe que seus microserviços degradem pela indisponibilidade das integrações, existem soluções padrão para isso e esperamos que você implemente isso.

4. Qualquer melhoria, como por exemplo validar se é um CPF verdadeiro, conta positivamente para o seu desafio.

5. A implementação necessáriamente precisa sem em Java com Spring Boot ou algum outro framework como Micronaut e Quarkus.

## Prazo

A entrega deve ser feita em até 5 dias a contar a partir do recebimento do desafio, com a possíbilidade de extensão do prazo por mais 6 horas mediante solicitação por e-mail antes do fim do prazo.

Suba seu projeto para um repositório Git público de sua escolha e envie o link para os endereços abaixo:

Destinatário: victor.ximenis@smilego.com.br

Cópia: leonardo.brito@smilego.com.br, 
jativa.cysneiros@baseservice.io

# Onboarding Platform Challange!

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


## Development

Será obrigatório o uso de algum serviço de mensageria para a comunicação entre os microserviços, podendo ser Kafka, RabbitMQ ou Amazon SQS.

## Prazo

A entrega deve ser feita até 03/06/2023 as 23:59 com a possíbilidade de extensão do prazo por mais 5 horas mediante solicitação por e-mail antes do fim do prazo.

Suba seu projeto para um repositório Git público de sua escolha e envie o link para os endereços abaixo:

Destinatário: victor.ximenis@smilego.com.br

Cópia: leonardo.brito@smilego.com.br, 
jativa.cysneiros@baseservice.io
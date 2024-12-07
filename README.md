# resumo-do-lab-azure
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

Durante  as aulas introdutórias do curso de Azure da DIO, aprendi sobre as Nuvens Privada, Pública e Híbrida, como também aprendi a respeito de CAPex e OPex.

Nuvem Pública: Nuvem disponibilida pela Azure compartilhado entre empresas e usuários. Em teoria, toda a parte de Hardware de servidores é de responsabilidade da empresa que fornece a nuvem.

Nuvem Provada: Nuvem disponibilizada apenas a uma empresa, na qual os serviços são em cloud, mas a maior parte de responsabilidade de Hardware cabe ao contratante. Não é possível que usuários de fora acessem a núvem privada.

Nuvem Híbrida:Uma junção de pública e privada, na qual pode ocorrer uma comunicação entre elas. Alguns serviços de uma empresa podem estar na nuvem privada, e pode haver comunicação com serviços que estejam na pública.

CAPex: Pagamento prévio por Hardwares, no qual o gasto tende a reduzir com o tempo.

OPex:Pagamento poe consumo do que for usado, sem a necessidade de um pagamento prévio.

## Entrega do desafio - Criando máquinas Virtuais na Azure

Como entrega foi solicitado um resumo sobre o que foi aprendido até o momento, então posso resumir que fui apresentada ao tema de Alta disponibilidade, o que envolve o termo SLA, que é o quão disponível aquele recurso deve funcionar, e a partir das horas/minutos ou segundos fora do que foi combinado em contrato, a empresa provedora (Microsoft) se dispoe de um credito ao seu cliente pelo tempo de não funcionamento do serviço.
Quanto maior o SLA, maior a porcentagem (99,9%), menos ele deve ficar indisponível ao usuário. Isso gera um custo, claro, então é necessário entender o quanto você precisa desta escalabilidade, para acionar o SLA correto para sua funcionalidade.
Entendi outros pontos, como Segurança, Disponibilidade, Gerenciabilidade e Governança

## Tipos de Serviço de Nuvem

IaaS (Azure Virtual Machines) oferece a infraestrutura virtual.
PaaS (Azure App Service) fornece uma plataforma de desenvolvimento para aplicativos.
SaaS (Microsoft 365) disponibiliza aplicativos prontos para o uso direto.

## Entrega do desafio - Construindo Arquiteturas no Azure

Nestas ultimas aulas, aprofundei meus conhecimentos a respeeito de Regiões de Disponibilidade, e o quanto elas influenciam após escolhidas no custo do projeto, como também na sua latência e delay, principalmente se a area escolhida para alocar o serviço for longe da localização da minha empresa, e de quem irá acessar estes recursos.

Vi também a respeitos de que uma conta pode ter varias assinaturas, porém estas assinaturas devem pertencer apenas a uma conta. Por isso, as assinaturas de produção, testes e até desenvolvimento são de posse de uma conta, e as mesmas só podem pertencer a ela. Vi a respeito do Grupo de recursos, no qual serve para organizar projetos, máquinas, servidores, redes etc. Você pode escolher a forma como ira organizar estes recursos dentro de um grupo, porém este Grupo deve possuir um nome que não será mais alterado (PAI), e seus recusos se necessários podem ser realocados ou não a outros Grupos de Recurso. Aplicativos podem pertencem a mais de um Grupo, mas recursos não. Outro ponto importante é que meu grupo de recurso pode ser de uma localidade, e meus recursos criados dentro dele de outras regiões do mundo.

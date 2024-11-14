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

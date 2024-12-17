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

## Entrega do Desafio - Construindo Arquiteturas no Azure

Nestas ultimas aulas, aprofundei meus conhecimentos a respeeito de Regiões de Disponibilidade, e o quanto elas influenciam após escolhidas no custo do projeto, como também na sua latência e delay, principalmente se a area escolhida para alocar o serviço for longe da localização da minha empresa, e de quem irá acessar estes recursos.

Vi também a respeitos de que uma conta pode ter varias assinaturas, porém estas assinaturas devem pertencer apenas a uma conta. Por isso, as assinaturas de produção, testes e até desenvolvimento são de posse de uma conta, e as mesmas só podem pertencer a ela. Vi a respeito do Grupo de recursos, no qual serve para organizar projetos, máquinas, servidores, redes etc. Você pode escolher a forma como ira organizar estes recursos dentro de um grupo, porém este Grupo deve possuir um nome que não será mais alterado (PAI), e seus recusos se necessários podem ser realocados ou não a outros Grupos de Recurso. Aplicativos podem pertencem a mais de um Grupo, mas recursos não. Outro ponto importante é que meu grupo de recurso pode ser de uma localidade, e meus recursos criados dentro dele de outras regiões do mundo.

## Entrega do Desafio - Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure
Este breve resumo posso dizer que consegui entender de forma prática, após muitas teorias a respeito do laboratório da Azure, como funciona a criação de recursos, como uma VNET, Máquinas Virtuais, entre outros. Importante se atentar aos detalhes de custo, região, backup, ativação e desligamento automático, além da escolha do SO correto, e memória certa para o que este servidor ou máquina for atuar.

## Entrega do Desafio - Dominando o Armazenamento na Azure
Neste módulo lidei ainda mais com a questão de armazenamento e migração do Azure. É sempre importante se atentar a quais tipos de migração são interessantes para o seu cliente/empresa.

Contas de Armazenamento: Ter um nome exclusivo globalmente. São elas que determinam os serviços de armazenamento e as opções de redundância

Azure data box: Até 80T
Azure data disk: 35T
Azure Heavy: 800T

Blobs: Dados massivos não estruturados:
Disco: Discos para máquinas virtuais
Filas: Armazenamento de mensagens e recuperação. Cada uma com até 64kb
Arquivos: Compartilhamento de arquivos de rede altamente disponíveis
Tabelas: Fornece uma opção de chave/atributo para o armazenamento de dados não estruturados com um design sem esquema

AZ-Copy: Faz a cópia de arquivos locais para o Ambiente de Nuvem da Azure. Sincronização em uma direção.
Gerenciador de armazenamento Azure: Interface Gráfica Intuitiva para o usuário (MacOS, Linus e Windows)
Sincronização de Arquivos do Azure: Sincronização de forma Bilateral, ou seja, ele pode ser configurado para enviar arquivos menos acessados para a nuvem, deixando localmente apenas os mais acessados. Mesmo assim, caso eu precise acessar algum arquivo na nuvem e baixá-lo, isso poderá ser feito sem nenhuma lentidão, quase imperceptivel ao usuário de que aquele arquivo acaba de ser baixado.

## Entrega do Desafio - Entendendo sobre Segurança e Identidade na Azure

Foi expliccado neste tópico a respeito do Entra ID, antigo Active Directory, e com este assunto, foi abordado pontos de autenticação, autorização, identidade, MFA, SSO, entre muitos outros recursos disponíveis para a segurança e acesso na Nuvem do Azure.

## Entrega do Desafio - Otimizando Custos no Azure

Nesta primeira entrega do desafio, pude aprender a respeito dos custos do Azure, que basicamenta há duas formas de calcular.

Você pode verificar quanto sairia migrar seus serviços para a nuvem vs comparação de quanto você gasta atualmente. Existe também a calculadora para serviços e recursos, no qual voc~e calcula aproximadamente quanto sairia por ex: criação de uma máquina, quanto tempo ficaria ligada, sua localização geografica, etc. Existe também a manutenção destes gastos, após já criados na nuvem, verificando sempre se há um gasto maior que o planejado, ou se está sobrando recursos de hardware pela demanda que você utiliza deles, podendo aplicar um downgrade destes recursos. TAGs ou Marcas são importante pois são as etiquetas de um recurso ou de produtos adquiridos. TAG não é obrigatório, mas pode te auxiliar na hora de entender a fatura mental, e saber de onde todos os seus gastos estão surgindo. Se uma TAG existe em um grupo de recursos, novos serviços ou recursos criados não herdarão ela, mas voc~e pode aplicar regras para que toda vez que criado um novo recurso naquele grupo, seja atribuido uma TAG, criando assim uma regra e costume, que irálhe auxiliar futuramente a entender o que está demandando custo ou não.

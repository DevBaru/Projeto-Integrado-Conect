# Conect Info — Functional and Non-Functional Requirements

## English

### Functional Requirements

#### RF01 — Customer Profiles

The system must allow the registration and management of customer profiles, distinguishing between residential and corporate profiles.

#### RF02 — Contract Management

The system must register and store contracts linked to customers.

#### RF03 — SLA Management

The system must register and track service-level agreements (SLAs) by customer or contract.

#### RF04 — Customer Service History

The system must maintain a complete service history for each customer.

#### RF05 — Plan Subscriptions

The system must manage new plan subscriptions.

#### RF06 — Plan Changes

The system must allow changes to existing plans.

#### RF07 — Plan Cancellations

The system must manage plan cancellation requests.

#### RF08 — Billing

The system must handle billing for services provided.

#### RF09 — SMS Billing Notifications

The system must automate the sending of billing notifications by SMS to help reduce delinquency.

#### RF10 — Equipment Procurement

The system must track the acquisition of equipment from suppliers, such as Furukawa and Huawei.

#### RF11 — Acquisition Costs and Exchange Rate Variations

The system must record acquisition costs and the related exchange rate variations.

#### RF12 — Inventory Management

The system must control equipment and material inventory.

#### RF13 — Software Licenses

The system must manage and record software licenses.

#### RF14 — Service Orders

The system must manage the creation and tracking of service orders for field teams.

#### RF15 — Maintenance Classification

The system must classify maintenance activities as preventive inspections or corrective repairs.

#### RF16 — Unexpected Event Records

The system must record unexpected events, such as fiber cuts.

#### RF17 — Field Team Dispatch

The system must automatically dispatch field teams when incidents occur.

#### RF18 — Customer Notifications by SMS

The system must notify customers affected by network failures, interruptions, or events by SMS, including when internet service is unavailable.

#### RF19 — NOC-TI Integration

The system must integrate data from all modules to provide information to the NOC-TI.

#### RF20 — Sales and Cancellations Report

The system must generate comparative reports of sales versus cancellations.

#### RF21 — Purchases and Operating Expenses Report

The system must generate comparative reports of purchases versus operating expenses.

#### RF22 — Delinquency Report

The system must generate reports on delinquency rates.

#### RF23 — Network Availability by POP Report

The system must generate network availability reports by Point of Presence (POP).

### Non-Functional Requirements

#### RNF01 — Individual Authentication

The system must require authentication with individual credentials before allowing access to its functionalities. Each employee or technician must have their own account, identified by a username and password, without sharing credentials. Disabled accounts must not be allowed to access the system.

#### RNF02 — Role-Based Permissions

The system must apply permissions according to each user's assigned role. The Administrator must have access to all modules and functionalities, including user account and access profile management. Customer service/support must be able to manage customer records and service records and view contracts; finance/billing must access billing, charges, and delinquency reports; purchasing/inventory must manage suppliers, purchases, equipment, materials, inventory, and licenses; field technicians must view and update assigned service orders and record technical activities; and the NOC-TI must view operational data, incidents, POPs, and network metrics. Each role must be prevented from performing unauthorized operations.

#### RNF03 — Traceability and Auditing

Actions performed by internal and external technicians, route changes, and access to Points of Presence (POPs) must generate audit records identifying the user, date and time, action performed, and affected record. These records must not be modifiable by users without auditing permissions.

#### RNF04 — Data Protection and Security

Customers' personal data, contracts, and financial information must be accessible only to authorized users and protected against unauthorized access. The solution must comply with the LGPD and provide security controls appropriate to the system's risks, including perimeter protection through firewall rules and mechanisms against cyberattacks, as described in the project overview.

#### RNF05 — Operational Availability

The system must provide availability compatible with the company's operational activities, especially NOC-TI monitoring, support services, and the tracking of network incidents. Outages and maintenance activities that affect access to the system must be identifiable by the responsible personnel.

#### RNF06 — Response Time

In tests with up to 10 simultaneous users, at least 95% of queries, registrations, and updates involving customers, contracts, inventory, and service orders must return results within 3 seconds, and none of these operations must exceed 5 seconds. Management reports covering periods of up to 12 months must be generated within 10 seconds. Measurement must run from the user's request until the result is displayed and must not include SMS delivery time by the mobile operator.

#### RNF07 — Data Integrity Across Modules

Information shared among customers and contracts, sales and billing, purchasing and inventory, maintenance, and the NOC-TI must remain consistent. A confirmed operation must not create duplicate entries or leave updates partially saved; failures during saving must be identifiable and allow correction without silent data loss.

#### RNF08 — Report Reliability

Reports on sales versus cancellations, purchases versus operating expenses, delinquency, and availability by POP must indicate the period covered and the date and time of the latest data update. Calculations must be based on consolidated records from the corresponding modules, and missing or outdated data must not be presented as complete and current.

#### RNF09 — Backup and Recovery

The system must perform periodic backups of operational data and audit records, allowing information to be recovered in the event of failure, loss, or data corruption.

#### RNF10 — Notification Reliability

For automated billing notifications and alerts about network interruptions or events, the system must record the recipient, notification type, date and time of the attempt, and the sending service's reported result. Failed attempts must remain visible for follow-up and must not be recorded as successful deliveries.

#### RNF11 — Usability by Department

The interface must organize information according to the tasks of the departments using the system: customer service and support, field teams, finance and billing, purchasing/inventory, and NOC-TI. Relevant information and actions must be identifiable without requiring users to navigate through data from other departments that is not needed for their tasks.

#### RNF12 — Maintainability and History Preservation

The solution must keep the customer/contracts, sales/billing, purchasing/inventory/licenses, and maintenance/NOC-TI modules organized and documented to facilitate fixes and future improvements. Updates must not delete previously recorded service histories, contracts, purchases, service orders, or audit records.

---

## Português (Brasil)

### Requisitos Funcionais

#### RF01 — Cadastro de clientes

O sistema deve permitir o cadastro e gerenciamento de perfis de clientes, diferenciando perfis residenciais e corporativos.

#### RF02 — Gestão de contratos

O sistema deve registrar e armazenar contratos vinculados aos clientes.

#### RF03 — Gestão de SLAs

O sistema deve registrar e acompanhar acordos de nível de serviço (SLAs) por cliente ou contrato.

#### RF04 — Histórico de atendimento

O sistema deve manter um histórico completo de atendimento de cada cliente.

#### RF05 — Adesão a planos

O sistema deve gerenciar novas adesões de planos.

#### RF06 — Alteração de planos

O sistema deve permitir a realização de alterações de planos existentes.

#### RF07 — Cancelamento de planos

O sistema deve gerenciar solicitações de cancelamento de planos.

#### RF08 — Faturamento

O sistema deve realizar o faturamento dos serviços prestados.

#### RF09 — Cobranças por SMS

O sistema deve automatizar o envio de cobranças por SMS para combater a inadimplência.

#### RF10 — Aquisição de equipamentos

O sistema deve acompanhar a aquisição de equipamentos de parceiros (como Furukawa e Huawei).

#### RF11 — Custos e variações cambiais

O sistema deve registrar os custos de aquisição e as variações cambiais envolvidas.

#### RF12 — Controle de estoque

O sistema deve controlar o estoque de equipamentos e materiais.

#### RF13 — Licenças de software

O sistema deve gerenciar e registrar licenças de software.

#### RF14 — Ordens de serviço

O sistema deve gerenciar a abertura e o acompanhamento de ordens de serviço para as equipes de campo.

#### RF15 — Classificação de manutenções

O sistema deve categorizar as manutenções em revisões preventivas e reparos corretivos.

#### RF16 — Registro de eventos fortuitos

O sistema deve registrar eventos fortuitos (como rompimentos de fibra).

#### RF17 — Acionamento de equipes de campo

O sistema deve acionar automaticamente as equipes de campo diante de ocorrências.

#### RF18 — Notificação de clientes por SMS

O sistema deve notificar por SMS os clientes afetados por falhas, interrupções ou eventos na rede, inclusive quando o serviço de internet estiver indisponível.

#### RF19 — Integração com o NOC-TI

O sistema deve integrar dados de todos os módulos para alimentar o NOC-TI.

#### RF20 — Relatório de vendas e cancelamentos

O sistema deve gerar relatórios comparativos de vendas versus cancelamentos.

#### RF21 — Relatório de compras e gastos operacionais

O sistema deve gerar relatórios comparativos de compras versus gastos operacionais.

#### RF22 — Relatório de inadimplência

O sistema deve gerar relatórios com as taxas de inadimplência.

#### RF23 — Relatório de disponibilidade por POP

O sistema deve gerar relatórios de disponibilidade de rede por Ponto de Presença.

### Requisitos Não Funcionais

#### RNF01 — Autenticação individual

O sistema deve exigir autenticação por credenciais individuais antes de permitir o acesso às suas funcionalidades. Cada funcionário ou técnico deve possuir uma conta própria, identificada por nome de usuário e senha, sem compartilhamento de credenciais. Contas desativadas não devem permitir acesso ao sistema.

#### RNF02 — Permissões por função

O sistema deve aplicar permissões conforme o perfil atribuído a cada usuário. O Administrador deve ter acesso a todos os módulos e funcionalidades, incluindo o gerenciamento de contas e perfis de acesso. O atendimento/suporte deve poder gerenciar cadastros de clientes e registros de atendimento e consultar contratos; o financeiro/cobrança deve acessar faturamento, cobranças e relatórios de inadimplência; compras/estoque deve gerenciar fornecedores, compras, equipamentos, materiais, estoque e licenças; técnicos de campo devem consultar e atualizar as ordens de serviço atribuídas e registrar atividades técnicas; e o NOC-TI deve consultar dados operacionais, ocorrências, POPs e métricas de rede. Cada perfil deve ser impedido de executar operações não autorizadas.

#### RNF03 — Rastreabilidade e auditoria

As ações dos técnicos internos e externos, as alterações de rotas e os acessos aos Pontos de Presença (POPs) devem gerar registros de auditoria que identifiquem o usuário, a data e hora, a ação realizada e o registro afetado. Esses registros não devem poder ser alterados por usuários sem permissão de auditoria.

#### RNF04 — Proteção de dados e segurança

Os dados pessoais dos clientes, contratos e informações financeiras devem ser acessíveis somente a usuários autorizados e protegidos contra acesso indevido. A solução deve observar a LGPD e prever controles de segurança compatíveis com os riscos do sistema, incluindo proteção do perímetro por regras de firewall e mecanismos contra ataques cibernéticos, conforme descrito no minimundo.

#### RNF05 — Disponibilidade operacional

O sistema deve apresentar disponibilidade compatível com as atividades operacionais da empresa, especialmente o monitoramento realizado pelo NOC-TI, o atendimento de suporte e o acompanhamento de ocorrências de rede. Indisponibilidades e manutenções que afetem o acesso ao sistema devem ser identificáveis pelos responsáveis.

#### RNF06 — Tempo de resposta

Em testes com até 10 usuários simultâneos, pelo menos 95% das consultas, cadastros e atualizações de clientes, contratos, estoque e ordens de serviço devem apresentar o resultado em até 3 segundos, e nenhuma dessas operações deve ultrapassar 5 segundos. Relatórios gerenciais referentes a períodos de até 12 meses devem ser gerados em até 10 segundos. A medição deve ocorrer entre a solicitação do usuário e a apresentação do resultado, sem incluir o tempo de entrega de SMS pela operadora.

#### RNF07 — Integridade entre módulos

As informações compartilhadas entre clientes e contratos, vendas e faturamento, compras e estoque, manutenção e NOC-TI devem permanecer consistentes. Uma operação confirmada não deve gerar lançamentos duplicados nem deixar atualizações parcialmente gravadas; falhas durante a gravação devem ser identificáveis e permitir correção sem perda silenciosa de dados.

#### RNF08 — Confiabilidade dos relatórios

Os relatórios de vendas versus cancelamentos, compras versus gastos operacionais, inadimplência e disponibilidade por POP devem indicar o período consultado e a data e hora da última atualização dos dados. Os cálculos devem ser baseados nos registros consolidados dos módulos correspondentes, e dados ausentes ou desatualizados não devem ser apresentados como se fossem completos e atuais.

#### RNF09 — Cópia de segurança e recuperação

O sistema deve realizar cópias de segurança periódicas dos dados operacionais e dos registros de auditoria, permitindo a recuperação das informações em caso de falha, perda ou corrupção de dados.

#### RNF10 — Confiabilidade das notificações

Para as cobranças automatizadas e os avisos de interrupções ou eventos de rede, o sistema deve registrar o destinatário, o tipo de aviso, a data e hora da tentativa e o resultado do envio. Falhas devem ficar visíveis para acompanhamento, sem serem registradas como envios bem-sucedidos.

#### RNF11 — Usabilidade por setor

A interface deve organizar as informações de acordo com as tarefas dos setores que utilizarão o sistema: atendimento e suporte, equipe de campo, financeiro e cobrança, compras/estoque e NOC-TI. As informações e ações relevantes para cada tarefa devem ser identificáveis sem exigir que o usuário navegue por dados de outros setores que não sejam necessários ao seu trabalho.

#### RNF12 — Manutenibilidade e preservação do histórico

A solução deve manter os módulos de clientes/contratos, vendas/faturamento, compras/estoque/licenças e manutenção/NOC-TI organizados e documentados, para facilitar correções e futuras melhorias. Atualizações não devem apagar o histórico de atendimentos, contratos, compras, ordens de serviço ou auditoria já registrado.

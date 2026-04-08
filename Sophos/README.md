# Sophos XG Firewall Template (Advanced)

## 🎯 Por que este template existe?
Este projeto nasceu de uma necessidade real em ambiente de produção na infraestrutura que gerencio. Após buscar em diversas comunidades e repositórios oficiais, notei uma carência de templates para Sophos XG/XGS que fossem realmente completos e atendessem a infraestruturas críticas. 

Muitos templates disponíveis ignoravam pontos vitais para o dia a dia de um administrador de redes, o que me motivou a desenvolver uma solução "dentro de casa" que unisse performance, segurança e alta disponibilidade em um único lugar.

## 📊 O que é monitorado?

Este template foi forjado para não deixar o administrador no escuro. Ele utiliza **LDR (Low Level Discovery)** para automatizar o processo.

### 🛡️ Segurança e Licenciamento
* **Status e Expiração:** Monitoramento de todas as licenças (Base, Network, Web, Email, Zero Day, etc) com alertas de 30 e 7 dias antes do vencimento.
* **Serviços Críticos:** Acompanha o status de execução de daemons vitais como IPS, Antivírus, DNS, WAF e Banco de Dados.
* **Firmware:** Coleta a versão atual e gera alertas de auditoria caso ocorra uma mudança/atualização.

### 🔗 Conectividade e VPN
* **IPSec Discovery:** Descoberta automática de túneis ativos e inativos.
* **VPN Status:** Monitoramento de túneis UP/DOWN e contagem de SAs (Security Associations).
* **IPSec Policies:** Alerta se houver alteração nas políticas de criptografia (Key Life, Algoritmos).
* **Interfaces de Rede:** Tráfego em tempo real (bps), Erros de entrada/saída, Descartes (Discards) e alertas de utilização acima de 80%.

### 🏗️ Alta Disponibilidade (HA)
* **Cluster Status:** Monitoramento do estado (Active/Passive/Faulty).
* **Failover:** Alerta de alta prioridade caso os firewalls troquem de papel no cluster.
* **Link de Sincronismo:** Monitoramento físico da porta de HA (Heartbeat).

### 🖥️ Recursos do Sistema
* **CPU:** Uso médio geral e monitoramento individual por **Core do Processador**.
* **Memória:** Uso de RAM e SWAP com gatilhos de performance.
* **Armazenamento:** Capacidade total e ocupação de disco.
* **Saúde:** Uptime do dispositivo e alertas de reinicialização recente.

## 🚀 Configuração
1. **Sophos:** Habilite o **SNMP v2c** em `Administration > SNMP`.
2. **Sophos:** Libere o acesso SNMP na zona correspondente (geralmente LAN ou Local) em `Administration > Device Access`.
3. **Zabbix:** Importe o arquivo `.yaml`.
4. **Zabbix:** No Host do Firewall, configure a macro `{$SNMP_COMMUNITY}` com a sua comunidade definida no Sophos.

## 🤝 Contribuições e Melhorias
Este template foi desenvolvido com foco em cenários de produção reais, mas sempre há espaço para evolução!

Sinta-se à vontade para:

Abrir uma Issue se encontrar algum erro de OID ou comportamento inesperado.
Enviar um Pull Request com novos protótipos de itens, gatilhos ou dashboards.
Sugerir melhorias na documentação.
Sua contribuição é muito bem-vinda! 🚀

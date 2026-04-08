# 🚀 Zabbix Templates Collection

Repositório centralizado de templates otimizados para monitoramento de infraestrutura corporativa via Zabbix.

## 📁 Estrutura do Repositório

O monitoramento está organizado por fabricante/tecnologia para facilitar a localização:

* **/sophos**: Templates para Firewalls Sophos (XG, XGS).
* *(Em breve)* Outros templates de rede e servidores.

## 🛠️ Como utilizar
1. Faça o download do arquivo `.yaml` ou `.xml` desejado.
2. No seu painel Zabbix, vá em **Data collection > Templates**.
3. Clique em **Import** e selecione o arquivo.
4. Certifique-se de configurar as **Macros** (como `{$SNMP_COMMUNITY}`) no host ou template.

---
**Mantido por [Rodrigo Miranda]** *Focado em infraestrutura, segurança e alta disponibilidade.*

## 🤝 Contribuições e Melhorias
Este template foi desenvolvido com foco em cenários de produção reais, mas sempre há espaço para evolução! 

Sinta-se à vontade para:
* Abrir uma **Issue** se encontrar algum erro de OID ou comportamento inesperado.
* Enviar um **Pull Request** com novos protótipos de itens, gatilhos ou dashboards.
* Sugerir melhorias na documentação.

**Sua contribuição é muito bem-vinda!** 🚀

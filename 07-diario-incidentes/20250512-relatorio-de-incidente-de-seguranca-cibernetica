# Relatório de Incidente de Segurança Cibernética

## Seção 1: Identificação do Tipo de Ataque

**Incidente:** Interrupção de rede

Uma possível explicação para a mensagem de erro _"tempo limite de conexão"_ apresentada pelo site é um ataque de negação de serviço (DoS).

**Evidência nos registros:**
Os registros coletados por meio de um sniffer no servidor mostram um grande número de solicitações do tipo **SYN** originadas de um único endereço IP.

**Conclusão preliminar:**
Esse padrão de tráfego é típico de um **ataque DoS**, mais especificamente uma variação chamada **SYN Flood**, que visa sobrecarregar os recursos do servidor.

---

## Seção 2: Como o Ataque Afeta o Funcionamento do Site

Quando um visitante tenta acessar o site, ocorre um processo conhecido como **handshake triplo** do protocolo TCP, que estabelece a conexão entre cliente e servidor. Esse processo é composto pelas seguintes etapas:

1. **SYN** – O cliente envia um pacote solicitando a conexão.
2. **SYN/ACK** – O servidor responde confirmando a solicitação e reservando recursos.
3. **ACK** – O cliente envia um pacote final para confirmar a conexão.

No caso de um ataque **SYN Flood**, um agente malicioso envia um número excessivo de pacotes SYN sem nunca concluir o handshake. Isso faz com que:

- O servidor reserve recursos para conexões que nunca serão finalizadas;
- Com o tempo, o servidor atinja sua capacidade máxima de conexões pendentes;
- Solicitações legítimas não possam ser processadas, resultando em falhas e mensagens de _timeout_ para os usuários reais.

**Impacto observado:**
Os logs indicam que o servidor foi alvo de um ataque DoS, resultando em sobrecarga e indisponibilidade do serviço para requisições legítimas.

---

## Conclusão

A análise aponta fortemente para um ataque do tipo **SYN Flood DoS** como causa da interrupção no serviço. Recomenda-se implementar medidas de mitigação, como:

- Filtragem de IPs suspeitos;
- Utilização de firewalls com capacidade de inspeção de pacotes;
- Aplicação de limites de conexão por origem (rate limiting);
- Adoção de mecanismos como o SYN Cookies.
# Relatório de Incidente de Segurança Cibernética

## Exemplo de Atividade: Aplicar Técnicas de Proteção ao Sistema Operacional

---

## Seção 1: Protocolo de Rede Envolvido

O protocolo identificado neste incidente foi o **HTTP (Hypertext Transfer Protocol)**. Isso foi confirmado pela natureza do problema — o acesso ao servidor web `yummyrecipesforme.com` — que naturalmente envolve tráfego HTTP.

Além disso, ao utilizar a ferramenta `tcpdump` para capturar pacotes de rede durante o acesso ao site, foi observado que o tráfego era transmitido via HTTP, incluindo o transporte de um arquivo malicioso baixado pelos usuários. Esse comportamento foi registrado no log gerado pelo `tcpdump`.

---

## Seção 2: Documentação do Incidente

**Descrição do problema:**

Vários usuários relataram ao helpdesk que, ao acessar o site `yummyrecipesforme.com`, foram induzidos a baixar e executar um arquivo que supostamente oferecia acesso a receitas exclusivas. Após a execução, seus computadores passaram a apresentar lentidão e comportamento anormal.

Simultaneamente, o proprietário do site relatou não conseguir acessar sua conta de administrador — aparentemente bloqueada por terceiros.

**Ação do analista:**

Um analista de segurança cibernética utilizou um ambiente isolado (sandbox) para investigar o incidente de forma segura. Durante o processo:

- A ferramenta `tcpdump` foi usada para capturar o tráfego de rede.
- O analista visitou o site, fez o download do arquivo suspeito e o executou.
- Após a execução, o navegador foi redirecionado automaticamente para um domínio falso: `greatrecipesforme.com`.

**Análise do tráfego:**

A inspeção dos pacotes revelou que, após o primeiro contato via HTTP com `yummyrecipesforme.com`, houve uma mudança abrupta no tráfego, direcionando os dados para um novo endereço IP associado ao site falso `greatrecipesforme.com`.

**Análise técnica:**

Um analista sênior revisou o código-fonte dos sites envolvidos e o arquivo baixado. Foi identificado que o site original havia sido comprometido com um código malicioso, que induzia o download de um falso “atualizador de navegador”. O invasor, provavelmente usando um ataque de **força bruta**, obteve acesso à conta de administrador, alterou as credenciais e inseriu o código malicioso.

A execução do arquivo comprometeu os dispositivos dos usuários finais, demonstrando a eficácia do ataque e a necessidade urgente de remediação.

---

## Seção 3: Recomendações para Prevenção de Ataques de Força Bruta

Para prevenir futuros ataques semelhantes, a equipe de segurança recomenda as seguintes medidas:

1. **Bloqueio do uso de senhas anteriores:** Impedir que senhas antigas ou padrão sejam reutilizadas, especialmente durante redefinições de senha.

2. **Política de expiração de senhas:** Forçar trocas periódicas de senha. Isso limita o tempo útil de uma credencial comprometida.

3. **Autenticação de dois fatores (2FA):** Implementar 2FA para todas as contas administrativas. Esse recurso exige a verificação por meio de um código único (OTP) enviado ao e-mail ou telefone do usuário, além da senha tradicional.

Com essas medidas, mesmo que uma senha seja descoberta por um agente malicioso, o acesso ao sistema continuará restrito devido à autenticação adicional.

---
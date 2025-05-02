# Relatório de Auditoria de Segurança - Botium Toys

**Auditor:** José Eduardo Bonifácio Dantas  
**Data:** 02 de Abril de 2025  
**Objetivo:** Avaliar os controles técnicos e as práticas de conformidade da empresa Botium Toys, com foco na proteção de dados, integridade da informação e aderência a normas de segurança reconhecidas (como PCI DSS, RGPD e SOC 2).

---

## ✅ Lista de Verificação de Controles

| Controle                                        | Implementado? |
|------------------------------------------------|---------------|
| Menor privilégio                               | ❌ Não        |
| Planos de recuperação de desastres             | ❌ Não        |
| Políticas de senha                             | ✅ Sim        |
| Separação de funções                           | ❌ Não        |
| Firewall                                        | ✅ Sim        |
| Sistema de detecção de intrusão (IDS)          | ❌ Não        |
| Cópias de segurança                            | ✅ Sim        |
| Software antivírus                             | ✅ Sim        |
| Monitoramento de sistemas legados              | ❌ Não        |
| Criptografia                                   | ❌ Não        |
| Sistema de gerenciamento de senha              | ✅ Sim        |
| Fechaduras físicas (escritório, estoque etc.)  | ✅ Sim        |
| Vigilância por CCTV                            | ✅ Sim        |
| Sistemas de detecção/prevenção de incêndio     | ✅ Sim        |

---

## ✅ Lista de Verificação de Conformidade

### Padrão PCI DSS

| Prática recomendada                                                       | Implementado? |
|---------------------------------------------------------------------------|---------------|
| Somente usuários autorizados acessam dados de cartões                    | ✅ Sim        |
| Ambiente seguro para armazenamento e transmissão                         | ✅ Sim        |
| Uso de criptografia para dados sensíveis                                 | ❌ Não        |
| Política segura de senhas                                                | ✅ Sim        |

### Regulamento Geral de Proteção de Dados (RGPD)

| Prática recomendada                                                       | Implementado? |
|---------------------------------------------------------------------------|---------------|
| Dados de clientes da UE são protegidos                                   | ✅ Sim        |
| Plano de notificação em até 72h após violação                            | ✅ Sim        |
| Classificação e inventário de dados                                      | ❌ Não        |
| Políticas e processos de privacidade documentados                        | ❌ Não        |

### Controles de Sistema e Organização (SOC 1 / SOC 2)

| Prática recomendada                                                       | Implementado? |
|---------------------------------------------------------------------------|---------------|
| Políticas de acesso de usuários estabelecidas                            | ✅ Sim        |
| Proteção de dados sensíveis (PII/SPII)                                    | ✅ Sim        |
| Garantia de integridade dos dados                                         | ❌ Não        |
| Disponibilidade de dados a usuários autorizados                          | ✅ Sim        |

---

## 📌 Recomendações

Com base nos controles e nas práticas avaliadas, recomenda-se à Botium Toys as seguintes ações:

1. **Implementar política de menor privilégio:** Reduz o risco de movimentação lateral em caso de comprometimento.
2. **Desenvolver um plano formal de recuperação de desastres:** Garante continuidade em cenários críticos.
3. **Estabelecer separação de funções (SoD):** Evita conflitos de interesse e aumenta o controle interno.
4. **Implementar IDS ou IPS:** Detecta atividades anômalas e responde a incidentes rapidamente.
5. **Aplicar criptografia a dados sensíveis e transações:** Melhora a proteção de dados em repouso e em trânsito.
6. **Criar plano de classificação e inventário de dados:** Essencial para conformidade com a LGPD e para priorização de segurança.
7. **Documentar processos de privacidade e segurança da informação:** Fortalece a governança e prepara para auditorias externas.
8. **Monitorar sistemas legados regularmente:** Corrige falhas, melhora desempenho e reduz riscos não tratados.

Essas ações devem ser priorizadas conforme análise de risco e viabilidade técnica.

---

**Documento elaborado para fins acadêmicos e profissionais no contexto do portfólio de Segurança da Informação.**

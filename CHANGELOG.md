# CHANGELOG - SISTEMA MMN

## [7.1] - 01/05/2026

### CORREÇÕES E MELHORIAS

#### Corrigido
- **Login:** Agora o sistema seleciona a cota Start Ativa (em vez de qualquer cota) ao fazer login

#### Adicionado
- **Nova função `rede_completa`:** retorna todos os membros da rede (independente do status), com informações de indicador, nível e posição
- **Nova seção na Área do Participante:** 'Membros Inativos/Atrasados/Pendentes' mostrando TODA a rede inativa
- **Informação do patrocinador:** exibe quem indicou cada membro inativo
- **Critério `data_pagamento`:** diferencia inativos reais (já ativaram) de cadastros nunca pagos
- **Backup completo no Supabase:** script com verificação de existência de tabelas e sufixo de data para manter histórico

### DECISÕES DE PROJETO REGISTRADAS (V7.1)
- Login prioriza cota Start Ativa para ser a raiz da rede
- `testar_rede` mantida para árvore de ativos; `rede_completa` para inativos/atrasados/pendentes
- Inativos/atrasados/pendentes mostrados com indicador, nível e posição

## [7.0] - 28/04/2026

### CONSOLIDAÇÃO FINAL + VERSÃO WEB

#### Adicionado
- **VERSÃO WEB (ÁREA DO PARTICIPANTE)** - implementada em 28/04/2026
  - Link: https://mutualidade-code.github.io/comunidade-business/
  - Autenticação: CPF + código (MMN-XXXX-XXXX)
  - Dashboard com cards de saldo e indicadores
  - Extrato Consolidado com 11 colunas
  - Árvore da rede expansível (clique para expandir/contrair)
  - Solicitação de saque com status 'Em processamento'
  - Painel administrativo: aprovar saques, gerar códigos, parâmetros pioneiro, log
  - Parâmetros de Pioneiro editáveis via interface (E3:G7)
  - Contador de pioneiros = 7 (importado do Excel)
- Regra de Substituição de cota Inativa sem rede ativa abaixo
- Regra de Detecção de ciclo na árvore (alerta, não corrige)
- Regra de Plano inconsistente (superior ativo sem inferior) - alerta grave
- Opção 16: Mesclar formatação com preservação de mesclagens (células E3:G3)
- Padronização de fontes: cabeçalhos = 14, negrito, branco sobre #366092

#### Decisões Registradas (Web)
- Contagem de indicados: por COTA (não por pessoa)
- Login simplificado: CPF + código (sem email)
- Lançamentos: via Excel (Web apenas consulta)

#### Pendências para versões futuras
- Lançamentos na Web (Fase 2)
- Senha mestra na Web
- Posicionamento na matriz via Web
- Saque_Acum_Livre (acúmulo mensal)

### Status
- Nenhuma pendência no escopo atual
- Documentação 100% alinhada com o sistema (Excel + Web)

---

**Versão atual:** 7.1
**Data:** 01/05/2026
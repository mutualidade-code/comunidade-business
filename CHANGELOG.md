# CHANGELOG - SISTEMA MAP

## [7.2] - 04/05/2026

### CORREÇÕES CRÍTICAS

#### Corrigido
- **Tamanho da Rede Ativa:** função `calcular_tamanho_rede_ativa_completa` criada
  - Agora conta todas as cotas ativas (própria pessoa + rede)
  - Respeita regra de acumulação de planos
  - Exemplo: P001 agora mostra 16 (antes 5)
- **Reserva Mensalidade:** ajuste no cálculo
  - Exibição: limite de 1 mês (R$ 35,00 para P002)
  - Acumulação: permite até 2 meses internamente
- **Disponível para Saque:** transferência dinâmica implementada
  - Saldo_Bruto agora é transferido para Saque_Mês_Livre em tempo real
  - Exemplo: P002 agora mostra R$ 68,50 (antes R$ 0,00)

#### Adicionado
- Função `verifica_acumulacao(id)` - valida hierarquia de planos
- Função `calcular_tamanho_rede_ativa_completa(id)` - cálculo correto da rede
- Função `calcular_saldo_consolidado(pessoa)` atualizada com transferência dinâmica
- Conceito de Saldo_Bruto como acumulador temporário (sempre zera no fim do mês)
- Conceito de Depósito Reservado (documentado, pendente implementação)

### PENDENTES PARA PRÓXIMAS VERSÕES

- Lançamentos na Web (Fase 2)
- Posicionamento na matriz via Web
- Depósito Reservado (implementação)
- Transferência entre participantes

---

## [7.1] - 01/05/2026

### CORREÇÕES E MELHORIAS

- **Login:** seleciona a cota Start Ativa
- **Nova função `rede_completa`:** retorna todos os membros da rede
- **Seção de inativos:** mostra toda a rede inativa
- **Backup no Supabase:** script completo com sufixo de data

---

**Versão atual:** 7.2
**Data:** 04/05/2026
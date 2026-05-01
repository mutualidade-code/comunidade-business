# SISTEMA MMN - MATRIZ FORÇADA 3x10 COM DERRAMAMENTO

## Comunidade Business - Versão 7.1

### Acesso Web (Área do Participante)

Link: https://mutualidade-code.github.io/comunidade-business/

### Requisitos (Script Local)

- Python 3.8+
- pandas
- openpyxl
- python-docx

### Instalação

```bash
pip install pandas openpyxl python-docx
```

### Documentação

Dois formatos de documentação estão disponíveis:

- **Formato DOCX:** `Documento_Definicoes_V7.1.docx` (completo, com formatação, cores e seção Web)
- **Formato TXT:** `Documento_Definicoes_V7.1_20260501.txt` (resumido)

### Principais Regras

- **BI:** Pago apenas uma vez, na ativação da cota
- **BR:** Distribuído para níveis ATIVOS acima (até 10 níveis)
- **Limite de saque:** Valor do Título + Adicional Pioneiro
- **Pioneiro:** Período promocional (NÃO é herdado)
- **Substituição:** Cota Inativa sem rede ativa abaixo é substituída
- **Ciclo na árvore:** Detectado e alertado, NÃO corrigido
- **Descontos:** Apenas UM campo por linha (VALOR, CUPOM ou PARCERIA)

### Correções Versão 7.1 (01/05/2026)

- **Login corrigido:** seleciona a cota Start Ativa (raiz da rede)
- **Nova função `rede_completa`:** retorna todos os membros da rede (todos status)
- **Seção de inativos:** mostra toda a rede inativa com indicador, nível e posição
- **Backup no Supabase:** script completo com sufixo de data

---

**Versão:** 7.1
**Data:** 01/05/2026
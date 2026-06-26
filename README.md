# Análise de Inadimplência de Cartão de Crédito — foco em Cobrança

**Pergunta de negócio:** que perfil de cliente tem maior risco de calote no próximo mês,
para a área de cobrança priorizar quem abordar primeiro?

**Contexto:** base pública de uma operadora de cartão (UCI — *Default of Credit Card Clients*),
30.000 clientes, com 6 meses de histórico de pagamento, fatura e valor pago. Alvo: o cliente
deu calote no mês seguinte (sim/não). Taxa-base de inadimplência: **22,1%**.

## Entregáveis
1. **Notebook Python** (`notebooks/`) — limpeza (pandas), exploração do perfil de risco (seaborn)
   e um modelo simples de probabilidade de calote (regressão logística).
2. **Relatório Excel** (`relatorio/`) — tabela dinâmica de taxa de calote por faixa de risco,
   para entregar à gestão/cobrança.

## Principais achados
> _(preencher conforme a análise avança)_

## Dicionário de dados
| Coluna | Significado |
|---|---|
| `LIMIT_BAL` | Limite de crédito (NT$) |
| `SEX` | 1 = masculino, 2 = feminino |
| `EDUCATION` | 1 = pós, 2 = universidade, 3 = ensino médio, 4 = outros (0/5/6 = desconhecido) |
| `MARRIAGE` | 1 = casado, 2 = solteiro, 3 = outros |
| `AGE` | Idade (anos) |
| `PAY_0`,`PAY_2`..`PAY_6` | Status de pagamento dos últimos 6 meses. `-1` = pago em dia; `1` = 1 mês de atraso; `2` = 2 meses... |
| `BILL_AMT1`..`6` | Valor da fatura nos 6 meses |
| `PAY_AMT1`..`6` | Valor pago nos 6 meses |
| `default payment next month` | **Alvo:** 1 = deu calote no mês seguinte, 0 = não |

## Como rodar
```bash
conda activate ds
jupyter lab
```

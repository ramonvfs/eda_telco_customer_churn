# Análise Exploratória: Telco Customer Churn

Análise exploratória do dataset [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (IBM) para entender **quem** cancela o serviço de uma operadora de telecomunicações e **quando**.

## Perguntas

1. Qual a proporção de clientes que cancelaram (churn)?
2. Em quanto tempo, em média, eles cancelam?
3. Quais variáveis têm mais relação com o churn?
4. Qual o perfil do cliente que mais cancela?

## Dados

7043 clientes e 21 colunas: dados demográficos (gênero, idoso, parceiro, dependentes), tempo como cliente (`tenure`), serviços contratados (telefone, internet, segurança, suporte, streaming), contrato, forma de pagamento, cobranças mensal e total, e a variável alvo `Churn`.

O arquivo está em `data/WA_Fn-UseC_-Telco-Customer-Churn.csv`.

## Principais resultados

- **Taxa de churn: 26,5%** (1869 de 7043 clientes).
- **Tempo até cancelar:** quem cancelou ficou em média 18 meses (mediana de 10), contra 38 meses de quem continua; 55% dos cancelamentos acontecem no primeiro ano.
- **Variáveis mais associadas ao churn:**

| Variável | Maior churn | Menor churn |
|---|---|---|
| Contrato | Mensal: 42,7% | Dois anos: 2,8% |
| Pagamento | Boleto eletrônico: 45,3% | Cartão automático: 15,2% |
| Internet | Fibra óptica: 41,9% | Sem internet: 7,4% |
| Segurança online | Não tem: 41,8% | Tem: 14,6% |
| Idoso | Sim: 41,7% | Não: 23,6% |
| Gênero | Feminino: 26,9% | Masculino: 26,2% |

- **Perfil de maior risco:** cliente recente, com contrato mensal, internet por fibra, mensalidade alta, pagamento por boleto eletrônico e sem serviços adicionais de segurança ou suporte.

## Como executar

```bash
pip install -r requirements.txt
jupyter notebook eda_telco_customer_churn.ipynb
```

## Estrutura

```
.
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── eda_telco_customer_churn.ipynb
└── requirements.txt
```

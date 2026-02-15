# Projeto Final de Machine Learning - Titanic (OpenML)

Notebook principal: `projeto_final_openml.ipynb`

## Objetivo
Projeto de classificacao binaria para prever `survived` no dataset Titanic (OpenML `data_id=40945`), cobrindo pipeline completo de ML: exploracao, limpeza, comparacao de hipoteses, tuning, avaliacao final e conclusao.

## Estrutura de dados
- `data/raw/openml_titanic_40945.csv`: cache local dos dados brutos do OpenML.
- `data/processed/titanic_clean.csv`: dataset limpo para reutilizacao.

O notebook segue estas regras de reproducao:
- Se existir `data/raw/openml_titanic_40945.csv`, carrega localmente.
- Se nao existir, faz `fetch_openml(...)` e grava esse ficheiro em `data/raw/`.
- Se existir `data/processed/titanic_clean.csv`, reutiliza sem repetir limpeza.
- Se nao existir, limpa/prepara e exporta para `data/processed/titanic_clean.csv`.

## Requisitos
- Python 3.10+
- Dependencias em `requirements.txt`

## Como executar
1. Criar ambiente virtual:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Abrir notebook:
   ```bash
   jupyter notebook projeto_final_openml.ipynb
   ```
4. No Jupyter, executar `Restart Kernel`, `Clear All Outputs` e `Run All`.

## Execucao nao interativa (opcional)
```bash
jupyter nbconvert --to notebook --execute --inplace projeto_final_openml.ipynb
```

## Entregaveis principais
- Notebook com outputs finais (metricas + graficos).
- Comparacao de 3 hipoteses/modelos.
- Treino aprofundado com `Pipeline` + `RandomizedSearchCV` + `StratifiedKFold`.
- Avaliacao final com accuracy, precision, recall, F1, confusion matrix e ROC-AUC.
- Secao final de conclusao e checklist de entrega.

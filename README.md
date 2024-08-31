# atmaCup17_20thSolution
- solution write up is [here](https://www.guruguru.science/competitions/24/discussions/b57086c1-e61d-4c96-87d0-52eb2fe59dfd/)

| model | description |CV | Public LB |
| ---- | ---- | ---- | ---- |
| microsoft/deberta-v3-large | label: [recommended (CrossEntropy), rating (MSE)], CLS | 0.96755 | 0.9699 |
| microsoft/deberta-v3-base | label: recommended (CrossEntropy), MeanPooling |0.96859 |  |
| intfloat/e5-mistral-7b-instruct (exp021_llm_svc) | LLM で embedding 取得 → SVC で2値分類  |0.9648 | 0.9617
| microsoft/deberta-v3-large | label: [recommended (CrossEntropy), rating (MSE)], CLS, freeze(6) |0.9717| 0.9729 |
| microsoft/deberta-v3-large (exp025_deberta_auxiliary_loss) | label: [recommended (CrossEntropy), rating (MSE)], MeanPooling, freeze(2), 改行トークン |0.9725 | 0.9720 |
| ensemble (ensemble.ipynb) | rank average | 0.9741 | 0.9709 |

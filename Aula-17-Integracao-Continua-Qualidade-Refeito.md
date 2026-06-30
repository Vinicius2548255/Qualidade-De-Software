# Aula 17 – Integração Contínua, Qualidade Automatizada, Métricas e Gestão de Defeitos

## Integrantes
- Vinicius dias soares


---

# 1. Objetivo
Esta atividade apresenta a aplicação de Integração Contínua (CI), testes automatizados e métricas de qualidade em um projeto fictício do LocalEats.

# 2. Repositório
| Item | Descrição |
|---|---|
| Projeto | localeats-ci-qualidade |
| Finalidade | Automatizar testes e validações do código |

## Estrutura
```text
localeats-ci-qualidade/
├── src/
├── tests/
├── .github/workflows/ci.yml
├── requirements.txt
└── README.md
```

# 3. Funcionalidade
Foi implementada uma rotina para calcular automaticamente o valor total de um pedido, reduzindo erros manuais.

## Teste Unitário
```python
from order import calculate_total

def test_calculate_total():
    assert calculate_total([15,25,10]) == 50
```

# 4. Pipeline CI
Sempre que ocorre um **push** ou **pull request**, o GitHub Actions:
1. Baixa o projeto;
2. Instala dependências;
3. Executa os testes;
4. Informa o resultado.

```yaml
name: Continuous Integration
on: [push, pull_request]

jobs:
  tests:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install pytest
      - run: pytest
```

# 5. Indicadores
| Indicador | Resultado |
|---|---:|
| Testes executados | 1 |
| Testes aprovados | 1 |
| Testes reprovados | 0 |
| Status | Sucesso |

# 6. Registro de Defeito
Foi simulado um erro no cálculo do total. O teste automatizado identificou a falha imediatamente. Após a correção do código, todos os testes foram aprovados novamente.

# 7. Conclusão
A Integração Contínua e os testes automatizados aumentam a confiabilidade do software, reduzem falhas em produção e tornam o processo de desenvolvimento mais seguro e eficiente.

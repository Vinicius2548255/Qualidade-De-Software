# 🧩 Atividade PBL – Aula 12
# BDD e Automação Orientada a Comportamento – LocalEats

---

## 👥 Integrante(s)

- Vinicius Dias Soares

---

# 1. Fluxo Escolhido

## Funcionalidade
**Histórico de Pedidos**

### Objetivo
Validar se os pedidos realizados pelos usuários são apresentados corretamente no sistema LocalEats, garantindo a exibição adequada das informações e dos valores das transações.

### Importância do Fluxo
O histórico de pedidos é uma funcionalidade relevante para a experiência do usuário, permitindo acompanhar compras anteriores, conferir valores pagos e consultar informações sobre pedidos já concluídos.

---

# 2. Cenários BDD

## Arquivo de Cenários

```text
features/historico_pedidos.feature
```

## Cenários em Gherkin

```gherkin
Feature: Histórico de pedidos

  Scenario: Visualizar pedidos realizados
    Given que o usuário acessa a página de pedidos
    When visualizar o histórico de transações
    Then o sistema deve exibir os pedidos cadastrados

  Scenario: Validar valor total do pedido
    Given que o usuário acessa a página de pedidos
    When visualizar um pedido realizado
    Then o sistema deve exibir o valor total do pedido
```

### Benefícios da Utilização do BDD

- Facilita a compreensão dos requisitos;
- Aproxima equipes técnicas e de negócio;
- Documenta o comportamento esperado do sistema;
- Melhora a comunicação durante o desenvolvimento.

---

# 3. Automação com Pytest-BDD e Playwright

## Estrutura do Projeto

```text
projeto/
│
├── features/
│   └── historico_pedidos.feature
│
├── tests/
│   └── test_historico_pedidos.py
│
├── evidencias/
│
└── README.md
```

## Objetivo da Automação

Automatizar os cenários descritos em linguagem natural utilizando pytest-bdd e Playwright, garantindo que o comportamento especificado seja validado automaticamente.

### Principais Validações

- Acesso à página de pedidos;
- Exibição do histórico de transações;
- Visualização de pedidos realizados;
- Verificação dos valores apresentados pelo sistema.

---

# 4. Execução dos Testes

## Comando Executado

```bash
pytest -v
```

## Resultado Obtido

```text
=================== test session starts ===================

2 passed in 5.32s

==========================================================
```

### Interpretação

Todos os cenários executados foram aprovados, indicando que o comportamento esperado estava funcionando corretamente durante a execução dos testes.

---

# 5. Evidências

## Evidência da Execução

```text
evidencias/
  execucao-testes.png
```

## Evidência da Aplicação

```text
evidencias/
  historico-pedidos.png
```

### Observação

As evidências visuais auxiliam na comprovação dos resultados obtidos e facilitam futuras auditorias e análises dos testes realizados.

---

# 6. Análise Crítica

### O cenário ficou compreensível?

Sim. A estrutura Given-When-Then torna a leitura intuitiva e facilita o entendimento do comportamento esperado.

### O BDD contribuiu para a compreensão dos requisitos?

Sim. Os cenários descrevem claramente as funcionalidades e podem ser entendidos tanto por desenvolvedores quanto por pessoas da área de negócio.

### O teste é totalmente robusto?

Não completamente. Alguns seletores dependem de textos presentes na interface e podem ser afetados por alterações visuais.

### Principais desafios encontrados

- Identificação de seletores confiáveis;
- Organização dos steps do BDD;
- Integração entre Playwright e pytest-bdd;
- Manutenção dos testes conforme a evolução da interface.

### Dependência da Interface

Existe dependência parcial da interface gráfica, principalmente em validações baseadas em textos visíveis na tela.

---

# 7. Reflexão Final

### O BDD melhora a comunicação da equipe?

Sim. O comportamento do sistema passa a ser descrito em uma linguagem acessível para todos os envolvidos no projeto.

### Todo teste deve utilizar BDD?

Não. O BDD é mais indicado para funcionalidades importantes do negócio e para cenários que exigem documentação clara do comportamento esperado.

### Quando vale a pena utilizar BDD?

- Em fluxos críticos;
- Em projetos colaborativos;
- Quando há necessidade de alinhar requisitos entre diferentes áreas;
- Em funcionalidades que exigem documentação viva.

### Contribuição para o Projeto LocalEats

A utilização do BDD ajudou a transformar requisitos em cenários executáveis, promovendo maior organização, clareza e rastreabilidade dos testes automatizados.

---

# 📦 Repositório GitHub

Substituir pelo link real do repositório do grupo:

```text
https://github.com/seu-grupo/local-eats
```

---

# ✅ Conclusão

A atividade permitiu compreender a aplicação prática do BDD no projeto LocalEats, demonstrando como requisitos podem ser convertidos em cenários claros e posteriormente automatizados.

Além disso, foi possível explorar a integração entre pytest-bdd e Playwright, reforçando a importância da automação de testes, da documentação de comportamento e da manutenção contínua das aplicações modernas.

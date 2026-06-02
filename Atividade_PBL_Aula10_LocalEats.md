# 🧩 Atividade PBL – Aula 10
# Testes Funcionais Automatizados – LocalEats

---

## 👥 Integrante(s)

- Vinicius Dias Soares

---

## 1. Fluxo Funcional Selecionado

### Fluxo Escolhido
**Login de Usuário**

### Descrição
O fluxo de login do sistema LocalEats permite que usuários autenticados acessem funcionalidades exclusivas da plataforma, como avaliações, gerenciamento de perfil e interação com estabelecimentos cadastrados.

### Importância do Fluxo
A autenticação é uma das funcionalidades mais importantes da aplicação, pois garante a segurança dos dados e controla o acesso às áreas restritas do sistema.

---

## 2. Geração Inicial do Teste com Codegen

### Comando Utilizado

```bash
playwright codegen https://local-eats-unisenac.vercel.app/
```

### Objetivo

Utilizar o Codegen do Playwright para registrar automaticamente as ações realizadas no navegador e gerar um teste inicial para o fluxo de login.

### Observações

- O Codegen acelerou a criação do primeiro teste;
- Foram gerados seletores automaticamente;
- O código precisou ser ajustado para melhorar a organização e manutenção.

---

## 3. Implementação do Teste Automatizado com Pytest

### O que o teste realiza

1. Acessa a aplicação LocalEats;
2. Navega até a tela de login;
3. Preenche os campos de autenticação;
4. Envia as credenciais do usuário;
5. Verifica se o login foi realizado com sucesso.

### Benefícios

- Validação automática do fluxo principal;
- Redução de testes repetitivos manuais;
- Maior confiabilidade durante atualizações do sistema.

---

## 4. Refatoração com Page Object Model (POM)

### Objetivo da Refatoração

Aplicar o padrão Page Object Model para separar a lógica de interação com a interface da lógica de teste.

### Melhorias Obtidas

- Código mais limpo;
- Facilidade de manutenção;
- Reutilização de componentes;
- Melhor organização da estrutura do projeto.

---

## 5. Execução dos Testes

### Comando

```bash
pytest
```

### Resultado Esperado

| Métrica | Resultado |
|----------|------------|
| Total de testes | 1 |
| Testes aprovados | 1 |
| Testes falharam | 0 |

### Evidência

Inserir captura de tela da execução ou relatório gerado pelo Pytest.

---

## 6. Análise Crítica

Durante o desenvolvimento dos testes foi possível observar que:

- Mudanças na interface podem quebrar seletores;
- Seletores baseados apenas em texto são mais frágeis;
- Identificadores únicos tornam os testes mais robustos;
- A manutenção dos testes é fundamental para garantir sua eficiência.

---

## 7. Reflexão

Os testes funcionais automatizados ajudam a identificar problemas rapidamente e aumentam a qualidade do software.

Apesar disso, eles não substituem completamente os testes manuais, sendo mais eficazes quando utilizados em conjunto para validar fluxos críticos da aplicação.

---

# 💡 Conclusão

A utilização do Playwright e do Pytest no projeto LocalEats permitiu automatizar a validação de funcionalidades essenciais da aplicação. A adoção do padrão POM tornou o código mais organizado e preparado para futuras expansões, contribuindo para a qualidade e confiabilidade do sistema.

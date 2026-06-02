# 🏫 Sistema de Gestão Escolar - Intelectos

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Repo Size](https://img.shields.io/github/repo-size/seu-usuario/seu-repositorio)

Este é um sistema em terminal desenvolvido em Python para o **Ensino Fundamental 1** da instituição **Intelectos**. O script automatiza o gerenciamento de notas bimestrais, controle de assiduidade (frequência) e determina a situação final do aluno com base nas regras pedagógicas da escola.

---

## 🚀 Funcionalidades

* **Cadastro por Disciplina:** Registro do nome do aluno e da matéria avaliada.
* **Validação de Entradas:** Bloqueia notas ou frequências que estejam fora dos limites permitidos, evitando erros de digitação.
* **Cálculo de Frequência Automático:** Converte o número de dias presentes em taxa percentual.
* **Fechamento de Notas:** Consolida as notas das 4 etapas letivas (bimestres).
* **Painel de Resultados:** Exibe um relatório final formatado com o status de todos os alunos cadastrados na sessão.

---

## 📋 Regras de Negócio & Critérios Pedagógicos

### 1. Composição da Nota Bimestral
Cada um dos 4 bimestres possui uma nota máxima de **10.0 pontos**, distribuída entre as seguintes atividades:

| Avaliação | Pontuação Máxima |
| :--- | :--- |
| 📓 Caderno | Até 2.5 |
| 📝 Teste | Até 1.5 |
| 👥 Trabalho em Grupo | Até 1.0 |
| ✍️ Prova | Até 5.0 |

### 2. Fórmulas de Cálculo

* **Porcentagem de Presença:** Baseada em um ano letivo padrão de 200 dias de classe.
$$\text{Porcentagem de Presença} = \left( \frac{\text{Presenças}}{200} \right) \times 100$$

* **Média Final:** Média aritmética simples dos 4 bimestres calculados.
$$\text{Média Final} = \frac{\text{B1} + \text{B2} + \text{B3} + \text{B4}}{4}$$

### 3. Critérios de Aprovação

O sistema avalia as condições do estudante na seguinte ordem de prioridade:

1. **Frequência Insuficiente:** Se a presença for **menor que 75%**, o aluno é automaticamente classificado como `Reprovado por falta`.
2. **Aprovação por Média:** Caso tenha a frequência necessária e a Média Final seja **maior ou igual a 6.0**, a situação será `Aprovado !!`.
3. **Recuperação:** Caso tenha a frequência necessária, mas a Média Final seja **menor que 6.0**, a situação será `Recuperação !!`.

---

## 🛠️ Como Executar o Projeto

### Pré-requisitos
Certifique-se de ter o [Python 3](https://www.python.org/downloads/) instalado no seu computador.

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)

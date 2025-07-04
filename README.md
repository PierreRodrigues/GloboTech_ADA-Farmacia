# ada_farmacia
# 🧪 Prog. Orientada a Objetos - Desafio Final

## 📋 Descrição do Trabalho

Este projeto tem como objetivo a implementação de uma aplicação para uma **Farmácia** que vende produtos por meio de **e-commerce**, utilizando os princípios da **Programação Orientada a Objetos (POO)** em Python.

---

## 🧠 Objetivo

Aplicar técnicas de orientação a objetos para estruturar o sistema de maneira modular, reutilizável e organizada. O trabalho poderá ser realizado **individualmente ou em grupo**, conforme definido pelo professor.

---

## 🚀 Funcionalidades

O sistema deve oferecer os seguintes serviços por **menu interativo no console**:

- ✅ **Cadastro de Clientes**:
  - Busca por CPF (sem pontuação).
- ✅ **Cadastro de Medicamentos**:
  - Busca por nome, fabricante ou descrição parcial.
  - Dois tipos: **Quimioterápicos** e **Fitoterápicos**.
  - Medicamentos Quimioterápicos devem indicar se precisam de **receita médica**.
- ✅ **Realização de Vendas**:
  - Somente para clientes cadastrados.
  - Aplicação automática de descontos:
    - 20% para **idosos** (acima de 65 anos).
    - 10% para **compras acima de R$ 150,00**.
    - **Descontos não cumulativos** (aplica-se o maior).
  - Alerta para medicamentos **controlados**, exigindo confirmação de receita.
- ✅ **Relatórios**:
  - Listagem de clientes ordenada por nome (A-Z).
  - Listagem de todos os medicamentos em ordem alfabética.
  - Listagem separada de medicamentos Quimioterápicos e Fitoterápicos.
  - **Relatório final ao sair do sistema**, incluindo:
    - Medicamento mais vendido (quantidade e valor total).
    - Total de clientes atendidos.
    - Quantidade e valor total de medicamentos Quimioterápicos vendidos.
    - Quantidade e valor total de medicamentos Fitoterápicos vendidos.

---

## 🧱 Estrutura de Classes (Obrigatórias)

### 👤 Classe Cliente
- CPF (identificador único)
- Nome
- Data de nascimento

### 💊 Classe MedicamentoQuimioterapico (herda de Medicamento)
- Nome
- Principal composto
- Laboratório
- Descrição
- Necessita receita (bool)

### 🌿 Classe MedicamentoFitoterapico (herda de Medicamento)
- Nome
- Principal composto
- Laboratório
- Descrição

### 🏭 Classe Laboratorio
- Nome
- Endereço
- Telefone para contato
- Cidade
- Estado

### 🧾 Classe Venda
- Data e hora da venda
- Produtos vendidos
- Cliente
- Valor total

---

## 🗃️ Armazenamento de Dados

- Os dados devem ser armazenados **em memória**, utilizando **listas** ou **dicionários**.
- **Não utilizar bancos de dados** nem arquivos externos, conforme orientação do módulo.

---

## 🖤 Componentes:
 - Pierre
 - Beatriz
 - Maria
 - Nando

## 🗂️ Estrutura Sugerida de Pastas

```bash
farmacia_poo/
├── main.py                          # Arquivo principal com menu e execução
├── entidades/
│   ├── __init__.py
│   ├── cliente.py                   # Classe Cliente
│   ├── laboratorio.py              # Classe Laboratório
│   ├── medicamento.py              # Classe base e subclasses MedicamentoQuimioterapico / Fitoterapico
│   └── venda.py                    # Classe Venda
├── relatorios/
│   ├── __init__.py
│   └── gerador_relatorios.py       # Geração de relatórios diversos
├── utils/
│   ├── __init__.py
│   └── validacoes.py               # Validações de entrada, CPF, data, etc.
└── README.md                       # Este arquivo


=== MENU FARMÁCIA ===
1. Cadastrar Cliente
2. Cadastrar Medicamento Quimioterápico
3. Cadastrar Medicamento Fitoterápico
4. Realizar Venda
5. Relatório de Clientes
6. Relatório de Medicamentos
7. Relatório de Medicamentos Quimioterápicos
8. Relatório de Medicamentos Fitoterápicos
9. Relatório de Estatísticas
0. Sair

# 🏋️‍♀️ Academia Corpo em Forma

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)


Este projeto foi desenvolvido como parte de um desafio prático da disciplina de Cloud Computing, com o objetivo de simular o gerenciamento de uma academia real em ambiente de nuvem.

A aplicação foi escrita em **Python**, hospedada em uma instância **EC2 da AWS**, com banco de dados relacional provisionado via **RDS**, e **deploy automatizado utilizando GitHub Actions**. Toda a infraestrutura foi provisionada com **Terraform**, seguindo o modelo **IaaS (Infrastructure as a Service)**.

---

## 🚀 Tecnologias Utilizadas

- 🐍 Python 3
- ☁️ Amazon EC2
- 🛢️ Amazon RDS (PostgreSQL)
- 📦 Terraform (IaC)
- 🔁 GitHub Actions (CI/CD)
- 🐧 Ubuntu Server

---

## ⚙️ Funcionalidades

- API simples de simulação de uma academia
- Deploy automatizado ao fazer push no repositório
- Provisionamento de infraestrutura completo com Terraform
- Banco de dados gerenciado integrado ao backend

---

## ☁️ Executando na AWS (EC2)

1. **Acesse sua instância EC2 via SSH:**

   ```bash
   ssh -i sua-chave.pem ubuntu@seu-endereco-ec2.amazonaws.com
   
   ```
   A aplicação será iniciada e estará disponível na porta configurada (por padrão, 8000).
Verifique se a porta está liberada nas regras de segurança da sua instância EC2.

---

## 🛠️ Infraestrutura com Terraform

A pasta infra/ contém todos os arquivos responsáveis por provisionar os recursos em nuvem:

```
infra/
├── main.tf
├── outputs.tf
├── variables.tf
└── terraform.tfstate
```
Esses arquivos definem a criação da instância EC2, do banco RDS, regras de segurança, e variáveis necessárias.

---

## 🔁 Integração Contínua (CI/CD)

O projeto utiliza GitHub Actions para automatizar o deploy. Ao realizar um push na branch principal, o workflow definido em:

```bash
.github/workflows/deploy.yml
```

irá automaticamente:

Conectar via SSH na EC2

Atualizar o código do projeto

Reiniciar a aplicação com o novo código

---

## 📂 Estrutura do Projeto

 ```bash
Academia-corpo-em-forma/
├── app/
│   ├── main.py
│   └── app.sh (script de execução opcional)
├── infra/
│   └── arquivos Terraform
├── .github/
│   └── workflows/deploy.yml
├── README.md
└── .gitignore
```
---

## ⚖️ Licença

Este projeto está licenciado sob a licença MIT.








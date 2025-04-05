Projeto: Academia Corpo em Forma 🏋️‍♀️☁️

 📖 Introdução
Este projeto faz parte da avaliação prática da disciplina de Cloud Computing. O grupo desenvolveu e implantou uma aplicação simples com o objetivo de simular o funcionamento de uma academia fictícia chamada "Corpo em Forma", utilizando serviços em nuvem (AWS EC2) e integração e entrega contínuas (CI/CD) através do GitHub Actions.
O modelo de serviço adotado foi o IaaS - Infrastructure as a Service, no qual provisionamos uma instância EC2 com infraestrutura definida como código via Terraform, permitindo a automação de todo o processo de criação do ambiente.


 🔧 Implementação Prática
 🚀 Tecnologias Utilizadas:

➡️AWS EC2 (Ubuntu 22.04)
➡️Terraform
➡️Python 3
➡️Shell Script
➡️GitHub Actions
➡️GitHub Secrets



🛠️Pipeline CI/CD (GitHub Actions):
➡️Faz o checkout do código da branch master.
➡️Cria o arquivo .pem a partir da variável secreta EC2_PRIVATE_KEY configurada nos Secrets do repositório.
➡️Conecta-se via SSH à instância EC2 usando o IP público.
➡️Atualiza os pacotes e instala Python e Git na máquina remota.
➡️Clona novamente o repositório.
➡️Executa a aplicação Python (main.py) automaticamente.



 🌐 Infraestrutura como Código (IaC)
    🌐 A infraestrutura foi criada utilizando o Terraform com os arquivos:
➡️main.tf: define os recursos da AWS, como a instância EC2.
➡️variables.tf: declara as variáveis utilizadas no projeto.
➡️outputs.tf: define os valores de saída como IP público.
➡️.terraform.lock.hcl: controle de dependências.
➡️.gitignore: protege arquivos sensíveis como terraform.tfstate.


 📁 Estrutura do Projeto

 Academia-corpo-em-forma/

 
├── .github/


│   └── workflows/


│       └── deploy.yml          → CI/CD com GitHub Actions


├── app/


│   ├── main.py                 → Código principal em Python


│   └── app.sh                  → Shell Script


├── infra/
│   ├── main.tf                 → Infraestrutura com Terraform


│   ├── variables.tf


│   ├── outputs.tf


│   └── terraform.tfstate       → Ignorado no git


├── .gitignore


├── README.md



✨ ✨ ✨ ✨ ✨  Conclusão ✨ ✨ ✨ ✨ ✨ 

Conclusão
Este projeto mostra, de forma prática e objetiva, como criar e gerenciar uma aplicação simples em nuvem com automação de deploy.

Com o uso de boas práticas e ferramentas modernas (como Terraform e GitHub Actions), foi possível implantar uma solução eficiente, reutilizável e com foco em agilidade.

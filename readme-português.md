# How to? - Módulos do Terraform

Este projeto consiste em um módulo com a estrutura para criação de um recurso da AWS juntamente com as configurações necessárias para executá-lo. Também permite que a configuração de cada um desses recursos seja melhor inserida em seu ambiente de forma rápida e simples, com o Terraform. Baseamo-nos no AWS Console e na documentação oficial https://registry.terraform.io/ para a criação deste módulo.

## Requisitos

- Instalar Terraform
- Instalar Visual Studio Code
- Instalar AWS CLI

## Links para download

- Terraform - https://www.terraform.io/downloads
- Visual Studio Code - https://code.visualstudio.com/?wt.mc_id=vscom_downloads
- AWS CLI - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html


## Deploy

Para fazer o deploy deste projeto você tem que clonar o repositório para a sua máquina. Na sua prompt de comando, execute:

```bash
  LINK
```
Abra este repositório com o Visual Studio Code e procure pelo arquivo `tfvars`.

Em `tfvars`insira os valores vazios com as informações desejadas do seu recurso à ser criado.

Quando tudo estiver preenchido, execute:
- (Você deve estar no mesmo diretório que os arquivos)

```bash
  terraform init
```

Para inicializar o backend

```bash
  terraform plan 
```

Para criar um `terraform.tfstate` e construir um state com os seus recursos. Você conseguirá ver todos os recursos e configurações que serão criadas, também.

## Resultado final

Você pode verificar se seus recursos foram criados da maneiroq que você desejou no aws console. Clique em https://aws.amazon.com/pt/console/ e veja os recursos criados e as configurações.

![Logo](https://fcortes.com.br/static/1fa99d7351e4f4c5b4313e933de57031/d9199/terraform_logo.png)

### Comandos extras

```bash
    terraform destroy
```

Destrói todos os recursos criados anteriormente.

```bash
    terraform validate
```

Verifica se você tem algo de errado com o seu código. (isto não evita ter problema com os valores da sua configuração)

```bash
    terraform plan -out (file name)
```

Cria um arquivo específico para o seu state
## Autores

- [TrendSolutions - Soluções Inteligentes](https://tsit.com.br/)
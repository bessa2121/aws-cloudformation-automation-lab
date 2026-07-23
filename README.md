# ☁️ AWS CloudFormation Automation Lab

![AWS](https://img.shields.io/badge/AWS-CloudFormation-orange)
![IaC](https://img.shields.io/badge/IaC-Infrastructure_as_Code-blue)
![YAML](https://img.shields.io/badge/YAML-Templates-red)
![Status](https://img.shields.io/badge/Status-Concluído-success)

Projeto desenvolvido durante o laboratório da DIO com foco em **automação de infraestrutura na AWS utilizando CloudFormation**, aplicando conceitos de **Infrastructure as Code (IaC), padronização, replicação de ambientes e segurança em nuvem**.

---

## 📑 Índice

* [Sobre o Projeto](#-sobre-o-projeto)
* [Objetivos](#-objetivos)
* [Arquitetura](#-arquitetura)
* [Tecnologias Utilizadas](#-tecnologias-utilizadas)
* [Estrutura do Repositório](#-estrutura-do-repositório)
* [Templates CloudFormation](#-templates-cloudformation)
* [Fluxo de Provisionamento](#-fluxo-de-provisionamento)
* [Segurança Aplicada](#-segurança-aplicada)
* [Conceitos de IaC](#-conceitos-de-iac)
* [Insights da Prática](#-insights-da-prática)
* [Como Exibir Imagens no GitHub](#-como-exibir-imagens-no-github)
* [Observação sobre a Execução](#-observação-sobre-a-execução)
* [Autor](#-autor)

---

## 📌 Sobre o Projeto

Este repositório foi criado para documentar os estudos e aprendizados obtidos no desafio **Automatizando Infraestrutura com AWS CloudFormation** da DIO.

O projeto simula um cenário real de provisionamento automatizado de uma infraestrutura web na AWS, utilizando templates em **YAML** para definir recursos de rede, segurança e computação de forma declarativa.

---

## 🎯 Objetivos

* Compreender o funcionamento do AWS CloudFormation.
* Aplicar conceitos de **Infrastructure as Code (IaC)**.
* Automatizar a criação de recursos na nuvem.
* Estruturar templates reutilizáveis e organizados.
* Documentar processos técnicos utilizando GitHub.

---

## 🏗️ Arquitetura

### Componentes da infraestrutura

* **Amazon VPC**
* **Public Subnet**
* **Internet Gateway**
* **Route Table**
* **Security Group**
* **Amazon EC2**
* **CloudFormation Stack**

---

## 🛠️ Tecnologias Utilizadas

* AWS CloudFormation
* YAML
* Amazon EC2
* Amazon VPC
* Security Groups
* Infrastructure as Code (IaC)
* Git & GitHub
* Markdown

---

## 📄 Templates CloudFormation

### `network.yaml`

Responsável pelos recursos de rede:

* VPC
* Subnet pública
* Internet Gateway
* Route Table

### `security.yaml`

Define as regras de segurança da aplicação:

* Acesso HTTP (porta 80)
* Acesso SSH (porta 22)
* Controle de tráfego de entrada

### `compute.yaml`

Provisiona a camada computacional:

* Instância EC2
* Configuração inicial via **UserData**
* Instalação automática do servidor web Apache

### `complete-stack.yaml`

Template consolidado contendo toda a infraestrutura em um único arquivo para facilitar o provisionamento completo do ambiente.

---

## 🔄 Fluxo de Provisionamento

```text
Template YAML
      ↓
CloudFormation
      ↓
Criação da Stack
      ↓
Provisionamento da Rede
      ↓
Configuração de Segurança
      ↓
Inicialização da EC2
      ↓
Servidor Web Disponível
```

Esse fluxo demonstra como o CloudFormation orquestra automaticamente a criação dos recursos na ordem correta.

---

## 🔐 Segurança Aplicada

A infraestrutura foi modelada considerando boas práticas básicas de segurança:

* **VPC isolada** para segmentação da rede.
* **Security Groups** atuando como firewall virtual.
* Exposição apenas das portas necessárias (**80** e **22**).
* Templates versionados no GitHub para auditoria e rastreabilidade.
* Redução de erros manuais por meio da automação.

Essas práticas ajudam a criar ambientes mais consistentes e seguros.

---

## 📚 Conceitos de IaC

### O que é Infrastructure as Code?

Infrastructure as Code (IaC) é a prática de definir infraestrutura através de arquivos de código em vez de configurações manuais.

### Principais benefícios

* **Padronização** entre ambientes.
* **Reprodutibilidade** da infraestrutura.
* **Versionamento** com Git.
* **Automação** de deploys.
* **Escalabilidade** da operação.

O CloudFormation utiliza um modelo **declarativo**, onde descrevemos o estado desejado da infraestrutura e a AWS se encarrega de criá-la.

---

## 🧠 Insights da Prática

Durante o laboratório, os principais aprendizados foram:

* A infraestrutura pode ser tratada como código e versionada da mesma forma que aplicações.
* A separação em camadas (**rede, segurança e computação**) melhora a organização do projeto.
* Templates reutilizáveis facilitam a replicação de ambientes.
* A automação reduz inconsistências e acelera o provisionamento.
* O CloudFormation permite gerenciar o ciclo de vida completo da infraestrutura.

---

## 📝 Observação sobre a Execução

Este projeto foi desenvolvido com foco na **modelagem da infraestrutura** e na aplicação dos conceitos de **Infrastructure as Code** utilizando AWS CloudFormation.

Os templates apresentados seguem a sintaxe oficial da AWS e foram estruturados para representar um cenário real de provisionamento automatizado, servindo como material de estudo e referência para futuras implementações em um ambiente AWS.

---

## 👨‍💻 Autor

**Davi Tavares**

Estudante de Desenvolvimento de Sistemas com foco em **Back-end Java, Spring Boot e Computação em Nuvem**.

* GitHub: https://github.com/bessa2121

# Servidor Web Automatizado com Vagrant & WordPress

Projeto de infraestrutura focado na automação e provisionamento de um ambiente de desenvolvimento local contendo uma stack LAMP (Linux, Apache, MySQL e PHP) rodando WordPress em uma máquina virtual gerenciada pelo Vagrant.

---

## Tecnologias Utilizadas

- Vagrant
- VirtualBox
- Ubuntu Server
- Apache2
- MySQL
- PHP
- WordPress

---

## Arquitetura do Projeto

    [ Máquina Host (Windows) ]
                │
                ├── Vagrant / VirtualBox
                │
                └── [ VM Ubuntu Server ]
                        ├── Apache Web Server (Porta 80)
                        ├── MySQL Database
                        └── WordPress CMS

---

## Estrutura do Repositório

    .
    ├── Vagrantfile         # Configuração da máquina virtual e rede
    ├── .gitignore          # Arquivos ignorados pelo Git
    └── README.md           # Documentação do projeto

---

## O que o Provisionamento Faz

Ao executar a máquina pela primeira vez, a automação realiza as seguintes etapas:

1. Atualização dos pacotes do sistema operacional.
2. Instalação do servidor web Apache2 e ativação do serviço.
3. Instalação e configuração do banco de dados MySQL.
4. Instalação do PHP e suas extensões necessárias para o WordPress.
5. Download, extração e configuração do WordPress na pasta raiz do Apache.

---

## Pré-requisitos

- Vagrant instalado
- VirtualBox instalado
- Git instalado

---

## Passo a Passo

### 1. Clonar o repositório

    git clone https://github.com/jamesoaress/servidor-web-vagrant.git
    cd servidor-web-vagrant

### 2. Subir a Máquina Virtual

    vagrant up

*(O Vagrant fará o download da imagem base do Ubuntu e executará os scripts de instalação automaticamente.)*

### 3. Acessar a aplicação
Abra o navegador e acesse: http://localhost:8080 (ou o IP configurado no seu Vagrantfile)

### 4. Desligar a máquina

    vagrant halt

---

## Autor

Desenvolvido por James Soares  
GitHub: https://github.com/jamesoaress

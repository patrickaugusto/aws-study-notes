# 🚀 Lab 02 – Introdução ao Amazon Linux

Este laboratório tem como objetivo reforçar o uso básico da **linha de comando no Linux**, explorando o acesso via **SSH** a uma instância EC2 e o sistema de ajuda padrão do Linux, conhecido como man pages.
 
## 🎯 Objetivos do Lab

- Conectar-se a uma instância Amazon Linux via SSH

- Entender a função do comando **man**

- Navegar pelas man pages e utilizar a busca

- Identificar os principais cabeçalhos de documentação (NAME, SYNOPSIS, DESCRIPTION, etc.)


## 🛠️ Pré-requisitos

- Ambiente de laboratório já inicializado (Vocareum Labs ou AWS Academy)

- Chave privada disponibilizada pelo ambiente (.ppk para Windows ou .pem para macOS/Linux)

- Cliente SSH instalado (PuTTY para Windows, Terminal nativo para macOS/Linux)

## 📝 Passo a Passo

### 🔹 Tarefa 1: Conectar-se via SSH a uma Instância Amazon Linux

#### Usuários macOS/Linux (Terminal)

- Faça o download da chave labsuser.pem.

- Anote o IP público da instância.

- Ajuste as permissões da chave:

```bash
chmod 400 labsuser.pem
``` 

Conecte-se com o comando:

```bash
ssh -i labsuser.pem ec2-user@<public-ip>
```

Digite **yes** ao confirmar a primeira conexão.

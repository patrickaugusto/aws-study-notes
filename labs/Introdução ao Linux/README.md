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

<img width="94" height="98" alt="Image" src="https://github.com/user-attachments/assets/bab8b6c0-0b8d-4f34-a1c6-1f8fe17b1897" />
 -->  
<img width="94" height="98" alt="Image" src="https://github.com/user-attachments/assets/2d454b1f-a83a-44cf-8448-8fb825e0c301" />

> Explicar brevemente o comando e o que ocorreu.

Conecte-se com o comando:

```bash
ssh -i labsuser.pem ec2-user@<public-ip>
```
> substituir "<public-ip>" pelo ip publico do servidor.

> explicar brevemente o comando.

Digite **yes** ao confirmar a primeira conexão.

<img width="655" height="441" alt="Image" src="https://github.com/user-attachments/assets/87fcb5a0-f4aa-45b9-9dac-c814e6a648f1" />

> explicar pq o user foi para ec2-user@ip-10-0-10-17.

## 🔹 
Tarefa 2: Explorando as man pages no Linux

# 🚀 Lab 01 – Introdução ao Amazon EC2

Este laboratório tem como objetivo **criar, configurar, monitorar e modificar uma instância EC2** na AWS
Ao final, você terá um **servidor web simples** rodando em uma instância EC2

---

## 🎯 Objetivos do Lab
- Criar uma instância EC2 com **proteção contra término (termination protection)**  
- Executar um script **User Data** para configurar automaticamente um servidor web  
- Monitorar o estado da instância  
- Atualizar regras de segurança no Security Group  
- Redimensionar instância (tipo e volume EBS)  
- Testar a **proteção contra término**
---

## 📝 Passo a Passo

### 🔹 Tarefa 1: Criar Instância EC2
#### Acesse o **EC2 Dashboard** no Console da AWS
<img width="904" height="412" alt="Image" src="https://github.com/user-attachments/assets/78122a8a-bb7d-406d-a401-9f7f0b13fec2" />

#### Clique em **Executar Instância**
<img width="353" height="281" alt="Image" src="https://github.com/user-attachments/assets/0a46ca32-b229-4560-ae5d-169f120ac847" />

#### Configuração da Instancia:  
- **Passo 1**: Nomear instância EC2
<img width="879" height="141" alt="Image" src="https://github.com/user-attachments/assets/0efd6836-f6f7-4739-a3bb-4edd0c19aa5b" />

- **Passo 2**: Escolher uma Amazon Machine Image (AMI)  
<img width="816" height="557" alt="Image" src="https://github.com/user-attachments/assets/722ffc84-9053-4f27-9b0b-1b05c81807b8" />

- **Passo 3**: Escolher o tipo da instância
<img width="875" height="257" alt="Image" src="https://github.com/user-attachments/assets/9161bc03-0f4e-4a00-b78b-4a689332cbd4" />

- **Passo 4**: Configurando um par de chaves
<img width="879" height="202" alt="Image" src="https://github.com/user-attachments/assets/e12036eb-fd8e-449e-a330-6c76b48142a1" />

- **Passo 5**: Configurações de redes
<img width="866" height="585" alt="Image" src="https://github.com/user-attachments/assets/a191cc59-7895-416b-8598-69fd46cd9057" />

- **Passo 6**: Adicionar Armazenamento  
<img width="875" height="328" alt="Image" src="https://github.com/user-attachments/assets/57288a0d-6e4d-4340-a90a-5d5812ff4ddd" />

- **Passo 7**: Configurando detalhes avançados 
<img width="875" height="538" alt="Image" src="https://github.com/user-attachments/assets/ff07a56d-c13f-4a4d-8c64-ae61690a5bb0" />

<img width="586" height="487" alt="Image" src="https://github.com/user-attachments/assets/0585e2f6-c921-4174-9e89-f4c42c9ec63f" />

- **Passo 8**: Iniciando a instância EC2

_No painel direito, clique em "Executar Instância"_

<img width="432" height="517" alt="Image" src="https://github.com/user-attachments/assets/0b4d135b-af86-402c-8718-7932fb6a65b0" />

<img width="1367" height="557" alt="Image" src="https://github.com/user-attachments/assets/dcb3a88e-d36b-4a62-b4cb-1d8e58266ede" />

<img width="1343" height="167" alt="Image" src="https://github.com/user-attachments/assets/0e353e83-7203-4061-a97e-15ba6839f2d1" />

---

### 🔹 Tarefa 2: Monitorando a Instância EC2

#### Aba de Monitoramento
Selecione a instância marcando a caixa ao lado da instância e navegue até a parte inferior da tela para o Verificações de status aba.

Selecione o Monitoramento aba.

<img width="1349" height="611" alt="Image" src="https://github.com/user-attachments/assets/0ab85828-803f-400e-a064-40dddfd695cb" />

Escolhemos um gráfico para ver uma visualização expandida.

<img width="1269" height="603" alt="Image" src="https://github.com/user-attachments/assets/8f79f565-b1cf-4b7d-a231-9f75f56e8986" />

#### Obter captura de tela da instância

<img width="1354" height="455" alt="Image" src="https://github.com/user-attachments/assets/1a22a498-6a34-442d-927a-66127117be20" />

![Image](https://github.com/user-attachments/assets/3407d16f-9aa2-48ce-a604-1fb5745488c9)

---

### Tarefa 3: Atualizando o grupo de segurança e acessando o servidor Web

Se tentarmos acessar o servidor a partir de seu IP publico, a pagina não sera renderizada, indicando que não permite que ninguém tenha acesso. Para isso precisamos acessor nosso grupo de segurança.

<img width="1366" height="599" alt="Image" src="https://github.com/user-attachments/assets/671ee40c-f041-49a1-abb0-605f4ab2818a" />

<img width="1347" height="372" alt="Image" src="https://github.com/user-attachments/assets/17b86542-a090-41b3-9156-5379844a35db" />

<img width="888" height="306" alt="Image" src="https://github.com/user-attachments/assets/306b6ce1-3655-4803-baf7-46cd7b1a6a47" />

---

### Tarefa 4: Redimensionando a instância: tipo de instância e volume EBS

#### Pare sua instância
<img width="1099" height="235" alt="Image" src="https://github.com/user-attachments/assets/91b071cf-d081-46f1-bf29-5c47a7800cc3" />

<img width="1101" height="181" alt="Image" src="https://github.com/user-attachments/assets/141385bd-6d18-4258-9546-1e613abbc7c1" />

#### Alterar o tipo de instância
<img width="1088" height="320" alt="Image" src="https://github.com/user-attachments/assets/0a38708a-1f39-4ae7-bc9a-0c6a6f5be9d2" />

<img width="803" height="316" alt="Image" src="https://github.com/user-attachments/assets/f8276be1-4e9c-477c-aa1c-e5fc8b68a050" />

<img width="1083" height="240" alt="Image" src="https://github.com/user-attachments/assets/83692b5e-80e0-4ef2-b72b-1c65de965623" />

#### Redimensione o volume EBS

<img width="1368" height="597" alt="Image" src="https://github.com/user-attachments/assets/4acc95ef-ea41-487a-997e-288c1a04210d" />

<img width="1325" height="561" alt="Image" src="https://github.com/user-attachments/assets/e80c8dfa-28b4-4894-b723-96e58119d2c0" />

<img width="1120" height="173" alt="Image" src="https://github.com/user-attachments/assets/1319f581-b3f5-47e2-b925-2a377f709731" />

#### Iniciar a instância redimensionada

<img width="1098" height="239" alt="Image" src="https://github.com/user-attachments/assets/8b01de51-d4aa-4887-9cc3-3f744f11aaa9" />

<img width="1088" height="247" alt="Image" src="https://github.com/user-attachments/assets/a0736ca9-f252-43fa-bad0-a45b083e2103" />

---

### Tarefa 5: Proteção contra término de teste

Selecione o Servidor Web instância marcando a caixa e navegue até o topo e selecione Estado da instância menu, selecione  Encerrar (excluir) instância.

<img width="1094" height="226" alt="Image" src="https://github.com/user-attachments/assets/12eb1544-bed6-4c54-bf14-4e2577814491" />

<img width="1070" height="83" alt="Image" src="https://github.com/user-attachments/assets/910cb7e6-3de7-4beb-a7ac-c0691111dcad" />

No Ações  menu, selecione Configurações de instância  Alterar proteção de terminação.

<img width="1333" height="295" alt="Image" src="https://github.com/user-attachments/assets/51565d1a-5464-4fd3-8775-4de1587832f3" />

Desmarcar Habilitar seguido por Salvar

<img width="603" height="408" alt="Image" src="https://github.com/user-attachments/assets/b9215b51-df8b-4262-802e-d4faee0a2803" />

<img width="1316" height="55" alt="Image" src="https://github.com/user-attachments/assets/1a2710e8-dbe6-44ae-bcb3-a5fe0b4b2ba0" />

No Ações  menu, selecione Estado da instância  Encerrar instância.
<img width="1094" height="226" alt="Image" src="https://github.com/user-attachments/assets/12eb1544-bed6-4c54-bf14-4e2577814491" />

<img width="824" height="442" alt="Image" src="https://github.com/user-attachments/assets/8ed0331c-4296-4421-a1fc-3dc8e558622d" />

<img width="1089" height="190" alt="Image" src="https://github.com/user-attachments/assets/bc4ac4a1-59a3-4cf2-a6c0-403b7ca5e300" />

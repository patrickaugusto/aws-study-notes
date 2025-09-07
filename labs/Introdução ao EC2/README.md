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
> Como não é preciso fazer login na instância, o par de chaves é ignorado.

<img width="879" height="202" alt="Image" src="https://github.com/user-attachments/assets/e12036eb-fd8e-449e-a330-6c76b48142a1" />

- **Passo 5**: Configurações de redes
> Escolhemos o Lab VPC.

> O nome do grupo de segurança é definido como: "Web Server security group".

> Descrição: "Security group for my web server".

> Como não vai ser necessario o login usando SSH, essa opção é excluida.

<img width="866" height="585" alt="Image" src="https://github.com/user-attachments/assets/a191cc59-7895-416b-8598-69fd46cd9057" />

- **Passo 6**: Adicionar Armazenamento  

> Deixar o padrão(8gb).

<img width="875" height="328" alt="Image" src="https://github.com/user-attachments/assets/57288a0d-6e4d-4340-a90a-5d5812ff4ddd" />

- **Passo 7**: Configurando detalhes avançados 

> Expandir "Detalhes Avançados" e habilitar a opção "Proteção contra encerramento".

<img width="875" height="538" alt="Image" src="https://github.com/user-attachments/assets/ff07a56d-c13f-4a4d-8c64-ae61690a5bb0" />

> No fim de Detalhes Avançados, inserimos um script para instalar e iniciar automaticamente um servidor web.

<img width="586" height="487" alt="Image" src="https://github.com/user-attachments/assets/0585e2f6-c921-4174-9e89-f4c42c9ec63f" />

- **Passo 8**: Iniciando a instância EC2

> No painel direito, Resumo, clique em "Executar Instância".

<img width="432" height="517" alt="Image" src="https://github.com/user-attachments/assets/0b4d135b-af86-402c-8718-7932fb6a65b0" />

Com isso esses passos finalizados, podemos ver nossa instância criada.

<img width="1367" height="557" alt="Image" src="https://github.com/user-attachments/assets/dcb3a88e-d36b-4a62-b4cb-1d8e58266ede" />

<img width="1343" height="167" alt="Image" src="https://github.com/user-attachments/assets/0e353e83-7203-4061-a97e-15ba6839f2d1" />

---

### 🔹 Tarefa 2: Monitorando a Instância EC2

#### Aba de Monitoramento

> Nesta etapa, vamos verificar se a instância está funcionando corretamente e analisar suas métricas. Selecione a instância e acesse a aba de Monitoramento.

> Podemos escolher um gráfico para ter uma visualização expandida.

<img width="1349" height="611" alt="Image" src="https://github.com/user-attachments/assets/0ab85828-803f-400e-a064-40dddfd695cb" />

<img width="1269" height="603" alt="Image" src="https://github.com/user-attachments/assets/8f79f565-b1cf-4b7d-a231-9f75f56e8986" />

#### Obter captura de tela da instância

> É possivel fazer a captura da tela de uma simulação de visualização do console da instância do Amazon EC2 .

<img width="1354" height="455" alt="Image" src="https://github.com/user-attachments/assets/1a22a498-6a34-442d-927a-66127117be20" />

![Image](https://github.com/user-attachments/assets/3407d16f-9aa2-48ce-a604-1fb5745488c9)

---

### Tarefa 3: Atualizando o grupo de segurança e acessando o servidor Web

> Ao tentar acessar o servidor pelo IP público da instância, a página não será exibida. Isso acontece porque, por padrão, o grupo de segurança atua como um firewall e não permite tráfego de entrada na porta 80 (HTTP).

> Para liberar o acesso, acesse as configurações do grupo de segurança associado à instância, edite as regras de entrada e adicione uma nova regra para permitir conexões HTTP.

<img width="1366" height="599" alt="Image" src="https://github.com/user-attachments/assets/671ee40c-f041-49a1-abb0-605f4ab2818a" />

> Configure a regra para aceitar tráfego HTTP (porta 80) de qualquer endereço IPv4. Dessa forma, qualquer usuário poderá acessar o servidor web pela internet.

<img width="1347" height="372" alt="Image" src="https://github.com/user-attachments/assets/17b86542-a090-41b3-9156-5379844a35db" />

> Após salvar as alterações, atualize o navegador e o site será exibido corretamente.

<img width="888" height="306" alt="Image" src="https://github.com/user-attachments/assets/306b6ce1-3655-4803-baf7-46cd7b1a6a47" />

---

### Tarefa 4: Redimensionando a instância: tipo de instância e volume EBS

> Em alguns cenários, a instância pode estar sobrecarregada (muito pequena) ou subutilizada (muito grande). Nesses casos, é possível ajustar tanto o tipo de instância (CPU e memória) quanto o tamanho do disco (EBS).

#### Parando a instância

> Antes de qualquer modificação, a instância deve ser interrompida.
Isso garante que as alterações sejam aplicadas corretamente.

<img width="1099" height="235" alt="Image" src="https://github.com/user-attachments/assets/91b071cf-d081-46f1-bf29-5c47a7800cc3" />

> Aguardar até que o estado mude para Stopped (Interrompida).

<img width="1101" height="181" alt="Image" src="https://github.com/user-attachments/assets/141385bd-6d18-4258-9546-1e613abbc7c1" />

#### Alterando o tipo de instância

> Após interromper, é possível escolher um novo tipo de instância, que define a quantidade de CPU, memória e capacidade de rede.

<img width="1088" height="320" alt="Image" src="https://github.com/user-attachments/assets/0a38708a-1f39-4ae7-bc9a-0c6a6f5be9d2" />

> No exemplo, a instância foi alterada de t3.micro para t3.small, dobrando a quantidade de memória disponível.

<img width="803" height="316" alt="Image" src="https://github.com/user-attachments/assets/f8276be1-4e9c-477c-aa1c-e5fc8b68a050" />

<img width="1083" height="240" alt="Image" src="https://github.com/user-attachments/assets/83692b5e-80e0-4ef2-b72b-1c65de965623" />

#### Redimensionando o volume EBS do EC2

> O armazenamento da instância é feito em volumes EBS. Caso seja necessário mais espaço, é possível ampliar o disco.

<img width="1368" height="597" alt="Image" src="https://github.com/user-attachments/assets/4acc95ef-ea41-487a-997e-288c1a04210d" />

> O volume foi aumentado de 8 GiB (padrão) para 10 GiB, garantindo mais espaço para arquivos e aplicações.

<img width="1325" height="561" alt="Image" src="https://github.com/user-attachments/assets/e80c8dfa-28b4-4894-b723-96e58119d2c0" />

<img width="1120" height="173" alt="Image" src="https://github.com/user-attachments/assets/1319f581-b3f5-47e2-b925-2a377f709731" />

#### Iniciar a instância redimensionada

> Depois das alterações, basta reiniciar a instância para que o novo tipo e o novo tamanho de disco entrem em vigor.

<img width="1098" height="239" alt="Image" src="https://github.com/user-attachments/assets/8b01de51-d4aa-4887-9cc3-3f744f11aaa9" />

<img width="1088" height="247" alt="Image" src="https://github.com/user-attachments/assets/a0736ca9-f252-43fa-bad0-a45b083e2103" />

---

### Tarefa 5: Proteção contra término de teste

> A proteção contra término é um recurso que impede que uma instância EC2 seja encerrada acidentalmente.

#### Tentando encerrar a instância

Selecionar a instância Web Server, ir até o menu Estado da instância e clicar em Encerrar instância.

<img width="1094" height="226" alt="Image" src="https://github.com/user-attachments/assets/12eb1544-bed6-4c54-bf14-4e2577814491" />

> A tentativa falhará, pois a instância está protegida contra término.

<img width="1070" height="83" alt="Image" src="https://github.com/user-attachments/assets/910cb7e6-3de7-4beb-a7ac-c0691111dcad" />

#### Desabilitando a proteção
> Para prosseguir, abra o menu Ações > Configurações de instância > Alterar proteção de terminação.

<img width="1333" height="295" alt="Image" src="https://github.com/user-attachments/assets/51565d1a-5464-4fd3-8775-4de1587832f3" />

> Desmarcar a opção **Habilitar proteção contra término** e clicar em Salvar.

<img width="603" height="408" alt="Image" src="https://github.com/user-attachments/assets/b9215b51-df8b-4262-802e-d4faee0a2803" />

<img width="1316" height="55" alt="Image" src="https://github.com/user-attachments/assets/1a2710e8-dbe6-44ae-bcb3-a5fe0b4b2ba0" />

#### Encerrando a instância

> Agora é so repetir o processo de encerramento da instância e confirmar a exclusão.

<img width="1094" height="226" alt="Image" src="https://github.com/user-attachments/assets/12eb1544-bed6-4c54-bf14-4e2577814491" />

<img width="824" height="442" alt="Image" src="https://github.com/user-attachments/assets/8ed0331c-4296-4421-a1fc-3dc8e558622d" />

<img width="1089" height="190" alt="Image" src="https://github.com/user-attachments/assets/bc4ac4a1-59a3-4cf2-a6c0-403b7ca5e300" />

---

## ✅ Conclusão
Neste laboratório aprendia a:  
- Criar e configurar uma instância EC2  
- Implantar automaticamente um servidor Apache com página HTML  
- Testar o monitoramento básico via CloudWatch  
- Ajustamos regras de firewall (Security Group) para liberar acesso HTTP  
- Redimensionar os recursos da instância (CPU/Memória + disco EBS)  
- Validar a proteção contra término

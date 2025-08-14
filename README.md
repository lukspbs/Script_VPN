# VPN Auto-Connect Manager

![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)

## 📋 Descrição

Script PowerShell para automação de conexão VPN no Windows que:
- Mantém a VPN conectada durante horário comercial
- Desconecta automaticamente fora do expediente
- Executa verificações a cada 30 segundos

## 🛠 Configuração

Edite as variáveis no script:

```powershell
$vpn     = "NOME_DA_VPN"      # Nome da conexão VPN
$usuario = "SEU_USUARIO"      # Seu usuário de VPN
$senha   = "SUA_SENHA"        # Sua senha de VPN
$horaOn  = "08:00"            # Início do horário comercial
$horaOff = "18:00"            # Término do horário comercial#
````

- Crie uma pasta em "C:\Scripts\" e adicione os arquivos .vps e .vbs
- Aperte Win + R e digite "taskschd.msc".
- Crie uma nova tarefa (Não Tarefa Básica)
- Nome: VPN_Auto.
- Marque Executar com privilégios mais altos
- Aba Gatilhos > Novo ... 
- Configure um gatilho apartir do logon do usuário
- Selecione onde ficará o Arquivo .vbs
- Argumentos vazios e aceite.
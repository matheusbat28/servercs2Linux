# Guia de Instalação de Servidor CS2 no Linux

Um guia completo e passo a passo para instalar e configurar um servidor de Counter-Strike 2 no Linux usando LinuxGSM.

## 📋 Requisitos do Sistema

### Hardware Mínimo
| Componente | Recomendado |
|------------|-------------|
| CPU | 4 núcleos/threads |
| RAM | 4GB (8GB ideal) |
| Armazenamento | 85GB livre |
| Rede | Porta 27015 UDP liberada |

### Sistema Operacional
- Ubuntu 22.04 LTS ou superior
- Debian 11/12 ou superior

## 🚀 Instalação Rápida

Execute os comandos abaixo em sequência:

```bash
# 1. Instalar dependências
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install -y mailutils postfix curl wget file tar bzip2 gzip unzip \
  bsdmainutils python3 util-linux ca-certificates binutils bc jq tmux \
  lib32gcc-s1 lib32stdc++6 steamcmd

# 2. Baixar e configurar LinuxGSM
wget -O linuxgsm.sh https://linuxgsm.sh && chmod +x linuxgsm.sh
bash linuxgsm.sh cs2server

# 3. Instalar o servidor CS2
./cs2server install


# Ver todos os comandos disponíveis
./cs2server

# Comandos principais do dia a dia
./cs2server start          # Inicia o servidor
./cs2server stop           # Para o servidor
./cs2server restart        # Reinicia o servidor
./cs2server console        # Abre o console (CTRL+b, d para sair)
./cs2server update         # Atualiza o servidor
./cs2server force-update   # Força atualização via SteamCMD
./cs2server validate       # Valida todos os arquivos
./cs2server backup         # Cria backup completo
./cs2server details        # Mostra informações do servidor
./cs2server debug          # Modo de depuração
./cs2server monitor        # Monitora e reinicia automaticamente
./cs2server logs           # Exibe logs do servidor

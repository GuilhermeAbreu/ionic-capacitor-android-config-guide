# ionic-capacitor-android-config-guide
🛠️ Configuração completa do ambiente para desenvolvimento de aplicativos Android com Ionic + Angular (standalone) e Capacitor no Linux. Inclui instalação do Node.js, Java, Android Studio, SDKs, variáveis de ambiente.


# 🚀 Setup Android com Ionic + Angular (Standalone) e Capacitor

Este repositório fornece um guia completo e atualizado para configurar seu ambiente de desenvolvimento Android com **Ionic + Angular (modo standalone)** usando **Capacitor** no Linux (Ubuntu e derivados).

---

## ✅ Requisitos

- Sistema operacional Linux (Ubuntu, Mint, Pop!_OS etc)
- Terminal básico
- Permissões de superusuário (sudo)

---

## 📦 Tecnologias Utilizadas

- [Ionic Framework](https://ionicframework.com/)
- [Angular (Standalone)](https://angular.io/)
- [Capacitor](https://capacitorjs.com/)
- Android Studio + SDK
- Node.js LTS
- Java JDK 17+

---

## 🛠️ Etapas da Instalação

### 1. Instalar Node.js

```bash
sudo apt update
sudo apt install curl -y
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
---

2. Instalar Ionic CLI
bash
Copiar
Editar
npm install -g @ionic/cli
3. Instalar o Java JDK
bash
Copiar
Editar
sudo apt install openjdk-17-jdk -y
4. Baixar e instalar o Android Studio
Acesse: https://developer.android.com/studio

Extraia e execute:

bash
Copiar
Editar
tar -xvf android-studio-*.tar.gz
sudo mv android-studio /opt
/opt/android-studio/bin/studio.sh
5. Configurar variáveis de ambiente
Adicione ao final do seu ~/.bashrc:

bash
Copiar
Editar
export ANDROID_SDK_ROOT=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
export PATH=$PATH:$ANDROID_SDK_ROOT/cmdline-tools/latest/bin
E ative com:

bash
Copiar
Editar
source ~/.bashrc
6. Instalar dependências do Capacitor
bash
Copiar
Editar
npm install @capacitor/android
7. Criar novo projeto (exemplo)
bash
Copiar
Editar
ionic start meuApp blank --type=angular
cd meuApp
npx cap add android
npx cap open android
📱 Como gerar um APK
No Android Studio:

Build > Build Bundle(s) / APK(s) > Build APK

🧠 Dica
Se for usar dispositivos físicos:

Ative o modo desenvolvedor e depuração USB

Conecte via cabo USB

Confirme a permissão no Android

📌 Licença
Este repositório é open-source sob a MIT License.

👨‍💻 Autor
Desenvolvido por [Seu Nome] — contribuições e melhorias são bem-vindas!

yaml
Copiar
Editar

---

Se quiser, posso gerar uma **versão com badges**, emojis ou em inglês. Quer que eu crie também uma versão com imagem/capa pro repositório?

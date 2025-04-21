# ionic-capacitor-android-config-guide
🛠️ Configuração completa do ambiente para desenvolvimento de aplicativos Android com Ionic + Angular (standalone) e Capacitor no Linux. Inclui instalação do Node.js, Java, Android Studio, SDKs, variáveis de ambiente.


# 🚀 Setup Android com Ionic + Angular e Capacitor

Este repositório fornece um guia completo e atualizado para configurar seu ambiente de desenvolvimento Android com **Ionic + Angular** usando **Capacitor** no Linux (Ubuntu e derivados).

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

- [NodeJs Oficial - Arquivo Tar.xz](https://nodejs.org/)

Ou instalar via Terminal
```bash
sudo apt update
sudo apt install nodejs
```
## 2. Instalar o Java JDK

Recomendo fortemente o uso do [SDKMAN!](https://sdkman.io/), um gerenciador de versões que facilita a instalação e troca de ferramentas como o Java e o Gradle.

Com o tempo, o Capacitor pode exigir versões específicas dessas ferramentas, e o SDKMAN permite gerenciar isso com muito mais praticidade.

🔧 Ainda assim, nada impede que você instale tudo manualmente, se preferir.


## 4. Baixar e instalar o Android Studio
Acesse: https://developer.android.com/studio

***
### Importante
O Android Studio será utilizado apenas para algumas configurações iniciais — como instalação dos SDKs, build tools e emuladores.

Isso pode agilizar o processo de setup para quem está começando. Porém, não será utilizado diretamente no desenvolvimento do app.

Caso você já tenha familiaridade com a linha de comando do Android (via sdkmanager, por exemplo), também é totalmente possível configurar tudo manualmente pelo terminal ou baixar os componentes de forma independente.
Extraia e execute:
***

```bash
#descompactar arquivo
tar -xvf android-studio-*.tar.gz

#mover pasta
sudo mv android-studio /opt

#executar
/opt/android-studio/bin/studio.sh
```
***De começo ele pode pedir para instalar alguns pacotes inicias***

### Download componentes no android studio
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/tela-inicial.jpeg)

Caso ja tenha o android configurado com um projeto aberto
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/tela-projeto-aberto.jpeg)

Download api, pode selecionar a escolha no meu caso estou usando a 15.
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/download-api-android.jpeg)

Download de sdk para desenvolvimento e rodar o projeto no android
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/download-sdk.jpeg)

## 5. Configurar variáveis de ambiente


Adicione ao final do seu ~/.bashrc:

```bash

#Java path
export JAVA_HOME

#Aqui será a path onde foi instalado os Sdk, veja nas imagens a cima o local.
#mas pode ser customizado, no meu caso está na minha pasta pessoal.
export ANDROID_SDK_ROOT=$HOME/Android/Sdk
export ANDROID_HOME=$ANDROID_SDK_ROOT

export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/build-tools

#Java path bin
export PATH=$PATH:$JAVA_HOME/bin
```
E ative com:

```bash
source ~/.bashrc
```

👨‍💻 Autor
Desenvolvido por Guilherme Abreu — contribuições e melhorias são bem-vindas!


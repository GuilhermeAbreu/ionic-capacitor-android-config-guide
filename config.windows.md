# ionic-capacitor-android-config-guide
🛠️ Configuração completa do ambiente para desenvolvimento de aplicativos Android com Ionic + Angular no Windows. Inclui instalação do Node.js, Java, Android Studio, SDKs, variáveis de ambiente.


# 🚀 Setup Android com Ionic + Angular

Este repositório fornece um guia completo e atualizado para configurar seu ambiente de desenvolvimento Android com **Ionic + Angular** usando **Capacitor** no Windows.

---

## ✅ Requisitos

- Sistema operacional Windows
- Permissões de Administrador: Para instalações e configurações

---

## 📦 Tecnologias Utilizadas

- [Ionic Framework](https://ionicframework.com/)
- [Angular (Standalone)](https://angular.io/)
- [Capacitor](https://capacitorjs.com/)
- Android Studio + SDK
- Node.js LTS
- Java JDK 17+
- Gradle 8+

---

## 🛠️ Etapas da Instalação

### 1. Instalar o Node.js (LTS)

- Acesse o site oficial do [NodeJs](https://nodejs.org/)
- Baixe a versão LTS recomendada para a maioria dos usuários.
- Execute o instalador e siga as instruções padrão.

Verifique a instalação abrindo o Prompt de Comando e executando:

```bash
node -v
npm -v
```

## 2. Instalar de JDKs e Nodejs

Recomendo fortemente o uso do [vFox for windows!](https://vfox.dev/), um gerenciador de versões que facilita a instalação e troca de ferramentas como o Java e o Gradle e ate o nodeJs.

Com o tempo, o Capacitor pode exigir versões específicas dessas ferramentas, e o vFox permite gerenciar isso com muito mais praticidade.

Links auxiliares

- https://github.com/version-fox/vfox
- https://github.com/version-fox/vfox-nodejs
- https://github.com/version-fox/vfox-java
- https://github.com/version-fox/vfox-gradle


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

```txt
Durante a instalação, certifique-se de incluir:

Android SDK

Android SDK Command-line Tools

Android Emulator

Após a instalação, abra o Android Studio e, através do SDK Manager, instale as versões necessárias do SDK e ferramentas de build.
```

### Validar download componentes no android studio
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/tela-inicial.jpeg)

Caso ja tenha o android configurado com um projeto aberto
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/tela-projeto-aberto.jpeg)

Download api, pode selecionar a escolha no meu caso estou usando a 15.
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/download-api-android.jpeg)

Download de sdk para desenvolvimento e rodar o projeto no android
![img](https://github.com/GuilhermeAbreu/ionic-capacitor-android-config-guide/blob/main/image/download-sdk.jpeg)

## 5. Configurar variáveis de ambiente

Configure as variáveis de ambiente para que o sistema reconheça as ferramentas do Android SDK.

-  adicionar variável ANDROID_SDK_ROOT
    - Caminho padrão: C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk


- Atualizar a variável de ambiente ***PATH***

    Adicione os seguintes caminhos ao PATH
    - %ANDROID_SDK_ROOT%\platform-tools
    - %ANDROID_SDK_ROOT%\emulator
    
        Caso tenha
    - %ANDROID_SDK_ROOT%\cmdline-tools\latest\bin 

Para configurar:

- Pressione ***Win + R***, digite ***sysdm.cpl*** e pressione Enter.

- Vá para a aba ***Avançado*** e clique em ***Variáveis de Ambiente.***

- Em ***Variáveis do sistema***, edite ou crie as variáveis conforme necessário.



👨‍💻 Autor
Desenvolvido por Guilherme Abreu — contribuições e melhorias são bem-vindas!

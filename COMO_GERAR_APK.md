# 🚀 Guia Oficial: Como Gerar e Instalar o APK do Leandro Corrêa Launcher

Este guia foi criado especialmente para o **Leandro Corrêa** gerar o arquivo `.apk` final pronto para instalação na **Smart TV TCL OLED 55" Google TV**, no **Xiaomi Mi TV Stick** e em **smartphones Android**.

---

## ⚡ Método 1: Gerar o APK Online em 2 Minutos (Sem precisar instalar nada no PC)

Este é o método mais rápido e fácil do mercado. Ele usa a ferramenta oficial e gratuita **PWABuilder** (mantida pela Microsoft).

1. Copie o link do seu Launcher publicado:
   - **URL do Launcher:** `https://ais-pre-hulkydwfypesyjts3g43fy-736264144770.us-west2.run.app`
2. Acesse no navegador do seu computador ou celular:
   👉 **[https://www.pwabuilder.com](https://www.pwabuilder.com)**
3. Cole a URL no campo de texto e clique em **Start**.
4. Quando a análise terminar, clique no botão **Package for Stores** e selecione **Android**.
5. Na tela que abrir:
   - **Package ID:** `com.leandrocorrea.launchertv`
   - **App Name:** `Leandro Corrêa Launcher`
   - **Launcher / Home Screen:** Marque a opção de compatibilidade com TV.
6. Clique em **Generate Package**.
7. O site vai compilar o pacote na nuvem e baixar um arquivo `.zip`. Dentro dele estará o seu arquivo **`app-release.apk`** pronto para instalar!

---

## 🛠️ Método 2: Gerar o APK Nativo com Capacitor & Android Studio (Controle Total)

Se você tem o Node.js e o Android Studio no computador e quer um APK 100% nativo com suporte oficial a botão Home de TV:

### Passo 1: No terminal do projeto, instale o Capacitor:
```bash
npm install @capacitor/core @capacitor/cli @capacitor/android
```

### Passo 2: Gere o build do projeto:
```bash
npm run build
```

### Passo 3: Adicione a plataforma Android:
```bash
npx cap add android
npx cap sync
```

### Passo 4: Configurar o AndroidManifest.xml para TV e Launcher Padrão:
Abra o arquivo `android/app/src/main/AndroidManifest.xml` e adicione as seguintes linhas essenciais para Android TV:

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android">
    <!-- Habilita suporte a TV sem touch screen -->
    <uses-feature android:name="android.software.leanback" android:required="false" />
    <uses-feature android:name="android.hardware.touchscreen" android:required="false" />

    <application
        android:label="Leandro Corrêa Launcher"
        android:banner="@mipmap/ic_launcher"
        android:icon="@mipmap/ic_launcher"
        android:theme="@style/AppTheme.NoActionBar">
        
        <activity
            android:name=".MainActivity"
            android:exported="true"
            android:launchMode="singleTask"
            android:screenOrientation="landscape">
            
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <!-- Torna o app um Launcher Home Oficial -->
                <category android:name="android.intent.category.HOME" />
                <category android:name="android.intent.category.DEFAULT" />
                <category android:name="android.intent.category.LAUNCHER" />
                <category android:name="android.intent.category.LEANBACK_LAUNCHER" />
            </intent-filter>
        </activity>
    </application>
</manifest>
```

### Passo 5: Gerar o APK no Android Studio:
```bash
npx cap open android
```
No Android Studio:
- Vá no menu **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
- O arquivo `.apk` final será gerado em: `android/app/build/outputs/apk/debug/app-debug.apk`.

---

## 📺 Como Instalar o APK na Smart TV TCL OLED 55 e Mi TV Stick

### Opção A: Pelo aplicativo "Downloader" (Mais Fácil - Direto pela TV)
1. Na sua TV TCL ou Mi Stick, abra a **Google Play Store** e instale o app gratuito **Downloader by AFTVnews**.
2. Abra as **Configurações da TV > Sistema > Segurança e Restrições** (ou Opções do Desenvolvedor) e ative **Permitir Fontes Desconhecidas** para o app Downloader.
3. Se você subiu o APK no MediaFire, Google Drive ou GitHub Releases, digite o link curto ou código numérico no Downloader.
4. O download começará automaticamente e a tela de **Instalar** aparecerá. Clique em **Instalar** e depois em **Abrir**.

### Opção B: Via Pendrive USB (Para a TV TCL 55")
1. Copie o arquivo `.apk` para um pendrive formatado em FAT32.
2. Conecte o pendrive na entrada USB da sua TV TCL OLED 55.
3. Instale um gerenciador de arquivos na TV (como **FX File Explorer** ou **X-plore** pela Play Store).
4. Abra o pendrive pelo gerenciador, clique no `.apk` do **Leandro Corrêa Launcher** e confirme a instalação.

---

## 🏠 Como Definir como Launcher Padrão na sua TCL Google TV & Mi Stick

No Google TV moderno, o sistema vem de fábrica com a interface do Google. Para fazer o seu Launcher abrir sempre que apertar o botão Home do controle:

1. **Instale o app "Button Mapper"** na Google Play Store da TV.
2. Abra o Button Mapper, selecione o botão **Home** do controle remoto.
3. Marque a opção **Personalizar**.
4. Em **Toque Único**, escolha **Aplicativo** e selecione o **Leandro Corrêa Launcher**.
5. Pronto! Toda vez que você ligar a TV ou apertar o botão Home, ela entrará diretamente no seu Launcher personalizado com todas as cores, favoritos e sons!

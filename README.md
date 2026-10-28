# 📺 Leandro Corrêa Launcher TV

> **Launcher moderno para Smart TV TCL OLED 55" Google TV, Xiaomi Mi TV Stick e Smartphones Android.**  
> Criado e desenvolvido por **Leandro Corrêa**.

---

## ✨ Recursos

- 🎨 **Interface Idêntica & OLED Pure Black**: Otimizado para telas OLED com proteção anti-burn-in e tema escuro suave.
- 🔊 **Sons Modernos de Navegação**: Efeitos sonoros sintetizados em tempo real via Web Audio API (0ms de atraso).
- 🎮 **Controle Remoto TV & D-Pad**: Suporte nativo aos botões direcionais, OK, Voltar, Home e Menu de Smart TVs.
- 📱 **Compatível com Celulares**: Visualização responsiva com controle remoto virtual integrado na tela.
- ☁️ **Previsão do Tempo Completa**: Painel com temperatura, previsão para 5 dias e estatísticas meteorológicas.
- 📺 **Entradas HDMI**: Chaveamento para HDMI 1, HDMI 2 (eARC) e HDMI 3.
- ⭐ **Gestão de Favoritos**: Adicione, exclua e reordene aplicativos na tela inicial.
- 🎬 **Linha de Filmes e Séries**: Pôsteres com player simulado em alta definição.

---

## 🚀 Como Subir para o seu GitHub

1. Abra o terminal na pasta deste projeto:
```bash
git init
git add .
git commit -m "feat: Leandro Corrêa Launcher TV - Versão Oficial"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/leandro-correa-launcher.git
git push -u origin main
```

---

## 🤖 Compilação Automática do APK via GitHub Actions

Este repositório já inclui um fluxo de trabalho do **GitHub Actions** em `.github/workflows/build-apk.yml`.  
Toda vez que você fizer `git push`, o GitHub compilará automaticamente o arquivo `.apk` e o disponibilizará na aba **Actions > Artifacts** para download direto!

---

## 💻 Como Rodar Localmente no seu PC

1. Clone o repositório:
```bash
git clone https://github.com/SEU_USUARIO/leandro-correa-launcher.git
cd leandro-correa-launcher
```

2. Instale as dependências:
```bash
npm install
```

3. Inicie o servidor de desenvolvimento:
```bash
npm run dev
```
Acesse `http://localhost:3000` no seu navegador!

---

## 📦 Como Gerar o APK com Capacitor

```bash
npm run build
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap add android
npx cap sync
npx cap open android
```
No Android Studio, clique em **Build > Build APK(s)**.

---

## 👨‍💻 Autor

Criado por **Leandro Corrêa**.
Otimizado para Smart TV TCL 55", Mi TV Stick e Android.

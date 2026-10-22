# Minecraft Total — porte para Android (APK)

WebView em tela cheia (paisagem) rodando o jogo HTML + controles de toque
(joystick, arrastar para olhar, botões de quebrar/colocar/pular/agachar, inventário, pausa).
O mundo é salvo automaticamente (localStorage) e o three.js é embutido no APK (funciona offline).

## Opção 1 — Sem instalar nada (GitHub Actions)
1. Crie um repositório no GitHub e envie o conteúdo desta pasta (inclusive a pasta .github).
2. Aba **Actions** → "Build APK" (roda a cada push; ou "Run workflow").
3. Ao terminar, baixe o artefato **MinecraftTotal-debug-apk** → `app-debug.apk`.
4. Instale no celular (permita "instalar apps de fontes desconhecidas").

## Opção 2 — Android Studio
Abra esta pasta (File → Open), espere o sync e use **Build → Build APK(s)**.
Saída: `app/build/outputs/apk/debug/app-debug.apk`.

## Opção 3 — Linha de comando
Com JDK 17 e Android SDK (platform 34): `gradle assembleDebug` (Gradle 8.7).

Obs.: o build baixa o three.js r128 automaticamente. Sem internet no build,
coloque o arquivo em `app/src/main/assets/three.min.js`.

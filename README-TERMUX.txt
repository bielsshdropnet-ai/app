DROPNET VPN — PROJETO INICIAL ANDROID

O que já existe:
- Tela Android nativa em Kotlin.
- Cadastro de vários perfis locais (host, porta, login, senha e SNI).
- Exclusão de perfis.
- Pedido de autorização VPN do Android.
- Serviço VpnService declarado no Manifest.
- Workflow do GitHub Actions para compilar APK de teste.

O que ainda NÃO existe:
- Motor SSH/TLS de túnel.
- Encaminhamento de tráfego pela interface VPN.
- Rotação/combinação automática de payload, proxy e SNI.
- Conexão VPN funcional. A tela informa claramente que ainda não há túnel.

SEGURANÇA:
Use somente servidores e proxies seus ou com autorização. Este projeto inicial não
implementa payloads de injeção nem mecanismos para contornar cobrança ou restrições
de operadoras. A senha é guardada localmente em SharedPreferences nesta versão de
protótipo; não use senha real até implementarmos armazenamento protegido.

DESENVOLVIMENTO PELO TERMUX:
1. Instale:
   pkg update -y && pkg upgrade -y
   pkg install git unzip nano -y

2. Extraia o ZIP:
   mkdir -p ~/DROPNET-VPN
   unzip DROPNET-VPN-ANDROID-STARTER.zip -d ~/DROPNET-VPN

3. Entre na pasta:
   cd ~/DROPNET-VPN/DROPNET-VPN-ANDROID-STARTER

4. Envie o conteúdo para um repositório GitHub e habilite Actions.
   O workflow .github/workflows/build-apk.yml compila o APK de debug.
   Depois abra Actions > Build DROPNET VPN APK > Artifacts para baixar o APK.

IMPORTANTE:
Este é o primeiro esqueleto do aplicativo, não um HTTP Injector pronto.

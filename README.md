# Lock — site público

Este pacote contém a página estática do Lock preparada para publicar com GitHub Pages.

## Publicar

1. Crie um repositório público no GitHub, por exemplo `lock-site`.
2. Envie para a raiz do repositório os arquivos `index.html` e `.nojekyll` deste pacote. O `README.md` é opcional.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/(root)`; clique em **Save**.
6. Aguarde o GitHub publicar o site. O endereço normalmente será `https://SEU-USUARIO.github.io/lock-site/`.
7. Abra a extensão Lock → **Configurar** e cole o endereço público do site, incluindo a barra final. Salve.

Os convites ficarão no formato `https://SEU-USUARIO.github.io/lock-site/#CODIGO-DA-SALA`.

## Importante

- Use o endereço real que o GitHub Pages mostrar em **Settings → Pages**; não copie o exemplo literalmente.
- O repositório e o site publicados são públicos. Não coloque senhas, tokens ou dados privados nele.
- O site é estático e usa PeerJS/WebRTC para negociação da conexão. O GitHub Pages hospeda os arquivos, mas não é um servidor de sinalização próprio; a conexão ainda depende do serviço PeerJS e das redes/navegadores dos participantes.

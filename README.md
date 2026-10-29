# Lock — site público (v1.5)

Esta é a página web do Lock, preparada para publicar no repositório `Gueten/lock-site` usando GitHub Pages.

## Atualizar o site

1. Extraia este ZIP.
2. Envie `index.html` e `.nojekyll` para a raiz do repositório `Gueten/lock-site`, substituindo o arquivo antigo.
3. Mantenha o GitHub Pages ativado em **Settings → Pages**, branch `main`, pasta `/(root)`.
4. O endereço base dos convites é fixo: `https://gueten.github.io/lock-site/`. Os links da sala acrescentam `#CODIGO` no final.

## O que mudou

- Na primeira visita, pede um nome e, opcionalmente, uma foto. O perfil e a foto ficam no `localStorage` do próprio navegador e não são enviados aos outros participantes. Para outras pessoas, o chat usa rótulos genéricos.
- A sala mantém o mesmo código/link ao parar e voltar a compartilhar tela, enquanto a aba do anfitrião continua aberta.
- Permite até duas transmissões simultâneas: a tela do anfitrião mais uma tela de participante, ou duas telas de participantes quando o anfitrião não está transmitindo.
- O anfitrião retransmite a segunda tela aos demais participantes por WebRTC/PeerJS.

## Limitações conhecidas

- O perfil é local; não é uma conta sincronizada entre dispositivos.
- O site é estático. O transporte de mídia depende do PeerJS e de WebRTC; firewalls, navegadores e redes podem impedir conexões ou causar baixa qualidade.
- O envio da tela para vários participantes passa pelo navegador anfitrião. A qualidade cai conforme a largura de banda e o número de pessoas aumentam.

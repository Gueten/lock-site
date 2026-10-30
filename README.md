# LockCall · Site v2.3

Versão web do LockCall para publicar no GitHub Pages, sem extensão.

## Atualizar o site
1. Baixe e extraia `Lock_GitHub_Pages_v2.3.zip`.
2. Envie `index.html`, `.nojekyll`, `robots.txt` e `sitemap.xml` para a raiz do repositório `Gueten/lock-site`, substituindo os arquivos anteriores.
3. Mantenha o GitHub Pages em `main` / `/(root)`.

## Novidades da v2.3: amizades e pedidos para entrar
- A página inicial abre o painel **Amigos** na lateral direita; dentro de uma sala, as abas permitem alternar entre Amigos e Chat.
- Cada navegador recebe um código de amigo. É possível copiar esse código ou adicionar alguém pelo código.
- Na lista de participantes da sala, o botão `+` envia um pedido de amizade.
- Os pedidos recebidos podem ser aceitos ou recusados; as amizades aceitas ficam salvas no navegador.
- A lista mostra amigos online e informa quando um amigo está em uma sala, com o código da sala.
- Quando você está em uma sala, também pode **Convidar** um amigo. O convite abre a opção de pedir entrada, sem pular a aprovação do anfitrião.
- O botão **Pedir para entrar** envia uma solicitação ao anfitrião da sala. O anfitrião vê o pedido na aba Amigos e pode aceitar ou recusar. A entrada pelo fluxo de pedido só começa após a aprovação; pedidos e respostas expirados são descartados.
- Os pedidos de amizade enviados são tentados novamente enquanto o Lock permanece aberto, caso a pessoa destinatária esteja temporariamente offline.

## Limites importantes do sistema social
Esta versão usa conexões de dados P2P via PeerJS para sinalização e comunicação em tempo real; o cliente PeerJS permite conexões entre IDs conhecidos e eventos de dados (`connection`, `open`, `data`). Documentação: https://peerjs.com/client/getting-started

A lista de amigos e os pedidos ficam no armazenamento local de cada navegador. Não há login/conta central nem banco de dados: portanto, a lista não sincroniza automaticamente entre dispositivos do mesmo usuário, e uma solicitação offline não é uma caixa de entrada durável de servidor. Para contas persistentes, pedidos garantidos mesmo com o remetente offline e sincronização entre aparelhos, será necessário ligar o site a um backend (por exemplo, Firebase ou Supabase). Os códigos de amigo são endereços de conexão, não senhas nem autenticação de identidade; não os publique em locais abertos.

O código de sala normal continua sendo um convite direto: quem já conhece o código/link ainda pode tentar entrar pelo fluxo normal. A aprovação é aplicada ao fluxo **Pedir para entrar** da lista de amigos.

## Recursos existentes
- Perfil com nome e foto, incluindo GIF animado leve.
- Chat com avatar, menções, respostas, emojis e URLs de GIF exibidas inline.
- Voz e até três transmissões simultâneas por sala.
- Prévia local de transmissão, histórico recente de chat durante a vida de cada sala e cores determinísticas por nome.
- Configurações locais de resolução, microfone, redução de ruído, eco, volume recebido e tema.

Rede, firewall, permissões do navegador e recursos do dispositivo podem afetar mídia e conexões em tempo real.

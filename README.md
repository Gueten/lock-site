# LockCall v2.9

## Atualizações
- O aviso de captura esclarece que não conseguir transmitir a própria tela não impede assistir às transmissões dos outros nem conversar normalmente pelo chat de voz, desde que a pessoa esteja conectada à sala.
- A limitação de `getDisplayMedia()` ficou separada dos erros de conexão ao canal.
- Erros ao conectar, desconexões e tempo limite agora aparecem em um aviso próprio e visível no cabeçalho da sala, sem depender do painel de vídeo estar aberto.
- O aviso de conexão oferece o botão **Tentar novamente**, que reconecta ao mesmo código de sala.
- O prazo inicial para estabelecer conexão foi ampliado para 20 segundos e a conexão de sinalização tenta se recuperar quando cai.
- Os botões de voz e compartilhamento só são habilitados depois que o participante abre a conexão de dados com o anfitrião. Isso evita mostrar falsamente que a pessoa já entrou no canal antes de conectar.
- Não possuir suporte a compartilhamento de tela continua não bloqueando a entrada na sala.

## Publicar
Extraia o ZIP e copie o conteúdo para a raiz do repositório `Gueten/lock-site`, substituindo os arquivos anteriores. O endereço permanece https://gueten.github.io/lock-site/.

## Limitação de teste
Os scripts podem ser verificados localmente, mas a conexão WebRTC precisa ser validada entre aparelhos reais, navegadores e redes diferentes. O LockCall usa sinalização PeerJS e mídia WebRTC ponto a ponto; firewalls, redes móveis restritas ou um anfitrião offline ainda podem impedir uma conexão real.

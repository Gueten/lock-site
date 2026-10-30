# LockCall v2.6

Atualização do site estático para GitHub Pages.

## Alterações
- Participantes convidados para uma sala não podem redistribuir convites. Apenas o anfitrião da sala vê a ação de convidar.
- Ações de adicionar/remover amizade ficam no botão pequeno da plaqueta do participante (`+` / `−`).
- As seções de convites e pedidos deixam de exibir mensagens vazias; só aparecem quando há itens pendentes.
- Balões de convite e pedido mostram foto de perfil quando disponível e nome da pessoa.
- Ajustes de reprodução inline, dimensões e layout de vídeos recebidos em telas pequenas.
- Corrigida a lógica que escondia a área de transmissão de participantes quando chegava uma transmissão de tela sem câmera.

## Limitação de captura móvel
A transmissão de tela pelo navegador depende de `navigator.mediaDevices.getDisplayMedia`. Muitos navegadores móveis não implementam essa API. O site detecta a disponibilidade e não consegue substituir as permissões de captura do sistema operacional. Para transmitir a tela inteira de Android/iOS de forma confiável, é necessário um aplicativo nativo ou um navegador móvel que implemente a API.

## Publicação
Substitua os arquivos do repositório GitHub Pages pelos arquivos deste pacote. A lista de amigos e o sinal de presença continuam usando PeerJS e armazenamento local; não há sincronização central de contas.

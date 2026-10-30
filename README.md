# LockCall · Site v2.4

Versão web do LockCall para GitHub Pages, sem extensão.

## Atualizar
1. Extraia `Lock_GitHub_Pages_v2.4.zip`.
2. Envie `index.html`, `.nojekyll`, `robots.txt` e `sitemap.xml` para a raiz do repositório `Gueten/lock-site`, substituindo os arquivos anteriores.
3. Mantenha o GitHub Pages em `main` / `/(root)`.

## Novidades da v2.4
- Pedidos para entrar aparecem em um pop-up no canto inferior direito do anfitrião.
- O pop-up tem botões **Aceitar** e **Recusar** e fecha automaticamente após 8 segundos.
- Fechar o pop-up não aprova nem recusa o pedido: a solicitação continua na aba **Amigos > Pedidos para entrar** até ser respondida ou expirar.
- Quando o anfitrião aceita, o convidado recebe a aprovação e só então começa a entrar na sala. Ao recusar, o convidado recebe a recusa.
- Na página inicial, a lista de amigos fica em um painel à direita em telas grandes. Em celulares, o botão **Amigos** abre o painel como gaveta para não cobrir a tela inicial.
- Os controles de convite ficam escondidos na página inicial e só são exibidos durante uma sala ativa. O código também bloqueia a abertura do modal de convite antes de entrar em uma sala.
- O site detecta quando o navegador não oferece captura de tela e mostra uma mensagem específica para celular.

## Limitação da transmissão de tela em celulares
O LockCall atual é um site estático. A transmissão de tela pela web depende de `navigator.mediaDevices.getDisplayMedia()`. A tabela de compatibilidade da MDN registra a API como indisponível no Chrome para Android e no Safari para iOS; portanto, um site comum não consegue pedir ao navegador móvel para capturar a tela inteira. Referência: https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getDisplayMedia e dados de compatibilidade MDN.

Em celulares, assistir à sala e transmitir a câmera continuam sendo fluxos web possíveis, mas a **transmissão da tela do aparelho** exige um app nativo: no Android, integração com a permissão de captura do sistema; no iOS, uma extensão de broadcast/ReplayKit. Isso não pode ser habilitado apenas com HTML/JavaScript no GitHub Pages. Não há botão falso habilitando uma função que o navegador não oferece.

## Sistema social: limitações mantidas
- Cada navegador gera um código de amigo; a lista de amigos e os pedidos ficam salvos localmente naquele navegador.
- A presença e os pedidos em tempo real usam conexões P2P via PeerJS enquanto as páginas dos usuários permanecem abertas.
- Não existe login central, banco de dados ou caixa de entrada permanente. Não há sincronização automática de amigos entre aparelhos nem garantia de entrega para pessoas offline.
- O pedido de entrada só controla o fluxo **Pedir para entrar**. Quem tem o código/link direto da sala ainda pode tentar entrar pelo fluxo normal.

## Recursos mantidos
- Perfil com nome e foto, incluindo GIF animado leve.
- Chat por sala, histórico recente durante a vida da sala, avatares e cores determinísticas por nome.
- Voz, câmera e até três transmissões simultâneas por sala nos navegadores compatíveis.
- Prévia local da transmissão, configurações de resolução/áudio e tema.

Rede, firewall, permissões do navegador e suporte de mídia do dispositivo podem afetar chamadas e transmissões. A sintaxe dos scripts é validada no pacote, mas a comunicação entre dispositivos ainda deve ser testada com duas pessoas reais em navegadores separados.

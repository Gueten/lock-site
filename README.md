# LockCall · Site v2.2

Versão web do LockCall para publicar no GitHub Pages, sem extensão.

## Atualizar o site
1. Baixe e extraia `Lock_GitHub_Pages_v2.2.zip`.
2. Envie `index.html`, `.nojekyll`, `robots.txt` e `sitemap.xml` para a raiz do repositório `Gueten/lock-site`, substituindo os arquivos anteriores.
3. Mantenha o GitHub Pages em `main` / `/(root)`.

## Correções desta versão
- A prévia da própria tela/câmera agora aparece na grade quando um participante transmite, em vez de ficar presa à tela exclusiva do anfitrião.
- O chat não tem mais o botão de lixeira.
- Criar uma sala nova limpa o histórico anterior; quem entra numa sala já criada recebe as mensagens recentes daquela sala enquanto ela estiver ativa.
- Nomes recebem cores determinísticas, iguais em cada dispositivo para o mesmo nome.

## Recursos existentes
- Perfil com nome e foto, incluindo GIF animado leve.
- Chat com avatar, menções, respostas, emojis e URLs de GIF exibidas inline.
- Voz e até três transmissões simultâneas por sala.
- Configurações locais de resolução, microfone, redução de ruído, eco, volume recebido e tema.

## Sobre amizades e pedidos para entrar
As funções sociais sincronizadas entre dispositivos **ainda não estão ativadas nesta versão**. Para suportar amizade persistente, presença online/na sala, pedidos de amizade e aprovação do anfitrião para entrar, o site precisa de autenticação e banco de dados em tempo real (por exemplo, Firebase). O GitHub Pages hospeda os arquivos estáticos, mas não armazena uma lista compartilhada de usuários. Não foi colocado um sistema falso baseado só em `localStorage`, porque isso não funcionaria entre pessoas/dispositivos.

As chamadas usam PeerJS/WebRTC. Rede, firewall, permissões do navegador e recursos do dispositivo podem afetar mídia em tempo real.

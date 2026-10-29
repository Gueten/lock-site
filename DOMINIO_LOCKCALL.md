# Usar lockcall.gg no LockCall

O endereço `https://lockcall.gg/` exige que você registre o domínio e consiga gerenciar o DNS. A disponibilidade atual não foi confirmada nesta preparação; consulte um registrador de domínios .gg antes de pagar.

## Depois de registrar o domínio

1. No repositório `Gueten/lock-site`, abra **Settings → Pages → Custom domain** e digite `lockcall.gg`. Salve e siga a verificação de domínio recomendada pelo GitHub. Faça isso antes de alterar o DNS.
2. No painel DNS do registrador, crie os quatro registros A abaixo para o domínio raiz (`@`):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Opcionalmente, para habilitar IPv6, adicione os registros AAAA oficiais do GitHub Pages: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`.
4. Para `www.lockcall.gg`, crie um CNAME `www` apontando para `gueten.github.io`.
5. Aguarde a propagação do DNS e, quando estiver disponível, ative **Enforce HTTPS** em Settings → Pages. A propagação pode levar até 24 horas.
6. No `index.html`, mude `const LOCK_BASE = 'https://gueten.github.io/lock-site/';` para `const LOCK_BASE = 'https://lockcall.gg/';`. Atualize também as URLs canônicas/OG, `robots.txt` e `sitemap.xml` para `https://lockcall.gg/`, então publique novamente.
7. Adicione `https://lockcall.gg/` ao Google Search Console, confirme que você controla o domínio e envie `https://lockcall.gg/sitemap.xml`. Use a inspeção de URL para solicitar indexação.

Ter o domínio não garante que o site apareça imediatamente nem em primeiro lugar no Google. O Google decide quando indexa e como classifica os resultados. Títulos, descrições e conteúdo textual ajudam os buscadores a entender o site, mas não garantem posição.

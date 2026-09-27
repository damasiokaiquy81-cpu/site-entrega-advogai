# site-entrega-advogai

Página que o cliente recebe depois da compra (junto com a chave): download do instalador, passo a passo e verificação do VirusTotal.

## Arquivos

- `index.html` — a página.
- `download/AdvogAI.Jev-Instalador.exe` — o instalador. O `npm run entregar` do app copia a versão nova para cá sozinho
  (e escreve a versão e o tamanho no botão “Baixar para Windows”).
- `assets/` — logo, favicon, fonte Inter e (opcional) `print-app.png`, um print do card “Cláusula citada”.

## A cada versão nova

1. No app: `npm run entregar` (atualiza o instalador aqui em `download/`).
2. Envie o instalador ao VirusTotal e troque o link do bloco “Instalador verificado” no `index.html`.
3. Atualize também o arquivo no Google Drive (se usar) e o link do botão “Abrir no Drive”.
4. Publique (GitHub Desktop → Commit → Push; a hospedagem publica sozinha).

Arquivos acima de 100 MB não sobem para o GitHub e o Google Drive não verifica vírus neles:
o `after-pack.js` do app mantém o instalador abaixo disso.

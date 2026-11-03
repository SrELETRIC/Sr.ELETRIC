# SR ELETRIC — versão para GitHub Pages

Este pacote contém a landing page e as nove fotografias originais do portfólio. As fotos foram copiadas sem edição ou recompressão.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Descompacte este pacote e envie **o conteúdo** para a raiz do repositório: `index.html`, `README.md` e a pasta `assets`.
3. Abra **Settings → Pages** no repositório.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`, depois salve.
6. Quando o GitHub terminar a publicação, use o endereço mostrado em **Settings → Pages**.

## Adicionar novas fotos usando somente o GitHub

O site não tem upload direto porque GitHub Pages publica arquivos estáticos. Mas você pode atualizar o portfólio pelo próprio GitHub, sem alterar o HTML:

1. Abra a pasta `assets/portfolio/` no repositório e envie a nova foto (`Add file → Upload files`).
2. Abra `assets/portfolio/portfolio-data.js` e clique no lápis para editar.
3. Dentro de `window.SR_PORTFOLIO_ITEMS`, acrescente uma linha seguindo este formato (ajuste o nome do arquivo e os textos):

```js
{ image: "10-nova-instalacao.jpg", category: "Iluminação", title: "Nova instalação", description: "Descrição breve do serviço.", alt: "Descrição da fotografia" },
```

4. Salve com **Commit changes**. O GitHub Pages publicará a atualização automaticamente.

**Importante:** GitHub Pages não executa código de servidor nem recebe uploads diretamente pelo site. Portanto, o envio de novas fotos é feito na área do repositório do GitHub. A galeria pública é atualizada a partir do arquivo `portfolio-data.js`.

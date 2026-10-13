# Pizzaría Amazing

Site estático da Pizzaria Amazing (HTML + CSS + JS puro, sem build).

## Estrutura

```
index.html                        página única (topo, cardápio e rodapé)
assets/
  hero-video.mp4                  vídeo de fundo (computador, 1280x720)
  hero-video-mobile.mp4           vídeo de fundo (celular/retrato, leve)
  hero-poster.webp                capa do vídeo (computador) — aparece na hora
  hero-poster-mobile.webp         capa do vídeo (celular)
  pizza-slice-640.webp            fatia em destaque (celular)
  pizza-slice-1000.webp           fatia em destaque (computador)
.nojekyll                         faz o GitHub Pages servir os arquivos como estão
```

Envie **todos** os arquivos de `assets`. Se o vídeo faltar, o site mostra a capa como fundo estático.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub (por exemplo `pizzaria-amazing`).
2. Envie o conteúdo desta pasta para a raiz do repositório (arraste os arquivos e a pasta `assets` em *Add file → Upload files*).
3. Em **Settings → Pages**, escolha *Deploy from a branch*, branch `main` e pasta `/ (root)`.
4. Em cerca de um minuto o site abre em `https://SEU-USUARIO.github.io/pizzaria-amazing/`.

## Desempenho (como o site foi otimizado)

- O vídeo só começa a baixar **depois** que a página carregou, e o celular recebe uma versão de ~230 KB.
- Em aparelhos com **economia de dados** o vídeo não é baixado; fica só a capa.
- A capa (primeiro quadro do vídeo) aparece imediatamente e o vídeo assume sem salto.
- As fontes do Google não bloqueiam a primeira renderização.
- A fatia tem duas resoluções; o celular baixa a menor.
- Há um botão de pausa no canto do topo (acessibilidade).
- O GitHub Pages define cache de apenas 10 minutos para os arquivos. Para cache longo (aviso "ciclos de vida de cache" do PageSpeed), publique pelo **Cloudflare Pages**, **Netlify** ou **Vercel**, que servem os mesmos arquivos com cache de 1 ano.

## Como editar

- **Preços e pratos:** procure `menu-card` no `index.html`.
- **Fotos reais das pizzas:** dentro de cada `<div class="image-slot">`, adicione `<img src="assets/margherita.webp" alt="Pizza Margherita" loading="lazy">` (formato 4:3).
- **Vídeo de fundo:** os arquivos já vêm fundidos ao degradê laranja do topo (50% de opacidade). Para trocar, é preciso gerar de novo com o mesmo processo; peça ajuda.
- **Cores e fontes:** variáveis no início do `<style>` (`:root`). Fontes (Fraunces e DM Sans) vêm do Google Fonts.
- **Endereço, horário e telefone:** procure os comentários `EDITE AQUI` na seção `#contato` do `index.html`.
- **Botão de contato:** no link `wa.me`, substitua `5500000000000` pelo WhatsApp real com DDI e DDD, usando apenas números. Exemplo: `5511999999999`.

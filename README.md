<p align="center">
  <img src="logo.png" alt="blame.sh" width="120">
</p>

<h1 align="center">blame.sh</h1>

<p align="center">Gerador de desculpas para devs que precisam explicar o inexplicavel.</p>

<p align="center"><a href="README.en.md">English version</a></p>

## Sobre

**blame.sh** e um gerador de desculpas para desenvolvedores. Escolha quem esta perguntando, o que deu errado, e receba tres desculpas em tons diferentes: tecnico, vago e dramatico.

O projeto nasceu como uma brincadeira, mas com aquela estrutura que todo dev respeita: sem frameworks, sem dependencias, sem desculpas (ironicamente).

## Como funciona

1. Escolha a **persona** (quem vai ouvir a desculpa: tech lead, PM, cliente...)
2. Escolha a **situacao** (o que aconteceu: deploy quebrou, bug em producao, PR gigante...)
3. Clique em `./blame.sh` e receba tres desculpas, cada uma em um tom diferente

As desculpas sao pre-escritas em JSON e servidas sem nenhuma chamada de API. Tudo roda no navegador.

## Stack

Vanilla HTML, CSS e JavaScript. Uma unica pagina, zero dependencias externas (alem da fonte JetBrains Mono via Google Fonts). Funciona em qualquer navegador moderno.

## Executando localmente

Abra o arquivo `index.html` no navegador. Nao precisa de build, bundler ou servidor.

## Autor

Feito por [Felipe Bossolani](https://github.com/felipebossolani).

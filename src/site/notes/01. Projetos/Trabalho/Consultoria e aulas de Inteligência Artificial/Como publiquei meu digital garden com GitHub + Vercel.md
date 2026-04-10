---
title: "Como publiquei meu digital garden com GitHub + Vercel"
tags:
  - digital-garden
  - github
  - vercel
  - obsidian
created: 2026-04-10
updated: 2026-04-10
dg-publish: true
permalink: /digital-garden/como-publiquei-meu-digital-garden-com-github-e-vercel/
---

# Como publiquei meu digital garden com GitHub + Vercel

Meu digital garden hoje roda com uma combinação simples:

- notas em Markdown
- repositório no GitHub
- deploy pela Vercel

O ponto forte desse arranjo não é “ter um site”.

É ter um fluxo publicável e versionado.

## O que esse setup me dá

### 1. versionamento real do conteúdo

Cada alteração importante vira histórico.

Isso facilita:

- testar mudanças
- revisar diffs
- entender regressões
- manter controle sobre o que foi publicado

### 2. deploy automático

Quando o branch certo entra no GitHub, a Vercel faz o resto.

Isso reduz muito o atrito de publicação.

Em vez de pensar em “subir site”, eu penso em “editar nota e publicar”.

### 3. separação entre conteúdo e infraestrutura

As notas continuam simples.

O build e a entrega ficam na camada certa:

- GitHub cuida da versão
- Vercel cuida da entrega

## O que eu aprendi com esse processo

O principal aprendizado é que publicar nota com consistência depende menos de ferramenta e mais de fluxo.

Se o processo for frágil, qualquer atualização vira risco.

Se o processo for previsível, o garden vira parte natural do trabalho.

## O setup que uso como referência

- **Repositório:** [apcjoaofilho/joao-filho](https://github.com/apcjoaofilho/joao-filho)
- **Produção:** [joao-filho.vercel.app](https://joao-filho.vercel.app/)
- **Documentação do template:** [docs.forestry.md](https://docs.forestry.md/)

## O que mudou quando deixei isso estável

Depois que o fluxo ficou confiável, o digital garden deixou de parecer “projeto paralelo”.

Ele passou a funcionar como:

- base pública de autoridade
- laboratório de formatos
- fonte de pauta para social media

É esse terceiro ponto que mais me interessa agora.

## Leitura relacionada

- [[O deploy que quebrou e o que isso ensinou]]
- [[Como eu uso Obsidian como centro de operação]]
- [[Da nota ao carrossel — meu fluxo de conteúdo]]

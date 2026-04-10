---
title: "O deploy que quebrou e o que isso ensinou"
tags:
  - deploy
  - vercel
  - github
  - aprendizados
created: 2026-04-10
updated: 2026-04-10
dg-publish: true
permalink: /digital-garden/o-deploy-que-quebrou-e-o-que-isso-ensinou/
---

# O deploy que quebrou e o que isso ensinou

Recentemente, um deploy do meu digital garden quebrou por um motivo simples:

o branch publicado tentava importar um arquivo que ainda não existia naquele commit.

Não foi um problema conceitualmente complexo.
Foi um problema de integridade entre versão, branch e deploy.

## O erro em termos práticos

O build falhava porque o `.eleventy.js` passou a exigir um módulo novo, mas o arquivo correspondente não estava presente no commit redeployado.

Em outras palavras:

- configuração já apontava para a nova peça
- repositório publicado ainda estava incompleto

Esse tipo de falha é chato justamente porque parece “quebra misteriosa”, mas a causa raiz é banal.

## O que isso reforçou para mim

### 1. branch velho aberto custa caro

Enquanto um branch antigo e quebrado continua aberto, ele segue existindo como fonte de erro operacional.

Mesmo depois de o projeto estar corrigido em outro branch, você ainda pode disparar redeploy da versão errada.

### 2. deploy saudável não é o mesmo que histórico saudável

Uma produção estável não elimina ruído operacional.

Se o histórico continua cheio de branches antigos prontos para serem reaproveitados, o risco volta.

### 3. corrigir o build não basta

Também é preciso remover a origem do problema:

- fechar PR obsoleta
- apagar branch antigo
- garantir que `main` está com o estado certo

## O aprendizado mais útil

Deploy quebrado quase nunca é “só deploy”.

Quase sempre ele revela um problema de processo:

- branch demais
- falta de limpeza
- validação incompleta
- confiança excessiva em estado implícito

## O lado bom

Quando o processo é ajustado, o ganho vai além de “resolver um erro”.

Você reduz atrito futuro.

Foi isso que aconteceu aqui:

- o branch correto foi mergeado
- a produção ficou saudável
- o branch antigo quebrado foi encerrado

## Leitura relacionada

- [[01. Projetos/Trabalho/Consultoria e aulas de Inteligência Artificial/Como publiquei meu digital garden com GitHub + Vercel|Como publiquei meu digital garden com GitHub + Vercel]]
- [[01. Projetos/Trabalho/Vibe Coding/Vibe coding sem fantasia|Vibe coding sem fantasia]]

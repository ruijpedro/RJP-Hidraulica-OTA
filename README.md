# RJP Hidráulica — distribuição OTA

Repositório **público de distribuição**, separado do código-fonte privado [RJP-Hidr-ulica](https://github.com/ruijpedro/RJP-Hidr-ulica).

Este repositório contém **apenas ficheiros compilados**, e não deve conter fontes originais, tokens, chaves de assinatura, dados pessoais ou ficheiros de trabalho.

## Distribuição direta sem GitHub Pages

A APK obtém o manifesto e os pacotes por HTTPS, diretamente do GitHub Raw:

- Manifesto: https://raw.githubusercontent.com/ruijpedro/RJP-Hidraulica-OTA/main/ota/latest.json
- Pacote: `https://raw.githubusercontent.com/ruijpedro/RJP-Hidraulica-OTA/main/ota/ota-vX.Y.Z/dist.zip`

**Não é obrigatório ativar GitHub Pages.** O URL `latest.json` dará 404 enquanto nenhuma versão tiver sido publicada; isso é normal. Os ficheiros são publicados a partir do repositório privado através de um workflow manual, com token restrito a este destino público. A CDN do GitHub pode introduzir algum atraso entre o commit e a disponibilidade da versão.

## WebApp

**Versão 6.7.3 — Dimensionamento assistido:** https://ruijpedro.github.io/RJP-Hidraulica-OTA/webapp/

A WebApp é servida pelo GitHub Pages a partir de `main / (root)`. Os ficheiros compilados estão em `webapp/`; a página inicial encaminha para a aplicação. O Pages é independente do OTA Android.

## Segurança

O código JavaScript compilado distribuído publicamente é inspecionável; nunca nele incluir credenciais, chaves privadas, identificadores confidenciais ou dados de obras reais. Apenas o repositório principal é privado.

As novas versões devem ser enviadas por workflow do projeto privado, usando um token fine-grained com permissão **Contents: Read and write**, limitado a este repositório de distribuição.

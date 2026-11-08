# RJP Hidráulica — distribuição OTA

Repositório **público de distribuição**, separado do código-fonte privado [RJP-Hidr-ulica](https://github.com/ruijpedro/RJP-Hidr-ulica).

Este repositório contém **apenas ficheiros compilados**, e não deve conter fontes originais, tokens, chaves de assinatura, dados pessoais ou ficheiros de trabalho.

## Ativar o GitHub Pages

Abre [Settings → Pages](https://github.com/ruijpedro/RJP-Hidraulica-OTA/settings/pages):

- **Source:** Deploy from a branch
- **Branch:** main
- **Folder:** /(root)
- **Save**

O URL esperado do site é https://ruijpedro.github.io/RJP-Hidraulica-OTA/ .

O cliente OTA consulta `ota/latest.json` e descarrega `ota/ota-vX.Y.Z/dist.zip`. Estes ficheiros só devem ser publicados depois de testes e de verificação da compatibilidade nativa.

## Segurança

O código JavaScript compilado distribuído publicamente é inspecionável; nunca nele incluir credenciais, chaves privadas, identificadores confidenciais ou dados de obras reais. Apenas o repositório principal é privado.

As novas versões devem ser enviadas por workflow do projeto privado, usando um token fine-grained com permissão **Contents: Read and write**, limitado a este repositório de distribuição.

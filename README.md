# maps-apk — distribuição Android

[**Descarregar APK 0.3.0-poc — 73 MB**](https://github.com/joaodvn/maps-apk-downloads/releases/download/v0.3.0-poc/maps-apk-v0.3.0-poc.apk)

[Release e SHA-256](https://github.com/joaodvn/maps-apk-downloads/releases/tag/v0.3.0-poc)

Download público, sem login. O código-fonte permanece privado. A branch `apk` contém instruções e política de atualização; os instaladores estão em Releases.

## Instalação e atualização

1. Descarregar e abrir o APK no Android.
2. Se solicitado, permitir instalação pelo navegador/gestor de ficheiros.
3. **Instalar por cima da versão anterior, sem desinstalar**, para preservar missões e UUID.
4. Na app: **Missão → Verificar pacote → Preparar offline → Mapa**.
5. Identificar o agente de teste **POC001** para selecionar polígonos e preencher o formulário.

Requer Android 8.0/API 26+. Versão 0.3.0-poc, código 2, mesma assinatura debug da 0.2. Missões anteriores podem ser reabertas nas abas Missão/Sync.

## Esta versão

- Ícone com avatar e versão visível.
- Imagem de Luanda e 677 polígonos reais de referência selecionáveis, disponíveis offline.
- Formulário, autosave, auditoria, outbox e Device UUID persistente.
- Avisos e exigência de atualização por [política remota](update-policy.json). Cache offline e notificações quando autorizadas; não é push instantâneo.
- Backend HTTPS/MySQL preparado para homologação. URL/token requerem provisionamento pelo responsável; não há produção configurada no APK.

IDs vêm do GeoPackage, não representam automaticamente cadastro fiscal confirmado. Usar dados fictícios no formulário até homologação. Sincronização mock é local e não prova custódia real. Não há submissão à AGT ou tracking de produção.

35 testes JVM, 13 testes MySQL e 1 teste nativo offline aprovados. A versão 0.2 foi testada pelo utilizador num Android físico; a nova 0.3 ainda deve ser ensaiada no ZTE T0802.

## Política de atualização

A 0.2 precisa desta primeira atualização manual. A partir da 0.3, a aplicação consulta `update-policy.json` no arranque/regresso, manualmente e periodicamente com rede. `latest_version_code` controla aviso opcional; `minimum_version_code` controla bloqueio de novas recolhas. Rascunhos são preservados e operações concluídas continuam sincronizáveis.

Publicar primeiro o APK e só depois uma política com revisão crescente. Nunca reutilizar uma revisão com conteúdo alterado. Não há segredos ou identificadores de agentes na política pública.

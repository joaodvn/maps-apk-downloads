# maps-apk — APK de teste Android

[**Descarregar APK v0.2.0-poc — 73 MB**](https://github.com/joaodvn/maps-apk-downloads/releases/download/v0.2.0-poc/maps-apk-v0.2.0-poc.apk)

[Release e checksum SHA-256](https://github.com/joaodvn/maps-apk-downloads/releases/tag/v0.2.0-poc)

Download público, sem conta GitHub. Este repositório distribui os APKs e as instruções; o código-fonte permanece no repositório privado.

## Instalar no celular ou tablet

1. Abrir o link de download no navegador do Android.
2. Descarregar e abrir o ficheiro APK.
3. Se solicitado, permitir instalação a partir do navegador ou gestor de ficheiros usado.
4. Na aplicação: **Verificar pacote → Preparar offline → Mapa**.
5. Para testar recolha: identificar o agente **POC001** na aba Missão.

Requer **Android 8.0/API 26 ou superior**. APK universal de teste, assinado com chave de debug; não é uma versão de produção nem uma publicação na Play Store. Hardware alvo: ZTE T0802, ainda por ensaiar fisicamente.

## Conteúdo

- Imagem real de referência de Luanda incluída: 159 tiles, zoom 14–19, preparada para uso offline.
- Polígonos, identidades e dados de recolha sintéticos.
- Formulário com rascunhos locais e sincronização mock.
- Sem ligação a produção ou à AGT. Guardado/sincronizado não significa validado fiscalmente.

Build e lint sem erros, 26 testes JVM e 1 teste nativo offline aprovados no projeto de origem. O SHA-256 do APK está nos assets da release.

A branch `apk` contém apenas documentação de distribuição. Os instaladores ficam em **Releases**, evitando guardar binários sucessivos no histórico Git.

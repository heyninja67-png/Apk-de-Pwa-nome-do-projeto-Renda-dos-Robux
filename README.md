# Renda dos Robuxs — GitHub Actions APK

Projeto adaptado do PWA fornecido para gerar um APK Android no GitHub Actions.

## Configuração mantida

- Site: https://rblx.earth/
- Nome: Renda dos Robuxs
- Package: earth.rblx.rendadosrobuxs
- PWA original preservado em `pwa/`
- Trusted Web Activity para abrir o site como aplicativo
- Build automático pelo `.github/workflows/build-apk.yml`

## Gerar APK

1. Crie um repositório no GitHub.
2. Envie todos os arquivos deste projeto.
3. Abra **Actions**.
4. Execute **Build Renda dos Robuxs APK** em **Run workflow**.
5. Baixe o artefato `Renda-dos-Robuxs-debug-apk`.

## APK de produção

Para uma versão release assinada, configure no GitHub os secrets:

- `ANDROID_KEYSTORE_BASE64`
- `ANDROID_KEYSTORE_PASSWORD`
- `ANDROID_KEY_ALIAS`
- `ANDROID_KEY_PASSWORD`

O certificado de uma nova keystore não será o mesmo do APK antigo. Por isso, para o TWA ser verificado pelo domínio, o `assetlinks.json` publicado em `https://rblx.earth/.well-known/assetlinks.json` precisa conter a impressão digital SHA-256 do certificado usado na nova release.

O APK antigo foi preservado apenas em `legacy/original-app-release.apk`.

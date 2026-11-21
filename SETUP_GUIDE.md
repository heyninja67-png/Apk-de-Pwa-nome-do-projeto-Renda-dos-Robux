# Configuração no GitHub

## 1. Subir o projeto

Envie o conteúdo desta pasta para um repositório GitHub.

Não é necessário colocar o APK antigo como arquivo de release; ele está em `legacy/` apenas como referência.

## 2. Executar a compilação

GitHub → Actions → Build Renda dos Robuxs APK → Run workflow.

Sem secrets de assinatura, o workflow sempre gera:
`Renda-dos-Robuxs-debug-apk`

## 3. Release assinada

Crie uma keystore permanente e converta para Base64:

```bash
base64 -w 0 release.keystore > release.keystore.b64
```

Depois crie os quatro GitHub Secrets indicados no README.

## 4. Digital Asset Links

O arquivo do projeto está em:
`website/.well-known/assetlinks.json`

Ele deve ser publicado no servidor como:
`https://rblx.earth/.well-known/assetlinks.json`

A impressão digital precisa corresponder à chave que assina o APK de produção.

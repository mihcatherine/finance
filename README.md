# Organização Financeira — V5

Versão PWA do aplicativo Organização Financeira.

## Estrutura do GitHub Pages

Envie estes arquivos diretamente para a raiz do repositório:

- index.html
- app.js
- styles.css
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png

Não use uma pasta `icons/`. Os ícones ficam na raiz.

## Appwrite

Endpoint: https://nyc.cloud.appwrite.io/v1
Projeto: 6b01e299000b19ac36ce
Banco: 6b01e350001ca47807e5

O aplicativo usa as tabelas existentes `profiles`, `settings`, `transactions`, `goals`, `accounts`, `categories`, `bills` e `cards`.

## Importante sobre despesas fixas

A configuração de despesas fixas nesta versão fica vinculada ao dispositivo/navegador por enquanto, porque a tabela `bills` existente não possui campos suficientes para armazenar limite mensal e forma de pagamento sem alterar o schema. Cartões, contas, categorias, lançamentos, metas e configurações de salário são persistidos no Appwrite.

## Cartões

A área Cartões permite adicionar, editar, renomear, alterar limite, fechamento e vencimento e excluir cartões sem lançamentos vinculados.

Compras lançadas com `CARD:<id>` alimentam automaticamente a fatura e o limite disponível do cartão.

## PWA

Abra pelo Chrome em HTTPS e use `Instalar aplicativo` ou `Adicionar à tela inicial`. Se uma versão anterior ficar em cache, feche o PWA e abra novamente pelo navegador para o Service Worker V5 atualizar.

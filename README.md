# Organização Financeira — V3

Versão PWA conectada ao Appwrite, com autenticação e persistência de dados por usuário.

## O que esta versão entrega
- Login e cadastro com Appwrite Authentication.
- Recuperação de senha por e-mail.
- Sessão persistente do Appwrite.
- Lançamentos persistidos em `transactions`.
- Configuração de salário/adiantamento persistida em `settings`.
- Despesas fixas persistidas em `bills`.
- Cartões persistidos em `cards`.
- Contas persistidas em `accounts`.
- Categorias com limite mensal persistidas em `categories`.
- Meta de investimento persistida em `goals`.
- Fatura do cartão calculada pelos lançamentos marcados como cartão.
- Saldo disponível separado da fatura do cartão.
- PWA com atualização automática do Service Worker.
- Instalação pela tela inicial do Android quando o navegador oferecer o prompt.

## Banco usado
Endpoint: https://nyc.cloud.appwrite.io/v1
Projeto: 6b01e299000b19ac36ce
Database: 6b01e350001ca47807e5

## Importante sobre o esquema atual
O banco existente ainda não possui `card_id` e `account_id` em `transactions`. Por isso, a V3 usa `payment_method` para distinguir Pix de cartão e calcula a fatura agregando os lançamentos de cartão. Para suportar múltiplos cartões com faturas independentes, o próximo ajuste de schema recomendado é adicionar `card_id` e `account_id` à tabela `transactions`.

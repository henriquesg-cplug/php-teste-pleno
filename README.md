# Teste Técnico: API de Controle de Estoque e Vendas

## Objetivo

Desenvolver uma API REST utilizando Laravel que gerencie um módulo simplificado de controle de estoque e vendas para um ERP.

## Requisitos Técnicos

- Laravel 10+
- PHP 8.1+
- Banco de dados à sua escolha (MySQL, PostgreSQL, SQLite)
- Testes unitários com PHPUnit

## Funcionalidades

### 1. Gerenciamento de Estoque
- Registrar entrada de produtos no estoque com suas respectivas quantidades e preços de custo
- Consultar o estoque atual com valores totais e lucro projetado

### 2. Processamento de Vendas
- Registrar uma venda com diversos itens, calculando automaticamente o valor total e a margem de lucro
- Consultar os detalhes de uma venda

## Requisitos Obrigatórios

1. Implementar um evento que seja disparado quando uma venda for finalizada (atualizando o estoque)
2. Processar o cálculo de estatísticas de vendas
3. Aplicar testes unitários para as principais funcionalidades
4. Utilize a estrutura de arquivos que melhor convenha, pensando no desenvolvimento em equipe
5. Deve pensar em escalabilidade, aplique as melhores práticas para que isso aconteça

## Endpoints

```
POST /api/inventory (Registrar entrada de produtos no estoque)
GET /api/inventory (Obter situação atual do estoque)
POST /api/sales (Registrar uma nova venda)
GET /api/sales/{id} (Obter detalhes de uma venda específica)
```

## Estrutura da Base de Dados

1. **products**: 
   - id, sku, name, description, cost_price, sale_price, created_at, updated_at

2. **inventory**:
   - id, product_id, quantity, last_updated, created_at, updated_at

3. **sales**:
   - id, total_amount, total_cost, total_profit, status, created_at, updated_at

4. **sale_items**:
   - id, sale_id, product_id, quantity, unit_price, unit_cost, created_at, updated_at

## Dados para Teste

A aplicação deve incluir dados mocados para 5 produtos diferentes com seus respectivos preços de custo e venda.

## Entrega

1. Repositório Git público (GitHub, GitLab, Bitbucket)
2. README básico com instruções de instalação e execução

## Prazo

48 horas a partir do recebimento do teste.

Enviar para o e-mail: henrique.souza@cplug.com.br o link do repositório público.

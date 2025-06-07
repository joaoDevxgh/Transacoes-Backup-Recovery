# 🛒 E-commerce Database Project

Este projeto consiste em um sistema de banco de dados para um ambiente de e-commerce, com foco em:

- Criação de tabelas normalizadas
- Relacionamentos entre entidades
- Execução de transações manuais
- Procedures com controle de erro (ROLLBACK / SAVEPOINT)
- Backup e recuperação do banco com `mysqldump`
- Consultas úteis para análise

---

## 🗃️ Estrutura do Banco de Dados

O banco de dados `ecommerce` foi projetado com as seguintes tabelas principais:

- `clients` – Clientes
- `products` – Produtos
- `orders` – Pedidos
- `payments` – Pagamentos
- `productStorage` – Estoque
- `suppliers` – Fornecedores
- `sellers` – Vendedores
- Tabelas associativas para relacionamento N:N:
  - `productOrder`, `productSeller`, `productSupplier`, `productStorageLocation`

---

## ✅ Parte 1 – Transações Manuais

Transação com múltiplas instruções SQL executadas com **controle explícito**:

```sql
SET autocommit = 0;
START TRANSACTION;

-- Inserção de cliente
-- Inserção de pedido associado

COMMIT;

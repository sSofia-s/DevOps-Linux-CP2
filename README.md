# 📦 API de Transações

Esta API tem como objetivo gerenciar transações financeiras, permitindo operações de **consulta, criação, atualização e remoção** de registros.

---

## 🚀 Como acessar a API

### 🔹 Localhost

```
http://localhost:8080/api/transacoes
```

### 🔹 Rede

```
http://192.168.15.86:8080/api/transacoes
```

---

## 📊 Estrutura de uma Transação

```json
{
  "id": 1,
  "descricao": "Depósito bancário",
  "valor": 1500,
  "dataTransacao": "2025-06-01T10:00:00"
}
```

### Campos:

* `id` → Identificador da transação
* `descricao` → Descrição da operação
* `valor` → Valor (positivo = entrada, negativo = saída)
* `dataTransacao` → Data e hora da transação

---

## 🔗 Endpoints

### 📥 GET - Listar transações

```
GET /api/transacoes
```

Retorna todas as transações cadastradas.

---

### ➕ POST - Criar nova transação

```
POST /api/transacoes
```

#### Exemplo:

```json
{
  "descricao": "Compra no supermercado",
  "valor": 150.75
}
```

---

### ✏️ PUT - Atualizar transação

```
PUT /api/transacoes/{id}
```

#### Exemplo:

```json
{
  "descricao": "Compra no supermercado - ALTERADO",
  "valor": 150.76,
  "dataTransacao": "2024-06-18T00:00:00"
}
```

---

### ❌ DELETE - Remover transação

```
DELETE /api/transacoes/{id}
```

---

## 🧠 Funcionamento

A API:

* Recebe requisições HTTP
* Processa os dados das transações
* Persiste as informações em banco de dados
* Retorna os resultados em formato JSON

---

## 🐳 Execução com Docker

A aplicação roda em container Docker, garantindo:

* Isolamento do ambiente
* Facilidade de execução
* Portabilidade

---

## ✅ Status

✔️ API funcionando
✔️ Persistência em banco de dados
✔️ Acesso via localhost e rede

---

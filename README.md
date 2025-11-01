# Sistema-de-Games
Projeto acadêmico desenvolvido em Java para cadastro de jogos, clientes e vendas, aplicando conceitos de orientação a objetos.

---

## 🧠 Estrutura das Classes

| Classe | Função Principal |
|--------|------------------|
| **Main.java** | Classe principal que contém o menu e controla toda a execução do sistema. |
| **Jogo.java** | Representa os jogos disponíveis, com atributos como ID, título, gênero, ano, preço e status. |
| **Cliente.java** | Classe abstrata que define os atributos e métodos comuns a todos os tipos de clientes. |
| **ClienteRegular.java** | Herda de `Cliente`, aplica desconto de 5% nas compras. |
| **ClientePremium.java** | Herda de `Cliente`, aplica desconto de 10% nas compras. |
| **Venda.java** | Registra as informações de uma venda (cliente, jogo, valor final e data). |
| **SaldoInsuficienteException.java** | Exceção personalizada lançada quando o cliente não possui saldo suficiente. |

---

## 🧾 Roteiro de Teste

> Abaixo está um exemplo de como testar o sistema passo a passo pelo console.

### **1️⃣ Cadastrar um jogo**

- ID do jogo: 1
- Título: The Witcher 3
- Gênero: RPG
- Ano de lançamento: 2015
- Preço: 100,00

✅ Saída esperada:

Jogo cadastrado.


### **2️⃣ Cadastrar um cliente**
- ID do cliente: 1
- Nome: Lucas
- E-mail: lucas@email.com
- Saldo inicial: 150,00
- Tipo de cliente: 1- Regular | 2- Premium
- Digite o tipo: 2

✅ Saída esperada:

Cliente cadastrado.

### **3️⃣ Realizar uma venda**

- ID do cliente: 1
- ID do jogo: 1


✅ Saída esperada:

Venda realizada:  Venda #1 | Lucas comprou 'The Witcher 3' por R$100,00 em 31/10/2025 21:45

### **4️⃣ Exibir histórico de compras**

- ID do cliente: 1

✅ Saída esperada:

=== Histórico de Compras de Lucas ===

Venda #1 | Lucas comprou 'The Witcher 3' por R$100,00 em 31/10/2025 21:45

### **5️⃣ Saldo insuficiente**

- ID do cliente: 1 (neste exemplo o saldo de Lucas deve estar menor para realizar o teste)
- ID do jogo: 1

✅ Saída esperada:

Falha: Saldo insuficiente para realizar o saque.

---

## ⚠️ Observações Importantes

- Ao digitar valores com casas decimais, **use vírgula ( , )**  
  Exemplo: `60,00` e não `60.00`

- O ano do jogo deve ser **menor ou igual a 2025**, caso contrário o sistema exibirá uma exceção.

- Clientes com saldo insuficiente não conseguem realizar a compra (exceção `SaldoInsuficienteException`).

---

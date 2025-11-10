# 🚗 Projeto: Cálculo de Aluguel de Carros (Java)

Projeto desenvolvido em **Java** com base no curso de *Programação Orientada a Objetos com Java* (Nelio Alves).  
O objetivo é calcular o valor de um aluguel de carro considerando a duração (em horas ou dias) e aplicando imposto sobre o valor total.

---

## 📋 Funcionalidades

- Leitura dos dados do aluguel:
  - Modelo do carro
  - Data/hora de retirada e devolução
  - Preço por hora e por dia
- Cálculo automático da fatura:
  - Pagamento básico (por hora ou por dia)
  - Imposto (15% sobre o valor total, conforme regra da `BrazilTaxService`)
  - Total com imposto incluso

---

## 💡 Lógica de Cálculo

Exemplo de execução:

Entre com os dados do aluguel:
Modelo do carro: Civic
Retirada (dd/MM/yyyy HH:mm): 25/06/2018 10:30
Retorno (dd/MM/yyyy HH:mm): 27/06/2018 11:40
Entre com o preço por hora: 10.00
Entre com o preço por dia: 130.00

Cálculo:
- Duração total: 2 dias + 1h10min = arredondado para **3 dias**
- Pagamento básico: `3 * 130 = 390.00`
- Imposto (15%): `390 * 0.15 = 58.50`
- **Total: 448.50**

Saída esperada:
FATURA:
Pagamento básico: 390.00
Imposto: 58.50
Pagamento total: 448.50

---

## 🧱 Estrutura do Projeto

src/
├─ application/
│ └─ Program.java
│
├─ model/
│ ├─ entities/
│ │ ├─ CarRental.java
│ │ ├─ Vehicle.java
│ │ └─ Invoice.java
│ │
│ └─ services/
│ ├─ RentalService.java
│ ├─ BrazilTaxService.java
│ └─ TaxService.java (interface opcional)
│
└─ README.md


---

## ⚙️ Como Executar

1. Compile e execute o projeto no Eclipse, IntelliJ ou terminal:
   ```bash
   javac application/Program.java
   java application.Program
   
2. Insira os dados conforme solicitado no console.

3. O sistema exibirá a fatura final com o pagamento básico, imposto e total.

🧮 Classes Principais

Classe - Função
Program	- Ponto de entrada. Lê dados do usuário e instancia os serviços.
CarRental	- Representa o aluguel, com data de início, fim e veículo.
Vehicle	- Representa o carro alugado.
Invoice	- Representa a fatura com valores de pagamento e imposto.
RentalService	- Faz o cálculo do pagamento básico e delega o cálculo do imposto.
BrazilTaxService - Implementa o cálculo do imposto (15%).

🧠 Conceitos Envolvidos

Programação Orientada a Objetos (POO)

Encapsulamento

Composição de objetos

Injeção de dependência

Manipulação de datas com LocalDateTime e Duration

🧾 Exemplo de Saída Final

FATURA:
Pagamento básico: 390.00
Imposto: 58.50
Pagamento total: 448.50

👨‍💻 Autor

Luiz Pizzi
Estudante de Ciência da Computação
Desenvolvedor Back-end Java + Spring Boot 🚀

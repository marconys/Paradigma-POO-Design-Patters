# Paradigma-POO-Design-Patters
Anotações para reforço de estudos

# 📦 Pilares da Programação Orientada a Objetos (POO)

## Observação importante
Clássicamente, são **4 pilares**, não 5.

---

## 1. Abstração

- Focar no que o objeto faz, e não como ele faz  
- Expor apenas o necessário  
- Geralmente aplicada com **interfaces** ou **classes abstratas**

📌 **Exemplo:**  
Você sabe que um `Pagamento` pode ser processado, mas não precisa saber se é **Pix**, **Cartão** ou **Boleto**.

---

## 2. Encapsulamento

- Proteger os dados internos do objeto  
- Controlar acesso por meio de modificadores de acesso (`private`, `protected`, `public`)  
- Evita estados inválidos

📌 **Exemplo:**  
Não deixar alguém alterar diretamente o saldo de uma conta sem validação.

---

## 3. Herança

- Permite que uma classe herde comportamentos e atributos de outra  
- Representa a relação **“é um”**

📌 **Exemplo:**  
`Motoboy` é um `Funcionario`.

---

## 4. Polimorfismo

- Objetos diferentes respondem de formas diferentes à mesma chamada de método  
- Muito ligado a **interfaces** e **sobrescrita de métodos**

📌 **Exemplo:**  
`ProcessarPagamento()` funciona de forma diferente para **Pix**, **Cartão** ou **Boleto**.

# 🧱 Princípios do SOLID

O **SOLID** é um conjunto de **5 princípios de design de software** que ajudam a criar sistemas mais **manuteníveis, flexíveis e fáceis de evoluir**, especialmente em programação orientada a objetos.

---

## S — Single Responsibility Principle (SRP)

**Princípio da Responsabilidade Única**

- Uma classe deve ter **um único motivo para mudar**
- Cada classe deve ter **uma única responsabilidade**

📌 **Exemplo:**  
Uma classe `Relatorio` deve apenas gerar o relatório,  
e não se preocupar com salvar em arquivo ou enviar por e-mail.

---

## O — Open/Closed Principle (OCP)

**Princípio do Aberto/Fechado**

- Entidades de software devem estar **abertas para extensão**
- Mas **fechadas para modificação**

📌 **Exemplo:**  
Para adicionar um novo tipo de pagamento, cria-se uma nova classe  
sem alterar as classes já existentes.

---

## L — Liskov Substitution Principle (LSP)

**Princípio da Substituição de Liskov**

- Uma classe filha deve poder **substituir a classe pai**
- Sem quebrar o comportamento esperado do sistema

📌 **Exemplo:**  
Se `CartaoCredito` herda de `Pagamento`,  
ela deve poder ser usada em qualquer lugar onde um `Pagamento` é esperado.

---

## I — Interface Segregation Principle (ISP)

**Princípio da Segregação de Interfaces**

- Clientes não devem ser forçados a depender de interfaces que não usam
- Prefira **interfaces menores e específicas**

📌 **Exemplo:**  
É melhor ter interfaces separadas como `IImpressora` e `IScanner`  
do que uma interface grande que obrigue todas as classes a implementar tudo.

---

## D — Dependency Inversion Principle (DIP)

**Princípio da Inversão de Dependência**

- Módulos de alto nível não devem depender de módulos de baixo nível
- Ambos devem depender de **abstrações**
- Abstrações não devem depender de detalhes, detalhes dependem de abstrações

📌 **Exemplo:**  
Uma classe de serviço depende de uma interface `IRepositorio`,  
e não de uma implementação concreta como `RepositorioSql`.

---

## 📌 Conclusão

Aplicar os princípios do **SOLID** ajuda a:

- Reduzir acoplamento
- Aumentar coesão
- Facilitar testes
- Tornar o código mais flexível e sustentável a longo prazo


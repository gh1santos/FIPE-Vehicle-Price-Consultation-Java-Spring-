Aqui está o README.md completo e profissional para o seu projeto FIPE Cars Consultant.

Este modelo destaca a interatividade do terminal e o uso da Stream API, que são pontos fortes de projetos Java de linha de comando.

Markdown
# FIPE Vehicle Consultant

![Java](https://img.shields.io/badge/Java-17%2B-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=for-the-badge&logo=springboot)
![API](https://img.shields.io/badge/REST%20API-Consumptions-blue?style=for-the-badge&logo=postman)

Uma aplicação interativa de linha de comando (CLI) desenvolvida em **Java** e **Spring Boot** para consulta de preços médios de veículos, utilizando a **API da FIPE**.

---

## Funcionalidades

* **Consulta Multimodal:** Suporte para Carros, Motos e Caminhões.
* **Filtro Inteligente:** Permite filtrar modelos por trechos do nome (ex: "Palio").
* **Histórico de Preços:** Retorna a cotação FIPE para todos os anos disponíveis de um modelo específico.
* **Fluxo Interativo:** Simula a experiência do site oficial via terminal.
* **Desserialização Genérica:** Uso de Jackson para converter JSON em objetos Java de forma dinâmica.

---

## 🛠️ Tecnologias Utilizadas

* **Java 17+**
* **Spring Boot 3.x**
* **Maven** (Gerenciamento de dependências)
* **Jackson** (Processamento de JSON)
* **Java Streams & Collections** (Manipulação e filtragem de dados)

---

## 🔄 Fluxo da Aplicação

1. **Seleção de Tipo:** O usuário escolhe entre `Carros`, `Motos` ou `Caminhões`.
2. **Listagem de Marcas:** O sistema consome a API e exibe as marcas disponíveis.
3. **Seleção de Marca:** O usuário insere o código da marca desejada.
4. **Filtro de Modelos:** O usuário digita um trecho do nome do veículo para filtrar as opções.
5. **Seleção de Modelo:** O usuário escolhe o código do modelo específico.
6. **Resultado Final:** A aplicação exibe os preços de cada ano/combustível cadastrado para aquele modelo.

---

## 📂 Estrutura do Projeto

```text
src/main/java/com/ghdev/fipeconsultant
├─ model       # Records e Classes de domínio (Brand, Model, Vehicle)
├─ service     # Consumo da API (HttpClient) e Conversor de Dados (Jackson)
├─ principal   # Lógica principal de interação com o usuário
└─ main        # Ponto de entrada da aplicação
🌐 API Utilizada
O projeto consome a FIPE API de Deivid Fortuna, utilizando os seguintes endpoints:

.../{tipo}/marcas

.../{tipo}/marcas/{codMarca}/modelos

.../{tipo}/marcas/{codMarca}/modelos/{codModelo}/anos

🚀 Como Executar
Clonar o repositório:

Bash
git clone [https://github.com/seu-usuario/fipe-consultant.git](https://github.com/seu-usuario/fipe-consultant.git)
Importar na IDE: Abra o projeto no IntelliJ IDEA ou VS Code.

Rodar a aplicação: Execute a classe Main.java.

Interagir: Siga as instruções que aparecerão no terminal.

📊 Exemplo de Saída
Plaintext
Marca Selecionada: Fiat
Modelo Selecionado: Palio Weekend Stile 1.6 mpi 16V 4p
Avaliações por ano encontradas:
   - 2003 Gasolina: R$ 18.200,00
   - 2004 Gasolina: R$ 19.000,00
   - 2005 Gasolina: R$ 20.100,00
📫 Desenvolvido por GHDev


http://googleusercontent.com/interactive_content_block/0

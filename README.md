This project is a command-line Java application that allows users to consult the average vehicle price using the FIPE API.

The application simulates the workflow of the official FIPE website, allowing the user to select a vehicle type, brand, and model, returning the price information for all available years of that model.

The project was built focusing on API consumption, JSON deserialization, and collection manipulation in Java.

📌 Technologies Used
Java
Spring Boot
Maven
Jackson (JSON processing)
REST API
Scanner (terminal input)
⚙️ Features

The application allows the user to:

Select a vehicle type
Cars
Motorcycles
Trucks
List all available brands
Select a brand by its code
List models of the selected brand
Filter models by a part of the model name
Select a specific model
Retrieve FIPE prices for all available years
🔄 Application Flow

The application follows this workflow:

1️⃣ The user selects the vehicle type

car
motorcycle
truck

2️⃣ The application requests the API and lists all available brands

3️⃣ The user selects a brand using its code

4️⃣ The application lists all models from that brand

5️⃣ The user types a part of the model name

Example:

PALIO

6️⃣ The application filters and shows only models that contain the typed term

7️⃣ The user selects a specific model using its code

8️⃣ The application retrieves FIPE price data for all available years of that model

🌐 API Used

This project consumes the public FIPE API:

https://deividfortuna.github.io/fipe/

Endpoints used

List brands

https://parallelum.com.br/fipe/api/v1/carros/marcas
https://parallelum.com.br/fipe/api/v1/motos/marcas
https://parallelum.com.br/fipe/api/v1/caminhoes/marcas

List models

https://parallelum.com.br/fipe/api/v1/carros/marcas/{brandCode}/modelos

List available years

https://parallelum.com.br/fipe/api/v1/carros/marcas/{brandCode}/modelos/{modelCode}/anos

Get FIPE price

https://parallelum.com.br/fipe/api/v1/carros/marcas/{brandCode}/modelos/{modelCode}/anos/{yearCode}
🧠 Concepts Practiced

During the development of this project, the following concepts were applied:

REST API consumption
JSON deserialization using Jackson
Java Collections (List)
Stream API filtering
Loops and control structures
Domain modeling
User interaction through the terminal
📂 Project Structure
src
 ├── model
 │    ├── Brand.java
 │    ├── Model.java
 │    └── Vehicle.java
 │
 ├── service
 │    ├── ApiConsumer.java
 │    └── DataConverter.java
 │
 └── main
      └── Main.java
▶️ How to Run the Project

2️⃣ Open the project in your IDE (IntelliJ or VS Code)

3️⃣ Run the main class

JavaScreenmatchWebApplication

4️⃣ Interact with the application through the terminal

📊 Example Output
Selected brand: Fiat

Selected model: Palio Weekend Stile 1.6 mpi 16V 4p

Available price evaluations:

2003 - R$ 18,200
2004 - R$ 19,000
2005 - R$ 20,100
🎯 Project Purpose

This project was developed to practice API consumption, data manipulation, and backend development using Java, simulating a real-world vehicle price consultation system.

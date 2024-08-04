
# Student Registration System

A simple Student Registration System built with ASP.NET Core and PostgreSQL. This project provides an API for managing student records, including creating, reading, updating, and deleting student information.

## Features

- **CRUD Operations**: Create, Read, Update, and Delete student records.
- **PostgreSQL Integration**: Uses PostgreSQL as the database backend.
- **Swagger Integration**: Provides API documentation and testing interface via Swagger.
- **Entity Framework Core**: Utilizes EF Core for data access and migrations.

## Technologies Used

- **ASP.NET Core 8**: Framework for building the web API.
- **Entity Framework Core**: ORM for data access.
- **PostgreSQL**: Database server.
- **Swashbuckle**: Library for generating Swagger API documentation.

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [PostgreSQL 15](https://www.postgresql.org/download/)
- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) (or any other IDE)

### Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/harxite/Student_Registration.git
   cd Student_Registration
   ```

2. **Install Dependencies**

   Run the following commands to restore the project dependencies:

   ```bash
   dotnet restore
   ```

3. **Configure PostgreSQL**

   - Make sure PostgreSQL is installed and running.
   - Create a new database named `studentregistrationsystem`.
   - Update the `appsettings.json` file with your PostgreSQL connection string:

     ```json
     {
       "ConnectionStrings": {
         "DefaultConnection": "Host=localhost;Database=studentregistrationsystem;Username=postgres;Password=your_password;Port=5432"
       }
     }
     ```

4. **Apply Migrations**

   Run the following commands to create and apply migrations:

   ```bash
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```

5. **Run the Application**

   ```bash
   dotnet run
   ```

   The application will start, and you can access the Swagger UI at:

   ```
   https://localhost:5001/swagger/index.html
   ```

## Usage

- **GET /api/student**: Retrieves a list of all students.
- **GET /api/student/{id}**: Retrieves a student by ID.
- **POST /api/student**: Creates a new student.
- **PUT /api/student/{id}**: Updates an existing student by ID.
- **DELETE /api/student/{id}**: Deletes a student by ID.


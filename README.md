RazorPagesMovie

A simple ASP.NET Core Razor Pages application for managing a list of movies. Includes CRUD operations, search and filter functionality, and validation for input fields.

Features

Movie Management (CRUD):

Create, Read, Update, Delete movies.

Search and Filter:

Search movies by title.

Filter movies by genre using a dropdown.

Default Display:

Shows “Ghostbusters” movie on first page load as per tutorial example.

Rating Field:

Added Rating property to movies.

CRUD pages display and allow editing of ratings.

Validation:

Added [Required], [StringLength], [RegularExpression], and [Range] attributes.

Ensures valid input for Title, Genre, Price, and Rating.

Seed Data:

Preloaded movies include title, release date, genre, price, and rating.

Technologies Used

ASP.NET Core Razor Pages

Entity Framework Core (Code First)

SQL Server (localdb)

C#

Setup Instructions

Clone the repository:

git clone <your-repo-url>


Open in Visual Studio

Ensure .NET 6 SDK or later is installed.

Apply Migrations

Open Package Manager Console and run:

Add-Migration Rating
Update-Database


Run the application

Press F5 or run via terminal:

dotnet run


Access the Movies page

Navigate to https://localhost:5001/Movies (port may vary).

Use search and genre filters.

Database Schema
Column	Type	Validation
Id	int	Primary key
Title	string	Required, 3–60 characters
ReleaseDate	DateTime	Date format
Genre	string	Required, up to 30 characters, starts with uppercase
Price	decimal	1–100, currency format
Rating	string	Required, up to 5 characters, starts with uppercase
Migration

Created migration Rating to add the new Rating column to the database.

Updated SeedData to include Rating for all preloaded movies.

##TvMazeScraper
TvMazeScraper is an ASP.NET Core application that scrapes data from the TVMaze API and stores TV shows along with their cast information into a SQL Server database. This application demonstrates the use of ASP.NET Core Web API, Entity Framework Core, and SQL Server.

#Database Schema
The application uses the following tables:

TVShows Table
  Id	int	Primary key
  Name	string	

CastMembers Table
  Id	int	Primary key
  Name	string	
  Birthday	DateTime	
  TVShowId	int	Foreign key, references TVShows.Id.

#Troubleshooting
Common Issues
500 Internal Server Error during POST /scrape:

Check the logs for detailed error messages.
Ensure the database connection string is correct and the database is accessible.
Make sure the TVMaze API is reachable and responding as expected.

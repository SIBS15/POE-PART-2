# EF Core Migration Notes

The migration is generated locally using the actual project model:
`dotnet ef migrations add InitialRaceDayDatabase` then `dotnet ef database update`.

Review the generated migration before applying it. It should create Users, Events, Categories, Enrolments, Results, Payments and `__EFMigrationsHistory`. The SQL reference script drops/recreates the database; do not run it on a database containing data you need.

The environment that prepared this ZIP did not have the .NET SDK or SQL Server, so no generated migration has been falsely represented as locally compiled/verified.

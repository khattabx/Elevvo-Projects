# SQL Process

## Data Base Creation

Once the database script was downloaded and initialized in MySQL Workbench, the subsequent queries were executed to address these questions.

```sql
USE chinook;
```

### Q1 - Top-Selling Products?

- Retrieves the top 10 best-selling tracks by total quantity sold, including their names, total units sold, and total revenue generated.

```sql
SELECT
    T.Name AS ProductName,
    SUM(IL.Quantity) AS TotalQuantitySold,
    SUM(IL.Quantity * IL.UnitPrice) AS TotalRevenue
FROM
    InvoiceLine AS IL
JOIN
    Track AS T ON IL.TrackId = T.TrackId
GROUP BY
    T.Name
ORDER BY
    TotalQuantitySold DESC
LIMIT 10;
```

### Q2 - Revenue Per Region?

- Calculates total revenue per country (region), returning a list of regions ordered by highest revenue.

```sql
SELECT
    I.BillingCountry AS Region,
    SUM(I.Total) AS TotalRevenue
FROM
    Invoice AS I
GROUP BY
    I.BillingCountry
ORDER BY
    TotalRevenue DESC;
```

### Q3 - Monthly Performance?

- Calculates monthly revenue by formatting invoice dates (YYYY-MM), summing total sales per month, and ordering results chronologically.

```sql
SELECT
    DATE_FORMAT(InvoiceDate, '%Y-%m') AS SalesMonth,
    SUM(Total) AS MonthlyRevenue
FROM
    Invoice
GROUP BY
    SalesMonth
ORDER BY
    SalesMonth;
```

### Window Function : Top 3 Tracks by UnitPrice within each Genre using ROW_NUMBER

- Retrieves the top 3 most expensive tracks per genre, using ROW_NUMBER to rank tracks within each genre by unit price.

```sql
WITH RankedTracks AS (
    SELECT
        T.Name AS TrackName,
        G.Name AS GenreName,
        T.UnitPrice,
        ROW_NUMBER() OVER (PARTITION BY G.Name ORDER BY T.UnitPrice DESC) AS RankByUnitPrice
    FROM
        Track AS T
    JOIN
        Genre AS G ON T.GenreId = G.GenreId
)
SELECT
    TrackName,
    GenreName,
    UnitPrice
FROM
    RankedTracks
WHERE
    RankByUnitPrice <= 3;
```

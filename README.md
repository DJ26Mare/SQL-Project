# MusicStoreProject using SQL
# 🎵 SQL Music Store Project  

A data-driven project analyzing the **Music Store database** using SQL to extract insights and generate meaningful reports.  

## 🚀 Features & Analysis  
- **Database Exploration:** Queried and analyzed tables related to customers, invoices, tracks, albums, artists, and genres.  
- **Sales Insights:** Identified top-selling artists, most popular genres, and revenue trends.  
- **Customer Segmentation:** Analyzed customer spending patterns based on location and purchase history.  
- **Employee Performance:** Evaluated sales performance of different employees in the store.  
- **Query Optimization:** Improved SQL queries for efficiency and faster data retrieval.  

## 🛠️ Tech Stack  
- **SQL (PostgreSQL/MySQL/SQLite)** – For querying and analyzing the database   
- **MS Excel** – For additional data processing and reporting  

## 📂 Dataset & Schema  
The database consists of multiple tables, including:  
- **Customers** – Stores customer details.  
- **Invoices** – Contains purchase details for each transaction.  
- **Tracks, Albums, Artists** – Information about the music catalog.  
- **InvoiceLine** – Tracks individual items in an invoice.  



## 📊 Sample Queries  
```sql
-- Find the top 5 best-selling artists
SELECT a.Name, COUNT(il.TrackId) AS TotalSales 
FROM InvoiceLine il
JOIN Track t ON il.TrackId = t.TrackId
JOIN Album al ON t.AlbumId = al.AlbumId
JOIN Artist a ON al.ArtistId = a.ArtistId
GROUP BY a.Name
ORDER BY TotalSales DESC
LIMIT 5;
```


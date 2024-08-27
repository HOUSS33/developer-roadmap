# Foreign Key

A foreign key in SQL is a column or group of columns in one table that refers to the primary key of another table. It establishes a link between two tables, enforcing referential integrity and maintaining relationships between related data. Foreign keys ensure that values in the referencing table correspond to valid values in the referenced table, preventing orphaned records and maintaining data consistency across tables. They are crucial for implementing relational database designs and supporting complex queries that join multiple tables.

CREATE TABLE riders (
    "id" INTEGER,
    "name" TEXT,
    PRIMARY KEY("id")
);

CREATE TABLE stations (
    "id" INTEGER,
    "name" TEXT,
    "line" TEXT,
    PRIMARY KEY("id")
);

CREATE TABLE visits (
    "rider_id" INTEGER,
    "station_id" INTEGER,
    FOREIGN KEY("rider_id") REFERENCES "riders"("id"),
    FOREIGN KEY("station_id") REFERENCES "stations"("id")
);

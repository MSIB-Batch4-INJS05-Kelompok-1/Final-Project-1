# Final-Project-1
Final Project 1 Intro to NodeJS by Hacktiv8

## Database Setup
```
CREATE TABLE Users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL,
  "createdAt" TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
  "updatedAt" TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE Reflections (
  id SERIAL PRIMARY KEY,
  success TEXT NOT NULL,
  low_point TEXT NOT NULL,
  take_away TEXT NOT NULL,
  "UserId" INTEGER NOT NULL,
  "createdAt" TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
  "updatedAt" TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY ("UserId") REFERENCES Users(id)
);
```

## How to use
```
npm i
npm start
```

# DB Structure

## Table name

- books
- copies
- loans
- users
- genres
- conditions
  
## Books: Table structure

- ID | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- title | VARCHAR(200) - NOT NULL
- plot | TEXT(500) - NULL
- author | VARCHCHAR(255) - NOT NULL
- year | YEAR - NULL
- series | VARCHAR(50) - NULL
- age_range | VARCHAR(10) - NULL

## Copies: Table Structure

- ID | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- book_id | BIGINT (UNSIGNED)
- isbn | CHAR(13) - UNIQUE - NOT NULL
- publisher | VARCHAR(100) - NULL
- pages | SMALLINT - NULL
- position | VARCHAR(50) - NULL
- available | TINYINT - DEFAULT(0)
- language | CHAR(5) - DEFAULT('it-IT')

## Genres: Table Stucture (many to many)

- id | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- name VARCHAR(20) - NOT NULL
- slug VARCHAR(20) - NOT NULL

## Book_format (many to many)

- ID | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- name VARCHAR(20) - NOT NULL
- slug - NOT NULL

## Loans: Table structure (one many)

- ID | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- copy_id |  BIGINT (UNSIGNED)
- user_id |  BIGINT (UNSIGNED)
- start | DATETIME - NOT NULL
- end | DATETIME - NOT NULL

## Users: Table structure

- id | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- name | VARCHAR(50) NOTNULL
- lastname | VARCHAR(100) NOTNULL
- date_of_bith | DATE NULL
- address VARCHAR() | NOT NULL
- phone_number | VARCHAR(14)
- email | VARCHAR(50) - NOTNULL UNIQUE

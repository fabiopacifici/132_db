# DB Structure

Imparare a modellizzare un'entità della realtà.
In questo esempio, modelliamo una tabella per memorizzare le informazioni riguardanti i `libri` di una biblioteca (non un negozio!).

## Table name

- books
  
## Table structure

- ID | BIGINT - AUTO_INCREMENT - PRIMARY_KEY (UNIQUE, NOTNULL)
- isbn | CHAR(13) - UNIQUE - NOT NULL
- title | VARCHAR(200) - NOT NULL
- plot | TEXT(500) - NULL
- author | VARCHCHAR(255) - NOT NULL
- year | YEAR - NULL
- ?genre (horror)
- ?categories ()
- publisher | VARCHAR(100) - NULL
- pages | SMALLINT - NULL
- series | VARCHAR(50) - NULL
- available | TINYINT - DEFAULT(0)
- position | VARCHAR(50) - NULL
- ?age_range | VARCHAR(10) - NULL
- ?format | VARCHAR(20) - NULL
- language | CHAR(5) - DEFAULT('it-IT')

```js
const books = [
  {
    id: 1,
    isbn: '23234234234',
    title: 'harry potter'
    //...
  }
]

```

## Example Table

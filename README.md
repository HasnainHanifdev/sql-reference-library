# SQL Reference

A compact, JSON-based reference for common SQL database, table, row, and column operations. This project was built as a Git and SQL learning exercise.

## What's included

- Database: create, drop, and rename
- Tables: create, drop, and rename
- Rows: insert, update, and delete
- Columns: add, drop, rename, primary keys, and foreign keys

The statements use placeholders such as `table_name`, `column_name`, and `condition`. Replace them with values appropriate for your schema. SQL syntax can vary between database engines, so check your engine's documentation before using a statement.

## Use the reference

The reference is in [`sql_reference.json`](./sql_reference.json). For example, with Node.js:

```js
const sql = require('./sql_reference.json');

console.log(sql.table.create);
// CREATE TABLE table_name();
```

No dependencies or build step are required.

## Validate the JSON

With Node.js installed, run:

```sh
node -e "JSON.parse(require('node:fs').readFileSync('sql_reference.json', 'utf8')); console.log('Valid JSON');"
```

## Environment file

`sample.env` is a template for local environment variables. Copy it to `.env` if needed and replace the placeholder locally. `.env` is ignored by Git and should never contain values you intend to publish.

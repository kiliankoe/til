# Importing CSV to SQLite

Creating a table from CSV data is very straightforward.

```bash
sqlite3 file.sqlite
sqlite> .mode csv
sqlite> .import data.csv tablename
sqlite> .exit
```

That's it.

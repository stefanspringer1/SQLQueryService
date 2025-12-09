# SQLQueryService

---

⚠️ **NOTE:**

This repository is deprecated; use the following, currently maintained repository instead:

https://github.com/struktaris/SQLQueryService

Note the new version number: The last version of this repository corresponds to version 1.0.0 of the new repository.

---

Execute SQL queries against a PostgreSQL database via REST.

The application needs to be started with an API key. Get the list of arguments using the `--help` argument.

The OpenAPI specification is `Sources/SQLQueryOpenAPI/openapi.yaml`.

Example input:

```json
{
  "parameters" : {
    "apiKey" : "myKey"
  },
  "sql" : "SELECT prename,surname FROM person WHERE age > 30"
}
```

Example output:

```json
{
  "rows" : [
    {
      "prename" : "Stefan",
      "surname" : "Springer"
    }
  ],
  "sql" : "SELECT prename,surname FROM person WHERE age > 30"
}
```

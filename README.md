# Timestamp Microservice

A simple Express.js API that converts dates to Unix timestamps and UTC strings.

This project was completed as part of the freeCodeCamp Back End Development
and APIs certification curriculum.

## API

| Method | Path         | Response                                       |
|--------|--------------|------------------------------------------------|
| GET    | `/api/`      | Current time as `{ unix, utc }`                |
| GET    | `/api/:date` | Parsed date as `{ unix, utc }`                 |

The `:date` parameter accepts a Unix timestamp in milliseconds (e.g.
`1451001600000`), a date string (e.g. `2015-12-25`), or nothing (current time).

## Usage

```bash
npm i
npm start
```

Then open <http://localhost:8000> or test the API:

```bash
curl http://localhost:8000/api/1451001600000
```

Example response:

```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

## License

ISC
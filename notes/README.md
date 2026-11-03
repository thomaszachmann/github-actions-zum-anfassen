# notes – Demo-Anwendung für „GitHub Actions zum Anfassen"

notes-api (Go) speichert Notizen im Speicher oder in Postgres. Im Buch baut, testet,
scannt, signiert und veröffentlicht ein GitHub-Actions-Workflow diese Anwendung.

- `POST /notes` legt eine Notiz an und verlangt den Header `X-API-Key`
  (Laborwert `lab-api-key-123`).
- `GET /notes` listet alle Notizen als JSON, `GET /healthz` antwortet `ok`,
  `GET /version` mit der Version, `GET /metrics` mit Kennzahlen im Prometheus-Format.
- `go test ./...` läuft ohne Datenbank; der Postgres-Test braucht `NOTES_TEST_DB_URL`.

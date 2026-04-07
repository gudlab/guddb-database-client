# GudDB - Database Client

A lightweight, fast database client for VS Code, Cursor, Windsurf, and any compatible editor. Connect to **PostgreSQL**, **MySQL**, and **SQLite** databases directly from your editor.

## Features

### Connect with a URI or JDBC URL
Paste a connection string and GudDB auto-detects the database type and fills in all fields:
- `postgresql://user:pass@host:5432/mydb`
- `mysql://user:pass@host:3306/mydb`
- `mssql://user:pass@host:1433/mydb`
- `mongodb://user:pass@host:27017/mydb`
- `jdbc:postgresql://host:5432/mydb?sslmode=require`

Or fill in host, port, user, and database manually.

### Database Explorer
Browse your database structure in the sidebar — connections, databases, schemas, tables, views, and columns all in a navigable tree.

### Table Data Viewer
Click any table to browse its data with:
- Pagination with configurable page size
- Column sorting
- Inline filtering with SQL WHERE clauses
- Inline cell editing (double-click any cell)
- Row selection, insert, duplicate, and delete
- Syntax-highlighted query bar

### Query Editor
Open `.sql` files with full IntelliSense:
- SQL keyword completions
- Table and column name suggestions
- Syntax highlighting
- Run queries with `Ctrl+Enter` (`Cmd+Enter` on Mac)
- Results displayed in a dedicated grid panel

### Export
Export query results or table data to:
- **CSV** — comma-separated values
- **JSON** — array of objects
- **SQL** — INSERT statements

Choose scope (current page, all rows, selected rows, or custom limit) from the built-in export modal.

### AI Natural Language to SQL
Describe what you want in plain English and get SQL generated automatically.
- **Copilot** — uses VS Code's built-in language model API (requires Copilot subscription)
- **Anthropic Claude** — uses the Claude API (requires API key)

Trigger with `Ctrl+Shift+G` (`Cmd+Shift+G` on Mac) from any `.sql` file.

## Supported Databases

| Database | Status |
|----------|--------|
| PostgreSQL | Full support |
| MySQL | Full support |
| MariaDB | Full support |
| CockroachDB | Full support |
| Microsoft SQL Server | Full support |
| ClickHouse | Full support |
| MongoDB | Read-only (query + browse) |
| ElasticSearch | Read-only (query + browse) |
| SQLite | Full support |

All server-based databases support **SSH tunneling** — connect through a bastion host with key or password authentication.

## Getting Started

1. Install GudDB from the VS Code Marketplace or Open VSX
2. Click the database icon in the activity bar
3. Click **+** to add a connection
4. Paste a connection string or fill in details manually, then click **Save**
5. Click a table to browse data, or right-click to open a query editor

## Configuration

| Setting | Default | Description |
|---------|---------|-------------|
| `guddb.maxResultRows` | `1000` | Maximum rows displayed in query results |
| `guddb.tableView.pageSize` | `50` | Rows per page in table data viewer |
| `guddb.ai.provider` | `copilot` | AI provider: `copilot`, `anthropic`, or `disabled` |

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Enter` / `Cmd+Enter` | Run SQL query |
| `Ctrl+Shift+G` / `Cmd+Shift+G` | Natural language to SQL |

## Support

GudDB Manager is free. If it saves you time, consider supporting development:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/timchosen)

## License

Proprietary - free to use. See LICENSE file for details.

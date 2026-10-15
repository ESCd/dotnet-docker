# .NET in Docker (Enhanced)

## MSSQL

The following images are based on [`mcr.microsoft.com/artifact/mar/mssql/server`](https://mcr.microsoft.com/artifact/mar/mssql/server), merged with binaries from [`mcr.microsoft.com/artifact/mar/dotnet/sdk`](https://mcr.microsoft.com/artifact/mar/dotnet/sdk), with the `dotnet-ef` tool pre-installed.

Useful for multi-team or feature based development, running integration tests, generating migrations, *and more*...

| Image Variant                            | .NET Version | SQL Version   |
| ---------------------------------------- | ------------ | ------------- |
| `escd/dotnet-mssql-sdk:9.0-2025-latest`  | `net9.0`     | `2025-latest` |
| `escd/dotnet-mssql-sdk:9.0-2022-latest`  | `net9.0`     | `2022-latest` |
| `escd/dotnet-mssql-sdk:10.0-2025-latest` | `net10.0`    | `2025-latest` |
| `escd/dotnet-mssql-sdk:10.0-2022-latest` | `net10.0`    | `2022-latest` |
| `escd/dotnet-mssql-sdk:11.0-2025-latest` | `net11.0`    | `2025-latest` |
| `escd/dotnet-mssql-sdk:11.0-2022-latest` | `net11.0`    | `2022-latest` |

> *Images are based on upstream MSSQL images, with the following pre-installed software:*
> - `curl`
> - `dotnet`
> - `dotnet-ef` (.NET Tool)
> - `git`
> - `pwsh` (PowerShell)
> - `sqlcmd` (`/opt/mssql-tools18/bin/sqlcmd`)
> - `wget`

> *Images include a helper script, [`/sql_server.sh`](https://github.com/ESCd/mssql-dotnet-docker/tree/main/etc/sql_server.sh) with the following functions:*
> - `start_sql_server [timeout=120]`: Starts the SQL Server, outputs the Process ID of the server after waiting for it to be available
> - `stop_sql_server`: Shuts down the SQL Server, returns after waiting for process to exit
> - `wait_sql_server_exit`: Wait for the SQL Server process to exit

## WASM

The following images are based on [`mcr.microsoft.com/artifact/mar/dotnet/sdk`](https://mcr.microsoft.com/artifact/mar/dotnet/sdk), with the `wasm-tools` workload pre-installed.

Useful for building Blazor Wasm or .NET Browser projects.

| Image Variant                                  | .NET Version |
| ---------------------------------------------- | ------------ |
| `escd/dotnet-wasm-sdk:8.0`                     | `net8.0`     |
| `escd/dotnet-wasm-sdk:9.0`                     | `net9.0`     |
| `escd/dotnet-wasm-sdk:10.0`                    | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-aot`                | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-noble-amd64`        | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-noble-aot`          | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-noble-aot-amd64`    | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-resolute-amd64`     | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-resolute-aot`       | `net10.0`    |
| `escd/dotnet-wasm-sdk:10.0-resolute-aot-amd64` | `net10.0`    |
| `escd/dotnet-wasm-sdk:11.0`                    | `net11.0`    |
| `escd/dotnet-wasm-sdk:11.0-aot`                | `net11.0`    |
| `escd/dotnet-wasm-sdk:11.0-resolute-amd64`     | `net11.0`    |
| `escd/dotnet-wasm-sdk:11.0-resolute-aot`       | `net11.0`    |
| `escd/dotnet-wasm-sdk:11.0-resolute-aot-amd64` | `net11.0`    |

> *Images are based on upstream dotnet sdk images, with the following pre-installed software:*
> - `curl`
> - `dotnet`
> - `git`
> - `nodejs` (`v26`)
> - `pwsh` (PowerShell)
> - `python3`
> - `wasm-tools` (.NET Workload)
> - `wget`
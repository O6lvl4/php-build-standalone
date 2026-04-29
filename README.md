# php-build-standalone

Pre-built static PHP binaries for every platform. No apt, no brew, no Docker.

## What

Statically linked PHP binaries with a practical set of extensions baked in.
Download, extract, run `php -v`. That's it.

Built with [static-php-cli](https://github.com/crazywhalecc/static-php-cli),
published as GitHub Releases with sha256 checksums.

## Platforms

| Target | Status |
|---|---|
| `aarch64-apple-darwin` (macOS arm64) | ✓ |
| `x86_64-apple-darwin` (macOS Intel) | ✓ |
| `x86_64-unknown-linux-musl` (Linux x86_64) | ✓ |
| `aarch64-unknown-linux-musl` (Linux arm64) | ✓ |

## Included extensions

Practical set that covers Laravel, Symfony, and most modern PHP projects:

```
bcmath, calendar, ctype, curl, dom, fileinfo, filter, iconv,
json, mbstring, mysqlnd, mysqli, openssl, pdo, pdo_mysql,
pdo_sqlite, phar, posix, readline, session, simplexml,
sockets, sodium, tokenizer, xml, xmlreader, xmlwriter,
zip, zlib
```

## Usage

```bash
# Download (example: macOS arm64, PHP 8.4)
curl -fsSL https://github.com/O6lvl4/php-build-standalone/releases/download/php-8.4.20/php-8.4.20-aarch64-apple-darwin.tar.gz | tar xz
./php -v

# Or via qusp
qusp install php 8.4.20
```

## Building locally

```bash
# Requires Docker (Linux) or Homebrew prerequisites (macOS)
./build.sh 8.4.20
```

## License

MIT (this project). PHP itself is under the [PHP License](https://www.php.net/license/).
Bundled libraries retain their respective licenses (OpenSSL: Apache-2.0,
libxml2: MIT, curl: MIT, sqlite3: Public Domain, etc.).

Will eventually be logfmt.io

In the meantime if you have a logfmt related project/post that you would like to link to, please submit a PR to this file.

## EBNFish

```
ident_byte = any byte greater than ' ', excluding '=' and '"'
string_byte = any byte excluding '"' and '\'
garbage = !ident_byte
ident = ident_byte, { ident byte }
key = ident
value = ident | '"', { string_byte | '\', '"' }, '"'
pair = key, '=', value | key, '=' | key
message = { garbage, pair }, garbage
```

## Links

### Posts

* [Brandur's Logfmt post](https://brandur.org/logfmt)

### Code

* [github.com/kr/logfmt](https://github.com/kr/logfmt) Go package ([godoc](https://godoc.org/github.com/kr/logfmt))
* [Node logftm logger and parser](https://github.com/csquared/node-logfmt)
* [github.com/heroku/slog](github.com/heroku/slog) Go package for structured logging ([godoc](https://godoc.org/github.com/heroku/slog))

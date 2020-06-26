# DENO IPFS tests

<div align="center">
<img src="https://ipfs.io/ipfs/QmQKtMcLLnhQxY1pfKjDc1M19zqKq8WDTJhAwSKissVvns"/> + <img src="https://ipfs.io/ipfs/QmWbns85eo4nhZfWdUCWguQn7NTuwKDhPFGRPkCLSEUKSQ"/>
</div>

## Purpose

Let's get DENO work together with IPFS to get it's libraries.

## Phase 1 - Get Deno working

### Install Deno
```
brew install deno
```

### Test installation
```
$ deno run https://deno.land/std/examples/welcome.ts
Welcome to Deno 🦕
```

## Phase 2 - Use IPFS node for source

### Install iPFS
```
$ brew cask install ipfs
```

Start ipfs Desktop

### Store `welcome.ts` on IPFS

```
$ wget https://deno.land/std/examples/welcome.ts
```

```
$ ipfs add welcome.ts
added QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS welcome.ts
```

### Run by using local proxy
```
$ deno run http://127.0.0.1:8080/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS
Download http://127.0.0.1:8080/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS
Welcome to Deno 🦕
```

### Run by using public gateway

> Note: This can take a while (minutes) for new packages to be found...

```
$ deno run https://ipfs.io/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS
Download https://ipfs.io/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS
Welcome to Deno 🦕
```

```
$ deno run https://cloudflare-ipfs.com/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS 
Download https://cloudflare-ipfs.com/ipfs/QmTkMPJ5zrtoYBi7WSFqedF4ttL2ZgJDWrfuAKbXZHchpS
Welcome to Deno 🦕
```

## IPFS-Proxy

Package already known:
<img src="https://ipfs.io/ipfs/QmWEFQb9NApuGSCYjwuhGCUk8J7d5vWDbiqojTwhSBubfr"/>

New package:
<img src="https://ipfs.io/ipfs/QmdpC5RhT2xqE7gtjNLdfkRt3mJQYF7ZCehUf5tHwDov29"/>

Diagrams are made in [https://sequencediagram.org/](https://sequencediagram.org/).
Source is in: [sequence-diagram.uml](./sequence-diagram.uml)

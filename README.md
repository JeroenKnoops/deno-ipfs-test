# DENO tests

## Purpose

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

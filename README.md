# nextbsd.github.io

Source for [nextbsd.org](https://nextbsd.org/) — a GitHub Pages site for the
NextBSD project.

A single static `index.html` plus a `CNAME` for the apex domain. No build
step; GitHub Pages serves `index.html` directly.

## Local preview

```sh
open index.html
# or
python3 -m http.server 8000   # then http://localhost:8000/
```

## Deploying

1. Create the `nextbsd.github.io` repo under the `NextBSD` GitHub org.
2. Push `main` — Pages auto-publishes from the root of `main`.
3. In Pages settings, confirm the custom domain `nextbsd.org` and enable
   "Enforce HTTPS" once the certificate provisions.
4. At the DNS registrar for `nextbsd.org`, add either:
   - four `A` records to GitHub Pages' apex IPs
     (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`), or
   - an `ALIAS`/`ANAME` record to `nextbsd.github.io.` if the registrar supports it.

# Domain configuration

## Nginx

 - `git.*/<repo>` --> `https://github.com/joinemm/<repo>`
 - `sync.*` --> My syncthing cloud instance.
 - `analytics.*` | `pls.*` --> [Plausible](https://plausible.io) analytics, self hosted alternative to google analytics.
 - `digitalocean.*` | `hetzner.*` | `vultr.*` --> Redirects to my affiliate/referral links to these services.
 - any `listen: 80` is redirected to corresponding `listen: 443 ssl` because who is still using http.
 
## DNS

Managed by Namecheap.

 - `A` `*` --> Wildcard domain for any subdomains to be redirected to the nginx server.
 - `A` `@` --> Vercel hosted [website](https://git.joinemm.dev/website).
 - `A` `mc` --> Minecraft server (offline).
 - `SRV` `_minecraft | _tcp | 0 | 5 | 25565 | mc.joinemm.dev` --> Makes that minecraft server work.
 - `CNAME` `www` --> Redirect to `@`.
 - `CNAME` `socials` --> Digitalocean hosted [socials grid](https://git.joinemm.dev/socials-website).

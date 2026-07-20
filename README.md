# noted-redirect

Single purpose: keep `noted.melomaniacstudios.com` alive as a redirect to
**https://notedbymm.com**, which replaced it as NOTED's canonical home.

Old links and PWAs installed from the subdomain (installs are pinned to the
origin they were added from and can't be migrated by a cache bump) land here
and get forwarded.

GitHub Pages is a static host and can't emit a real 301, so the redirect is
`<meta http-equiv="refresh">` plus a `location.replace()` that preserves
path, query and hash. `404.html` is a copy of `index.html`, so *every* path
under the old subdomain redirects, not just the root.

Do not add content here. The custom domain is `noted.melomaniacstudios.com`
(see `CNAME`); the app itself lives in `armiiinsaber/noted`.

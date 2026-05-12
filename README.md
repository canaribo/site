# hubara-template

a [hubara](https://github.com/canaribo/hubara) site.

## structure

```
.
├── .github/workflows/deploy.yml   # deploys to vercel on every push
├── content/                       # pages and posts
│   ├── *.md                       # pages
│   └── posts/
│       └── *.md                   # blog posts
├── static/                        # css, images, etc.
│   └── main.css
└── hubara.yaml                    # site config
```

## setup

1. create a new repo from this template
2. connect the repo to vercel (but disable vercel's own build step — we build in github actions)
3. add these secrets to your repo settings:
   - `VERCEL_TOKEN` — from [vercel.com/account/tokens](https://vercel.com/account/tokens)
   - `VERCEL_ORG_ID` — from your vercel project settings
   - `VERCEL_PROJECT_ID` — from your vercel project settings
4. push to `main` — the site deploys automatically

## local preview

```bash
# install hubara (once)
curl -sL https://github.com/canaribo/hubara/releases/latest/download/hubara-linux-amd64 -o hubara
chmod +x hubara

# build
./hubara

# serve locally
./hubara -serve
```

## write

- add a post: `content/posts/my-post.md`
- add a page: `content/about.md`
- edit config: `hubara.yaml`
- edit styles: `static/main.css`

push to `main` and vercel updates automatically.

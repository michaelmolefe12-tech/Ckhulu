# smartAlgoinstitute

Demo and source for the Smart Algo Institute website.

Files and links

- [Open the demo (index.html)](smart-algo-institute/index.html)
- [Open the source folder](smart-algo-institute/)

Directory contents (summary)

- index.html
- register.html
- thankyou.html
- css/style.css
- js/script.js
- images/
name: Deploy Smart Algo Institute to GitHub Pages
on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Deploy to gh-pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./smart-algo-institute
          publish_branch: gh-pages
          user_name: github-actions[bot]
          user_email: 41898282+github-actions[bot]@users.noreply.github.com
          clean: true

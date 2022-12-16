<div id="badges" align="center">
  <a href="https://www.linkedin.com/in/yash-katiyar-4a222a21a/">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="https://www.instagram.com/yash_katiyar25" align="center">
    <img src="https://img.shields.io/badge/Instagram-red?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge"/>
  </a>
  <a href="https://twitter.com/yash_katiyar25" align="center">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
</div>
<div id="header" align="center">
  <img src="https://komarev.com/ghpvc/?username=yashkatiyar2503&style=flat-square&color=blue" alt=""/>
</div>
<h1 align="center">
  Hi
  <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px"/>
  , I'm YASH KATIYAR
</h1>

### :fire: My Stats :
[![GitHub Streak](http://github-readme-streak-stats.herokuapp.com?user=yashkatiyar2503&theme=dark&background=000000)](https://git.io/streak-stats)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=yashkatiyar2503&layout=compact&theme=vision-friendly-dark)](https://github.com/anuraghazra/github-readme-stats)


name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: {{your_username}}
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

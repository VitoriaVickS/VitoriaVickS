### Olá Sejam Bem-Vindos! 👋

- 🔭 Quality Assurance
- 🌱 Estudante de Análise e Desenvolvimento de Sistemas
- 👯 22 anos
- 📫 Contate -me e-mail: vitoriabiasioli18@gmail.com


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
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  

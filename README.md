
### Olá! Me chamo Felipe Quesada

Tenho 36 anos, trabalhei anos com tecnologia, porém na área de infraestrutura e gestão.
Possuo algumas certificações Microsoft, porém já ultrapassadas como Windows Server 2003 e 2008.
Atualmente estou me voltando a área de desenvolvimento.<br/>
### Abaixo alguma das minhas redes sociais:
[![Streaming](https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white)](https://twitch.tv/saladinoo)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/_fequesada)
[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)]([https://instagram.com/_fequesada](https://www.linkedin.com/in/felipe-xavier-446a1225/))


![Fequesada GitHub stats](https://github-readme-stats.vercel.app/api?username=fequesada&show_icons=true&theme=dracula)

#### Tecnologias que estou estudando
<div style="display: inline-block"><br/>
    <img align="center" alt="html5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
    <img align="center" alt="css3" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
    <img align="center" alt="javascript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
    <img align="center" alt="java" src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white">
    <img align="center" alt="php" src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white">
</div><br/>

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
          github_user_name: devemdobro
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

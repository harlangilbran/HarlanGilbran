<div style="float:right; margin-left:10px;">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=HarlanGilbran.HarlanGilbran" />
</div>

<h1 align="center">
    <img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=35&center=true&vCenter=true&width=500&height=70&duration=4000&lines=Hi+There!+👋;+I'm+Harlan+Gilbran!;" />
</h1>

<h3 align="center">"Currently, I am focusing on learning Front End Development. Every day, I absorb new knowledge and continue to practice. My goal is simple: to become proficient in creating visually appealing and functional interfaces on the web."</h3>

- 🔭 I’m currently working on [web simpel]

- 🌱 I’m currently learning **javascript.visual basic**

- 👯 I’m looking to collaborate on [-]

- 🤝 I’m looking for help with [-]

- 💬 Ask me about **"Ask me about anything! I'm here to help."**

- 📫 How to reach me **harlangilbran10@gmail.com**

- 📄 Know about my experiences [my github]

- ⚡ Fun fact **"Never say tired, but say for Allah."**

<h3 align="left">Connect with me:</h3>
<p align="left">
    <a href="https://instagram.com/harlan_gilbran10" target="_blank" rel="noreferrer">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="harlan_gilbran10" height="30" width="40" />
    </a>
    <a href="https://github.com/HarlanGilbran" target="_blank" rel="noreferrer">
        <img align="center" src="https://www.vectorlogo.zone/logos/github/github-icon.svg" alt="HarlanGilbran" height="30" width="40" />
    </a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left">
    <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer">
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" alt="html" width="40" height="40"/>
    </a>
    <a href="https://git-scm.com/HarlanGilbran" target="_blank" rel="noreferrer">
        <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/>
    </a>
    <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer">
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" alt="css" width="40" height="40"/>
    </a>
    <a href="https://visualstudio.microsoft.com/vs/features/net-development/" target="_blank" rel="noreferrer">
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dotnetcore/dotnetcore-original.svg" alt="dotnet" width="40" height="40"/>
    </a>
    <a href="https://code.visualstudio.com/" target="_blank" rel="noreferrer">
        <img src="https://img.icons8.com/color/48/000000/visual-studio-code-2019.png" alt="vs-code" width="40" height="40"/>
    </a>
</p>
name: Generate Snake

on:
  schedule:
    # Berjalan setiap 6 jam
    - cron: "0 */6 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Generate Snake Animation
        uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: HarlanGilbran
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - name: Set Outputs
        run: |
          echo "::set-output name=gif_path::dist/github-contribution-grid-snake.gif"
          echo "::set-output name=svg_path::dist/github-contribution-grid-snake.svg"
        shell: bash

      - name: Commit and Push Changes
        run: |
          git config --global user.email "actions@github.com"
          git config --global user.name "GitHub Actions"
          git add dist/
          git diff --quiet && git diff --staged --quiet || git commit -m "Update snake contributions"
          git push origin main || { echo "Failed to push changes"; exit 1; }
















# 💫 Welcome to My World

![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=header)

## 🔥 About Me
Hey there! I'm **Vaibhav** - a passionate Full-Stack Developer and AI/ML enthusiast. I've completed an internship as a Full-Stack Developer, building dynamic and scalable web applications. I'm always pushing the boundaries of what's possible with code!

### 💡 Tech Stack
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node-dot-js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)

### ⚡ GitHub Stats
![Vaibhav's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Vaibhav08080&show_icons=true&theme=radical)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Vaibhav08080&layout=compact&theme=radical)
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=Vaibhav08080&theme=radical)

### 💥 Crazy Code Magic
```python
from time import sleep
from random import choice

greetings = ['Hello', 'Hey', 'Hi', 'Hola', 'Bonjour', 'Namaste']
emojis = ['🔥', '💥', '⚡', '🚀', '💻', '✨']

for _ in range(10):
    print(f"{choice(greetings)} World {choice(emojis)}")
    sleep(0.5)
```
name: GitHub Snake Game

on:
  # Schedule the workflow to run daily at midnight UTC
  schedule:
    - cron: "0 0 * * *"
  # Allow manual triggering of the workflow
  workflow_dispatch:
  # Trigger the workflow on pushes to the main branch
  push:
    branches:
      - main
jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      # Step 1: Checkout the repository
      - name: Checkout Repository
        uses: actions/checkout@v3
      # Step 2: Generate the snake animations
      - name: Generate GitHub Contributions Snake Animations
        uses: Platane/snk@v3
        with:
          # GitHub username to generate the animation for
          github_user_name: ${{ github.repository_owner }}
          # Define the output files and their configurations
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
      # Step 3: Deploy the generated files to the 'output' branch
      - name: Deploy to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          # Optionally, you can set a custom commit message
          commit_message: "Update snake animation [skip ci]"

### 🌐 Connect with Me
- 🔗 LinkedIn: [fuck linkedin](#)
- 🐦 Twitter:[@vaibhaavvvvvv](https://x.com/vaibhaavvvvvv)

![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer)


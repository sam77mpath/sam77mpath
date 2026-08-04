<div align="center">
<svg width="1200" height="300" viewBox="0 0 1200 300" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0D1117"/>
      <stop offset="50%" stop-color="#0B1A2E"/>
      <stop offset="100%" stop-color="#0D1117"/>
    </linearGradient>
    <radialGradient id="glowBlue" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#58A6FF" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#58A6FF" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="glowCyan" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#39D0FF" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#39D0FF" stop-opacity="0"/>
    </radialGradient>
    <linearGradient id="textGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#8FD3FF"/>
      <stop offset="50%" stop-color="#58A6FF"/>
      <stop offset="100%" stop-color="#39D0FF"/>
    </linearGradient>
    <filter id="softBlur" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="18"/>
    </filter>
    <linearGradient id="flowGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#0D1117" stop-opacity="0"/>
      <stop offset="35%" stop-color="#1B4DFF" stop-opacity="0.35"/>
      <stop offset="55%" stop-color="#39D0FF" stop-opacity="0.4"/>
      <stop offset="80%" stop-color="#1B4DFF" stop-opacity="0.3"/>
      <stop offset="100%" stop-color="#0D1117" stop-opacity="0"/>
    </linearGradient>
    <filter id="flowBlur" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="14"/>
    </filter>
    <clipPath id="bannerClip">
      <rect width="1200" height="300"/>
    </clipPath>
  </defs>

  <!-- Background -->
  <rect width="1200" height="300" fill="url(#bg)"/>

  <!-- Flowing gradient current behind the name -->
  <g clip-path="url(#bannerClip)" filter="url(#flowBlur)">
    <path fill="none" stroke="url(#flowGrad)" stroke-width="70" opacity="0.9">
      <animate attributeName="d" dur="10s" repeatCount="indefinite"
        values="
          M-200,120 C150,60 350,180 650,110 S1150,60 1400,130;
          M-200,150 C150,190 350,70 650,150 S1150,190 1400,110;
          M-200,120 C150,60 350,180 650,110 S1150,60 1400,130"/>
    </path>
    <path fill="none" stroke="url(#flowGrad)" stroke-width="40" opacity="0.6">
      <animate attributeName="d" dur="13s" repeatCount="indefinite"
        values="
          M-200,170 C200,220 400,110 700,170 S1200,230 1400,160;
          M-200,140 C200,90 400,210 700,140 S1200,80 1400,190;
          M-200,170 C200,220 400,110 700,170 S1200,230 1400,160"/>
    </path>
    <rect width="1200" height="300" fill="url(#bg)" opacity="0">
      <!-- keeps clip bounds honest across renderers -->
    </rect>
  </g>

  <!-- Ambient glow blobs -->
  <circle cx="150" cy="60" r="160" fill="url(#glowBlue)" filter="url(#softBlur)">
    <animate attributeName="cy" values="60;90;60" dur="7s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1080" cy="240" r="200" fill="url(#glowCyan)" filter="url(#softBlur)">
    <animate attributeName="cy" values="240;210;240" dur="8s" repeatCount="indefinite"/>
  </circle>
  <circle cx="620" cy="30" r="120" fill="url(#glowBlue)" filter="url(#softBlur)" opacity="0.5">
    <animate attributeName="opacity" values="0.5;0.8;0.5" dur="5s" repeatCount="indefinite"/>
  </circle>

  <!-- Grid lines (subtle circuit / cloud feel) -->
  <g stroke="#1F2937" stroke-width="1" opacity="0.5">
    <line x1="0" y1="250" x2="1200" y2="250"/>
    <line x1="0" y1="255" x2="1200" y2="255"/>
    <line x1="100" y1="0" x2="100" y2="300" opacity="0.3"/>
    <line x1="1100" y1="0" x2="1100" y2="300" opacity="0.3"/>
  </g>

  <!-- Floating particles -->
  <g fill="#58A6FF">
    <circle cx="80" cy="200" r="2.5">
      <animate attributeName="cy" values="200;170;200" dur="4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;1;0.3" dur="4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="230" cy="250" r="2">
      <animate attributeName="cy" values="250;220;250" dur="5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.2;0.9;0.2" dur="5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="950" cy="60" r="2.5">
      <animate attributeName="cy" values="60;90;60" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.3;1;0.3" dur="6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="1050" cy="120" r="2">
      <animate attributeName="cy" values="120;95;120" dur="4.5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.2;0.8;0.2" dur="4.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="700" cy="255" r="2">
      <animate attributeName="opacity" values="0.2;0.9;0.2" dur="3.5s" repeatCount="indefinite"/>
    </circle>
    <circle cx="400" cy="40" r="2">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="4.2s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- Cloud + node motif (right side) -->
  <g transform="translate(980,150)" opacity="0.9">
    <path d="M0 20 a20 20 0 0 1 0 -40 a28 28 0 0 1 54 -6 a22 22 0 0 1 6 44 z"
          fill="none" stroke="#58A6FF" stroke-width="2.5" opacity="0.8"/>
    <circle cx="-4" cy="0" r="3" fill="#39D0FF"/>
    <circle cx="34" cy="-8" r="3" fill="#39D0FF"/>
    <circle cx="46" cy="14" r="3" fill="#39D0FF"/>
    <line x1="-4" y1="0" x2="34" y2="-8" stroke="#39D0FF" stroke-width="1" opacity="0.6"/>
    <line x1="34" y1="-8" x2="46" y2="14" stroke="#39D0FF" stroke-width="1" opacity="0.6"/>
  </g>

  <!-- Main headline -->
  <text x="60" y="140" font-family="'Segoe UI', 'Fira Code', monospace" font-size="52" font-weight="700" fill="url(#textGrad)">
    Sampath Vishwakarma
  </text>
  <text x="62" y="180" font-family="'Segoe UI', monospace" font-size="24" fill="#8B949E">
    AWS DevOps Engineer &#183; Cloud &amp; Infrastructure Automation
  </text>

  <!-- Tag chips -->
  <g font-family="'Fira Code', monospace" font-size="14" font-weight="600">
    <g transform="translate(62,210)">
      <rect width="72" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="36" y="19" text-anchor="middle" fill="#FF9900">AWS</text>
    </g>
    <g transform="translate(146,210)">
      <rect width="84" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="42" y="19" text-anchor="middle" fill="#39D0FF">Linux</text>
    </g>
    <g transform="translate(242,210)">
      <rect width="92" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="46" y="19" text-anchor="middle" fill="#2496ED">Docker</text>
    </g>
    <g transform="translate(346,210)">
      <rect width="120" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="60" y="19" text-anchor="middle" fill="#326CE5">Kubernetes</text>
    </g>
    <g transform="translate(478,210)">
      <rect width="112" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="56" y="19" text-anchor="middle" fill="#844FBA">Terraform</text>
    </g>
    <g transform="translate(602,210)">
      <rect width="98" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="49" y="19" text-anchor="middle" fill="#D24939">Jenkins</text>
    </g>
    <g transform="translate(712,210)">
      <rect width="92" height="28" rx="14" fill="#161B22" stroke="#30363D"/>
      <text x="46" y="19" text-anchor="middle" fill="#3776AB">Python</text>
    </g>
  </g>
</svg>

<!-- ================= HERO BANNER ================= -->
<img src="assets/banner.svg" alt="Sampath Vishwakarma — AWS DevOps Engineer" width="100%" />

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=2800&pause=1000&color=58A6FF&center=true&vCenter=true&width=780&lines=Hi+there%2C+I'm+Sampath+Vishwakarma+%F0%9F%91%8B;AWS+DevOps+Engineer+%E2%98%81%EF%B8%8F;Cloud+%26+Infrastructure+Automation+Enthusiast;Building+CI%2FCD+Pipelines+with+Jenkins+%26+Docker;Infrastructure+as+Code+with+Terraform+%F0%9F%8F%97%EF%B8%8F;Automating+Today+to+Build+a+Better+Tomorrow." alt="Typing SVG" />

<br/><br/>

<img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" width="260" alt="Coding cat" />

<br/>

<a href="https://www.linkedin.com/in/sampath-vishwakarma-3b73903a6" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-058CFF?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117" />
</a>
<a href="mailto:sampathpammi88@gmail.com">
  <img src="https://img.shields.io/badge/Email-058CFF?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" />
</a>
<a href="https://github.com/sam77mpath" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-058CFF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" />
</a>

<br/><br/>

<img src="https://komarev.com/ghpvc/?username=sam77mpath&label=Profile%20Views&color=058CFF&style=for-the-badge" alt="Profile Views" />

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🧊 About Me

<table width="100%">
<tr>
<td width="50%" valign="top">

### 🎯 Who I Am
- 🎓 B.Tech Computer Science Engineering student, JNTUK
- ☁️ Focused on **AWS Cloud** & **DevOps Engineering**
- 🛠️ Building real-world infra with **Linux, Docker, Kubernetes, Terraform & Jenkins**
- 📍 Based in Vijayawada, India

</td>
<td width="50%" valign="top">

### 🎯 What I'm Looking For
- AWS DevOps Engineer Intern
- DevOps Engineer / Cloud Engineer
- Site Reliability Engineer (SRE)
- Open Source Contributor roles

</td>
</tr>
</table>

> *"Automating today to build a better tomorrow."*

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🛠️ Tech Stack

<div align="center">

**Languages**
<br/>
<img src="https://skillicons.dev/icons?i=python,bash,yaml,mysql,html,css&theme=dark" />

**Cloud & Infrastructure**
<br/>
<img src="https://skillicons.dev/icons?i=aws,docker,kubernetes,terraform,jenkins,ansible,helm&theme=dark" />

**CI/CD & Version Control**
<br/>
<img src="https://skillicons.dev/icons?i=git,github,githubactions&theme=dark" />

**Monitoring & Observability**
<br/>
<img src="https://skillicons.dev/icons?i=prometheus,grafana,elasticsearch&theme=dark" />

**OS & Tools**
<br/>
<img src="https://skillicons.dev/icons?i=linux,ubuntu,windows,vscode,postman&theme=dark" />

**Databases**
<br/>
<img src="https://skillicons.dev/icons?i=mysql,postgres&theme=dark" />

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🗺️ DevOps Learning Roadmap

```text
  ✅ Linux Administration
  ✅ Git & GitHub
  ✅ Python & Bash Scripting
  ✅ Docker & Docker Compose
  🔄 Kubernetes (Advanced)
  🔄 Terraform (IaC)
  🔄 AWS Core Services
  🔄 Jenkins Pipelines
  🔜 GitHub Actions
  🔜 Argo CD (GitOps)
  🔜 Prometheus & Grafana
  🔜 DevSecOps Practices
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🚀 Featured Projects

<table width="100%">
<tr>
<td width="33%" valign="top">

### 🔹 AWS CI/CD Pipeline
Full pipeline to build, test & deploy a Python web app on AWS using Jenkins, Docker & Kubernetes. Infra managed with Terraform.

`AWS` `Jenkins` `Docker` `K8s` `Terraform`

**[View Repo →](https://github.com/sam77mpath/aws-devops-cicd-pipeline)**

</td>
<td width="33%" valign="top">

### 🔹 Linux Automation Toolkit
Bash & Python scripts automating user management, backups, log cleanup, disk monitoring, and package updates.

`Linux` `Bash` `Python` `Cron`

**[View Repo →](https://github.com/sam77mpath/linux-automation-toolkit)**

</td>
<td width="33%" valign="top">

### 🔹 Dockerized Web App
Python web application containerized with Docker and deployed via Docker Compose — demonstrating networking & scalable deployment.

`Python` `Docker` `Compose`

**[View Repo →](https://github.com/sam77mpath/docker-python-webapp)**

</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 📊 GitHub Analytics

<div align="center">
<img src="https://github-readme-stats.vercel.app/api?username=sam77mpath&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=58A6FF&count_private=true" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sam77mpath&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF" height="165"/>
</div>

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=sam77mpath&theme=tokyonight&hide_border=true&background=0D1117&stroke=58A6FF&ring=58A6FF&fire=58A6FF" alt="GitHub Streak" />
</div>

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=sam77mpath&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=58A6FF&line=58A6FF&point=FFFFFF" alt="Activity Graph" width="100%"/>
</div>

<div align="center">
<img src="https://github-profile-trophy.vercel.app/?username=sam77mpath&theme=tokyonight&no-frame=true&margin-w=8&column=7" alt="Trophies" />
</div>

### 🐍 Contribution Snake

<div align="center">
<img src="https://raw.githubusercontent.com/sam77mpath/sam77mpath/output/github-contribution-grid-snake.svg" alt="Snake animation" width="100%"/>
</div>

<sub>Generated automatically by <code>.github/workflows/snake.yml</code> — appears after the first run on the default branch.</sub>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🏆 Achievements & Certifications

<table width="100%">
<tr>
<td width="50%" valign="top">

**Achievements**
- 🎓 Accenture Developer Program (Forage) — Virtual Experience Program
- 🎓 B.Tech Computer Science Engineering student
- 🛠️ Actively building real-world DevOps projects
- 🏅 Hackathons: planning to participate in upcoming events

</td>
<td width="50%" valign="top">

**Certifications**
- ☁️ AWS Cloud & DevOps — in progress
- 📚 Continuous learner: AWS, Linux, Docker, Kubernetes, Terraform, Jenkins

</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 🤝 Open Source & Collaboration Goals

- 🌐 Contribute to open-source DevOps & cloud tooling projects
- 💼 Open to freelance infrastructure/automation work
- 🔬 Interested in research on cloud reliability & observability
- 🚀 Exploring startup ideas around developer tooling

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:0D1117&height=2&section=header" width="100%"/>

## 📫 Let's Connect

<div align="center">

<a href="https://www.linkedin.com/in/sampath-vishwakarma-3b73903a6" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-058CFF?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117" />
</a>
<a href="mailto:sampathpammi88@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-058CFF?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" />
</a>
<a href="https://github.com/sam77mpath" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-058CFF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" />
</a>

<br/><br/>

<i>⭐️ Thanks for visiting — feel free to explore my repos and connect!</i>

</div>

<img src="assets/footer.svg" width="100%"/>
<img width="1200" height="300" alt="banner" src="https://github.com/user-attachments/assets/cbefed8e-33dd-4d74-b5bc-ecb9ac743ed6" />

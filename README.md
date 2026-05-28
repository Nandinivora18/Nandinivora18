
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@400;500;700;800&display=swap');

  :root {
    --green: #39d353;
    --green-dim: #196127;
    --cyan: #58d6e8;
    --amber: #f0c34e;
    --red: #ff6b6b;
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #7d8590;
    --purple: #a371f7;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .gh-profile {
    font-family: 'JetBrains Mono', monospace;
    background: var(--bg);
    color: var(--text);
    border-radius: 12px;
    border: 1px solid var(--border);
    overflow: hidden;
    max-width: 680px;
  }

  .scanline-bar {
    height: 3px;
    background: linear-gradient(90deg, var(--green), var(--cyan), var(--purple));
    animation: scanSlide 3s ease-in-out infinite;
  }
  @keyframes scanSlide {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
  }

  .header {
    background: var(--bg2);
    padding: 28px 28px 22px;
    border-bottom: 1px solid var(--border);
  }

  .terminal-prefix {
    font-size: 11px;
    color: var(--muted);
    margin-bottom: 12px;
    letter-spacing: 0.08em;
  }
  .terminal-prefix span { color: var(--green); }

  .name-row {
    display: flex;
    align-items: flex-start;
    gap: 18px;
    margin-bottom: 14px;
  }

  .avatar-ring {
    width: 64px;
    height: 64px;
    border-radius: 50%;
    border: 2px solid var(--green);
    background: var(--bg3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 22px;
    color: var(--green);
    flex-shrink: 0;
    position: relative;
  }
  .avatar-ring::after {
    content: '';
    position: absolute;
    inset: -5px;
    border-radius: 50%;
    border: 1px solid var(--green-dim);
  }

  .name-block h1 {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 24px;
    color: var(--text);
    letter-spacing: -0.01em;
    line-height: 1.1;
  }
  .name-block .handle {
    font-size: 13px;
    color: var(--muted);
    margin-top: 3px;
  }
  .name-block .handle span { color: var(--purple); }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
    margin-top: 10px;
  }
  .badge {
    font-size: 11px;
    padding: 3px 9px;
    border-radius: 20px;
    border: 1px solid;
    font-weight: 500;
    letter-spacing: 0.04em;
  }
  .badge-green { border-color: var(--green); color: var(--green); background: rgba(57,211,83,0.08); }
  .badge-cyan { border-color: var(--cyan); color: var(--cyan); background: rgba(88,214,232,0.08); }
  .badge-amber { border-color: var(--amber); color: var(--amber); background: rgba(240,195,78,0.08); }
  .badge-purple { border-color: var(--purple); color: var(--purple); background: rgba(163,113,247,0.08); }
  .badge-red { border-color: var(--red); color: var(--red); background: rgba(255,107,107,0.08); }

  .bio {
    font-size: 13px;
    line-height: 1.65;
    color: #b1bac4;
    margin-top: 14px;
    padding-top: 14px;
    border-top: 1px solid var(--border);
  }
  .bio .hi { color: var(--amber); }
  .bio .accent { color: var(--green); }
  .bio .accent2 { color: var(--cyan); }

  .body { padding: 20px 28px; }

  .section-label {
    font-size: 10px;
    letter-spacing: 0.12em;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .skill-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 8px;
    margin-bottom: 22px;
  }
  .skill-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 11px 13px;
    font-size: 12px;
  }
  .skill-card .sk-label {
    color: var(--muted);
    font-size: 10px;
    letter-spacing: 0.06em;
    margin-bottom: 6px;
    text-transform: uppercase;
  }
  .skill-card .sk-items {
    color: var(--text);
    line-height: 1.7;
  }
  .skill-card .sk-items span {
    display: inline-block;
    color: var(--cyan);
    margin-right: 4px;
  }

  .stat-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
    margin-bottom: 22px;
  }
  .stat-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 14px 12px;
    text-align: center;
  }
  .stat-card .sv {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 20px;
    line-height: 1;
    margin-bottom: 5px;
  }
  .stat-card .sl {
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .focus-list {
    margin-bottom: 22px;
  }
  .focus-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 9px 0;
    border-bottom: 1px solid var(--border);
    font-size: 12.5px;
    line-height: 1.55;
  }
  .focus-item:last-child { border-bottom: none; }
  .focus-item .fi-icon {
    font-size: 14px;
    margin-top: 1px;
    flex-shrink: 0;
  }
  .focus-item .fi-text { color: #b1bac4; }
  .focus-item .fi-text strong { color: var(--text); font-weight: 500; }

  .footer-bar {
    background: var(--bg2);
    border-top: 1px solid var(--border);
    padding: 14px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 8px;
  }
  .footer-links {
    display: flex;
    gap: 16px;
  }
  .footer-links a {
    font-size: 11px;
    color: var(--muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--cyan); }
  .footer-status {
    font-size: 11px;
    color: var(--green);
    display: flex;
    align-items: center;
    gap: 5px;
  }
  .dot-pulse {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--green);
    animation: pulse 2s ease infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.4; transform: scale(0.8); }
  }

  .typewriter-line {
    font-size: 12px;
    color: var(--green);
    margin-top: 8px;
  }
  .typewriter-line::after {
    content: '|';
    animation: blink 1s step-end infinite;
  }
  @keyframes blink { 50% { opacity: 0; } }

  .copy-btn {
    display: block;
    margin: 0 28px 20px;
    padding: 10px;
    background: transparent;
    border: 1px dashed var(--border);
    border-radius: 8px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    text-align: center;
    cursor: pointer;
    transition: all 0.2s;
    width: calc(100% - 56px);
  }
  .copy-btn:hover {
    border-color: var(--green);
    color: var(--green);
    background: rgba(57,211,83,0.05);
  }
</style>

<div class="gh-profile">
  <div class="scanline-bar"></div>

  <div class="header">
    <div class="terminal-prefix">~ / github.com / <span>Nandinivora18</span></div>

    <div class="name-row">
      <div class="avatar-ring">NV</div>
      <div class="name-block">
        <h1>Nandini Vora</h1>
        <div class="handle">@Nandinivora18 · <span>she/her</span></div>
        <div class="badges">
          <span class="badge badge-green">🏴‍☠️ Ethical Hacker</span>
          <span class="badge badge-cyan">🔍 Bug Bounty Hunter</span>
          <span class="badge badge-amber">🏆 CTF Player</span>
          <span class="badge badge-purple">🔬 Digital Forensics</span>
          <span class="badge badge-red">Top 8% TryHackMe</span>
        </div>
      </div>
    </div>

    <div class="bio">
      <span class="hi">👋 Hey!</span> I'm a <span class="accent">Cybersecurity-specialized CSE student</span> at GLS University, Ahmedabad — obsessed with breaking things ethically and understanding how attackers think.<br><br>
      Currently hunting bugs, solving CTFs, and building security-focused projects. I believe <span class="accent2">consistent practice beats theory</span> — 90 days of TryHackMe proved that.<br><br>
      📍 Ahmedabad, India &nbsp;·&nbsp; 🎓 B.Tech CSE (Cybersecurity) · CGPA 8.1 &nbsp;·&nbsp; 🔐 Open to internships
    </div>

    <div class="typewriter-line">&gt; actively learning, actively hacking</div>
  </div>

  <div class="body">

    <div class="section-label">stats</div>
    <div class="stat-row">
      <div class="stat-card">
        <div class="sv" style="color: var(--green);">Top 8%</div>
        <div class="sl">TryHackMe global</div>
      </div>
      <div class="stat-card">
        <div class="sv" style="color: var(--amber);">90+</div>
        <div class="sl">day streak</div>
      </div>
      <div class="stat-card">
        <div class="sv" style="color: var(--cyan);">8.1</div>
        <div class="sl">CGPA (Sem VI)</div>
      </div>
    </div>

    <div class="section-label">arsenal</div>
    <div class="skill-grid">
      <div class="skill-card">
        <div class="sk-label">Recon & Scanning</div>
        <div class="sk-items">
          <span>▸</span>Nmap<br>
          <span>▸</span>Zenmap<br>
          <span>▸</span>Nikto<br>
          <span>▸</span>Wireshark
        </div>
      </div>
      <div class="skill-card">
        <div class="sk-label">Exploitation</div>
        <div class="sk-items">
          <span>▸</span>Metasploit<br>
          <span>▸</span>Burp Suite<br>
          <span>▸</span>DVWA<br>
          <span>▸</span>SQLi / XSS
        </div>
      </div>
      <div class="skill-card">
        <div class="sk-label">Environment</div>
        <div class="sk-items">
          <span>▸</span>Kali Linux<br>
          <span>▸</span>Bash<br>
          <span>▸</span>Python<br>
          <span>▸</span>MySQL
        </div>
      </div>
      <div class="skill-card">
        <div class="sk-label">Focus Areas</div>
        <div class="sk-items">
          <span>▸</span>Web AppSec<br>
          <span>▸</span>OSINT<br>
          <span>▸</span>Net Security<br>
          <span>▸</span>Forensics
        </div>
      </div>
    </div>

    <div class="section-label">currently</div>
    <div class="focus-list">
      <div class="focus-item">
        <span class="fi-icon" style="color:var(--green);">◈</span>
        <div class="fi-text"><strong>Capstone Project — Voice Unlock System</strong> · Offline password vault secured by hybrid voice biometrics using 76-dimensional acoustic fingerprint (MFCC + Cosine Similarity + DTW)</div>
      </div>
      <div class="focus-item">
        <span class="fi-icon" style="color:var(--cyan);">◈</span>
        <div class="fi-text"><strong>CTF Challenges</strong> · Actively competing on Razzify, focusing on vulnerability discovery, web exploitation, and privilege escalation</div>
      </div>
      <div class="focus-item">
        <span class="fi-icon" style="color:var(--amber);">◈</span>
        <div class="fi-text"><strong>Bug Bounty Prep</strong> · Sharpening web app attack skills via DVWA + Burp Suite — working toward my first public disclosure</div>
      </div>
      <div class="focus-item">
        <span class="fi-icon" style="color:var(--purple);">◈</span>
        <div class="fi-text"><strong>BSides Ahmedabad 2025</strong> · Attended as community member — learning from researchers & expanding network in the security community</div>
      </div>
    </div>

    <div class="section-label">certifications</div>
    <div class="skill-grid" style="margin-bottom:8px;">
      <div class="skill-card" style="border-color: rgba(57,211,83,0.3);">
        <div class="sk-label" style="color:var(--green);">TryHackMe</div>
        <div class="sk-items" style="font-size:11px;">Active Top 8% Global Rank<br><span style="color:var(--muted); font-size:10px;">Feb 2026</span></div>
      </div>
      <div class="skill-card" style="border-color: rgba(88,214,232,0.3);">
        <div class="sk-label" style="color:var(--cyan);">Cisco</div>
        <div class="sk-items" style="font-size:11px;">Intro to Cybersecurity<br><span style="color:var(--muted); font-size:10px;">May 2025</span></div>
      </div>
    </div>

  </div>

  <button class="copy-btn" onclick="copyReadme()">📋 click to copy README.md source for your GitHub profile</button>

  <div class="footer-bar">
    <div class="footer-links">
      <a href="https://in.linkedin.com/in/nandini-vora-7b358a276" target="_blank">LinkedIn ↗</a>
      <a href="https://tryhackme.com/p/nandinivora245" target="_blank">TryHackMe ↗</a>
      <a href="https://github.com/Nandinivora18" target="_blank">GitHub ↗</a>
    </div>
    <div class="footer-status">
      <div class="dot-pulse"></div>
      open to internships
    </div>
  </div>
</div>

<script>
function copyReadme() {
  const md = `<!-- Nandini Vora | GitHub Profile README -->

<div align="center">

# 👾 Nandini Vora

**\`Ethical Hacker · Bug Bounty Hunter · CTF Player · Digital Forensics\`**

[![TryHackMe](https://img.shields.io/badge/TryHackMe-Top_8%25_Global-red?style=flat-square&logo=tryhackme)](https://tryhackme.com/p/nandinivora245)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://in.linkedin.com/in/nandini-vora-7b358a276)
[![GitHub](https://img.shields.io/badge/GitHub-Nandinivora18-181717?style=flat-square&logo=github)](https://github.com/Nandinivora18)

</div>

---

## 🧠 About Me

> *"I think like an attacker so I can defend like a pro."*

Hey! I'm a **Cybersecurity-specialized CSE student** at GLS University, Ahmedabad — obsessed with ethical hacking, bug bounty hunting, and digital forensics. I believe **consistent hands-on practice beats theory** — 90+ days on TryHackMe proved that.

- 🎓 B.Tech CSE (Cybersecurity Specialization) · CGPA 8.1 (Sem VI) · GLS University
- 🏆 **Top 8% Globally** on TryHackMe · 90-day learning streak
- 🔐 Focused on: Web Application Security, OSINT, Network Recon, Digital Forensics
- 🎯 Goal: Bug Bounty Hunter · Seeking Cybersecurity Internships
- 📍 Ahmedabad, India

---

## 🛠️ Arsenal

\`\`\`
Recon & Scanning    →  Nmap · Zenmap · Nikto · Wireshark
Exploitation        →  Metasploit · Burp Suite · DVWA (SQLi, XSS, CMDi, BruteForce)
Environment         →  Kali Linux · Bash · Python · MySQL · Java
Concepts            →  Vulnerability Assessment · Web AppSec · OSINT · Network Scanning
\`\`\`

---

## 🚀 Featured Projects

### 🔐 [Voice-Unlock](https://github.com/Nandinivora18/Voice-unlock)
> Offline password vault secured by **hybrid voice biometrics**
- 76-dimensional acoustic fingerprint using MFCC + Cosine Similarity + DTW
- Local neural speech recognition via Vosk (fully offline)
- Dual-factor authentication: voice identity + spoken passphrase

---

## ⚔️ CTF & Community

- 🏴‍☠️ **CTF Player** — Razzify platform (vulnerability discovery, web exploitation, privilege escalation)
- 🎤 **BSides Ahmedabad 2025** — Attendee, cybersecurity conference
- 🔥 90-day TryHackMe streak across network security, web exploitation, vulnerability analysis

---

## 📜 Certifications

| Certificate | Issuer | Date |
|---|---|---|
| Active Top 8% Global Rank | TryHackMe | Feb 2026 |
| Introduction to Cybersecurity | Cisco | May 2025 |

---

## 📊 Stats

<div align="center">

[![TryHackMe](https://tryhackme-badges.s3.amazonaws.com/nandinivora245.png)](https://tryhackme.com/p/nandinivora245)

</div>

---

<div align="center">

📬 **nandinivora245@gmail.com** · +91 6354684112

*Open to cybersecurity internships & bug bounty collaborations*

</div>
`;
  navigator.clipboard.writeText(md).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ copied! paste into your GitHub profile README.md';
    btn.style.borderColor = 'var(--green)';
    btn.style.color = 'var(--green)';
    setTimeout(() => {
      btn.textContent = '📋 click to copy README.md source for your GitHub profile';
      btn.style.borderColor = '';
      btn.style.color = '';
    }, 3000);
  });
}
</script>

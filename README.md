<!-- The banner, covers and doodle stickers live in assets/. The doodles are my own drawings. -->

<p align="center">
  <img src="assets/banner.png" alt="Hand-drawn oranges, orange slices and leaves on blush-pink stripes." width="100%">
</p>

<h1 align="center">Chloe Robinson</h1>

<p align="center">
  <b>UX/UI designer and frontend developer</b> · Pretoria, South Africa<br>
  I like designing pretty things and then making them work.
</p>

<p align="center">
  <a href="https://www.chloerdesigns.co.za/"><img alt="Portfolio: chloerdesigns.co.za" src="https://img.shields.io/badge/Portfolio-chloerdesigns.co.za-E8590C?style=flat-square"></a>
  <a href="https://www.behance.net/chloerobinson28"><img alt="Behance" src="https://img.shields.io/badge/Behance-case%20studies-2B211E?style=flat-square&logo=behance&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/chloe-robinson-25b123351"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Chloe%20Robinson-2B211E?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:corbyncrobinson@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-say%20hello-2B211E?style=flat-square&logo=gmail&logoColor=white"></a>
</p>

<p align="center">
  <a href="#about-me">About</a> ·
  <a href="#flagship-project-sonata">Sonata</a> ·
  <a href="#development-projects">Development</a> ·
  <a href="#uxui-case-studies">UX/UI</a> ·
  <a href="#live-sites">Live sites</a> ·
  <a href="#toolkit">Toolkit</a> ·
  <a href="#contact">Contact</a>
</p>

<p align="center">
  <img src="assets/stickers/soot-sprite-stars.svg" alt="" height="56">&nbsp;
  <img src="assets/stickers/daisy.svg" alt="" height="56">&nbsp;
  <img src="assets/stickers/headphones.svg" alt="" height="56">&nbsp;
  <img src="assets/stickers/totoro.svg" alt="" height="56">&nbsp;
  <img src="assets/stickers/lily-of-the-valley.svg" alt="" height="56">&nbsp;
  <img src="assets/stickers/soot-sprite-shooting-star.svg" alt="" height="56">
</p>

## About me

<img src="assets/stickers/chloe.svg" alt="A hand-drawn self-portrait: curly hair and round glasses." align="right" width="150">

I'm a UX/UI designer and frontend developer in my final year at Open Window. I chose design because I loved IT but didn't want to lose the creative spark, so now I get both. I enjoy the research side of a project, but what I really love is turning that research into working code that looks beautiful and actually works.

In a team I'll lead when the work needs it; on Koru I was the project manager. Otherwise you'll find me on research and documentation, or working alongside the backend to bring the frontend to life. My coding style includes tea, a hunched back and my cat trying to sit on my keyboard.

Away from the screen, I've been riding since I was five, and my horse Gedenk has been my partner since I was thirteen. I also love reading, birdwatching (it's where Envol came from), RPGs and indie games, and I'll rewatch *Kiki's Delivery Service*, *How to Train Your Dragon* or *Star Wars* any day. Every doodle in this README is mine.

<br clear="right">

## Flagship project: Sonata

<p align="center">
  <img src="assets/covers/sonata.webp" alt="Sonata's cover: the app's night-sky screens with glowing orbs." width="100%">
</p>

<p align="center">
  <img alt="Expo SDK 57" src="https://img.shields.io/badge/Expo-SDK%2057-2B211E?style=flat-square&logo=expo&logoColor=white">
  <img alt="React Native 0.86" src="https://img.shields.io/badge/React%20Native-0.86-2B211E?style=flat-square&logo=react&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-2B211E?style=flat-square&logo=typescript&logoColor=white">
  <img alt="Firebase" src="https://img.shields.io/badge/Firebase-2B211E?style=flat-square&logo=firebase&logoColor=white">
  <img alt="213 tests passing" src="https://img.shields.io/badge/tests-213%20passing-2B211E?style=flat-square">
</p>

**A mood check-in you can hear. Final-year DV300 project, built solo from first sketch to release.**

Most mood trackers ask you to put your day into a word. In Sonata you pick one of 14 glowing orbs (seven notes, in major or minor) by how it sounds. At the end of the week, an AI on your phone, trained on Bach's chorales, writes those seven notes into a song, and every month becomes a record. There's no account, no trackers, and not one emotion word in the interface.

<table>
  <tr>
    <td align="center"><img src="https://raw.githubusercontent.com/corbyn-jpg/sonata/main/docs/readme/gif-checkin.gif" alt="Swiping through the orbs and saving a check-in." width="200"><br><sub>A check-in</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/corbyn-jpg/sonata/main/docs/readme/gif-weekly.gif" alt="The week's notes arriving on a staff, then the song playing on its record." width="200"><br><sub>The week's song</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/corbyn-jpg/sonata/main/docs/readme/gif-monthly.gif" alt="The month's calendar of orbs and its song." width="200"><br><sub>The month</sub></td>
  </tr>
</table>

**Technologies:** React Native 0.86 (Expo SDK 57), TypeScript, Expo Router, NativeWind, React Native Skia, Reanimated, expo-audio, Firebase (anonymous auth, Cloud Firestore, security rules), EAS Build and EAS Update, Jest, Figma

**Highlights:**
- Trained the composer myself, from scratch in TypeScript: a Markov chain for chords and a small GRU neural network for melody, learned from 382 Bach chorales, with backpropagation, the Adam optimiser and a test that checks every gradient
- Measured it rather than assuming it: on 77 unseen chorales, chord perplexity fell from 5.77 (hand-written rules) to 4.60, melody perplexity from 4.71 to 2.43, and the network's top guess for the next note is right 72% of the time
- The AI runs entirely on the phone, so nobody's daily moods are ever sent to a third party
- Private by design: every check-in is sealed with AES-256-GCM on the phone before it's saved, works offline, and syncs to Firestore in the background as ciphertext only
- Drew every orb, glow and night sky in shared Skia canvases, and replaced live synthesis with pre-rendered instrument recordings mixed on the phone, after both lagged and crackled on a mid-range Android
- Accessible beyond sound: Feel notes give every note its own vibration pattern for deaf and hard-of-hearing users
- Grew past the brief with an Oasis (paced breathing, calming sounds, a thought record and South African helplines), a Composer, sheet music export (PDF and MusicXML) and playlists
- 213 automated tests in 28 suites, a problem log of every bug with its cause and fix, and user and lecturer feedback shipped as over-the-air updates the same day

<p>
  <a href="https://github.com/corbyn-jpg/sonata"><img alt="View the repository" src="https://img.shields.io/badge/View%20the%20repo-2B211E?style=for-the-badge&logo=github&logoColor=white"></a>
  <a href="https://www.behance.net/gallery/257232199/Sonata"><img alt="Read the case study" src="https://img.shields.io/badge/Case%20study-2B211E?style=for-the-badge&logo=behance&logoColor=white"></a>
  <a href="https://github.com/corbyn-jpg/sonata/releases/latest"><img alt="Download for Android" src="https://img.shields.io/badge/Android%20APK-E8590C?style=for-the-badge&logo=android&logoColor=white"></a>
  <a href="https://appetize.io/app/b_ty5ozfyg7ml2jcpatqfwmehbpa"><img alt="Try it in the browser" src="https://img.shields.io/badge/Try%20it%20in%20the%20browser-E8590C?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

<p align="center">
  <img src="assets/stickers/cat-stretching.svg" alt="" height="48">
</p>

## Development projects

### Koru

<img src="assets/covers/koru.webp" alt="Koru's cover: the logo with floating dashboard cards." width="100%">

**Full-stack learning management system for a real client brief. Third-year team project; I was the project manager.**

Koru brings courses, scheduling, assessments, analytics and communication into one cross-platform desktop app for students, teachers and administrators, and complies with South Africa's POPIA by design.

**Technologies:** React 19, TypeScript, Vite, Electron, Tailwind CSS, DaisyUI, Framer Motion, Chart.js, ASP.NET Core (C#), Entity Framework Core, PostgreSQL, BCrypt, Swagger

**Highlights:**
- Ran the sprints, kept the backlog prioritised and wrote all of the project documentation
- A native desktop app for Windows and macOS through Electron, wrapping a React and Vite frontend
- A normalised, POPIA-compliant PostgreSQL schema with role-based access for three user types, behind 15 REST API controllers
- 216 automated tests (xUnit.net and FluentAssertions on the backend, Vitest and React Testing Library on the frontend), with 83% backend and about 80% frontend line coverage
- Acted on client and lecturer feedback: a clearer dashboard hierarchy, a 3,500-line component split into focused modules, and per-course due dates

[View the repository](https://github.com/corbyn-jpg/learn-online)

### Envol

<img src="assets/covers/envol.webp" alt="Envol's cover: the birdwatching race app on a phone." width="100%">

**A location-based birdwatching race for Android. DV300 term project, built solo.**

Players travel to real-world arenas, race to identify the birds found there, and prove each sighting with a timestamped photo.

**Technologies:** React Native 0.81 (Expo SDK 54), TypeScript, Expo Router (typed routes), Firebase (Authentication and Cloud Firestore), react-native-maps, expo-location, expo-image-picker

**Highlights:**
- GPS-gated arenas that only unlock inside a location's radius, using the haversine formula
- Two race modes sharing one clock that derives elapsed time from timestamps, so it stays accurate across navigation and throttling
- Photo verification through EXIF capture times, rejecting screenshots and forwarded images; an AI vision check was costed and prototyped, and this free, offline approach chosen instead
- Eight achievement medals derived from race history rather than stored, and every meaningful permission enforced by Firestore security rules

[View the repository](https://github.com/corbyn-jpg/envol)

### This portfolio

**My own site, [chloerdesigns.co.za](https://www.chloerdesigns.co.za/): a "studio wall" where every project is pinned up like a note, stuck on with my own hand-drawn tape and thumbtacks.**

**Technologies:** React, Vite, Motion, hand-traced SVG drawings

### Earlier projects

| Project | What it is | Built with |
| --- | --- | --- |
| [Poseidon's Notebook](https://github.com/corbyn-jpg/poseidons-notebook) | A full-stack logbook for marine species sightings, with sign-in and full CRUD | React, Node.js, Express, MySQL, JWT |
| [Open Library Explorer](https://github.com/corbyn-jpg/formative-one-openlibrary) | A dashboard that turns Open Library data into charts, trends and author comparisons | React, Chart.js, Axios, CSS Modules |
| [Vinoir](https://github.com/corbyn-jpg/summative-vinoir) | A team-built luxury perfume shop with accounts, a catalogue and a cart | React, Node.js, Express, MongoDB, Material UI |

## UX/UI case studies

<table>
  <tr>
    <td width="33%" valign="top">
      <a href="https://www.behance.net/gallery/257232199/Sonata"><img src="assets/covers/sonata.webp" alt="Sonata's case study cover." width="100%"></a>
      <b>Sonata</b><br>From research to a working app, built around one rule: no emotion words.
    </td>
    <td width="33%" valign="top">
      <a href="https://www.behance.net/gallery/250929689/Ontora-Design-for-accessibility"><img src="assets/covers/ontora.webp" alt="Ontora's case study cover." width="100%"></a>
      <b>Ontora</b><br>Design for accessibility.
    </td>
    <td width="33%" valign="top">
      <a href="https://www.behance.net/gallery/250837171/Waddle-wearable-AI"><img src="assets/covers/waddle.webp" alt="Waddle's case study cover." width="100%"></a>
      <b>Waddle</b><br>A wearable AI.
    </td>
  </tr>
</table>

## Live sites

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://www.bilanciaaccounting.co.za/"><img src="assets/covers/bilancia.webp" alt="Bilancia Accounting's website on a desktop and a phone." width="100%"></a>
      <b><a href="https://www.bilanciaaccounting.co.za/">Bilancia Accounting</a></b><br>A live client website, built with React.
    </td>
    <td width="50%" valign="top">
      <a href="https://www.erinrobinsoncounselling.co.za/"><img src="assets/covers/erin-robinson.webp" alt="Erin Robinson Counselling's website on a desktop and a phone." width="100%"></a>
      <b><a href="https://www.erinrobinsoncounselling.co.za/">Erin Robinson Counselling</a></b><br>A live client website, built with React.
    </td>
  </tr>
</table>

## Toolkit

<img src="assets/stickers/headphones.svg" alt="" align="right" height="90">

**Languages**<br>
<img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-2B211E?style=flat-square&logo=typescript&logoColor=F97316"> <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-2B211E?style=flat-square&logo=javascript&logoColor=F97316"> <img alt="C#" src="https://img.shields.io/badge/C%23-2B211E?style=flat-square&logo=dotnet&logoColor=F97316"> <img alt="HTML" src="https://img.shields.io/badge/HTML-2B211E?style=flat-square&logo=html5&logoColor=F97316"> <img alt="CSS" src="https://img.shields.io/badge/CSS-2B211E?style=flat-square&logo=css&logoColor=F97316"> <img alt="SQL" src="https://img.shields.io/badge/SQL-2B211E?style=flat-square&logo=postgresql&logoColor=F97316">

**Web and desktop**<br>
<img alt="React" src="https://img.shields.io/badge/React-2B211E?style=flat-square&logo=react&logoColor=F97316"> <img alt="Vite" src="https://img.shields.io/badge/Vite-2B211E?style=flat-square&logo=vite&logoColor=F97316"> <img alt="Angular" src="https://img.shields.io/badge/Angular-2B211E?style=flat-square&logo=angular&logoColor=F97316"> <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind%20CSS-2B211E?style=flat-square&logo=tailwindcss&logoColor=F97316"> <img alt="DaisyUI" src="https://img.shields.io/badge/DaisyUI-2B211E?style=flat-square&logo=daisyui&logoColor=F97316"> <img alt="Motion" src="https://img.shields.io/badge/Motion-2B211E?style=flat-square&logo=framer&logoColor=F97316"> <img alt="Material UI" src="https://img.shields.io/badge/Material%20UI-2B211E?style=flat-square&logo=mui&logoColor=F97316"> <img alt="Chart.js" src="https://img.shields.io/badge/Chart.js-2B211E?style=flat-square&logo=chartdotjs&logoColor=F97316"> <img alt="Electron" src="https://img.shields.io/badge/Electron-2B211E?style=flat-square&logo=electron&logoColor=F97316">

**Mobile**<br>
<img alt="React Native" src="https://img.shields.io/badge/React%20Native-2B211E?style=flat-square&logo=react&logoColor=F97316"> <img alt="Expo" src="https://img.shields.io/badge/Expo-2B211E?style=flat-square&logo=expo&logoColor=F97316"> <img alt="Expo Router" src="https://img.shields.io/badge/Expo%20Router-2B211E?style=flat-square&logo=expo&logoColor=F97316"> <img alt="EAS Build and Update" src="https://img.shields.io/badge/EAS%20Build%20%26%20Update-2B211E?style=flat-square&logo=expo&logoColor=F97316"> <img alt="NativeWind" src="https://img.shields.io/badge/NativeWind-2B211E?style=flat-square&logo=tailwindcss&logoColor=F97316"> <img alt="React Native Skia" src="https://img.shields.io/badge/Skia-2B211E?style=flat-square"> <img alt="Reanimated" src="https://img.shields.io/badge/Reanimated-2B211E?style=flat-square"> <img alt="React Native Maps" src="https://img.shields.io/badge/react--native--maps-2B211E?style=flat-square&logo=googlemaps&logoColor=F97316">

**Backend and data**<br>
<img alt="Firebase" src="https://img.shields.io/badge/Firebase-2B211E?style=flat-square&logo=firebase&logoColor=F97316"> <img alt="ASP.NET Core" src="https://img.shields.io/badge/ASP.NET%20Core-2B211E?style=flat-square&logo=dotnet&logoColor=F97316"> <img alt="Entity Framework Core" src="https://img.shields.io/badge/EF%20Core-2B211E?style=flat-square&logo=dotnet&logoColor=F97316"> <img alt="Node.js" src="https://img.shields.io/badge/Node.js-2B211E?style=flat-square&logo=nodedotjs&logoColor=F97316"> <img alt="Express" src="https://img.shields.io/badge/Express-2B211E?style=flat-square&logo=express&logoColor=F97316"> <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-2B211E?style=flat-square&logo=postgresql&logoColor=F97316"> <img alt="MySQL" src="https://img.shields.io/badge/MySQL-2B211E?style=flat-square&logo=mysql&logoColor=F97316"> <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-2B211E?style=flat-square&logo=mongodb&logoColor=F97316"> <img alt="REST APIs" src="https://img.shields.io/badge/REST%20APIs-2B211E?style=flat-square&logo=swagger&logoColor=F97316">

**AI, audio and video**<br>
<img alt="Neural networks trained from scratch" src="https://img.shields.io/badge/Neural%20networks%20(GRU)-2B211E?style=flat-square"> <img alt="Markov chains" src="https://img.shields.io/badge/Markov%20chains-2B211E?style=flat-square"> <img alt="expo-audio" src="https://img.shields.io/badge/expo--audio-2B211E?style=flat-square&logo=expo&logoColor=F97316"> <img alt="Remotion" src="https://img.shields.io/badge/Remotion-2B211E?style=flat-square">

**Testing and tools**<br>
<img alt="Jest" src="https://img.shields.io/badge/Jest-2B211E?style=flat-square&logo=jest&logoColor=F97316"> <img alt="Vitest" src="https://img.shields.io/badge/Vitest-2B211E?style=flat-square&logo=vitest&logoColor=F97316"> <img alt="xUnit.net" src="https://img.shields.io/badge/xUnit.net-2B211E?style=flat-square&logo=dotnet&logoColor=F97316"> <img alt="React Testing Library" src="https://img.shields.io/badge/Testing%20Library-2B211E?style=flat-square&logo=testinglibrary&logoColor=F97316"> <img alt="ESLint" src="https://img.shields.io/badge/ESLint-2B211E?style=flat-square&logo=eslint&logoColor=F97316"> <img alt="Git" src="https://img.shields.io/badge/Git-2B211E?style=flat-square&logo=git&logoColor=F97316"> <img alt="GitHub" src="https://img.shields.io/badge/GitHub-2B211E?style=flat-square&logo=github&logoColor=F97316"> <img alt="Docker" src="https://img.shields.io/badge/Docker-2B211E?style=flat-square&logo=docker&logoColor=F97316"> <img alt="AWS" src="https://img.shields.io/badge/AWS-2B211E?style=flat-square">

**Design**<br>
<img alt="Figma" src="https://img.shields.io/badge/Figma-2B211E?style=flat-square&logo=figma&logoColor=F97316"> <img alt="Adobe Illustrator" src="https://img.shields.io/badge/Illustrator-2B211E?style=flat-square"> <img alt="Adobe Photoshop" src="https://img.shields.io/badge/Photoshop-2B211E?style=flat-square"> <img alt="Adobe Premiere Pro" src="https://img.shields.io/badge/Premiere%20Pro-2B211E?style=flat-square"> <img alt="Adobe Lightroom" src="https://img.shields.io/badge/Lightroom-2B211E?style=flat-square"> <img alt="Canva" src="https://img.shields.io/badge/Canva-2B211E?style=flat-square"> <img alt="Sketching on iPad" src="https://img.shields.io/badge/iPad%20sketching-2B211E?style=flat-square&logo=apple&logoColor=F97316">

**What I bring:** user research and testing, wireframes to high-fidelity prototypes, design systems and style tiles, accessible design, full-stack apps from database to UI, privacy and POPIA compliance by design, automated testing, client requirements and feedback, sprint planning and documentation.

<br clear="right">

## Currently learning

- **Motion for mobile:** springs, gestures and GPU-drawn effects with Reanimated and Skia
- **On-device machine learning:** small models that are measurable, explainable and private
- **Testing at scale:** branch coverage, integration tests and automated build checks
- **Cloud deployment:** CI/CD pipelines and scalable infrastructure

<p align="center">
  <img src="https://github.com/user-attachments/assets/de2362e3-e9ff-49e6-bcdb-37f3d41d3c2d" alt="Learning journey" width="80%">
</p>

## GitHub activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=corbyn-jpg&hide_border=true&background=FFFBF5&ring=E8590C&fire=E8590C&currStreakNum=2B211E&currStreakLabel=E8590C&sideNums=2B211E&sideLabels=2B211E&dates=7A6A64&stroke=F3C1B5" alt="GitHub streak stats for corbyn-jpg">
</p>

## Contact

I'm finishing my degree this year and looking for UX/UI or frontend roles, on-site around Pretoria and Johannesburg or remotely, full-time or freelance.

<p>
  <a href="mailto:corbyncrobinson@gmail.com"><img alt="Email" src="https://img.shields.io/badge/corbyncrobinson%40gmail.com-E8590C?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://www.chloerdesigns.co.za/"><img alt="Portfolio" src="https://img.shields.io/badge/chloerdesigns.co.za-2B211E?style=for-the-badge"></a>
  <a href="https://www.linkedin.com/in/chloe-robinson-25b123351"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-2B211E?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="https://www.behance.net/chloerobinson28"><img alt="Behance" src="https://img.shields.io/badge/Behance-2B211E?style=for-the-badge&logo=behance&logoColor=white"></a>
</p>

## Off the clock

<p>
  <img src="assets/stickers/horse.svg" alt="Gedenk, my horse, lying down." height="80">&nbsp;
  <img src="assets/stickers/jiji.svg" alt="Jiji the cat." height="80">&nbsp;
  <img src="assets/stickers/toothless-tail.svg" alt="Toothless's tail fin." height="80">&nbsp;
  <img src="assets/stickers/millennium-falcon.svg" alt="The Millennium Falcon." height="80">&nbsp;
  <img src="assets/stickers/bb8.svg" alt="BB-8." height="80">&nbsp;
  <img src="assets/stickers/baymax.svg" alt="Baymax." height="80">&nbsp;
  <img src="assets/stickers/penguin.svg" alt="A penguin." height="80">&nbsp;
  <img src="assets/stickers/tangled-sun.svg" alt="The Tangled sun." height="80">
</p>

Riding (with Gedenk, since I was thirteen), fantasy and sci-fi books, RPGs and indie games, birdwatching, and Studio Ghibli on repeat.

> "In the spirit of science, there really is no such thing as a 'failed experiment.' Any test that yields valid data is a valid test." — Adam Savage

<p align="center">
  <img src="assets/stickers/soot-sprite-shooting-star.svg" alt="" height="44">
</p>

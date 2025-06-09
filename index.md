---
layout: base
title: Student Home 
description: Home Page
hide: true
---


<img src="{{site.baseurl}}/images/apcompscihome.png">


<div style="background-color: #05034b; padding: 20px; border-radius: 15px;">
  <h2 style="color: white;">Important Links</h2>
  <p style="color: white;"> It is helpful to have an easy-to-access navigation menu, especially for important links and pages on this site. </p>
  <button onclick="window.location.href='https://nighthawkcoders.github.io/portfolio_2025/';">Nighthawk Coders Portfolio 2025</button>
</div>
<p> </p>

<div style="background-color: #05034b; padding: 20px; border-radius: 15px;">
  <a href="about/">
    <button class="block"><b>About Page</b></button>
  </a>
  <p> </p>
  <a href="tools/">
    <button class="block"><b>Tools Page</b></button>
  </a>
  <p> </p>
  <p style="color: white;"> Use the buttons above to navigate to important pages on this site. </p>

</div>

<style>
  /* Ensure the 'Games' button is a big rounded square with a blue background */
  .games-menu {
    display: inline-block;
    background-color: #05034b !important; /* Blue background */
    padding: 15px 30px;
    border-radius: 25px;
    color: white !important; /* Text color */
    font-size: 18px;
    text-align: center;
    cursor: pointer;
    text-decoration: none;
  }

  /* Dropdown menu container */
  .dropdown-menu {
    display: none;
    position: absolute;
    background-color: #05034b !important; /* Blue background */
    border-radius: 10px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    padding: 10px;
    top: 100%;
    left: 0;
    z-index: 1000;
  }

  /* Dropdown menu links */
  .dropdown-menu a {
    display: block;
    color: white !important; /* Text color */
    padding: 10px;
    text-decoration: none;
    border-radius: 5px;
    font-size: 16px;
  }

  /* Dropdown menu link hover effect */
  .dropdown-menu a:hover {
    background-color: white !important; /* Hover background color */
    color: black !important; /* Hover text color */
  }

  /* Show dropdown menu when 'Games' button is clicked */
  .games-menu.active + .dropdown-menu {
    display: block;
  }
</style>

<!-- Add this HTML to your index.md file where you want the menu to appear -->
<div class="dropdown">
  <a href="#" class="games-menu">SASS Hacks and JavaScript Project Playground</a>
  <div class="dropdown-menu">
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/project/calculator">Calculator</a>
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/project/binary-calculator">Binary Calculator</a>    
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/project/cookie-clicker">Cookie Clicker Game</a>
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/project/snake">Snake Game</a>
    <a href="{{site.baseurl}}/javascript/project/npc-game">SPRINT 2: NPC Game</a>
  </div>
</div>

<script>
  // Toggle dropdown menu visibility
  document.querySelector('.games-menu').addEventListener('click', function(e) {
    e.preventDefault();
    this.classList.toggle('active');
  });
</script>

<p> </p>
<p> </p>

<details>
    <summary>Sprint 1</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/1/planning-and-emoji">Planning and Emoji Notebook</a></li>
        <li><a href="{{site.baseurl}}/sprint/1/frontend-hacks">Frontend Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/1/sass-hacks">SASS Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/1/brazil">Brazil Guide</a></li>
        <li><a href="{{site.baseurl}}/sprint/1/italy">Italy Guide</a></li>
    </ul>
</details>

<details>
    <summary>Sprint 2</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-1">3.1 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-2">3.2 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-3">3.3 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-4">3.4 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-5">3.5 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-8">3.8 Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-10a">3.10a Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/hacks_3-10b">3.10b Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/blog">Sprint 2 Personal Learnings Blog</a></li>
        <li><a href="{{site.baseurl}}/sprint/2/team-blog">Sprint 2 Team Blog</a></li>
    </ul>
</details>

<details>
    <summary>Sprint 3</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/3/blog">Sprint 3 Personal Learnings Blog</a></li>
        <li><a href="{{site.baseurl}}/sprint/3/teamplan">Sprint 3 Team Plan</a></li>
        <li><a href="{{site.baseurl}}/sprint/3/natm">Sprint 3 NATM Presentation</a></li>
        <li><a href="{{site.baseurl}}/sprint/3/review">Tri 1-3 Review Ticket</a></li>
        <li><a href="{{site.baseurl}}/sprint/3/mc">2018 College Board MC</a></li>
    </ul>
</details>

<details>
    <summary>Sprint 4</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/4/tech-talk">Sprint 4 Tech Talk Notes</a></li>
        <li><a href="{{site.baseurl}}/sprint/4/flask-intro">Flask and Python Web Server Dev Intro</a></li>
        <li><a href="{{site.baseurl}}/sprint/4/tech-talk">Sprint 4 Tech Talk Notes</a></li>
        <li><a href="{{site.baseurl}}/sprint/4/flask-intro">Flask and Python Web Server Dev Intro</a></li>
        <li><a href="{{site.baseurl}}/sprint/4/cs-panel">GiCS Panel Notes</a></li>
    </ul>
</details>

<details>
    <summary>Sprint 5</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/5/tech-talk-3">Sprint 5 Tech Talk Notes</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/sqlalchemy">SQLAlchemy Code</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/sqlconnect">SQLConnect Code</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/tech-talk-3">API Tech Talk 2 Notes</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/CRUD_review">Sprint 5 CRUD Review</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/bigidea4">Big Idea 4 Learnings</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/final">Final Exam Blog</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/finalmc">2020 MC Review</a></li>
        <li><a href="{{site.baseurl}}/sprint/5/ppr">Personalized Project Repository</a></li>
    </ul>
</details>

<details>
    <summary>Sprint 7</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/7/tech_talks">Sprint 7 Tech Talk Notes </a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_1">Beneficial and Harmful Lesson Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_2">Digital Divide Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_3">Computing Bias Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_4">Crowdsoucing Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_5">Legal and Ethical Implications Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_6">Safe Computing Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_7">Binary Search Algorithms Hacks</a></li>
        <li><a href="{{site.baseurl}}/github/pages/cyber_extracredit">Cyber Extra Credit</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_8">Lists and Filtering Algorithms Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_9">Big O Hacks<</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_10">Undecidable Problems and Graphs and Heuristics Hacks</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/mcreflect">MC Reflection 2021</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/studyplan">Study Plan</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_11">Binary</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_12">Logic Gates</a></li>
        <li><a href="{{site.baseurl}}/sprint/7/hacks_13">Digital Images</a></li>
    </ul>
</details>

<details>
    <summary>Final</summary>
    <ul>
        <li><a href="{{site.baseurl}}/sprint/7/final">Final Blog</a></li>
    </ul>
</details>

<p></p>  

<script src="https://utteranc.es/client.js"
        repo="blackstar3092/risha_guha_2025_1"
        issue-term="pathname"
        theme="preferred-color-scheme"
        crossorigin="anonymous"
        async>
</script>
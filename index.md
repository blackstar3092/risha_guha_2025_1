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
  /* Ensure the 'Games' button is a big rounded square with a purple background */
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
  <a href="#" class="games-menu">Games</a>
  <div class="dropdown-menu">
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/projects/calculator">Calculator</a>
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/projects/binary-calculator">Binary Calculator</a>    
    <a href="https://blackstar3092.github.io/risha_guha_2025_1/javascript/projects/cookie-clicker">Cookie Clicker Game</a>
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
<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
    }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for coding languages
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var earth_pictures = [
        {"picture": "0/00/Earth_from_space.jpg", "description": "Earth from Space"},
        {"picture": "9/97/The_Earth_seen_from_Apollo_17.jpg", "description": "Earth from Apollo 17"},
        {"picture": "e/e0/AS08-14-2383.jpg", "description": "Earth from Moon"},
    ];

    // 3b. Build grid items inside of our container for each row of data
    for (const language of earth_pictures) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the logo
        var img = document.createElement("img");
        img.src = http_source + language.picture; // concatenate the source and logo
        img.alt = language.description + " Picture"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = language.description; // extract the description

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>
<p> </p>
<comment>
Pictures are made using Wikipedia images.
</comment>

<p> </p>
<p> </p>

<table>
    <tr>
        <td><img src="{{site.baseurl}}/images/cslogo.jpg" height="60" title="Notebooks and Hacks" alt=""></td>
        <td><a href="{{site.baseurl}}/github/pages/planning-and-emoji">Planning and Emoji Notebook</a></td>
        <td><a href="{{site.baseurl}}/github/pages/frontend-hacks">Frontend Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/sass-hacks">SASS Hacks</a></td>
        <td><a href="{{site.baseurl}}/github/pages/brazil">Brazil Guide</a></td>
        <td><a href="{{site.baseurl}}/github/pages/italy">Italy Guide</a></td>
    </tr>
</table>

<script src="https://utteranc.es/client.js"
        repo="blackstar3092/risha_guha_2025_1"
        issue-term="pathname"
        theme="preferred-color-scheme"
        crossorigin="anonymous"
        async>
</script>
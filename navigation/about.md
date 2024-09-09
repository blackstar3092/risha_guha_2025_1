---
layout: page
title: About
permalink: /about/
---

<h2 style="color: #eaeaea;"> My name is Risha Guha and I am a sophomore at DNHS. </h2> 
<h3 style="color: #75b5aa;"> I am interested in engineering, computer science, and cybersecurity. 💻🔍👩‍💻 </h3>
<p> </p>

<img src="{{site.baseurl}}/images/aboutme.png">

<p> </p>
<h3> I am familiar with Python, HTML, and CSS coding. </h3>

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
    var coding_languages = [
        {"logo": "c/c3/Python-logo-notext.svg", "description": "Python"},
        {"logo": "6/61/HTML5_logo_and_wordmark.svg", "description": "HTML"},
        {"logo": "d/d5/CSS3_logo_and_wordmark.svg", "description": "CSS"},
    ];

    // 3b. Build grid items inside of our container for each row of data
    for (const language of coding_languages) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the logo
        var img = document.createElement("img");
        img.src = http_source + language.logo; // concatenate the source and logo
        img.alt = language.description + " Logo"; // add alt text for accessibility

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
<comment>
Logos are made using Wikipedia images.
</comment>



<script src="https://utteranc.es/client.js"
        repo="blackstar3092/risha_guha_2025_1"
        issue-term="pathname"
        theme="icy-dark"
        crossorigin="anonymous"
        async>
</script>
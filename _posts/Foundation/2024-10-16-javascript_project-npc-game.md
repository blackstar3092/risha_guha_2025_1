---
title: NPC Game
layout: post
description: A Game Made Using Sprint 2 Skills
categories: [Javascript]
permalink: /javascript/project/npc-game
menu: nav/javascript_project.html
toc: true
comments: false
---

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gameplay with NPCs</title>
  <style>
    .grid {
      display: grid;
      grid-template-columns: repeat(5, 50px);
      grid-template-rows: repeat(5, 50px);
      gap: 5px;
    }
    .cell {
      width: 50px;
      height: 50px;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: lightgray;
      border: 1px solid #000;
    }
    .npc {
      background-color: yellow;
    }
    .player {
      background-color: blue;
    }
  </style>
</head>
<body>

<h1>Game with NPCs</h1>

<div class="grid" id="gameGrid"></div>
<p id="message"></p>

<script>
  // 2D array representing the game grid (5x5 grid)
  const grid = [
    ['empty', 'empty', 'npc', 'empty', 'empty'],
    ['empty', 'empty', 'empty', 'empty', 'empty'],
    ['empty', 'empty', 'player', 'empty', 'npc'],
    ['empty', 'npc', 'empty', 'empty', 'empty'],
    ['empty', 'empty', 'empty', 'empty', 'empty']
  ];

  const playerPosition = { x: 2, y: 2 };
  const npcDialogs = [
    "Hello, traveler! Need help?",
    "Have you seen the ancient temple?",
    "Careful, monsters lurk in the shadows!"
  ];

  // Function to render the grid
  function renderGrid() {
    const gridContainer = document.getElementById('gameGrid');
    gridContainer.innerHTML = ''; // Clear the grid

    // Nested loops to create grid elements
    for (let y = 0; y < grid.length; y++) {
      for (let x = 0; x < grid[y].length; x++) {
        const cell = document.createElement('div');
        cell.classList.add('cell');
        
        if (grid[y][x] === 'npc') {
          cell.classList.add('npc');
        } else if (grid[y][x] === 'player') {
          cell.classList.add('player');
        }

        cell.dataset.x = x;
        cell.dataset.y = y;

        // Add event listener to NPC cells
        if (grid[y][x] === 'npc') {
          cell.addEventListener('click', () => interactWithNPC(x, y));
        }

        gridContainer.appendChild(cell);
      }
    }
  }

  // Function to interact with NPC
  function interactWithNPC(npcX, npcY) {
    if (Math.abs(playerPosition.x - npcX) <= 1 && Math.abs(playerPosition.y - npcY) <= 1) {
      const dialog = npcDialogs[Math.floor(Math.random() * npcDialogs.length)];
      document.getElementById('message').textContent = `NPC says: "${dialog}"`;
    } else {
      document.getElementById('message').textContent = "You are too far from the NPC.";
    }
  }

  // Initial render
  renderGrid();
</script>

</body>
</html>

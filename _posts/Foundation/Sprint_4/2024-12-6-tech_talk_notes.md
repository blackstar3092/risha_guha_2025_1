---
layout: post
title: Sprint 4 12-6 Tech Talk Notes
description: What I learned from Mr. Mortensen's tech talk
categories: ['Javascript']
permalink: /sprint/4/tech-talk
type: ccc
author: Risha Guha
menu: nav/sprint_4.html
---

- We need to focus more on backend for this Sprint
- Plan 3, Code 2: BACKEND
- Portfolio 2025, Big Idea 4: Python Flask in Jupyter

### Web Servers:

- New libraries of the world
- Have been making Github Pages webservers based on flocker and student_2025 templates
- Transitioning to Flask: creating a minimal server with Python
- When using code and creating servers, we use code from libraries developed by other people

## Flask

- Flask is a micro webserver
- ```app = Flask(__name__)``` is the fundamental building block for the whole server
- CORS: Resource service/allocation (security measure) - Star indicates everyone can access
- Currently, adding 2 rows, each with 6 elements with InfoDb.append (static list)
- Jsonify: Restful API (standard for returning data from backend to frontend)
- - JSON: Standard data returned
- - Returning in HTML is not the JSON standard but can still do it


## Web Analysis

- Curl & lsof: depicts what's running on the port (similar to cyber)
- Printing status: pinging web server and returning data in readable format
- When calling unknown API endpoint, will return a 404 error or 400 error


## Debugging: 
- Can't have global variables in notebook running
- Need to fix the issue with database

## Homework:
- Make static API that returns from real webserver (minimally)
- - Move it to the backend and return data 



### Successes So Far

- Linking of frontend and backend post systems
- Fetching data from About for student API

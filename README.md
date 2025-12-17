# RateGames – Raspberry Pi Web Server Project

## Overview
RateGames is a web application for rating video games, developed on a Raspberry Pi 5 using Ubuntu Server.  
The project uses Apache2 as the web server, PHP for dynamic pages, MySQL for database management, and Python scripts to fetch game data from the Steam API automatically.  
The website was hosted externally via a Cloudflared tunnel at [https://rategames.se](https://rategames.se) for several weeks during development.  
The server is no longer live, but all setup, scripts, and configurations are fully documented here.

---

## Technologies
- **Raspberry Pi 5** with Ubuntu Server
- **Apache2** – web server
- **PHP** – dynamic web pages and form handling
- **MySQL** – database for storing games and user reviews
- **Python** – script to fetch and update games via Steam API
- **Cloudflared Tunnel** – external access without router changes
- **HTML/CSS** – frontend layout and styling

---

## Project Structure

- `index.php` – Homepage showing all games and top games list
- `game.php` – Individual game pages where users can leave ratings
- `add_review.php` – Handles storing ratings and optional comments
- `search.php` – Allows users to search for games with live suggestions
- `css/style.css` – Frontend styling and layout

Additional files in the repository include:
- `report.pdf` – School report documenting the project
- `screenshots/` – Images showing the website and server status
- `configs/nginx-example.conf` (optional) – Example configuration files

---

## What I Did
- Installed and configured Apache2, PHP, and MySQL on Raspberry Pi 5  
- Created MySQL database with tables for **Games** and **Reviews**  
- Developed PHP pages:
  - `index.php` – homepage with top games list  
  - `game.php` – individual game pages with reviews  
  - `add_review.php` – submission form for ratings/comments  
  - `search.php` – search function with live suggestions  
- Built a rating system with buttons and slider (1–10 scale), allowing optional comments  
- Added logic to limit one rating per IP per game  
- Developed Python script to fetch and update games automatically via Steam API  
- Designed frontend layout based on Steam color theme  
- Set up **Cloudflared tunnel** to make the web server accessible externally  
- Linked purchased domain (`rategames.se`) via Cloudflared

---

## Lessons Learned
- Linux server setup and management  
- Web server configuration with Apache2  
- PHP/MySQL integration for dynamic web applications  
- Using APIs to fetch and manage data automatically  
- Frontend layout, usability, and iterative design  
- Setting up secure external access via Cloudflared tunnel

---

## Notes
- Project was developed on a school network, which initially blocked direct access via domain. This was solved using a Cloudflared tunnel.  
- The server was live externally for several weeks during development. It is no longer live, but the setup and scripts are fully reproducible.  
- All changes were tested incrementally to quickly identify and fix issues.

---

## Screenshots
Include images of:
- Homepage  
- Game page  
- Terminal showing Apache2 & Cloudflared running

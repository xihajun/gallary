---
layout: post
title:  Eight-Puzzle Game
description: A playable Javascript implementation of the classical 8-puzzle game that can also be solved using AI if you're stuck
image: assets/alternate_images/eightPuzzle_front.png
nav-menu: false
main_tile: false
show_tile: true
date: 2020-10-25
categories: puzzle AI
tags: write
permalink: 8puzzle
---

### This is a JavaScript implementation of the classic 8-puzzle game.
### Features:
* Uses the A* algorithm to find the shortest way to solve the puzzle
* You can choose any image to show in the tiles. It will replace the numbers though.
* The blank tile can also be controlled using hand gestures. It was trained using supervised learning on a set of over 5000 photos.


### Controls:
<div style="display:flex">
    <div style="flex:1;padding:0 1% 0 0">
        <h1>
            <div ALIGN=Center>
                ↑
            </div>
            <div ALIGN=Center>
                ←  ↓  →
            </div>
        </h1>
        <h3>
            <div ALIGN=Center>
                Arrow keys
            </div>
        </h3>
    </div>
    <div style="flex:1;padding:0 1% 0 0">
        <h1>
            <div ALIGN=Center>
                ✋
            </div>
            <div ALIGN=Center>
                👈 👇 👉
            </div>
        </h1>
        <h3>
            <div ALIGN=Center>
                Hand Gestures (using camera)
            </div>
        </h3>
    </div>
    <div style="flex:1;padding:0 1% 0 0">
        <h1>
            <div ALIGN=Center>
                W
            </div>
            <div ALIGN=Center>
                A  S  D
            </div>
        </h1>
        <h3>
            <div ALIGN=Center>
                Keyboard keys
            </div>
        </h3>
    </div>
</div>


<style>
	*.videoWrapper {
		position: relative;
		padding-bottom: 56.25%; /* 16:9 */
		height: 0;
	}
	*.videoWrapper iframe {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}
    *.grid{
        display: grid;
        place-items:center;
        width: 100%;
    }
}
</style>

<style> iframe{ border: none; } </style>
<div class="videoWrapper" style="--aspect-ratio: 3 / 4;">
    <iframe 
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/EightPuzzle"
        data-position="center center">
    </iframe>
</div>

<!-- <div class="videoWrapper" style="--aspect-ratio: 3 / 4;">
    <iframe 
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/EightPuzzle"
        data-position="center center">
    </iframe>
</div> -->
<p>
</p>

Here's the code for A* path finding algorithm that solves the puzzle:
<style>
    @import url('https://cdn.rawgit.com/lonekorean/gist-syntax-themes/848d6580/stylesheets/monokai.css');
    @import url('https://fonts.googleapis.com/css?family=Open+Sans');
  .gist-file
  .gist-data {max-height: 700px; max-width: auto;}
  .gistContainer {width: 75%; margin: 0 auto;}
</style>
<div class = "gistContainer">
<script src="https://gist.github.com/TahsinTariq/5c4ba6b74dd1279f6d4bcfea6a3cbefd.js"></script>
</div>




---
layout: post
title: A Study on Triangulation
description: A small demonstration of my love of Triangulating anything and everything
image: assets/images/shaan_triangulated.jpg
nav-menu: false
main_tile: false
tags: write
permalink: triangulation
---
## My implementation:
Here I've used [`poisson disc sampling`]("https://en.wikipedia.org/wiki/Supersampling#Poisson_disk")to get an even distribution of points and then triangulated them.

I've tried various methods to speed up the algorithm. Although some algorithms are easy to understand and implement, they may not be as efficient. So, in order to get quick results, I used the [`Delunator library`]("https://mapbox.github.io/delaunator/") which I do not understand at all. But hey, it gets the job done faster.


###	Click on the render to get a new set of points


<!-- <div class="videoWrapper">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/r9JzMWXTGwQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<p> -->

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
}
</style>
<style> iframe{ border: none; } </style>
<div class="videoWrapper" style="--aspect-ratio: 4 / 4;">
    <iframe
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/Delunay_triangulation"
        data-position="center center">
    </iframe>
</div>
<p>
</p>

## How Delaunay Triangulation works

<p>In geometry, triangulation is a partition of a geometric object into simplexes. On a 2D plane, these are triangles. In 3D space, they are tetrahedrons</p>
Let's introduce some constrains:
<ul>
	<li>Let a geometric object be described by a set of points on the  <b>S</b>  plane. Triangulation for a finite set of points  <b>S</b>  is the problem of triangulation of the convex hull  <b>CH( S )</b> , which covers all points of the set  <b>S</b> .</li>
	<li> Segments of straight lines cannot intersect, but can meet at common points belonging to the set  <b>S</b> . We will call these segments <b> edges </b>.</li>
	<li> A set of points is <b> circular </b> if there is a circle on which all the points of the set lie. For this set of points, this circle will be circumscribed. For a triangle, this circle will pass through all three of its non-collinear vertices.</li>
	<li> The circle will be <b> free of points </b> if there are no points from the set  <b>S</b>  inside the circle.</li>
	<li> Triangulation for a set of points  <b>S</b>  - <b> Delaunay triangulation </b> if each circumcircle for each triangle is free of points.</li>
</ul>
Two conclusions can be drawn from these definitions:
<ul>
	<li> For triangulation to exist, there must be at least three non-collinear points in the  <b>S</b>  set.</li>
	<li> For the Delaunay triangulation to be unique, it is necessary that no 4 points from the set  <b>S</b>  lie on the same circumcircle.</li>
</ul>

#### You can find some python code and a bit more explanation [`here`](https://github.com/TahsinTariq/Jupyter-stuff/blob/main/triangulation/Triangulation%20-%20Copy.ipynb) and the code I used to make this in [`JavaScript`](https://github.com/TahsinTariq/p5js/tree/master/P5_Sketches/P5_Web_Collection/Delunay_triangulation)

<p>
</p>

Here's a different render I made using triangulation. For this, the points were sampled from an image using a color threshold.
<!-- <div style="display:flex"> -->
<div style="display: grid; place-items:center;">
	<img src = "{% link assets/images/shaan_triangulated.jpg %}" alt = "Triangulated Image 1">
</div>
<!-- </div> -->
<!-- <div class="videoWrapper" style="--aspect-ratio: 3 / 4;">
<iframe src="https://www.youtube.com/embed/fY4qkfjJo6A" alt="" data-position="center center" /></iframe>
</div> -->

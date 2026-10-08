---
layout: splash
permalink: /index_proposed.html
sitemap: false
excerpt: "Research group<br><br>Department of Mathematical Sciences<br>University of Bath<br><br><br>"
header:
  overlay_image: "/assets/pics/covers/cover_composite.jpg"
  actions:
    - label: "More info"
      url: /about/
title: "Numerical Analysis & Data Science"
---

<!-- Proposed front page: rotating computed cover images.
     The images are in assets/pics/covers/ (computed in Python).
     overlay_image above is the fallback for visitors without JavaScript and for link previews.
     To adopt: copy the front matter and everything below into index.md. -->

<style>
  .page__hero--overlay { position: relative; overflow: hidden; }
  .page__hero--overlay > .wrapper { position: relative; z-index: 1; }
  .hero-rotator {
    position: absolute; inset: 0; z-index: 0;
    background-size: cover; background-position: center;
    opacity: 0; transition: opacity 1.6s ease;
  }
  .hero-rotator.is-active { opacity: 1; }
  @media (prefers-reduced-motion: reduce) { .hero-rotator { transition: none; } }
</style>

<script>
(function () {
  var hero = document.querySelector('.page__hero--overlay');
  if (!hero) return;
  var base = '{{ "/assets/pics/covers/" | relative_url }}';
  var imgs = ['cover_composite.jpg', 'cover_langevin.jpg', 'cover_graph.jpg', 'cover_atmosphere.jpg', 'cover_imaging.jpg', 'cover_leaf.jpg'];
  var SECONDS = 9;
  var start = Math.floor(Math.random() * imgs.length);   // random image on each visit
  var layers = imgs.map(function (name, i) {
    var d = document.createElement('div');
    d.className = 'hero-rotator' + (i === start ? ' is-active' : '');
    d.style.backgroundImage = 'url(' + base + name + ')';
    hero.insertBefore(d, hero.firstChild);
    return d;
  });
  if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) return;
  var cur = start;
  setInterval(function () {
    if (document.hidden) return;
    layers[cur].classList.remove('is-active');
    cur = (cur + 1) % layers.length;
    layers[cur].classList.add('is-active');
  }, SECONDS * 1000);
})();
</script>

---
layout: splash
permalink: /index_proposed.html
sitemap: false
excerpt: "Research group<br><br>Department of Mathematical Sciences<br>University of Bath<br><br><br>"
header:
  overlay_image: "/assets/pics/covers/cover_composite.jpg"
title: "Numerical Analysis & Data Science"
---

<!-- Proposed front page: rotating computed cover images.
     The images are in assets/pics/covers/ (computed in Python).
     overlay_image above is the fallback for visitors without JavaScript and for link previews.
     To adopt: copy the front matter and everything below into index.md. -->

<div class="na-intro" markdown="1">

One of the largest numerical analysis groups in the UK, with [expertise](/people/) across numerical analysis and a growing strength in data science, including inverse problems and machine learning. Our [research](/research/) is internationally recognised. We teach a full range of undergraduate and postgraduate [units](/teaching/), run [workshops and conferences](/events/index.html), and host a long-standing [seminar](/events/all_seminars.html).

We welcome applications for [PhD study](/research/phd.html) and are always happy to discuss problems in scientific computing, data science and numerical analysis. Contact: [bath-na@lists.bath.ac.uk](mailto:bath-na@lists.bath.ac.uk).

</div>

<style>
  .page__hero--overlay { position: relative; overflow: hidden; }
  .page__hero--overlay > .wrapper { position: relative; z-index: 1; }
  .hero-rotator {
    position: absolute; inset: 0; z-index: 0;
    background-size: cover; background-position: center;
    opacity: 0; transition: opacity 1.6s ease;
  }
  .hero-rotator.is-active { opacity: 1; }
  .hero-next {
    position: absolute; right: 16px; bottom: 16px; z-index: 2;
    width: 40px; height: 40px; padding: 0; border-radius: 50%;
    border: 1px solid rgba(255,255,255,.45); background: rgba(6,12,26,.35);
    color: #fff; cursor: pointer; opacity: .6;
    display: flex; align-items: center; justify-content: center;
    transition: opacity .2s, background-color .2s;
  }
  .hero-next:hover, .hero-next:focus-visible { opacity: 1; background: rgba(6,12,26,.6); }
  .hero-next:focus-visible { outline: 2px solid #f2b632; outline-offset: 2px; }
  .hero-next svg { width: 18px; height: 18px; }
  .na-intro { max-width: 44rem; margin: 2.5em auto 3em; font-size: 1.05em; line-height: 1.6; }
  .na-intro p { margin: 0 0 1em; }
  .na-intro a[href^="mailto"] { white-space: nowrap; }
  @media (prefers-reduced-motion: reduce) { .hero-rotator, .hero-next { transition: none; } }
</style>
<script>
(function () {
  var hero = document.querySelector('.page__hero--overlay');
  if (!hero) return;
  var base = '{{ "/assets/pics/covers/" | relative_url }}';
  var imgs = ['cover_composite.jpg', 'cover_langevin.jpg', 'cover_graph.jpg', 'cover_atmosphere.jpg', 'cover_imaging.jpg', 'cover_leaf.jpg', 'cover_ct.jpg'];
  var SECONDS = 9;
  var cur = Math.floor(Math.random() * imgs.length);    // random image on each visit
  var layers = imgs.map(function (name, i) {
    var d = document.createElement('div');
    d.className = 'hero-rotator' + (i === cur ? ' is-active' : '');
    d.style.backgroundImage = 'url(' + base + name + ')';
    hero.insertBefore(d, hero.firstChild);
    return d;
  });
  function next() {
    layers[cur].classList.remove('is-active');
    cur = (cur + 1) % layers.length;
    layers[cur].classList.add('is-active');
  }
  var auto = !window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var timer = null;
  function restart() {
    if (timer) clearInterval(timer);
    if (auto) timer = setInterval(function () { if (!document.hidden) next(); }, SECONDS * 1000);
  }
  var btn = document.createElement('button');
  btn.type = 'button';
  btn.className = 'hero-next';
  btn.setAttribute('aria-label', 'Next cover image');
  btn.title = 'Next image';
  btn.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M9 5l7 7-7 7"/></svg>';
  btn.addEventListener('click', function () { next(); restart(); });
  hero.appendChild(btn);
  restart();
})();
</script>

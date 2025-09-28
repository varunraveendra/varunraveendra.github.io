---
layout: page
title: Outdoors
permalink: /outdoors/
order: 7
---


<!-- ---  GALLERY CSS (once per page) --- -->
<style>
  /* Grid that you can control per-section with --cols: 3 or 4 */
  .gallery {
    --cols: 3;                    /* default columns */
    display: grid;
    grid-template-columns: repeat(var(--cols), 1fr);
    gap: 12px;
    margin: 12px 0 28px 0;
  }
  .gallery figure {
    margin: 0;
    border-radius: 8px;
    overflow: hidden;
    background: #f7f7f7;
  }
  .gallery img {
    width: 100%;
    height: 100%;
    aspect-ratio: 4 / 3;          /* uniform tiles */
    object-fit: cover;
    display: block;
  }
  .gallery figcaption {
    font-size: 0.9rem;
    padding: 6px 8px;
    background: #fff;
  }

  /* Responsive fallbacks */
  @media (max-width: 768px) {
    .gallery { --cols: 2; }
  }
  @media (max-width: 480px) {
    .gallery { --cols: 1; }
  }
</style>

<!-- ===================== -->
<!-- Car spotting (Row 1)  -->
<!-- ===================== -->
<h3>Car spotting</h3>
<div class="gallery" style="--cols: 3;">
  <figure>
    <img src="{{ site.url }}/assets\IMG_1790.jpeg" alt="Car 1">
    <figcaption>Car 1</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_1795.JPG" alt="Car 2">
    <figcaption>Car 2</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_2708.JPG" alt="Car 3">
    <figcaption>Car 3</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_2785.JPG" alt="Car 4">
    <figcaption>Car 4</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_6014.jpeg" alt="Car 4">
    <figcaption>Car 5</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_6015.jpeg" alt="Car 4">
    <figcaption>Car 6</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_6018.jpeg" alt="Car 4">
    <figcaption>Car 7</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_6020.jpeg" alt="Car 4">
    <figcaption>Car 8</figcaption>
  </figure>
  
</div>

<!-- ===================== -->
<!-- Kayaking (Row 2)      -->
<!-- ===================== -->
<h3>Kayaking</h3>
<!-- Change --cols to 3 to show 3 images per row -->
<div class="gallery" style="--cols: 3;">
  <figure>
    <img src="{{ site.url }}/assets\IMG_4105.jpeg" alt="Kayak 1">
    <figcaption>Kayak 1</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_4111.jpeg" alt="Kayak 2">
    <figcaption>Kayak 2</figcaption>
  </figure>
  <!-- <figure>
    <img src="{{ site.url }}/assets/birding/kinglet.jpg" alt="Kayak 3">
    <figcaption>Kayak 3</figcaption>
  </figure> -->
  <!-- add more figures if you want; they’ll wrap to the next row -->
</div>

<!-- ===================== -->
<!-- Motorbiking (Row 3)   -->
<!-- ===================== -->
<h3>Motorbiking</h3>
<div class="gallery" style="--cols: 3;">
  <figure>
    <img src="{{ site.url }}/assets\45c496f0-9a3b-4f07-b925-47542e64bd08.jpg" alt="Bike 1">
    <figcaption>Bike 1</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_0923.jpeg" alt="Bike 2">
    <figcaption>Bike 2</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_20200215_200927_103_Original.jpg" alt="Bike 3">
    <figcaption>Bike 3</figcaption>
  </figure>
  <figure>
    <img src="{{ site.url }}/assets\IMG_20220524_203522_902_Original.jpg" alt="Bike 4" style="object-position: 50% 10%;">
    <figcaption>Bike 4</figcaption>
  </figure>
</div>


---
layout: page
title: Outdoors
permalink: /outdoors/
order: 7
---


<style>
  .photo-strip { margin-bottom: 28px; }
  .photo-strip-window { overflow: hidden; }
  .moving-gallery { display: flex; width: max-content; gap: 12px; margin: 12px 0; }
  .moving-gallery figure {
    flex: 0 0 239px;
    width: 239px;
    margin: 0;
    border-radius: 8px;
    overflow: hidden;
    background: #f7f7f7;
  }
  .moving-gallery img { width: 100%; aspect-ratio: 4 / 3; object-fit: cover; display: block; }
  @media (prefers-reduced-motion: reduce) {
    .photo-strip-window { overflow-x: auto; }
  }
</style>

<div class="photo-strip">
  <div class="photo-strip-window" tabindex="0" role="region" aria-label="Photo row 1. Focus or hover to pause movement.">
    <div class="moving-gallery">
      <figure><img src="{{ '/assets/IMG_1790.jpeg' | relative_url }}" alt="Car 1" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_9162.jpeg' | relative_url }}" alt="White car with its hood open at a mountain overlook" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_4707.jpeg' | relative_url }}" alt="Water cascading over a broad waterfall" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_1795.JPG' | relative_url }}" alt="Car 2" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_0918.jpeg' | relative_url }}" alt="Bugatti on display in an automotive museum" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_3398.jpeg' | relative_url }}" alt="Bison crossing a road beside a meadow" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_2708.JPG' | relative_url }}" alt="Car 3" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_4105.jpeg' | relative_url }}" alt="Kayak 1" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_3038.jpeg' | relative_url }}" alt="Mountain reflected in a calm lake" loading="lazy"></figure>
    </div>
  </div>
</div>

<div class="photo-strip">
  <div class="photo-strip-window" tabindex="0" role="region" aria-label="Photo row 2. Focus or hover to pause movement.">
    <div class="moving-gallery">
      <figure><img src="{{ '/assets/IMG_2785.JPG' | relative_url }}" alt="Car 4" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_4111.jpeg' | relative_url }}" alt="Kayak 2" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_2612.jpeg' | relative_url }}" alt="River flowing through a tall rock canyon" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_6014.jpeg' | relative_url }}" alt="Car 4" loading="lazy"></figure>
      <figure><img src="{{ '/assets/45c496f0-9a3b-4f07-b925-47542e64bd08.jpg' | relative_url }}" alt="Bike 1" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_3035.jpeg' | relative_url }}" alt="Starry night sky above red-lit trees" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_6015.jpeg' | relative_url }}" alt="Car 4" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_0923.jpeg' | relative_url }}" alt="Bike 2" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_1334.jpeg' | relative_url }}" alt="Heat warning sign against red sandstone" loading="lazy"></figure>
    </div>
  </div>
</div>

<div class="photo-strip">
  <div class="photo-strip-window" tabindex="0" role="region" aria-label="Photo row 3. Focus or hover to pause movement.">
    <div class="moving-gallery">
      <figure><img src="{{ '/assets/IMG_6018.jpeg' | relative_url }}" alt="Car 4" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_20200215_200927_103_Original.jpg' | relative_url }}" alt="Bike 3" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_0686.jpeg' | relative_url }}" alt="Rainbow in the mist beneath a waterfall" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_6020.jpeg' | relative_url }}" alt="Car 4" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_20220524_203522_902_Original.jpg' | relative_url }}" alt="Bike 4" style="object-position: 50% 10%;" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_0774.jpeg' | relative_url }}" alt="Granite cliffs overlooking a mountain valley" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_9225.jpeg' | relative_url }}" alt="Black car with its hood open at sunset" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_6883.jpg' | relative_url }}" alt="Red Formula 1 race car on track" loading="lazy"></figure>
      <figure><img src="{{ '/assets/IMG_9617.jpeg' | relative_url }}" alt="Golden Gate Bridge tower with the moon behind it" loading="lazy"></figure>
    </div>
  </div>
</div>

<script>
  const reducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)');
  const tracks = Array.from(document.querySelectorAll('.moving-gallery'));
  const shuffled = tracks.flatMap(track => Array.from(track.children));
  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }
  shuffled.forEach((photo, i) => tracks[i % tracks.length].appendChild(photo));
  document.querySelectorAll('.photo-strip').forEach((strip, index) => {
    const track = strip.querySelector('.moving-gallery');
    const viewport = strip.querySelector('.photo-strip-window');
    const photos = Array.from(track.children);
    let animation;
    function updateMotion() {
      if (animation) animation.cancel();
      animation = null;
      track.querySelectorAll('[data-copy]').forEach(copy => copy.remove());
      if (reducedMotion.matches) return;
      photos.forEach(photo => {
        const copy = photo.cloneNode(true);
        copy.dataset.copy = '';
        copy.setAttribute('aria-hidden', 'true');
        copy.inert = true;
        track.appendChild(copy);
      });
      const distance = photos.length * (239 + 12);
      animation = track.animate(
        [{ transform: 'translateX(0)' }, { transform: `translateX(-${distance}px)` }],
        { duration: distance / 45 * 1000, iterations: Infinity, direction: index % 2 ? 'reverse' : 'normal' }
      );
      if (viewport.matches(':hover, :focus-within')) animation.pause();
    }
    function pause() { if (animation) animation.pause(); }
    function resume() {
      if (animation && !viewport.matches(':hover, :focus-within')) animation.play();
    }
    viewport.addEventListener('mouseenter', pause);
    viewport.addEventListener('mouseleave', resume);
    viewport.addEventListener('focusin', pause);
    viewport.addEventListener('focusout', resume);
    reducedMotion.addEventListener('change', updateMotion);
    updateMotion();
  });
</script>

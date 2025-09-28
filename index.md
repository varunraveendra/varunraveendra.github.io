---
layout: page
---
{% include JB/setup %}

<!-- put this BEFORE your first paragraph -->
<div id="slideshow" class="portrait-wrap">
  <img src="{{ '/assets/IMG_3154.JPG' | relative_url }}" class="fade-slide active">
  <img src="{{ '/assets/IMG_5833.PNG' | relative_url }}" class="fade-slide">
  <img src="{{ '/assets/IMG_6196.PNG' | relative_url }}" class="fade-slide">
  <img src="{{ '/assets/IMG_3902.jpg' | relative_url }}" class="fade-slide">
  <img src="{{ '/assets/IMG_1035.jpg' | relative_url }}" class="fade-slide">
</div>

<style>
.portrait-wrap{
  float: right;
  width: 255px;              /* tweak: 280–360px */
  aspect-ratio: 1 / 1;       /* gives the box real height so text won’t overlap */
  margin: 0 0 12px 24px;
  position: relative;
  border-radius: 8px;         /* optional */
  overflow: hidden;           /* trims edges on fade */
}

.fade-slide{
  position: absolute; inset: 0;
  width: 100%; height: 100%; object-fit: cover;
  opacity: 0; transition: opacity .9s ease-in-out;
}
.fade-slide.active{ opacity: 1; z-index: 1; }

/* Mobile: stack above text, full width */
@media (max-width: 768px){
  .portrait-wrap{ float:none; width:100%; aspect-ratio:auto; height:auto; margin:0 0 16px 0; }
  .fade-slide{ position:static; opacity:1; display:none; }   /* show only active */
  .fade-slide.active{ display:block; }
}
</style>

<script>
  const slides = document.querySelectorAll("#slideshow .fade-slide");
  let index = 0;
  function showSlide(i){ slides.forEach((s,n)=>s.classList.toggle("active", n===i)); }
  function nextSlide(){ index = (index+1) % slides.length; showSlide(index); }
  showSlide(index);
  setInterval(nextSlide, 3000);
</script>




I am Varun Raveendra, a first-year PhD Student in Robotics at the [University of Utah](https://www.utah.edu/), where I am a part of the [Aligned, Robust and Interactive Autonomy Lab (ARIA)](https://aria-lab.cs.utah.edu/) advised by Prof. [Daniel S Brown](https://users.cs.utah.edu/~dsbrown/). My research focuses on embodied multi-agent systems, Reinforcement Learning for embodied intelligence, and swarm robots, with a broader interest in advancing AI for embodied robots. 


I previously completed my Master's Electrical Engineering at the University of Utah, also in robotics, under the guidance of Prof. [Daniel S Drew](https://danieldrew.me/). Before The U, I received my undergraduate degree in Electronics and Communication from [NMIT, India](https://nitte.edu.in/nmit/). I've worked on a range of electronics and robotics projects, including an internship at Tevatron Technologies in Bangalore, India where I worked on STM microcontrollers and embedded systems.

These academic and industry experiences have shaped my background in robotics and motivated my transition from coursework to research-driven exploration. I've started publishing my research recently and have started to maintain a list of my publications under the [Research]({{ site.url }}/research) section. 

[CV / Resume]({{ site.url }}/assets/cv.pdf), [Google Scholar](https://scholar.google.com/citations?user=dXmPROMAAAAJ&hl=en)  
Email ID: [varunraveendra@gmail.com](mailto:varunraveendra@gmail.com)  

#### Updates

<div style="height:300px;overflow:auto; border:1px solid #999; padding-left: 0.7em; padding-right: 0.7em">
<table>
<col width="100px">
<col width="650px">
<tr><td><b>Jun 2025:</b></td><td> Presented my research on Swarm robots at the Inaugral <a href="https://www.price.utah.edu/ai/summit-2025">Utah AI Summit.</a></td></tr>
<tr><td><b>May 2025:</b></td><td> Presented at workshop <a href="https://arms2025.di.unimi.it/">ARMS 2025</a> at AAMAS 2025 on "Emergent Swarm Behavior Prediction using 1D-Convolution for Autonomous Closed-Loop Behavior Control". Won the MOASEI Competetion @ AAMAS25 on Open-agent systems! </td></tr>
<tr><td><b>Jan 2025:</b></td><td> Started PhD program in Robotics, advised by Prof. Daniel S Brown continuing at The U.</td></tr>
<tr><td><b>Dec 2024:</b></td><td> A paper I co-authored <a href="https://dl.acm.org/doi/10.5555/3709347.3743781">Discovery and Deployment of Emergent Robot Swarm Behaviors via Representation Learning and Real2Sim2Real Transfer</a> was accepted at <a href="https://aamas2025.org/">AAMAS 2025.</a></td></tr>
<tr><td><b>Jun 2024:</b></td><td> Released new version of HeRo robots, <a href="https://github.com/varunraveendra/hero_plus">HeRo+</a></td></tr>
<tr><td><b>Jul 2022:</b></td><td> Graduated with M.S in ECE at The U.</td></tr>
<tr><td><b>Dec 2023:</b></td><td> Started working on <a href="https://verlab.github.io/hero_common/">HeRo Robots</a> and improving them for swarm research.</td></tr>
<tr><td><b>Jan 2023:</b></td><td> Research from Undergrad was published, <a href="https://link.springer.com/article/10.1007/s13198-025-02872-8">Waste managenment in urban localities: an IoT and machine learning solution.</a></td></tr>
<tr><td><b>Aug 2022:</b></td><td> Started Master's in Electrical and Computer Science focusing on Robotics at <a href="https://www.utah.edu/">The U.</a></td></tr>
<tr><td><b>Jul 2022:</b></td><td> Graduated with B.S in ECE from <a href="https://nitte.edu.in/nmit/">NMIT Bangalore,India</a>.</td></tr>
<tr><td><b>May 2022:</b></td><td> Research on  <a href="https://drive.google.com/drive/folders/1pCy_ppWxKcfx-DhZBDNICF0Fmjpsm-39?usp=sharing">MEMS Sensors</a></td></tr>


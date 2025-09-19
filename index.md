---
layout: page
---
{% include JB/setup %}

<!-- put this BEFORE your first paragraph -->
<div id="slideshow" class="portrait-wrap">
  <img src="{{ '/assets/IMG_3154.JPG' | relative_url }}" class="fade-slide active">
  <img src="{{ '/assets/IMG_5833.PNG' | relative_url }}" class="fade-slide">
  <img src="{{ '/assets/IMG_6196.PNG' | relative_url }}" class="fade-slide">
</div>

<style>
.portrait-wrap{
  float: right;
  width: 320px;              /* tweak: 280–360px */
  aspect-ratio: 4 / 3;       /* gives the box real height so text won’t overlap */
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
  setInterval(nextSlide, 4000);
</script>




I am Varun Raveendra a 1st-year Robotics PhD Student at [The University of Utah](https://www.utah.edu/) in [ARIA Lab](https://aria-lab.cs.utah.edu/). I work Currently work on embodied multi-agent robots, RL on embodied robots, swarm robots. Focusing on AI for embodied robots. 


I'm currently advised by Prof. [Daniel S Brown](https://profiles.faculty.utah.edu/u6044225) in my Robotics PhD. Previously, I completed my Master's Electrical Engineering doing robotics, while being advised by Prof. [Daniel S Drew](https://danieldrew.me/). Before being at The U, I received my undergraduate degree in Electronics and Communication at [NMIT](https://nitte.edu.in/nmit/). I've worked on many electronics projects and an internship at Tevatron Technologies in Bangalore, India where i worked on STM microcontrollers, all of which have given me the background and motivation to pursue the field of robotics. 


I've shifted from academics to research recently and have started to maintain a list of my publications under the [Research]({{ site.url }}/research) tab. I also plan to [blog]({{ site.url }}/archive) every now and then compiling my personal experiences.

[CV / Resume]({{ site.url }}/assets/cv.pdf), [Google Scholar](https://scholar.google.com/citations?user=dXmPROMAAAAJ&hl=en)  
Email ID: [varunraveendra@gmail.com](mailto:varunraveendra@gmail.com)  

#### Updates

<div style="height:300px;overflow:auto; border:1px solid #999; padding-left: 0.7em; padding-right: 0.7em">
<table>
<col width="100px">
<col width="650px">
<tr><td><b>Jun 2025:</b></td><td> Presented my research on Swarm robots at the Inaugral <a href="https://www.price.utah.edu/ai/summit-2025">Utah AI Summit</a></td></tr>
<tr><td><b>May 2025:</b></td><td> Presented at workshop <a href="https://arms2025.di.unimi.it/">ARMS 2025</a> at AAMAS 2025 on "Emergent Swarm Behavior Prediction using 1D-Convolution for Autonomous Closed-Loop Behavior Control". Won the MOASEI Competetion @ AAMAS25 on Open-agent systems! </td></tr>
<tr><td><b>Jan 2025:</b></td><td> Started PhD program in Robotics, advised by Prof. Daniel S Brown continuing at The U.</td></tr>
<tr><td><b>Dec 2024:</b></td><td> A paper I co-authored <a href="https://dl.acm.org/doi/10.5555/3709347.3743781">Discovery and Deployment of Emergent Robot Swarm Behaviors via Representation Learning and Real2Sim2Real Transfer</a> was accepted at <a href="https://aamas2025.org/">AAMAS 2025</a></td></tr>
<tr><td><b>Jun 2024:</b></td><td> Released new version of HeRo robots, <a href="https://github.com/varunraveendra/hero_plus">HeRo+</a></td></tr>
<tr><td><b>Jul 2022:</b></td><td> Graduated with M.S in ECE at The UU.</td></tr>
<tr><td><b>Dec 2023:</b></td><td> Started working on <a href="https://verlab.github.io/hero_common/">HeRo Robots</a> and improving them for swarm research.</td></tr>
<tr><td><b>Jan 2023:</b></td><td> Research from Undergrad was published, <a href="https://link.springer.com/article/10.1007/s13198-025-02872-8">Waste managenment in urban localities: an IoT and machine learning solution.</a></td></tr>
<tr><td><b>Aug 2022:</b></td><td> Started Master's in Electrical and Computer Science focusing on Robotics at <a href="https://www.utah.edu/">The U.</a></td></tr>
<tr><td><b>Jul 2022:</b></td><td> Graduated with B.S in ECE from <a href="https://nitte.edu.in/nmit/">NMIT Bangalore,India</a>.</td></tr>
<tr><td><b>May 2022:</b></td><td> Research on  <a href="https://drive.google.com/drive/folders/1pCy_ppWxKcfx-DhZBDNICF0Fmjpsm-39?usp=sharing">MEMS Sensors</a></td></tr>


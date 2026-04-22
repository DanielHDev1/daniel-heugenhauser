---
layout: default
title: Home
---

<style>
  .project-thumb {
    display: block;
    max-width: 420px;
    width: 100%;
    border-radius: 10px;
    cursor: zoom-in;
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.12);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .project-thumb:hover {
    transform: translateY(-2px);
    box-shadow: 0 14px 30px rgba(0, 0, 0, 0.16);
  }

  .lightbox {
    display: none;
    position: fixed;
    inset: 0;
    z-index: 999;
    background: rgba(0, 0, 0, 0.8);
    padding: 24px;
    cursor: zoom-out;
  }

  .lightbox.open {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .lightbox img {
    max-width: min(1100px, 92vw);
    max-height: 88vh;
    width: auto;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 18px 50px rgba(0, 0, 0, 0.35);
    cursor: default;
  }
</style>

Recent engineering graduate specializing in game development with Unity and C#.

## Projects

### Walk the Dog on paper
<img
  src="./assets/images/projects/walk-the-dog.svg"
  alt="Walk the Dog on paper"
  class="project-thumb"
  onclick="openLightbox(this.src, this.alt)"
>

Paper prototype project. Replace this placeholder with a cover image or screenshot at `assets/images/projects/walk-the-dog.svg`.

### Crops & Corpses
<img
  src="./assets/images/projects/crops-and-corpses.svg"
  alt="Crops & Corpses"
  class="project-thumb"
  onclick="openLightbox(this.src, this.alt)"
>

Game project. Replace this placeholder with a cover image or screenshot at `assets/images/projects/crops-and-corpses.svg`.

### HymyApp
<img
  src="./assets/images/projects/hymyapp.svg"
  alt="HymyApp"
  class="project-thumb"
  onclick="openLightbox(this.src, this.alt)"
>

Application project. Replace this placeholder with a cover image or screenshot at `assets/images/projects/hymyapp.svg`.

## CV
[Download CV](./assets/resume/Daniel_Heugenhauser_CV.pdf)

## Contact
- [GitHub](https://github.com/yourusername)
- [LinkedIn](https://linkedin.com/in/yourname)
- [Email](mailto:you@example.com)

<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <img id="lightbox-image" src="" alt="">
</div>

<script>
  function openLightbox(src, alt) {
    var lightbox = document.getElementById("lightbox");
    var image = document.getElementById("lightbox-image");

    image.src = src;
    image.alt = alt;
    lightbox.classList.add("open");
  }

  function closeLightbox() {
    var lightbox = document.getElementById("lightbox");
    lightbox.classList.remove("open");
  }

  document.addEventListener("keydown", function (event) {
    if (event.key === "Escape") {
      closeLightbox();
    }
  });

  document.getElementById("lightbox-image").addEventListener("click", function (event) {
    event.stopPropagation();
  });
</script>

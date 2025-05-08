---
draft: false
toc: false
sidebar:
  exclude: true
---

<div class="hero-section">
  <video class="hero-background" autoplay muted loop playsinline>
    <source src="/Video/Diluvian.mp4" type="video/mp4">
     
  </video>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <h1 class="text-center text-white" style="text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.5);"><strong style="font-size: 3.5vw; color: #10b981; text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.5);">Flynn Coulter</strong> <br> Game programmer building robust, high performance game systems and tools.</h1>
  </div>
</div>

{{< cards cols=2 >}}
<!-- TODO: move this to a class -->
<div class="mb-3 pt-0" style="margin-top: 0.5em;">
    <h3 class="challenges-head">Primary skills</h3>
    <head>
        <title>Horizontal List</title>
        <style>
            ul {
                list-style-type: none; /* Removes default bullets */
                margin: 0;
                padding: 0;
                overflow: hidden;
            }

            li {
                display: inline-block; /* Makes list items display horizontally */
                margin-right: 10px; /* Adds spacing between items */
            }
        </style>
    </head>
    <body>
        <ul>
             <button class="btn-primary" >C++</button>
             <button class="btn-primary" >Odin</button>
             <button class="btn-primary" >Unreal Engine</button>
             <button class="btn-primary" >Perforce</button>
             <button class="btn-primary" >Git</button>
             <button class="btn-primary" >Steamworks</button>
             <button class="btn-primary" >EOS</button>
             <button class="btn-primary" >GOG</button>
             <button class="btn-primary" >FMOD</button>
        </ul>
    </body>
</div>

<!-- TODO: move this to a class -->
<div class="mb-3 pt-0" style="margin-top: 0.5em;">
    <h3 class="challenges-head">Secondary skills</h3>
    <head>
        <title>Horizontal List</title>
        <style>
            ul {
                list-style-type: none; /* Removes default bullets */
                margin: 0;
                padding: 0;
                overflow: hidden;
            }

            li {
                display: inline-block; /* Makes list items display horizontally */
                margin-right: 10px; /* Adds spacing between items */
            }
        </style>
    </head>
    <body>
        <ul>
            <button class="btn-secondary" >C#</button>
            <button class="btn-secondary" >Python</button>
            <button class="btn-secondary" >Beef</button>
            <button class="btn-secondary" >Game Maker Studio 2</button>
            <button class="btn-secondary" >Godot</button>
            <button class="btn-secondary" >Unity</button>
            <button class="btn-secondary" >Blender</button>
            <button class="btn-secondary" >Linux</button>
        </ul>
    </body>
</div>
{{< /cards >}}

<br>

<div class="mb-3 pt-0" style="margin-top: 2.5em;">
    <h1>Game Programming</h1>
</div>
{{< cards cols=2 >}}
{{< card
    link="/games"
    title="Diluvian Ultra - [Released]"
    image="/images/DiluvianUltra.jpg"
    method="Resize" 
    options="1920x1080 q100 jpg"
>}}
{{< card
    link="/games"
    title="Hels Rebellion - [canceled]"
    image="/images/HB.webp"
    method="Resize" 
    options="1920x1080 q100 webp"
>}}
{{< /cards >}}

<div class="mb-3 pt-0" style="margin-top: 2.5em;">
    <h1>Projects</h1>
</div>
{{< cards cols=2 >}}
    {{< card 
        link="/projects/#dino" 
        icon="chip" 
        title="Dino" 
        subtitle="Hobby game engine written in Odin" 
        image="/images/Dino.png" 
        method="Resize" 
        options="1920x1080 q100 jpg" 
    >}}
    
    {{< card 
        link="/projects/#dismember-plugin" 
        icon="brick" 
        title="Dismember Plugin" 
        subtitle="Runtime limb dismemberment" 
        image="/images/Dismember.jpg" 
        method="Resize" 
        options="1920x1080 q100 jpg" 
    >}}

    {{< card 
        link="/projects/#dumb-robot" 
        icon="beaker" title="Dumb Robot" 
        subtitle="Small prototype where you manage vacuum robots" 
        image="/images/DumbRobot3.jpg" 
        method="Resize" 
        options="1920x1080 q100 jpg" 
    >}}

    {{< card 
        link="/projects/#untitled-prototype" 
        icon="beaker" 
        title="Untitled prototype" 
        subtitle="Small isometric city builder prototype" 
        image="/images/UntitledProto.gif" 
    >}}

{{< /cards >}}

{{< cards cols=1 >}}
<button 
  id="resume-button-container" 
  class="btn-res w-full mt-10 font-bold uppercase text-xl py-3"
  onclick="window.open('/Resume/Flynn_Coulter_Resume-2025.pdf', '_blank')"
  role="button"
  >Resume</button>
<script>
    document.addEventListener("DOMContentLoaded", function () {
      const target = document.getElementById("resume-button-container");

      if (!target) return;

      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            target.classList.add("flash");
            observer.unobserve(target);
          }
        });
      });

      observer.observe(target);
    });
</script>
{{< /cards >}}

{{< contactform >}}
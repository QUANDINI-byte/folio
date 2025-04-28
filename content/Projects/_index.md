---
draft: false
---

### Projects
{{< cards >}}
    {{< card link="/Projects/#dino" icon="chip" title="Dino" subtitle="Hobby game engine written in Odin" image="/images/Dino.jpg" >}}
    {{< card link="/Projects/#dumb-robot" icon="beaker" title="Dumb Robot" subtitle="Small prototype where you manage vacuum robots" image="/images/DumbRobot3.jpg" >}}
{{< /cards >}}


## Dino
<span style="color: grey;">*Odin Language*</span>

![Dino](/images/Dino2.jpg "Some crash debugging tools")

Dino is a hobby game engine */ framework* that i decided to start after trying [Odin](https://odin-lang.org/).

I had seen Odin around and after trying [Beef](https://www.beeflang.org/) and [Zig](https://ziglang.org/), none of which had me feeling like it had so much more to offer than other options *i.m.o.* . Around the same time i decided that i wanted to gain a deeper understanding of the graphics pipeline instead of using existing tools, and being a hands on learner i dived right in with DirectX11.

This is not my first time making a small engine as i have previously written super small engines using C++ before. However Dino is primarally a project to learn as much as i can with a low level understanding.

**Dino currently uses:**
- **SDL2 -** window & event / input handling.
- **Imgui -** debug tooling.
- **DirectX11 -** graphics.
- **GLM -** vector math.


## Dumb Robot
<span style="color: grey;">*Unreal Engine 5 - one week*</span>

Dumb Robot is a cleaning-like simulator but with *less* manual work and more [*"personality"*](## "each robot would need to be managed to keep them working while you the player clean"). It gave me the opertunity to learn editor debug visualization and runtime render targets in Unreal Engine 5 in much more detail.

The vacuum
{{< youtube ppLUZFv3hCA >}}

Any texture can be used to generate Mess Actor Data (MAD) and a transparentcy threshold is used to aid in control for what contributes to MAD.
![DumbRobot](/images/DumbRobot.jpg)
MAD is built in editor and is cached to an asset for each level. The obvious downside to this is having to load all MAD data, however it is rather tiny in size and is only required at the beginning of a level.

Each Mess Actor texture has its own voxel resolution and is automatically sagests smaller sizes or larger ones when a new texture is selected or a designer asks for it, to keep consistancy and performance impact at a minimum.
![DumbRobot2](/images/DumbRobot2.jpg "nice and easy to see what has been cleaned")
Each Mess Actor also has a "Percent cleaned for complete" property. This helps when there is *practically* no mess left, but also gives an easy way to configure Mess Actors that might be only partially visible.

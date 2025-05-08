---
draft: false
---

## Projects
{{< cards cols=2 >}}
    {{< card link="/Projects/#dino" icon="chip" title="Dino" subtitle="Hobby game engine written in Odin" image="/images/Dino.png" method="Resize" options="1920x1080 q100 jpg" >}}
    {{< card link="/Projects/#dismember-plugin" icon="brick" title="Dismember Plugin" subtitle="Runtime limb dismemberment" image="/images/Dismember.jpg" method="Resize" options="1920x1080 q100 jpg" >}}
    {{< card link="/Projects/#dumb-robot" icon="beaker" title="Dumb Robot" subtitle="Small prototype where you manage vacuum robots" image="/images/DumbRobot3.jpg" method="Resize" options="1920x1080 q100 jpg" >}}
    {{< card link="/Projects/#untitled-prototype" icon="beaker" title="Untitled prototype" subtitle="Small isometric city builder prototype" image="/images/UntitledProto.gif" >}}
{{< /cards >}}

## Dino
<span style="color: grey;">*Odin Language*</span>

![Dino](/images/Dino2.jpg "Some crash debugging tools")

A hobby game engine / framework that started after trying out the [Odin programming language](https://odin-lang.org/). Dino is not aimed at being a general engine, but more specific to hobby projects focusing on tooling and technical design. A key focus for creating Dino was to learn more about the graphics pipeline.

{{< cards cols=1 >}}
<div class="flex" style="margin-top: 0.8em;">
    <h2 class="challenges-head">Challenges:</h2>
    <p class="challenges-paragraph"><strong>Architecture and scope:</strong> <br> Keeping Dino’s architecture lean for hobby projects while supporting a robust graphics pipeline, avoiding the bloat common in larger engines has been a challenge. However it has also meant that itteration on general architecture and systems is fast and forgiving.</p>
    <p class="challenges-paragraph"><strong>Simplified Pipeline:</strong> <br> Designing an accessible graphics pipeline using Odin’s DirectX11 bindings that balances learning and functionality. Dino's rendermakes it easy to customise how a game is rendered, making it easy to stylize rendering. </p>
    <p class="challenges-paragraph"><strong>Tooling Without Bloat:</strong> <br> Creating friendly editor tools while maintaining a lightweight reusable framework where it makes sense. </p>
</div>
{{< /cards >}}

## Dismember plugin
<span style="color: grey;">*Unreal Engine 5*</span>

![Dino](/images/Dismember.gif "")

{{< cards cols=1 >}}
<div class="flex" style="margin-top: 0.8em;">
    <h2 class="challenges-head">Challenges:</h2>
    <p class="challenges-paragraph"><strong>Creating a custom asset editor:</strong> <br> Engine source was the primary source of how to do create a custom editor. I am verry familiar with how the Paper2D plugin works and used that as a base.</p>
    <p class="challenges-paragraph"><strong>Edge cases:</strong> <br> Skeletons can be vastly different case by case. Ensuring that the tools created work well was quite a challenge.  </p>
    <p class="challenges-paragraph"><strong>Memory & Performance:</strong> <br> Avoiding using multiple skeltons and or spawning in gib Actors was hard. The standard way that Physics, Animation, and Geometry skinning works in Unreal Engine 5 is quite limiting. It was necessary to ensure that memory was kept to a minimum and that there would only be 1 skeleton animated per character at a time. this made it really easy for Artists and Designers to configure some properties and then test it immedtiatly with out needing to go through a big pipeline. </p>
</div>
{{< /cards >}}

## Dumb Robot
<span style="color: grey;">*Unreal Engine 5*</span>

A cleaning-like simulator where you manage robot vacuums. With Dumb Robot, the goal was to explore Debug Visualizers and runtime Render Targets in Unreal Engine 5 in more detail along with the asset manager.

{{< cards cols=1 >}}
<div class="flex" style="margin-top: 0.8em;">
    <h2 class="challenges-head">Challenges:</h2>
    <p class="challenges-paragraph"><strong>Texture Analysis for Mess Generation:</strong> <br> Converting arbitrary designer-provided textures into usable voxel mess data introduced edge cases, especially with semi-transparent pixels.</p>
    <p class="challenges-paragraph"><strong>Level Dependency Management:</strong> <br> Ensuring MAD data was tightly coupled to the correct level while still being reusable or re-bakable when needed was a persistent challenge. </p>
    <p class="challenges-paragraph"><strong>Asset Manager Integration:</strong> <br> Hooking MAD into Unreal’s Asset Manager system involved non-trivial setup to ensure caching, referencing, and level-specific data were handled cleanly. In the end I opted for a single asset per level. </p>
</div>
{{< /cards >}}

The vacuum
{{< youtube ppLUZFv3hCA >}}

Any texture can be used to generate Mess Actor Data (MAD) and a transparentcy threshold is used to aid in control for what contributes to MAD.
![DumbRobot](/images/DumbRobot.jpg)
MAD is built in editor and is cached to an asset for each level. The obvious downside to this is having to load all MAD data, however it is rather tiny in size and is only required at the beginning of a level.

Each Mess Actor texture has its own voxel resolution and is automatically suggests a smaller sizes or larger resolution when a new texture is selected or a designer asks for it, to keep consistancy, and performance impact at a minimum.
![DumbRobot2](/images/DumbRobot2.jpg "nice and easy to see what has been cleaned")
Each Mess Actor also has a "Percent cleaned for complete" property. This helps when there is *practically* no mess left, but also gives an easy way to configure Mess Actors that might be only partially visible.

## Untitled prototype
<span style="color: grey;">*Game Maker Studio 2*</span>

![Dino](/images/UntitledProto.gif "")

This untitled prototype was a short project between me and a [friend](https://garethkeenan.artstation.com/). I handled all the programming and my [friend](https://garethkeenan.artstation.com/) handled all the art.

{{< cards cols=1 >}}
<div class="flex" style="margin-top: 0.8em;">
    <h2 class="challenges-head">Challenges:</h2>
    <p class="challenges-paragraph"><strong>Game Maker Studio scripting:</strong> <br> Game Maker Studio 2 had only got struct support just before this project. Although it was challenging to program, it meant finding creative ways to make things work. If i was to revisit this, I would use <a href="/projects/#dino" style="color: #0369a1; text-decoration: underline;">Dino</a> for it. </p> 
    <p class="challenges-paragraph"><strong>Isometric perspective in 2D:</strong> <br> This was my first time creating an isometric game in 2D. this meant i needed to learn new formulas for handling positions. </p>
    <p class="challenges-paragraph"><strong>UI:</strong> <br> Game Maker Studio 2 does not have any build in UI tools out of the box, just sprites and collision, the building blocks for UI. </p>
</div>
{{< /cards >}}

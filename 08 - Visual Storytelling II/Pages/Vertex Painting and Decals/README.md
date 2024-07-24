# Vertex Painting and Decals

<h2>Objective</h2>
<p>Learn how to effectively use decals&nbsp;and vertex painting to break up repetitions and to add variety to your scene.</p>
<h2>What We'll Cover</h2>
<ul>
<li>Prepping a mesh for Vertex Painting</li>
<li>Vertex Paintable Materials</li>
<li>Setting up Decals</li>
<li>Using Decals</li>
</ul>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Vertex Painting</h2>
<p dir="ltr"><img style="float: right; padding: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/860/preview?verifier=PqXnmuwK5AYeY4xPEcRmTZU1fRHpSidZZyCNxBC5" alt="VertexPainting.jpg" width="600" height="305" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/860" data-api-returntype="File"></p>
<p style="text-align: left;">Vertex painting is the act of painting directly on the mesh. As you paint, it is associating that color with the vertex point you are painting on. How we take advantage of Vertex Painting in Unreal Engine is by treating these vertex colors as masks. This means we can blend between different materials on a single mesh by painting the blends. This is really useful for creating variation in your scene and breaking up repetition.</p>
<p><strong>Things to Remember:</strong></p>
<ul>
<li>For Vertex Painting to work, your mesh needs to have enough vertices to be able to paint</li>
<li>A vertex paintable material is only one draw call, but all textures for each layer still have to be loaded into memory</li>
<li>Vertex painting lets seamlessly blend between two texture sets</li>
</ul>
<hr style="clear: both;">
<h2 style="text-align: left;">Decals</h2>
<p><img style="float: right; padding: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/862/preview?verifier=pcGDeW29jgPXNgw707NohUpPdX1mrM5Wj0NL1hFf" alt="DecalExample.jpg" width="600" height="355" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/862" data-api-returntype="File"></p>
<p>Decals are materials that are projected onto existing geometry. A decal can be something like a poster on a wall or trash on the ground. They allow you to add extra details into a level without having to create additional geometry or texture variations.</p>
<p>&nbsp;</p>
<p><strong>Things to Remember with Decals:</strong></p>
<ul>
<li>Decals have been widely used in the game industry for nearly 2 decades</li>
<li>Decals can be resized and rotated freely</li>
<li>Decals are most useful when they are reusable</li>
<li>Translucent decals don't work with baked static lighting. You need a dynamic or stationary light for it to show up.</li>
</ul>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Using Vertex Painting &amp; Decals</h2>
<p>Vertex painting and decals can be a powerful tool for enhancing your environment. They can add variation and break up repetition. In this video guide below, we'll walk through how to set up Vertex Painting and create Decal Materials.</p>
<p>&nbsp;</p>
<h3>Part 1: Setting up Vertex Painting</h3>
<p><iframe src="https://player.vimeo.com/video/453497490" width="640" height="360" allowfullscreen="allowfullscreen"></iframe></p>
<p>&nbsp;</p>
<h3>Part 2: Creating the Texture Parameters</h3>
<p><iframe src="https://player.vimeo.com/video/453497793" width="640" height="360" allowfullscreen="allowfullscreen"></iframe></p>
<p>&nbsp;</p>
<h3>Part 3: Creating a Decal Material</h3>
<p><iframe src="https://player.vimeo.com/video/453497910" width="640" height="360" allowfullscreen="allowfullscreen"></iframe></p>
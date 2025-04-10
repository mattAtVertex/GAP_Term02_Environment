# The Mid Poly Technique

<p>You're familiar with the idea of high poly modeling and low poly modeling. You build a high poly and bake it down to a low poly version. Simple enough.</p>
<p>Now we want to introduce you to a new concept: Mid Poly.</p>
<p>Mid Poly modeling is a technique used widely in the game industry. You've likely experienced quite a bit of mid poly models in games you may already be familiar with. Games such as Alien Isolation, Spiderman, and Cyberpunk 2077 have taken advantage of this technique at length. It can be really helpful for building out large open worlds, as well as making confined spaces look highly detailed.</p>
<p>&nbsp;</p>
<hr>
<h2>What is Mid Poly?</h2>
<p><img style="float: right; margin: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/817/preview?verifier=OcsljL5Pr8NjBVoq0BQsFp6lOQ2SBdayGEwG4snY" alt="LowPolyVsMidPoly.jpg" width="600" height="404" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/817" data-api-returntype="File"></p>
<p>Mid Poly modeling involves using additional smoothed normals instead of 90 degree angles. In simpler terms, it means beveling your edges instead of using hard edges. You can imagine how well this can make a fully baked model look --and it's true, our baked models are sporting higher polycounts these days -- but mid poly modeling reduces the need for high poly models to make a game model look fleshed out.&nbsp;</p>
<p><strong>Characteristics of a Low Poly</strong></p>
<ul>
<li>Mostly hard edges, bevels only used where needed</li>
<li>Multiple smoothing groups</li>
<li>As few triangles as possible</li>
<li>Highly optimized but less fidelity</li>
</ul>
<p>&nbsp;</p>
<p><strong>Characteristics of a Mid Poly</strong></p>
<ul>
<li>All 90 degree angles beveled</li>
<li>One smoothing group</li>
<li>Optimized triangle count while still maintaining beveled edges</li>
<li>Allows for unique style while also staying optimized</li>
</ul>
<div style="clear: both;">
<hr>
<h2>Smooth Normals</h2>
<p>Normals are the tangents that shoot out from vertices. The normal direction can be visualized in most 3D software.&nbsp;</p>
<p>&nbsp;</p>
<p><strong>Low Poly</strong> - In a low poly model, the hard edges are a clean 90 degree angle. These hard edges typically separate smoothing groups.&nbsp; At the junction of 3 hard edges, you can visualize how this one corner separates 3 faces in order for the graphics engine to compute the lighting.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/815/preview?verifier=ShEZT1jjhwSeaUqo9UHVxKlXY7t85Cl2GNS9NVv2" alt="LP-NormalDirection.jpg" width="460" height="191" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/815" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p><strong>Mid Poly</strong> - In the mid poly example, the edges have been beveled and the edges smoothed. The 3 normal directions are split so the lighting only has to compute one direction per vertex. This creates more realistic lighting and will result in nice highlights along these bevels.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/814/preview?verifier=kJvwDPtCLBWE16x2dqvbTcXs07ziPp9yclnRDpXB" alt="MP-NormalDirection.jpg" width="460" height="191" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/814" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p>Using the mid poly technique, allows you to create more complex shapes that react more realistically to lighting without the need to build a high poly and go through the baking process.</p>
<p>&nbsp;</p>
<hr>
<h2>Modularity, Mid Poly, and The Texture Conundrum</h2>
<p><img src="https://vertexschool.instructure.com/courses/17/files/822/preview?verifier=fl80pdU5zSEku2U2h7DJXjeyV9h6CkWXhebNaZFG" alt="TextureStyles_MidPoly.jpg" width="800" height="438" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/822" data-api-returntype="File"></p>
<p>Without the need to build a high poly, the mid poly process reduces the amount of time necessary to create finished looking assets. We can take advantage of this to enhance our modularity. Using modular kits speeds up level creation. Pairing modularity with mid poly modeling allows us to reuse the same models with different textures.&nbsp;</p>
<p>When talking about modularity with the mid poly technique, the main advantage is that you can build a solid model, then swap out textures. Without the need for a normal map baked from the high poly, it's as easy as switching materials. This is very similar to how we work with trim sheets.&nbsp; There are 3 major techniques that we can employ:</p>
<ul>
<li>Tileable Textures</li>
<li>Trim Sheets or Texture Atlases</li>
<li>Baked + Tileable</li>
</ul>
<p>In order to take advantage of these techniques to their fullest, we need to make sure that we are beveling our edges where necessary. For smaller corners, a 2 segment bevel usually works.&nbsp; For some of the larger corners, it's appropriate to use a 3 segment bevel. In the case of a silhouette changing chamfer on the model that is supposed to have sharp corners, it's a good idea to go in and bevel those edges as well.</p>
<p>&nbsp;</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/816/preview?verifier=Y8mRPTMCZBxNRD702tRQLzQYErSyOuYq4vWWTKik" alt="BeveledEdgesOnPillar.jpg" width="800" height="498" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/816" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<div style="clear: both;">
<hr>
<h2>Texturing with Tileable Textures</h2>
<img style="float: right; margin: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/818/preview?verifier=lEH8V8LKAed6uS4FCRQ49u9ogGDyIGZ9gIgpSlqw" alt="SameModel-DifferentMats.jpg" width="600" height="443" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/818" data-api-returntype="File">
<p style="text-align: left;">The first major method is using tileable textures on your mid poly models. One of the strongest benefits from this method is that when your scene is set up this way, large swatches of map can be changed varied just by switching a material. This actually gives level designers the power to make these changes and variations without relying on an environment artist to come in and do it for them. The speed that this adds to the development saves studios a lot of money and gets more complex games out the door to the consumer faster.</p>
<p>&nbsp;</p>
<h4><strong>How to work with Tileables in Mid Poly</strong></h4>
<ul>
<li>Mesh follows mid poly guidelines and utilizes bevels</li>
<li>Mesh has multiple material slots</li>
<li>Tileable materials can be assigned and swapped</li>
</ul>
<p>&nbsp;</p>
<div style="clear: both;">
<hr>
<h2>Texturing with Trim Sheets</h2>
<p><img style="margin: 0px 0px 20px 20px; float: right;" src="https://vertexschool.instructure.com/courses/17/files/819/preview?verifier=NLIu0BfEwIN7JdiUqtXIxU5e4lZQoDjK5m3oFrnI" alt="MidPoly-TrimSheet.jpg" width="600" height="437" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/819" data-api-returntype="File"></p>
<p>When working with trim sheets, the mid poly approach can push them further. You would still bevel your edges and try to avoid the 90 degree angles. Often times you might need more cuts to take full advantage of dividing up the faces, but this won't drive the polycount too far. When using the mid poly approach, the extra detail can mean a need for less trim sheets overall, because many of the larger details you would want to capture are now in the mesh itself. This ultimately ends up being better for performance that having lower polycounts but more trim sheet variants.</p>
<p>&nbsp;</p>
<h4><strong>How to work with Trim Sheets in Mid Poly</strong></h4>
<ul>
<li>Mesh follows mid poly guidelines and utilizes bevels</li>
<li>Mesh typically has one material slot</li>
<li>UVs are divided and arranged on trim sheet</li>
</ul>
<div style="clear: both;">
<hr>
<h2>Baked + Tileable</h2>
<p><img style="float: right; margin: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/820/preview?verifier=tkw1hQ8V3l9TLrj6ShX4VtIzVXjuhtaVtZonG7B0" alt="Desert-BakedTileable.jpg" width="600" height="323" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/820" data-api-returntype="File"></p>
<p>Another interesting technique that can help push the technique further involves taking advantage of the high poly normal map workflow. The difference here being that you would bake your high poly down onto something more mid poly than low poly. The process involves using a baked normal map (and sometimes even a baked height map) to establish the foundation, then overlaying a tileable texture on top of that. The normal and height maps are the only ones baked, the rest of the channels (base color, roughness, metalness, ambient occlusion) would utilize a tileable texture.&nbsp; For efficiency and variety, masks are often used with this method to add different materials to different areas.</p>
<p>&nbsp;</p>
<h4><strong>How to work with a Baked + Tileable Workflow</strong></h4>
<ul>
<li>High poly model baked down to a mid poly with proper bevels</li>
<li>Rely heavily on the mid poly for large silhouette changes</li>
<li>Rely on normal/height map for capturing large details</li>
<li>Use tilelable materials for the rest</li>
</ul>
</div>
</div>
</div>
</div>
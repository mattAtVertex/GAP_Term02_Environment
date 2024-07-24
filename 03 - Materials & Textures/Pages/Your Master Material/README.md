# Your Master Material

<h2>Creating Your Master Material</h2>
<p>To make life easier in building your scene, you'll want to create a master material so you can quickly create new instances and just assign textures to the instance. See the links below for assistance on creating your own Master Material in Unreal.</p>
<ul>
<li><a href="https://www.vertexschool.com/products/unreal-engine-level-one-foundations/categories/2256936/posts/7541428" target="_blank">Video Walkthrough of Creating Master Materials from Unreal Foundations Course</a></li>
<li><a href="https://docs.google.com/document/d/1KcfF1hXuiJOFuvHCWoQu0xjXOxDvWKkNdoYkXpOpfO4/edit?usp=sharing" target="_blank">Written Handout Guide for Creating Master Materials in Unreal</a></li>
</ul>
<hr>
<h2>Gray - Packed Textures</h2>
<p>To save on video memory and to optimize performance, we often use a technique called gray packing.&nbsp; Gray packing involves taking the material maps that are single channel grayscale and packing them into the RGBA channels of a single texture.&nbsp; We then set them as masks and use the individual channels separately. Even though individual grayscale image files use a similar amount of video memory, gray packing still saves on performance because it only has to load a single texture instead of multiple, thus leaving behind a smaller footprint.</p>
<p>For example, t<span style="font-weight: 400;">he <strong>ORM texture</strong> is a gray packed texture, which means individual color channels contain a grayscale map. The Letter combination tells us exactly what is in each channel.</span></p>
<p><span style="font-weight: 400;"><strong>Red Channel [O]</strong> - Ambient Occlusion<br><strong>Green Channel [R]</strong> - Roughness<br><strong>Blue Channel [M]</strong> - Metalness<br></span></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/857/preview?verifier=bd1ytN2NwYqq3yEb5vtdNgqK9Fv5NLkEvb3WVRfV" alt="GraypackedORM.png" width="700" height="394" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/857" data-api-returntype="File"></span></p>
<hr style="clear: both;">
<h2>Parameterization</h2>
<p>One of the primary benefits of using a Master Material is that you can parameterize many common elements. This allows you to define a consistency among materials and control how the instances work. Common details you might change --such as texture inputs or UV scaling multipliers -- can be converted to parameters and edited on the material instance. This will make it fast to create a new material within the standard parameters. In the example image below using a simple standard material for Unique textures, you would just need to create a material instance and swap out the textures on the new instance.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/858/preview?verifier=ntwfv9mCYl2AXzFwIOrI3vxV1R3STQEuzaWrggeK" alt="MaterialParameters.jpg" width="900" height="382" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/858" data-api-returntype="File"></p>
<hr style="clear: both;">
<h2>UV Scaling</h2>
<p>For your tileable textures, you can take advantage of Unreal's ability to scale the UVs. Each Texture Sample Node has an input called UVs. You can use this input to control the UV scale by multiplying the TexCoord node by a Constant node with the ratio you want to scale, then convert that Constant node to a parameter and control it on the instance. A value of 1 would mean the texture is mapped to the standard 0-1 UV space. This is the default as if you were not using a TexCoord scalar at all. On the instance, you could then increase the value of this number to make the texture tile more.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/859/preview?verifier=Jf6x9tnrXxXMe9pxITr7Yx15ZgB34NbLWLINQ9tN" alt="TexCoord-UVScaling.png" width="700" height="276" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/859" data-api-returntype="File"></p>
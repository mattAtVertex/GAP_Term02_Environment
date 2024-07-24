# Adding Fog to a Scene

<h2>Objective</h2>
<p>In this exercise, we're going to add fog to an exterior scene.</p>
<p>&nbsp;</p>
<p><em><strong>Things to Remember:</strong></em></p>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Our final fog color is going to be dependent on the surrounding sky light and the directional light.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">A Common mistake is using crazy numbers or large steps. Try to adjust in smaller steps.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Lighting is all about balance. If our fog density is too high or too low, some settings might not show a noticeable effect at all.</span></li>
</ul>
<p>&nbsp;</p>
<hr>
<h2>First Pass Fog</h2>
<p><span style="font-weight: 400;">We want to add an </span><strong>Exponential Height Fog</strong><span style="font-weight: 400;"> to our scene. Atmospheric is useful for larger open world scenes where you can see really far off in the distance. For most scenarios, the Exponential Height Fog is going to be our primary scene fog source. </span></p>
<p><span style="font-weight: 400;">With our <strong>Exponential Height Fog</strong> in the scene and our base lighting set up, we can start to make some adjustments.</span></p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/890/preview?verifier=vYYrUWNaOJ1YWB7dHc0dJhNwT7h000m2yjp5pScl" alt="fog-01.png" width="900" height="507" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/890" data-api-returntype="File"></p>
<h3>Setting Up the Base Fog Settings</h3>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">It’s good to set the </span><strong>fog density</strong><span style="font-weight: 400;"> to 1.0 for testing things out so you can see the actual changes.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Next we want to turn on </span><strong>Volumetric Fog</strong><span style="font-weight: 400;">. This is the bread and butter that holds our most powerful fog features.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Our </span><strong>Albedo </strong><span style="font-weight: 400;">is the overall ambient color and should be similar to the sky color. A good way to do this is to use the eyedropper to sample a color from a cloud in your sky sphere.&nbsp;</span>
</li>
<li style="font-weight: 400;">
<strong>Leave Volumetric Emissive and Max Fog Opacity alone for now</strong><span style="font-weight: 400;">. This comes later in the final steps.</span>
</li>
</ol>
<p>&nbsp;</p>
<h3>Using Inscattering Settings with Volumetric Fog</h3>
<p><span style="font-weight: 400;">With Volumetric Fog turned on, this disables the </span><strong>Inscattering Texture</strong><span style="font-weight: 400;"> and </span><strong>Directional Inscattering</strong><span style="font-weight: 400;"> sections. We can however reactivate these by explicitly telling the rendering engine to use them with volumetric fog. This can be useful for when you need to get some really good closeup fog effects in the foreground.&nbsp;</span></p>
<p><strong>These are not always needed</strong><span style="font-weight: 400;">.</span></p>
<p><span style="font-weight: 400;">If we do want to make use of these:</span></p>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Check </span><strong>Override Light Colors with Fog</strong><span style="font-weight: 400;">. This will allow us to use the Inscattering settings.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">The sky light and directional light will now use the Inscattering options we set in the Exponential Height Fog.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">We can set an HDRI texture in the </span><strong>Inscattering Texture</strong><span style="font-weight: 400;">. When setting this texture, the Fog </span><strong>Inscattering Color</strong><span style="font-weight: 400;"> in the main parameters section will be completely ignored. This HDRI will be used instead.</span>
</li>
</ol>
<p><br><strong>Common Mistake</strong><span style="font-weight: 400;">: Using crazy scattering numbers. Remember to make small adjustments.</span></p>
<p>&nbsp;</p>
<hr>
<h2>Adjusting the Initial Fog Settings</h2>
<p><img src="https://vertexschool.instructure.com/courses/17/files/920/preview?verifier=nbgBaMcssvAKZSMEJ7Alvf4xkDnmJ0Ufgav3TUkG" alt="fog-02.png" width="900" height="491" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/920" data-api-returntype="File"></p>
<p><span style="font-weight: 400;">With our fog set up, now it’s time to start tweaking the settings. Remember to make adjustments in small values. It’s best to follow the half step rule (adjust in amounts like 0.50 to 0.55 to 0.60).</span></p>
<p>&nbsp;</p>
<h3><span style="font-weight: 400;">Exponential Height Fog Component Parameters</span></h3>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/884/preview?verifier=2qPWnOtzfTnkYLoVzj5EPwBqzFJSN6wWjUIIRHRa" alt="fog-03.png" width="500" height="271" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/884" data-api-returntype="File"></span></p>
<ul>
<li style="font-weight: 400;">
<strong>Fog Density</strong><span style="font-weight: 400;"> - The global density factor. Remember the general number you set here, as we’ll often temporarily crank it up to 1.0 to judge effects then take it back down.</span>
</li>
<li style="font-weight: 400;">
<strong>Height Falloff</strong><span style="font-weight: 400;"> - This controls how dense the fog is as height increases, but note that the </span><strong>value relation appears reversed</strong><span style="font-weight: 400;">. Lower this value to make the fog thicker up high and raise it to thin out the fog up top and bring the thickness cutoff lower.</span>
</li>
<li style="font-weight: 400;">
<strong>Height Offset</strong><span style="font-weight: 400;"> - This is used to offset the origin point. This can be useful if your map is at a higher altitude and you need to raise the base of the fog to match.</span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">Second Fog Data</strong><span style="font-family: inherit; font-size: 1rem;"> - This adds an extra layer of fog thickness with similar parameters as above.</span>
</li>
</ul>
<p>&nbsp;</p>
<h3>Volumetric Fog Parameters</h3>
<p><img src="https://vertexschool.instructure.com/courses/17/files/912/preview?verifier=sq1Vboz29sV9Bi31OOXBwuunxC43XOBzfHkcPNtW" alt="fog-04.png" width="500" height="287" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/912" data-api-returntype="File"></p>
<ul>
<li style="font-weight: 400;">
<strong>Scattering Distribution</strong><span style="font-weight: 400;"> - This controls how much incoming light scatters in various directions. 0 scatters equally in all directions where 0.9 scatters predominantly in the light direction. You’ll typically get the most realistic effects on the lower end.</span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">View Distance</strong><span style="font-weight: 400;"> - Arguably one of the most powerful parameters, this affects how far you can see the fog. This controls the illusion of the thickness of the fog.</span>
</li>
</ul>
<p>&nbsp;</p>
<h3>Using the Directional Light to Affect the Fog</h3>
<p><img src="https://vertexschool.instructure.com/courses/17/files/878/preview?verifier=fv3K8a6q6nJUL7N3FNoafOFa0mHqJsOmjIchIA2f" alt="fog-05.png" width="500" height="338" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/878" data-api-returntype="File"></p>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Unifying fog color with the light source’s color will make the fog blend better.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">You can crank up the directional light intensity to get more scattering in the fog.</span></li>
<li style="font-weight: 400;">Higher values in <strong style="font-family: inherit; font-size: 1rem;">Volumetric Scattering Intensity</strong><span style="font-weight: 400;"> will push the sunlight scattering in the fog.</span>
</li>
</ul>
<p><span style="font-weight: 400;">At this point we want to have a really solid base with our fog before we dive deep into tweaking the settings further. We want to avoid over exposure and set things up as physically correct as possible so we get proper results from tweaking further settings.</span></p>
<p>&nbsp;</p>
<hr>
<h2>Tweaking the Scene</h2>
<p><img src="https://vertexschool.instructure.com/courses/17/files/906/preview?verifier=zVEbsZJGmvx9PNeEr2zrEzkUr4z4iwP7vDyAy5Hw" alt="fog-06.png" width="900" height="490" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/906" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p><span style="font-weight: 400;">Now that we have a strong base to work with, it’s time to start tweaking our settings to define the mood of our scene.&nbsp;</span></p>
<p><span style="font-weight: 400;"><strong>Note</strong>: your numbers will be different based on your scene. It’s all about taste.</span></p>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Taking the </span><strong>Volumetric Extinction Scale</strong><span style="font-weight: 400;"> down will push the fog back some.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">This might hide our skybox, so we can fix this by adjusting the </span><strong>Volumetric Scattering Intensity</strong><span style="font-weight: 400;"> in our </span><strong>Sky Light</strong><span style="font-weight: 400;">:</span>
</li>
<ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">Take the intensity lower when using higher fog density</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Take it higher when using a lower fog density</span></li>
</ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">For our scene, we can use a higher value paired with a lower fog density.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">We’ll take global fog density down a bit (ie: 0.06)</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">We want to use Second Fog Data so we’ll take the density up from 0 (ie: 0.5) and bring the falloff up from 0 (ie: 1).</span></li>
<li style="font-weight: 400;">Sky light color will affect the fog color through scattering. We can control the scattering colors by adjusting the <strong style="font-family: inherit; font-size: 1rem;">Sky Light’s Light Color</strong><span style="font-family: inherit; font-size: 1rem;">. Try adjusting the saturation first and then the value.<br></span><strong style="font-family: inherit; font-size: 1rem;">Be careful here</strong><span style="font-family: inherit; font-size: 1rem;">: while adjusting the sky light color will work well for the fog in the back, it can also kill off the fog closer to the camera.</span>
</li>
</ol>
<p>&nbsp;</p>
<hr>
<h2>Final Touches</h2>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">To finish up the fog in our scene, we make some more tweaks to get the atmosphere we want. At this point focusing largely on nailing the correct </span><strong>Fog Density</strong><span style="font-weight: 400;"> while pushing the View Distance of the </span><strong>Volumetric Fog</strong><span style="font-weight: 400;"> back. This will give us a heavier fog in the distance.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Here we can adjust the </span><strong>Emissive of the Volumetric Fog</strong><span style="font-weight: 400;"> to control the top area color of the fog. For example, driving warmer colors from the sun or cooler colors from the moon. But try to keep it on the less saturated side only slightly more than grayscale (ie: use brown for the sun, not yellow or orange).</span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">Fog Max Opacity</strong><span style="font-weight: 400;"> is the final touch. After we have built out our fog, we can take this value down if the fog is too thick.</span>
</li>
</ol>
<p><img src="https://vertexschool.instructure.com/courses/17/files/905/preview?verifier=Rgn7NA5E0CNsLGuQ6QsFXv26Ibq6JEhF2PZo1tv3" alt="fog-07.png" width="900" height="487" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/905" data-api-returntype="File"></p>
<p>&nbsp;</p>
<hr>
<h2>Final Thoughts</h2>
<p><span style="font-weight: 400;">Now that we’ve set up our fog, some takeaways to remember:</span></p>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Lighting is not about Maybe. It’s all about The Plan.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Build a really solid base with your fog before moving any further with complex lights. A solid base will give better results as you add more lights and color grading.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Set things up as physically correct as possible from the beginning so all of the settings provide proper results.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">The aim is to get good color gradients in the atmosphere.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Always keep composition in mind from the beginning.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Build in layers. Get each piece to a point and leave it alone. “Lock it.” Get the fog right and lock it. Get the directional light right and lock it. Get the sky light right and lock it. After this, leave them alone as you’re working with other elements to light your scene.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Always keep your lights and fog colors on the less saturated side. Higher value is fine, but saturation should never go above 0.5.</span></li>
</ul>
<p>&nbsp;</p>
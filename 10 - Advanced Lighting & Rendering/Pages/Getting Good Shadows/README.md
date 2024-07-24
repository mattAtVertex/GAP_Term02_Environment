# Getting Good Shadows

<p>Shadows are an important part of any good lighting scenario and getting good shadows is always an exciting part of the lighting process. Throughout your scene, you're going to have soft shadows from indirect lighting, but more defined shadows can often really help with your composition. How you approach these shadows can really affect how well you sell the lighting in your scene. For example, an overcast day might find a scene shrouded in mostly soft diffused shadows, where a strong light source could cast a sharp shadow from the silhouette of your hero prop.</p>
<p><span>Shadows make objects feel grounded in the world and give the viewer a sense of depth and space. Static shadows are free as far as rendering goes, but dynamic shadows can be one of the biggest drains on performance.</span></p>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Soft vs Sharp</h2>
<p><img style="float: right; padding: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/873/preview?verifier=VdPWq3fYsqbxIdeK4e0wuZoxT6nSffgNaRjF149I" alt="Soft-v-Sharp_shadows.jpg" width="600" height="423" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/873" data-api-returntype="File"></p>
<p>There are two ends to the spectrum of shadow: The razor sharp edge between dark and light of Sharp Shadows&nbsp; vs the soft and subtle diffusion of Soft Shadows.</p>
<p><em><strong>When working with Light Actors in Unreal, there are several parameters you can tweak to control the hardness and sharpness of your shadows:</strong></em></p>
<ul>
<li>
<strong>Attenuation Radius</strong> - The attenuation of the light affects how far the light reaches. The further it goes, the more falloff you tend to see at the edges.</li>
<li>
<strong>Light Falloff Exponent</strong> - This controls the actual falloff when not using Inverse Squared Lighting.</li>
<li>
<strong>Cone Angles</strong> - With spot lights, the distance between the inner and outer cones affects the softness of the falloff.</li>
</ul>
<hr style="clear: both;">
<h2>Contrast</h2>
<p><img style="float: right; padding: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/907/preview?verifier=29PzEBW5WQfpnmnTY3XWpKTBCpjHFquNbtXAwAnr" alt="Maria-Contrast.jpg" width="600" height="347" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/907" data-api-returntype="File"></p>
<p>The level of contrast between the lit areas and shadowed areas can illicit different feelings and emotions. Building a variety of contrasts in your scene can help drive focal points and help set the mood.</p>
<p>Notice in the image on the right how the light shining through the window casts as strong contrast between the light and sharp shadows. Next, notice how the lighting through the rest of the interior outside of direct sunlight is more subdued, the shadows are softer, and the contrast is smaller. This variety of contrast in your scene can help the lighting personality.</p>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Detail in your Shadows</h2>
<p><img style="float: right; padding: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/904/preview?verifier=katF0xNyqafkSLKGsJlW5o0X5vWIlQQ987ydGMyp" alt="warhammer-detail-lighting.jpg" width="600" height="347" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/904" data-api-returntype="File"></p>
<p>One primary mistake that environment artists make when they are first learning how to light a scene is that they go too dark with their shadows. While dark shadows have their place for certain moods, you want to try to avoid pure black wherever possible. Having detail in your shadows will make your environment more believable.&nbsp;</p>
<p>One of the easiest ways to control this is with the <strong>Sky Light</strong>. you should already have a sky light in your scene set up with an HDRI. This Sky Light is controlling the level of detail you see in your shadows. Adjusting the placement and intensities of lights in your scene will help control the variety of contrasts, but your Sky Light can globally control the darkest point your shadows reach. By increasing the intensity of the Sky Light, you can easily lighten up your shadows. Be careful with this though, as the Sky Light intensity is best modified in very small increments such as 0.1.</p>
<p>Notice in the image on the left (in Detail Lighting mode) how even in the shadowy areas, you can read the detail of the geometry and texture.</p>
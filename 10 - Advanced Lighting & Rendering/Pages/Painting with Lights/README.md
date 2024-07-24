# Painting with Lights

<p>When lighting exterior scenes, the largest portion of the light comes from the directional light. For interior scenes and even small areas within an exterior scene, you'll want to utilize other lights for your scene. When you're using additional lights, it's important to think about it from the perspective of "Painting" with the lights.</p>
<p><em><strong>Reasons for Additional Lights:</strong></em></p>
<ul>
<li>Light coming from another light source (ie: a Fire, a Lightbulb, or other light emitting object)</li>
<li>Light to help guide the player along a certain path</li>
<li>Fakking bounce lighting</li>
</ul>
<p>&nbsp;</p>
<hr>
<h2>Light Sources</h2>
<p><img style="float: right; margin: 0 0 20px 20px;" src="https://vertexschool.instructure.com/courses/17/files/899/preview?verifier=9akENDLLPYMTdQbJDYl91lDSMK98rtT881hUkKky" alt="Lamp_LightSources.jpg" width="700" height="396" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/899" data-api-returntype="File"></p>
<p>Our first example for where to use lights is the obvious one:<strong> Light sources</strong>. In the image example, our room has two table lamps. Since the lightbulb of each lamp is a light source, it makes sense to give it a light actor. The lightbulb would be radiating light in all directions, so we would want to use a <strong>Point Light</strong> for this.</p>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Inverse Square Falloff</h2>
<p><img style="float: right; margin: 0 0 20px;" src="https://vertexschool.instructure.com/courses/17/files/892/preview?verifier=l8ZkZdmvQA3wcB2NEOitGQqevOnpzVJuLqyHKy6o" alt="inverse_squared.png" width="354" height="338" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/892" data-api-returntype="File"></p>
<p>Lights in Unreal Engine have a setting called Inverse Square Falloff that is on by default.&nbsp; <strong>Inverse Square Falloff</strong> is a different type of light falloff that most closely replicates the behavior of light in the real world. It causes light to be very bright when closest to its source, and gets dimmer very quickly as it moves away.&nbsp; When you have this turned on for a light, you're telling Unreal Engine to behave like a real light falls off in the real physical world. However, this realistic behavior is very drastic. In some cases, this might work for your particular scene, while in others you may want more control.</p>
<h3>Inverse Square : On vs Off</h3>
<p><em><strong>On:</strong></em></p>
<ul>
<li>Larger Intensity numbers ( ie: 5000.0 )</li>
<li>The attenuation is controlled</li>
<li>Falloff is determined by real world physical behavior</li>
</ul>
<p><em><strong>Off:</strong></em></p>
<ul>
<li>Smaller Intensity numbers ( ie: 3.0 )</li>
<li>Attenuation is controlled by the <strong>Attenuation Radius</strong> parameter</li>
<li>Falloff is controlled by the <strong>Light Falloff Exponent</strong> parameter</li>
</ul>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Light to Guide the Path</h2>
<h2><img style="float: right; margin: 0 0 20px;" src="https://vertexschool.instructure.com/courses/17/files/919/preview?verifier=RpB40QFwP3Ca5ujimPbmqUnEhdesf9pxjFKElhAg" alt="LightingThePath.jpg" width="700" height="438" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/919" data-api-returntype="File"></h2>
<p>Lighting can also be used in games to guide the player on where they should go next. This is accomplished because brighter areas of a scene tend to attract attention. Often times the environment artist will try to work this concept in a way where the light is coming from a specific source. This could mean adjusting the angle of the sun light or it could mean using another light source like a fire or light bulb.</p>
<p>In the concept image from The Last of Us, the sun is reflecting off the water to create a bright area in the scene. This paired with the light coming from the other side of tunnel tells the player to focus their attention over here. This is an important aspect of Level Design and in a game production environment can often be pre-determined before the Environment Artist actually starts working on the lighting for a scene.</p>
<p>&nbsp;</p>
<hr style="clear: both;">
<h2>Applying the Guiding Light Technique in a Portfolio Scene</h2>
<p>When building an environment for your portfolio, you can use this technique to draw attention to certain focal points in your scene. <br>In the example images from Vertex students below, creative lighting is used to draw attention to focal points.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/889/preview?verifier=yP4ev5w3xItrslUhHU0HXYE5mWWkQ5bVUziEy2YU" alt="Andrew_FocalPoint.jpg" width="900" height="507" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/889" data-api-returntype="File"></p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/885/preview?verifier=xWvXh6LhaIOkM4Sx95aOYh7cK5sVWgt0FNMP62FA" alt="Angela_FocalPoints.jpg" width="900" height="507" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/885" data-api-returntype="File"></p>
<p>&nbsp;</p>
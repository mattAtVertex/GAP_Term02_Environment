# Initial Lighting Setup Overview

<h2>Turning off Eye Adaption</h2>
<p><strong>Project Settings: Turning Off Eye Adaption</strong><span style="font-weight: 400;"><br></span><span style="font-weight: 400;">Before we get started, to make our scene easier to work with, let’s go ahead and turn off Unreal’s Eye Adaption functionality. Unreal calls this Auto Exposure. This is the effect where the scene gets darker when you go into a dark room and ramps up brighter when you go into the light. This can cause some frustrations when lighting, so it’s best to turn it off during your first lighting pass, even if you plan to use it later in the game.</span></p>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Go to </span><strong>Edit </strong><span style="font-weight: 400;">&gt; </span><strong>Project Settings</strong><span style="font-weight: 400;"> in the main menu bar.</span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/881/preview?verifier=LSA8RV3K8ZmxqVNpJPq2sN0lRxo4xuyUoRoe7WCF" alt="eye-adaption-01.png" width="500" height="374" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/881" data-api-returntype="File"><br><br></span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Once the </span><strong>Project Settings</strong><span style="font-weight: 400;"> window opens, click in the </span><strong>Search Bar</strong><span style="font-weight: 400;"> up top and type “exposure”. This will filter out the settings we are looking for. Untick the checkbox for </span><strong>Auto Exposure</strong><span style="font-weight: 400;">.</span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/896/preview?verifier=JL4KwTNVRqzRaseAbBZq7sQxS2MBqE1G1U43sifO" alt="eye-adaption-02.png" width="900" height="312" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/896" data-api-returntype="File"><br><br></span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Now </span><strong>restart the editor</strong><span style="font-weight: 400;"> and the </span><strong>Eye Adaption</strong><span style="font-weight: 400;"> feature should be turned off.</span>
</li>
</ol>
<p>&nbsp;</p>
<hr>
<h2>Base Lights for Exterior Scenes</h2>
<p><span style="font-weight: 400;">The base setup of our exterior scene is dictated by two things:</span></p>
<ol>
<ol>
<li style="font-weight: 400;">
<strong>Directional Light Source</strong><span style="font-weight: 400;"> (Our sun or moon)</span>
</li>
<li style="font-weight: 400;"><strong>Sky Light</strong></li>
</ol>
</ol>
<p><span style="font-weight: 400;"><br>The Directional Light is the single most important aspect of your exterior scene. Roughly 40% of your quality will come from this light source. For day time scenes, this is your sun. For night time scenes, this is your moon.<br></span></p>
<p><span style="font-weight: 400;">The Sky Light is a powerful component that defines a large part of our lighting. It acts very much as an HDRI light setup.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/913/preview?verifier=tCg6mAByQmUIrmMGaW3Werkxz40jEtyUoVpUV38v" alt="base-lights.png" width="600" height="326" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/913" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<h3><span style="font-weight: 400;">How Exterior Lighting Affects Interiors</span></h3>
<p><span style="font-weight: 400;">For interior scenes, the initial exterior setup can have a huge impact in the following ways:</span></p>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Consider sunlight shining in through the windows or openings. Typically one of the best ways to accomplish this effect is your </span><strong>Directional Light</strong><span style="font-weight: 400;"> acting as the sun shining through. You can really crank up the light’s intensity to get a stronger sun value.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">The Sky Light is used as an overall scene HDRI setup. This means that it has a huge effect on interior scenes as well. For interior only maps, you can take advantage of this by using an interior focused HDRI.</span></li>
</ol>
<p>&nbsp;</p>
<hr>
<h2>Post Process Volume</h2>
<p><span style="font-weight: 400;">We shouldn’t be doing much with the Post Process at this point. However, this is a good time to get it in the scene so it’s available for later. After we drop one in our scene, there are two things we want to set right off the bat:</span></p>
<ol>
<li style="font-weight: 400;">
<strong>Check Infinite Extent (Unbound)</strong><span style="font-weight: 400;"> - This will allow the post process volume to affect the entire map</span>
</li>
<li style="font-weight: 400;">
<strong>Temp</strong><span style="font-weight: 400;"> under </span><strong>White Balance</strong><span style="font-weight: 400;"> will allow us to control the overall temperature of the scene and help to unify the lighting.&nbsp;</span>
</li>
</ol>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/911/preview?verifier=bVci8uyezjPwAkeHzwIuvcSGWrUg6Pd5BvCtTDLJ" alt="post-process-volume.png" width="497" height="599" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/911" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<hr>
<h2><span style="font-weight: 400;">Key Points to Remember</span></h2>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Lighting is everything. Bad lighting can make a good model look bad and a good lighting can make a bad model look good. Be sure to spend time here early on.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">This part can and should be done during your blockout phase.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Be sure to constantly switch between </span><strong>Lit</strong><span style="font-weight: 400;"> and </span><strong>Detail Lighting</strong><span style="font-weight: 400;"> mode as you are lighting.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">You can turn off shadow casting for individual objects</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Keep light saturation below 0.5 wherever possible.</span></li>
<li style="font-weight: 400;">If you’re not using custom exposure settings, it’s usually best to toggle off <strong style="font-family: inherit; font-size: 1rem;">Auto Exposure</strong><span style="font-family: inherit; font-size: 1rem;"> in the </span><strong style="font-family: inherit; font-size: 1rem;">Project Settings</strong><span style="font-family: inherit; font-size: 1rem;">.</span>
</li>
</ul>
<p>&nbsp;</p>
<hr>
<h2>Creating a Night Time Scene</h2>
<p><span style="font-weight: 400;">If you’re making a nighttime scene using the default Unreal Engine sky sphere, there are a couple of settings we need to keep in mind. Remember that the time of day is linked to the Directional Light actor.</span></p>
<p><span style="font-weight: 400;">When trying to create night, the first thought is to rotate the directional light sun to pointing straight up to bring the skysphere to night time and then add a new directional light to act as the moon. </span><strong>Do not do this</strong><span style="font-weight: 400;">.&nbsp;</span></p>
<h4><strong>To create a night time scene, follow these steps:</strong></h4>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">In the </span><strong>Sky Sphere</strong><span style="font-weight: 400;">, unlink your Light Source from the </span><strong>Directional Light Actor</strong><span style="font-weight: 400;">. You can quickly accomplish this by clicking the yellow back arrow. Your directional light’s rotation will no longer affect the time of day.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">With the light source unlinked, this unlocks the </span><strong>Sun Height</strong><span style="font-weight: 400;"> override setting. This will allow you to manually set the time of day.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Sun Height controlled by a directional light source works great from sunrise to sunset. For night time scenes, most of the time you’ll want to set Sun Height -1.0. This will give you a solid starry sky to work with.</span></li>
</ol>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/879/preview?verifier=qrbI1SG8Rg8NBsvwnfb7vPZMzbM4HLlal8Fc9pjC" alt="nighttime-settings.png" width="496" height="398" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/879" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<hr>
<h2>Working with Reflection Captures</h2>
<p><span style="font-weight: 400;">Unreal uses a system called the Reflection Environment to provide reflectivity in the level. This is essential for many important materials like metal and glossy plastics. The quickest way to get this set up and running in your scene is with Reflection Capture Spheres.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/908/preview?verifier=04Ii07o6Y8BqxwZNqYWVfYBQaY074bad04dWZP4N" alt="reflection-captures.png" width="700" height="383" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/908" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<h4><strong>Setting up a reflection capture is really easy:</strong></h4>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">From the </span><strong>Modes</strong><span style="font-weight: 400;"> panel under </span><strong>Visual Effects</strong><span style="font-weight: 400;">, drag in a </span><strong>Sphere Reflection Capture</strong><span style="font-weight: 400;"> into your scene.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">The reflection capture is going to capture a cubemap based on rays shot out from the sphere, so make sure not to place it too close to any geometry as that geo will block any details behind it. Make sure everything that needs to have reflections is located within the radius of the reflection capture.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Under the </span><strong>Build Menu</strong><span style="font-weight: 400;">, click </span><strong>Build Reflection Captures</strong><span style="font-weight: 400;">.</span>
</li>
<li style="font-weight: 400;">You can check the reflections by changing the viewport mode to <strong style="font-family: inherit; font-size: 1rem;">Reflections</strong><span style="font-family: inherit; font-size: 1rem;">.<br><br><img src="https://vertexschool.instructure.com/courses/17/files/917/preview?verifier=2zBIbJzdAlMFWBjJaGoG66j7L6dzamZVrr4Lc3tf" alt="reflection-02.png" width="400" height="308" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/917" data-api-returntype="File"><br></span>
</li>
</ol>
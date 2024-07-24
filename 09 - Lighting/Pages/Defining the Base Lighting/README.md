# Defining the Base Lighting

<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">First thing we want to do is make sure we are working without any </span><strong>Reflection Captures</strong><span style="font-weight: 400;"> or have them turned off. We can do this by selecting the </span><strong>Reflection Capture</strong><span style="font-weight: 400;"> and setting </span><strong>Visible</strong><span style="font-weight: 400;"> to false under </span><strong>Rendering</strong><span style="font-weight: 400;">.</span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/872/preview?verifier=JA9zqLNCH1nTsWffTSqZt6bLBxTcRQe2PxijcDT4" alt="baselighting-01.png" width="498" height="339" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/872" data-api-returntype="File"><br></span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;">The reason we want to work with them off is because they affect the localized lighting through reflective surfaces.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Next we typically determine our time of day. For this exercise, we will focus on day time. When using the default sky sphere, the directional light will control the time of day because it acts as the sun position.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Then it’s time to take control of our </span><strong>Directional Light</strong><span style="font-weight: 400;">. An effective directional light is all about balance.</span>
</li>
<ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">We want to capture good shadows from our directional light. Play with the directional angle of your light until you get something appropriate for your aesthetic. Try to avoid shadows that are too short or too long.&nbsp;</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">We should always be using </span><strong>Stationary or Moveable</strong><span style="font-weight: 400;"> with our </span><strong>Directional Light</strong><span style="font-weight: 400;"> so we capture dynamic shadows. The dynamic lighting will also infuse into the fog once we set it up.<br><img src="https://vertexschool.instructure.com/courses/17/files/876/preview?verifier=jMJP1mHQtXKyRyEZOnYevyplUdrbs2555b6NQiBu" alt="baselighting-02.png" width="400" height="32" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/876" data-api-returntype="File"><br></span><span style="font-weight: 400;"><br></span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">If we modify the color of the light, then we want to lean towards a warmer color for the sun and a cooler color for the moon. We don’t need much saturation here, so be careful not to go overboard.<br><img src="https://vertexschool.instructure.com/courses/17/files/875/preview?verifier=Mtopa5g6QvHAcEV2GxsP8B42IwJ4aM17t5r7biQB" alt="baselighting-03.png" width="400" height="307" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/875" data-api-returntype="File"><br></span><span style="font-weight: 400;"><br></span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Keep in mind that the sunlight color will translate into your fog.</span></li>
</ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Next we want to make sure our </span><strong>Sky Light</strong><span style="font-weight: 400;"> is set up.</span>
</li>
<ol>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Set the sky light’s mobility to </span><strong>Moveable</strong><span style="font-weight: 400;">. We do this so we can see updates in real time without having to rebuild lighting every time we make a change.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">We can use the </span><strong>Sky Light Color</strong><span style="font-weight: 400;"> to enhance the scene. Use a cooler color here and take note that it has major control over the color in the shadows.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Be sure to keep the saturation of the color low and use the value of the color to control brightness.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Make sure the sky light is set to </span><strong>Cast Shadows</strong><span style="font-weight: 400;">.</span>
</li>
</ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">This gives us a strong base to work with.</span></li>
</ol>
# Using the Skylight in Unreal Engine

<p>One of the first things you need to take control of is your <strong>Skylight</strong>. This goes for interiors too! The skylight is essentially an HDRI light setup for your scene. By default it will use the captured scene, but you can plug in your own HDRI too!</p>
<p><iframe src="https://player.vimeo.com/video/451633031" width="640" height="360" allowfullscreen="allowfullscreen"></iframe></p>
<hr>
<h2>Demystifying the Sky Light</h2>
<p><span style="font-weight: 400;">The Sky Light is a powerful component that defines a large part of our lighting. It acts very much as an HDRI light setup. It can do this in two different ways:</span></p>
<ol>
<li style="font-weight: 400;">
<strong>Captured Scene</strong><span style="font-weight: 400;"> - In this mode, the sky light takes a screen capture of the sky and uses that as an HDRI.</span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">Specified Cubemap</strong><span style="font-weight: 400;"> - In this mode, you assign an HDRI map.</span>
</li>
</ol>
<p><span style="font-weight: 400;">One of the primary purposes of the Skylight is to <strong>add detail in the shadows</strong>.</span></p>
<h3>Common Settings</h3>
<ul>
<li style="font-weight: 400;">
<span style="font-weight: 400;">When using the Captured Scene mode, the </span><strong>Sky Distance Threshold</strong><span style="font-weight: 400;"> sets distance from the sky light where any geometry is treated as the sky. Anything beyond this will contribute to the overall captured scene. This also affects the reflection captures as well.</span>
</li>
<li style="font-weight: 400;">
<strong>Light Color</strong><span style="font-weight: 400;"> works in both modes and affects the overall color tint. This can also affect the intensity of the light when adjusting the color value. This can drive the color of your shadows.</span>
</li>
<li style="font-weight: 400;">
<strong>Indirect Lighting Intensity</strong><span style="font-weight: 400;"> controls how much the sky light affects indirect light in the global illumination. This has a noticeable effect in the shadowed areas.</span>
</li>
<li style="font-weight: 400;">
<strong>Volumetric Scattering Intensity</strong><span style="font-weight: 400;"> controls the scattering of this light when using Volumetric Fog</span>
</li>
</ul>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/17/files/866/preview?verifier=jTxOPLojirsivICa7SXrq8OB4qmJtyPxFyQhY3Kc" alt="SkylightSettings.png" width="492" height="449" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/866" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<hr>
<h2>Setting Up Your HDRI</h2>
<p>The HDRI is one of the most important aspects of the sky light. It's going to help define the atmosphere the underlying tone of your scene and emphasize the color scheme in your shadows. Setting it up involves just a few steps:</p>
<ol>
<li>Set the Sky Light to use Specified Cubemap</li>
<li>Assign your HDRI texture to the Cubemap property</li>
<li>Adjust the Cubemap Angle to get the desired lighting effect</li>
</ol>
<p><img src="https://vertexschool.instructure.com/courses/17/files/863/preview?verifier=CeFVUo9l7rmxTyCzOmzRMCPhDUyiNcRJVZejJVcD" alt="Setting up Cubemap.png" width="495" height="458" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/863" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p>For a Step-by-Step, you can <a href="https://docs.google.com/document/d/1yyqoMfMgTRz6v9MTTles7BY8v-bQMBsJJaRK8bsofFg/edit#heading=h.c8ebf2cd3y2p">Follow This Guide</a></p>
<hr>
<h2>Finding an HDRI</h2>
<p>The HDRI is important to your mood, so finding the right one is vital. Having options to test out is even more vital. A good place to find free HDRI images to use is <a href="https://hdrihaven.com/"><span style="font-weight: 400;">https://hdrihaven.com/</span></a> . They have a lot of options in there that will usually cover all needs.</p>
<p><img src="https://vertexschool.instructure.com/courses/17/files/861/preview?verifier=li6pWxKkoeDJKMxwSEA5TP6qA6gY9NcxeJbVmlx8" alt="HDRIHaven.png" width="700" height="562" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/861" data-api-returntype="File"></p>
<p>&nbsp;</p>
<p>The files that you download should import into Unreal just fine as is and can be immediately plugged into your sky light. You don't need to grab a huge resolution either.&nbsp; The 2k size is more than efficient.&nbsp; Remember to choose an HDRI that is going to match the lighting scenario of your scene. Don't be afraid to try a couple of different ones until you get the right setup.&nbsp;</p>
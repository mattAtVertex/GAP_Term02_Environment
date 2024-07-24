# Demystifying the Skylight

<p><span style="font-weight: 400;">The Sky Light is a powerful component that defines a large part of our lighting. It acts very much as an HDRI light setup. It can do this in two different ways:</span></p>
<ol>
<li style="font-weight: 400;">
<strong>Captured Scene</strong><span style="font-weight: 400;"> - In this mode, the sky light takes a screen capture of the sky and uses that as an HDRI.</span>
</li>
<li style="font-weight: 400;">
<strong>Specified Cubemap</strong><span style="font-weight: 400;"> - In this mode, you assign an HDRI map.</span>
</li>
</ol>
<p>&nbsp;</p>
<h2>Common Settings</h2>
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
<strong>Volumetric Scattering Intensity</strong><span style="font-weight: 400;"> controls the scattering of this light when using Volumetric Fog<br><br><img src="https://vertexschool.instructure.com/courses/17/files/877/preview?verifier=kBbhpi3csXUn1PGE6miyfPPs12hsd2XSfamn3zIq" alt="demystify-skylight-01.png" width="492" height="449" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/877" data-api-returntype="File"><br></span>
</li>
</ul>
<p>&nbsp;</p>
<h2><span style="font-weight: 400;">Setting up the HDRI</span></h2>
<p><span style="font-weight: 400;">For our purposes here, we want to work with an HDRI.</span></p>
<ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">Set the Sky Light to use Specified Cubemap</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">We want to assign an HDRI in the texture slot. If you already have a collection, you can import those into Unreal. If you need to find an HDRI to use, a good place is HDRI Haven.</span><span style="font-weight: 400;"><br></span><a href="https://hdrihaven.com/"><span style="font-weight: 400;">https://hdrihaven.com/</span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><br><img src="https://vertexschool.instructure.com/courses/17/files/871/preview?verifier=WPrKOmM9Im25rJ0ZLRwAxYhUyPpv9JYKa1PS2Mnl" alt="demystify-skylight-02.png" width="400" height="321" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/871" data-api-returntype="File"></span></a><span style="font-weight: 400;"><br></span><span style="font-weight: 400;"><br></span><span style="font-weight: 400;">HDRI Haven has many free to use HDRIs. When choosing an HDRI, remember to find one that is going to match the lighting scenario you’re going for with your scene.</span>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Import your HDRI into Unreal. You should be able to drag and drop into the content browser or use the import button. There are no special settings needed for importing and using HDRIs.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Once your HDRI is applied, you can use the <strong style="font-family: inherit; font-size: 1rem;">Cubemap Angle</strong><span style="font-family: inherit; font-size: 1rem;"> slider to rotate the image. The intensity will now control the overall emissive power of the HDRI texture and the Light Color will add a tint to the texture.<br><br><img src="https://vertexschool.instructure.com/courses/17/files/915/preview?verifier=EIF0ykOXKdwf5Jqkwg8QQoG5UNCHT6yZ6yo97ytz" alt="demystify-skylight-03.png" width="495" height="458" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/17/files/915" data-api-returntype="File"></span><br></span></li>
</ol>
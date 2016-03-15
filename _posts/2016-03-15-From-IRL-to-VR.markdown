---
layout: post
title:  "From IRL to VR"
date:   2016-03-15 10:25:06 +0100
categories: blog post
---

I'm working on a workshop proposal for the next [Color Imaging Conference][link-CIC2016] November 7-11 in San Diego CA. The topic I want to discuss with the speakers and audience is VR. The idea is to present the state of the art of research - what's happening in the labs - and how this technology is spread to the mass - from digital dome to VR headset.

The acceptance of a new technology can be reach if normal users can embrace it. It's a challenge for all scientists, engineers, interaction designers to give easy access to often very complicated stuffs. By complicated stuff here I mean the production of an immersive movie with one or several cameras. The 360 degrees VR photography scene is almost established (see the photographer work of [tanjabarnes][link-tanjabarnes] and thanks to software tools such as [hugin][link-hugin]) one person *alone* can produce beautiful images. For immersive movies more resources are usually needed, digital dome and planetarium such as the [California Academy of Science][link-calacademy] have the team to create amazing contents for the visitors attending their shows.

I do think there is still a gap for people to create CGI content by themself, even so [minecraft][link-minecraft] or [lego with Chrome][link-googlelego] are contradicting me. But if you work already in a Virtual environment you eliminate many of the drawbacks usually present to generate multi-directional views: if you know where the objects in your scene are located, without talking about quality of rendering it's *easy* to generate views from virtual camera at various locations in space. So far I'm only describing techonological challenges and I'm not even tackling the story telling challenges in VR. To contradict me again, the people in the game industry didn't wait for me to tell story within a virtual envirronment.

### A few words about my background
I'm a [color scientist][link-tome], but over the almost last 10 years I have been involved in various VR projects regarding image quality, stichting, camera and projector calibration. Projects being the technology behind immersive displays and more specifically how to control several displays for the projection on curved surfaces. An immersirve display can be a cave, cylinder to a full sphere in that matter.

I had the chance to meet different communities, one of them being the [digital dome community][link-imersa]. Interesting fact for me is that these people are usually understanding/developping their technology to be able to create immersive contents for the digital domes. Another aspect I find very interesting about VR, it is now somehow easier to [consume VR content][link-thevergegdc] *alone* with your [smartphone][link-oculus] when digital dome offer a *group* immersive experience which is pretty cool too.

### Description of the workshop (draft)

The recent blossoming of VR headset has open the VR doors to new users. The technology is not anymore reserved to flight simulator, research center or high end gaming console. It is now relatively easy to consume VR content on the mobile display of your smartphone equipped with a [google Cardboard][link-cardboard] in the most simple case. 

In that workshop we want to explore the different factors leading the user to have a successful VR experience. More specifically we will look at the solution existing for creating panorama to spherical movies using several cameras or using a single acquisition device, investigate the different scenario for live contents to recorded movies. 

The usual approach to create panorama movie is to combine several different fields of view, the operation of stitching will allow to blend each image into a single frame. This process have to deal with hdr/tone mapping, the choice of algorithm modify the final image quality which influence the perceived feeling of immersion.

The general concept with immersive video is to consider the user in the middle of a sphere where the inner surface is the content of a frame. One aspect is to give the user the possibility to change its viewing direction by simply turning his head, a second aspect is to have the content ready at each frame. It’s possible to view immersive video on a regular video player where the viewing direction can be modified with a mouse (Youtube has this option), on the other side apps for VR headset will often use gaming tools (such as [Unity Game engine][link-unity]), rendering tools (openGL…) to control the environment. From that point of view, app developers can work easily with texture, camera matrix projection, stitching functions...

#### Content filmed with camera cluster
It is possible to combine several action cameras with a mounting rig, see [GoPro][link-gopro]. As each camera position is fixed, only one configuration file is required to stitch automatically the images, see the [panoramic UHD video][link-hhiuhd] from [HHI][link-hhi] in Berlin. Live streaming is possible, final quality is linked to the bandwidth, how fast can tone mapping be applied, how synchronized are the different camera streams ([Video-Stitch][link-videostitch], [Kolor][link-kolor] softwares can help). With this kind of installation ghosting effect can still be visible when an object is getting too close to the camera cluster and appear in only one camera field of view.

#### Content filmed with a single camera on the fly
It is possible if you can always consider your camera being located in the center of a sphere. Now giving the opportunity to the user to create himself with a single device an immersive movie is really interesting because it’s an invitation for him to take control on such new media/way of expression. And the challenges for the scientists and engineers to please the future immersive video directors are numerous as the users don’t really care about the science, it should work when you press the button (who knows about automatic white balance, autofocus, hdr, 3D, face detection, noise reduction, automatic quality improvement, photography in low light…). The challenge with a single camera is to able to follow the camera movement and to provide to the app this information under the form of a rotation matrix to process stitching in real time ([viorama and splash][link-splash] can help).

### Expected outcome

The people attending the workshop should gain knowledge about the imaging workflow for VR application using their smartphone as display: what are the key points and challenges from applied research to production.

### How to participate?

Regarding the participation to the workshop as one of the speakers to share your experience regarding the challenges listed, 
please contact me jeremie[point]gerhardt[at]gmail[point]com .

Check the conference webpage [Color Imaging Conference][link-CIC2016] where there is much more to discover than the few lines above.



[link-calacademy]: http://www.calacademy.org/incoming-trailer
[link-hugin]: http://hugin.sourceforge.net/
[link-cardboard]: https://www.google.com/get/cardboard/
[link-CIC2016]: https://www.imaging.org/site/IST/Conferences/Color_and_Imaging/IST/Conferences/CIC/CIC_Home.aspx?hkey=d2cf3f19-87b4-4164-8274-c40180e9dfa7
[link-minecraft]: https://minecraft.net/
[link-googlelego]: https://www.buildwithchrome.com/builder
[link-thevergegdc]:http://www.theverge.com/2016/3/14/11206552/vr-oculus-rift-htv-vive-valve-sony-psvr-GDC
[link-videostitch]: http://www.video-stitch.com/
[link-kolor]: http://www.kolor.com/
[link-splash]: https://www.splashapp.co/
[link-gopro]: http://www.360heros.com/
[link-tanjabarnes]: http://tanjabarnes.com/
[link-unity]: https://unity3d.com/
[link-imersa]: http://www.imersa.org/
[link-tome]: https://de.linkedin.com/in/jeremiegerhardt
[link-oculus]: https://www.oculus.com/
[link-hhiUHD]: http://www.hhi.fraunhofer.de/departments/vision-imaging-technologies/products-technologies/capture/panoramic-uhd-video.html
[link-hhi]: http://www.hhi.fraunhofer.de/start-page.html
---
title: "Mathematic"
excerpt: "Base mathematical knowledge about laser range finder"
tags: [math,"laser range finder","lidar","diy"]
use_math: true
---
The theory behind this laser range finder is very simple. Let consider the system in below figure.
![model]({{ site.baseurl }}/lrf/images/math.png "Model of system")
In above figure, O is optical center of the camera lens, AB is laser beam. When the beam reaches obstacle at B, we will see a small dot that will be captured on the image sensor of camera at E. All we need is calculate the distance *l* from obstacle to the optical center of camera.

Alright, recall to high school mathematic, triangles OEC and BOA are similar so that we have this equation:

$$l = f \times \frac{D}{d}$$

We have already known $D$ which is distance between laser source and camera. $f$ is also known because it is the focal length of camera and it should show off somewhere in device manual or case. We can get $d$ by measuring directly on the captured image.

One issue here, by measuring distance on the image, we get that value in pixels. Let describe $d$ as:

$$d = k \times p$$

In which $p$ is the distance in pixel measured on captured image. The first equation will become:

$$l = f \times \frac{D}{k \times p}$$

Alright, all we have to do now is figure the value of $k$. If we place obstacle at predefined distances called $l_{1}$ and $l_{2}$, we will have following equations:

$$l_{1} = f \times \frac{D}{k \times p_{1}}$$

$$l_{2} = f \times \frac{D}{k \times p_{2}}$$

Subtracting $l_{1}$ from $l_{2}$ (let's call the result $\Delta l$) and doing some transformation, then we will have:

$$k = \frac{f \times D \times (p_{1}-p_{2})}{\Delta l \times p_{1} \times p_{2}}$$

Above process needs to measure 2 predefined distances, but its advantage is that we don't have to care about internal distance $L$ inside the camera. Although $L$ is a fixed value, it would be difficult to measure.

That's all for mathematic. Have fun.

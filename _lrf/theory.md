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

We have already known $D$ which is distance between laser source and camera. We can get $d$ by measuring directly on the captured image.

One issue here, by measuring distance on the image, we get that value in pixels. Let describe $d$ as:

$$d = k \times p$$

In which $p$ is the distance in pixel measured on captured image. The first equation will become:

$$l = f \times \frac{D}{k \times p}$$
or
$$l = \frac{f}{k} \times \frac{D}{p}$$

$f$ is also known because it is the focal length of camera and it should show off somewhere in device manual or case. However, this value is often variable depending on the lens system.
But its value should not change during system operation and so does value of $k$. A straightforward method to find out the value of $\frac{f}{k}$ is measuring $p$ with predefined $l$, then run a linear regression algorithm to find approximative value.  

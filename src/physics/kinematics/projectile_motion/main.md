Near the surface of Earth, the gravitational field is roughly constant and is equal to $g \approx 9.81m/s^2$.
This causes **all objects to accelerate downwards** with $a_y = g$ towards Earth.

![Gravity Field](1.svg)

### Vector Components

To visualize the relationship between a vector and its components, consider the velocity of this arrow:

![Arrow](2.svg)

In the vector view, our arrow travels with speed $|v|$ at an angle of $\theta$ to the horizontal. Broken into components, it has speed $|v|\cos\theta$ in the x-direction and speed $|v|\sin\theta$ in the y-direction.


### No Height Difference

Let's say an arrow is fired at an angle $\theta$ and its initial velocity is $v$, and air resistance is neglected. The arrow would fly in a symmetrical curve. We would like to find the time $T$ the arrow remains in the air, and the horizontal displacement $s_x$.

![](3.svg){ width=800 }

First, we need to decompose the velocity into its horizontal and vertical components to get $v_x = v\cos\theta$ and $v_y = v\sin\theta$. $v_x$ and $v_y$ are independent of each other, and hence only $v_y$ is required to determine how long the arrow will remain in the air. Due to gravity, $a_y = -g$ (notice the negative sign). Using the kinematic relation $s = ut + \frac{1}{2}at^2$. As there is no net change in vertical displacement, we obtain

$$ 0 = T(v_y - \frac{1}{2}gT) $$

Throwing away $T=0$ as it is meaningless we have

$$ T = \frac{2v_y}{g} = \frac{2v\sin\theta}{g} $$

To find the horizontal displacement, notice that $v_x$ is constant as there is no acceleration in the horizontal direction. Thus

$$ s_x = v_xT = v\cos\theta T = v\cos\theta \frac{2v\sin\theta}{g} = \frac{2v^2\sin\theta\cos\theta}{g} = \frac{2v^2\sin{2\theta}}{g} $$

The **speed** at which the arrow hits the ground is the same as the speed at which it is fired since air resistance is neglected. The angle at which the arrow hits the ground is $90^\circ - \theta$.

### With Height Difference

Now assume the arrow is aiming to hit an apple on a pole $l$ meters away and $h$ meters above the ground. It is fired at an angle of $\theta$ and a velocity of $v$.

![](4.svg){ width=400 }

#### Finding Time

Let's say we want to find the time $T$ arrow will remain in the air. This is similar to the problem without height difference with the exception that the arrow will end up with $s_y = h$.

$$ h = v_yT - \frac{1}{2}gT^2 $$
$$ \frac{1}{2}gT^2 - v_yT + h = 0 $$

Solving with the quadratic formula $x=\frac{-b\pm\sqrt{b^2 - 4ac}}{2a}$, we have

$$ T = \frac{v_y\pm\sqrt{v_y^2 - 2gh}}{g} $$

Notice that there are 2 solutions, since we did not place restrictions on $\theta$ or $v$. Hence the arrow is able to hit the apple before or other it has reached its peak.

![](5.svg){ width=400 }

#### Finding X Displacement

Similar to the problem without height difference, $v_x$ remains constant and hence

$$ s_x = v_xT = \frac{v_xg + v_y \pm \sqrt{v_y^2 - 2gh}}{g} = \frac{vg\cos\theta + v\sin\theta \pm \sqrt{v\sin^2\theta - 2gh}}{g} $$

#### Finding Velocity

Now, the angle fixed at some specific value $\theta$. We would like to find the required velocity to fire the arrow such that it hits the apple (if it is possible).

To get started, we can write the trajectory of the arrow in component form

$$ s_x = vt\cos\theta $$
$$ s_y = vt\sin\theta - \frac{1}{2}gt^2 $$

Plugging in the values, and assuming the time the arrow hits the apple is $T$

$$ l = vT\cos\theta $$
$$ h = vT\sin\theta - \frac{1}{2}gT^2 $$

Rewriting the second equation as $h + \frac{1}{2}gT^2 = vT\sin\theta$ and making the substitution $T = \frac{l}{v\cos\theta}$ 

$$ \frac{h + \frac{1}{2}g\frac{l^2}{v^2\cos^2\theta}}{l} = v\sin\theta\frac{l}{v\cos\theta} = \tan\theta $$
$$ g\frac{l^2}{v^2\cos^2\theta} = 2(l\tan\theta - h) $$
$$ v^2\cos^2\theta = \frac{gl^2}{2(l\tan\theta - h)} $$
$$ v = \sec\theta\sqrt{\frac{gl^2}{2(l\tan\theta - h)}} $$

#### Finding Angle

This is the same problem as the above, except the velocity is now fixed at some value $v$ while we are trying to find $\theta$ for which the arrow still hits the apple.

The first couple of steps is the same as the previous problem and we will continue from there

$$ v^2\cos^2\theta = \frac{gl^2}{2(l\tan\theta - h)} $$
$$ \frac{1}{\cos^2\theta} = \frac{2v^2(l\tan\theta - h)}{gl^2} $$
$$ gl^2(\tan^2\theta + 1) = 2v^2(l\tan\theta - h) $$
$$ gl^2\tan^2\theta - 2lv^2\tan\theta + gl^2 + 2v^2h = 0 $$
$$ \tan\theta = \frac{2lv^2 \pm\sqrt{4l^2v^4 - 4g^2l^4 - 8gl^2v^2h}}{2gl^2} $$
$$ \tan\theta = \frac{2lv^2 \pm 2l\sqrt{v^4 - g^2l^2 - 2gv^2h}}{2gl^2} = \frac{v^2 \pm\sqrt{v^4 - g^2l^2 - 2gv^2h}}{gl} $$
$$ \theta = \arctan\left(\frac{v^2 \pm\sqrt{v^4 - g^2l^2 - 2gv^2h}}{gl}\right) $$

Notice that there can be 2 solutions. This is because the ball can hit the apple either before or after it has reached its peak vertical displacement. In the case that there is only 1 solution, the ball will hit the apple at its peak vertical displacement.
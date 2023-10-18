## Formulas

The kinematic equations below can be utilized to predict unknown information about an object's motion if other information is known. In the equations, $u$ represents initial velocity,
$v$ represents final velocity, $a$ represents acceleration which is constant, $s$ represents displacement,
and $t$ represents the amount of time that has passed.

$$ v = u + at $$
$$ s = \frac{u + v}{2}t $$
$$ s = ut + \frac{1}{2}at^2 $$
$$ v^2 = u^2 + 2as $$

The first and second equations are relatively straightforward. The derivation of the third and fourth equations can be found below.

## Derivation

Let's assume we start accelerating uniformly from **rest** for $T$ seconds. To derive $s = uT + \frac{1}{2}aT^2$, first we have to understand that $v(T) = \int_0^T a(t) \, dt$ and $s(T) = \int_0^T v(t) \, dt$. Hence

$$ s(T) = s(0) + \int_0^T \left( \int_0^t a(t') \, dt' \right) \, dt $$

Since we are only dealing with constant accerleration, let $a(t') = a_0$ which will be a constant

$$ s(T) = s(0) + \int_0^T \left( \int_0^t a_0 \, dt' \right) \, dt $$
$$ s(T) = s(0) + a_0 \int_0^T t \, dt $$
$$ s(T) = s(0) + a_0 \frac{T^2}{2} $$

We have obtained part of the formula, now suppose we have a **nonzero** initial velocity, $v(0) = u \not = 0$.

$$ s(T) = s(0) + a_0 \frac{T^2}{2} + \int_0^T u \, dt $$
$$ s(T) = s(0) + a_0 \frac{T^2}{2} + uT $$

Rearranging, we obtain the third formula

$$ s(T) - s(0) = \Delta s = uT + \frac{1}{2}a_0T^2 $$

We know that $s = \frac{u + v}{2}t$ from the second formula. As we accelerate at a constant rate, we also have
$a = \frac{\Delta v}{\Delta t} = \frac{v - u}{t}$. Multiplying both equations

$$ as = \frac{(v + u)(v - u)}{2} = \frac{v^2 - u^2}{2} $$

Thus, we can rearrange to obtain the fourth formula. Notice that this relationship is time independent.

$$ v^2 = u^2 + 2as $$

We've derived the relations in the context of 1D motion.
However, these derivations work just the same in 2 or more dimensions, just with higher dimensional vectors.

## Angular Kinematics

Angular kinematics is similar to the relationships derived above in linear spaces. By convention, the angular velocity and acceleration are also commonly referred to as $\omega$ and $\alpha$ respectively, and they follow exactly the same
kinematic relationships.

However, unlike motion in linear space, position in angular kinematics is represented by an angle $\theta$. The distance travelled is then the arc length, $s = r\theta$, where r is the radius. This implies that $v = r\omega$ and $a = r\alpha$. One thing to note is that $\theta$ is periodic ($0$ and $2\pi$ represent the same location), while $s$ has no bound.

## Projectile Motion

Near the surface of Earth, the gravitational field is roughly constant and is equal to $g \approx 9.81m/s^2$.
This causes **all objects to accelerate downwards** with $a_y = g$ towards Earth.

### No Height Difference

Let's say a ball on a flat ground is kicked at an angle $\theta$ and its initial velocity is $v$, and air resistance is neglected. The ball would fly in a symmetrical curve. We would like to find the time $T$ the ball will stay in the air, and the horizontal displacement $s_x$.

First, we need to decompose the velocity into its horizontal and vertical components to get $v_x = v\cos\theta$ and $v_y = v\sin\theta$. $v_x$ and $v_y$ are independent of each other, and hence only $v_y$ is required to determine how long the ball with be in the air. Due to gravity, $a_y = -g$ (notice the negative sign). Using the kinematic relation $s = ut + \frac{1}{2}at^2$. As there is no net change in vertical displacement, we obtain

$$ 0 = T(v_y - \frac{1}{2}gT) $$

Throwing away $T=0$ as it is meaningless we have

$$ T = \frac{2v_y}{g} = \frac{2v\sin\theta}{g} $$

To find the horizontal displacement, notice that $v_x$ is constant as there is no acceleration in the horizontal direction. Thus

$$ s_x = v_xT = v\cos\theta T = v\cos\theta \frac{2v\sin\theta}{g} = \frac{2v^2\sin\theta\cos\theta}{g} = \frac{2v^2\sin{2\theta}}{g} $$

The speed at which the ball hits the ground is the same as the speed at which it is kicked since air resistance is neglected. The angle at which the ball hits the ground is $90^\circ - \theta$.

### With Height Difference

Now assume the ball is on the edge of a hill $h$ meters above the ground. It is kicked at an angle $\theta$ and its initial velocity is $v$, and air resistance is neglected.

#### Finding Time

Let's say we want to find the time $T$ ball will remain in the air. This is similar to the problem without height difference with the exception that the ball will end up with $s_y = -h$.

$$ -h = v_yT - \frac{1}{2}gT^2 $$
$$ \frac{1}{2}gT^2 - v_yT - h = 0 $$

Solving with the quadratic formula $x=\frac{-b\pm\sqrt{b^2 - 4ac}}{2a}$, we have

$$ T = \frac{v_y\pm\sqrt{v_y^2 + 2gh}}{g} $$

Notice that $\sqrt{v_y^2 + 2gh} > v_y$ is always true when $h > 0$ and since $T > 0$

$$ T = \frac{v_y + \sqrt{v_y^2 + 2gh}}{g} = \frac{v\sin\theta + \sqrt{v\sin^2\theta + 2gh}}{g} $$

#### Finding X Displacement

Similar to the problem without height difference, $v_x$ remains constant and hence

$$ s_x = v_xT = \frac{v_xg + v_y + \sqrt{v_y^2 + 2gh}}{g} = \frac{vg\cos\theta + v\sin\theta + \sqrt{v\sin^2\theta + 2gh}}{g} $$

#### Finding Velocity

Now let's say the ball is on the ground again and its goal is to hit an apple on a pole $l$ meters away and $h$ meters above the ground. The angle at which the ball is fixed at $\theta$. We would like to find the required velocity to kick the ball such that it hits the apple (if it is possible).

To get started, we can write the trajectory of the ball in component form

$$ s_x = vt\cos\theta $$
$$ s_y = vt\sin\theta - \frac{1}{2}gt^2 $$

Plugging in the values, and assuming the time the ball hits the apple is $T$

$$ l = vT\cos\theta $$
$$ h = vT\sin\theta - \frac{1}{2}gT^2 $$

Rewriting the second equation as $h + \frac{1}{2}gT^2 = vT\sin\theta$ and making the substitution $T = \frac{l}{v\cos\theta}$ 

$$ \frac{h + \frac{1}{2}g\frac{l^2}{v^2\cos^2\theta}}{l} = v\sin\theta\frac{l}{v\cos\theta} = \tan\theta $$
$$ g\frac{l^2}{v^2\cos^2\theta} = 2(l\tan\theta - h) $$
$$ v^2\cos^2\theta = \frac{gl^2}{2(l\tan\theta - h)} $$
$$ v = \sec\theta\sqrt{\frac{gl^2}{2(l\tan\theta - h)}} $$

#### Finding Angle

This is the same problem as the above, except the velocity is now fixed at $v$ while $\theta$ is allowed to vary such that the ball still hits the apple.

The first couple steps is the same as the previous problem and we will continue from there

<!-- **Method 1**

$$ v^2\cos^2\theta = \frac{gl^2}{2(l\tan\theta - h)} $$
$$ 2v^2\cos^2\theta(l\tan\theta - h) = gl^2 $$
$$ lcos^2\theta\tan\theta - hcos^2\theta - \frac{gl^2}{2v^2} = 0 $$
$$ l\sin\theta\cos\theta - h(1-sin^2\theta) - \frac{gl^2}{2v^2} = 0 $$
$$ \frac{l}{2}\sin{2\theta} + hsin^2\theta - \frac{gl^2}{2v^2} - h = 0 $$
$$ \frac{l}{2}\sin{2\theta} + \frac{h}{2}cos{2\theta} - (\frac{gl^2}{2v^2} + h) = 0 $$
$$ l\sin{2\theta} + hcos{2\theta} - (\frac{gl^2}{v^2} + 2h) = 0 $$
$$ \sqrt{l^2 + h^2}\sin(2\theta - \arctan\frac{h}{l}) - (\frac{gl^2}{v^2} + 2h) = 0 $$
$$ \sin(2\theta - \arctan\frac{h}{l}) = \frac{2hv^2 + gl^2}{v^2\sqrt{l^2 + h^2}} $$
$$ \theta = \frac{1}{2} \left( \arcsin\left(\frac{2hv^2 + gl^2}{v^2\sqrt{l^2 + h^2}}\right) + \arctan\frac{h}{l}\right) $$

**Method 2** -->

$$ v^2\cos^2\theta = \frac{gl^2}{2(l\tan\theta - h)} $$
$$ \frac{1}{\cos^2\theta} = \frac{2v^2(l\tan\theta - h)}{gl^2} $$
$$ gl^2(\tan^2\theta + 1) = 2v^2(l\tan\theta - h) $$
$$ gl^2\tan^2\theta - 2lv^2\tan\theta + gl^2 + 2v^2h = 0 $$
$$ \tan\theta = \frac{2lv^2 \pm\sqrt{4l^2v^4 - 4g^2l^4 - 8gl^2v^2h}}{2gl^2} $$
$$ \tan\theta = \frac{2lv^2 \pm 2l\sqrt{v^4 - g^2l^2 - 2gv^2h}}{2gl^2} = \frac{v^2 \pm\sqrt{v^4 - g^2l^2 - 2gv^2h}}{gl} $$
$$ \theta = \arctan\left(\frac{v^2 \pm\sqrt{v^4 - g^2l^2 - 2gv^2h}}{gl}\right) $$

Notice that there can be 2 solutions. This is because the ball can hit the apple either before or after it has reached its peak vertical displacement. In the case that there is only 1 solution, the ball will hit the apple at its peak vertical displacement.

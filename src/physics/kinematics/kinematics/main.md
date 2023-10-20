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

Since we are only dealing with constant acceleration, let $a(t') = a_0$ which will be a constant

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
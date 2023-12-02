# Gravity

Physicists count four fundamental forces (Gravity, Electromagnetism, Strong force and Weak force) between matter particles, and although gravity is the weakest out of them, none impacts the large-scale structure of the universe more than gravity.

Gravity was also the first force to be understood through a modern scientific model. Inaugural scientists like Galileo and Newton pieced together a theory of gravity in the 1600s that is still used in applications today. However, modern developments in quantum mechanics challenge our understanding of gravity, but this is out of the scope of discussion for this topic.

## Force of Gravity

The force of gravity between 2 masses, $m_1$ and $m_2$ separated by a distance of $r$, can be calculated from a simple quantitative law

$$ F_g = \frac{G m_1 m_2}{r^2} $$

where $G = 6.67 \times 10^{-11} \; m^3/(kg\;s^2)$ is the gravitational constant. The distance $r$ is measured from the center of mass of one object to that of the other.

![Gravity](1.svg){ width=600 }

As an example, let's calculate the force of gravity of the Sun on Earth. Earth's mass is $5.97 \times 10^{24} \; kg$, Sun's mass is $1.99 \times 10^{30} \; kg$ and the distance between them is roughly $1.5 \times 10^{11} \; m$. Substituting the values, we find

$$ F_g = \frac{6.67 \times 10^{-11} \cdot 5.97 \times 10^{24} \cdot 1.99 \times 10^{30}}{(1.5 \times 10^{11})^2} = 3.5 \times 10^{22} \; N \; (2 sf) $$

The Sun's gravity is responsible for shepherding the planets around nearly **circular** orbits in our solar system.

## Mass of the Sun

Calculating gravitational forces in our solar system requires knowing the mass of the Sun, $M_{Sun}$, so you might wonder how astronomers first measured the Sun's mass. Clearly, putting it on a scale is not an option, so let's used Newton's theory of gravity, and measurements of Earth's orbital motion to find out answer.

Let's assume that Earth's orbit is circular — a pretty good approximation. Then its acceleration is just the centripetal acceleration $a = v^2/d_{Earth}$ where v is Earth's velocity in its orbit and $d_{Earth}$ is its distance from the Sun.

Newton's second law of motion relates accleration to the net force $F = ma$, hence

$$ F_g = M_{Earth}a = \frac{M_{Earth}v^2}{d_{Earth}} $$

so Newton's law of motion gives us an alternate way to compute the gravitational force on the Earth, without using Newton's law of gravitation.

We first need to estimate Earth's orbital velocity $v$. Earth orbits the Sun once per 365.25 days in a circular orbit with radius $d_{Earth} = 1.5 \times 10^8  \; km$. This distance is also known as **1 astronomical unit** or $1au$.

Assuming the speed of Earth in its orbit is constant, then

$$ v = \frac{s}{t} = \frac{2\pi \cdot 1.5 \times 10^8}{365.25 \times 24 \times 60 \times 60} = 30,000 \; m/s \; (2 sf) $$

Now that we have estimated the Earth's orbital velocity, a little algebra will lead us straight to the mass of the Sun. We know that gravity is the force that pulls on Earth as it orbits the Sun, so

$$ F_g = \frac{M_{Earth}v^2}{d_{Earth}} = \frac{G M_{Sun} M_{Earth}}{d_{Earth}^2} $$

Solving for $M_{Sun}$

$$ \frac{G M_{Sun}}{d_{Earth}} = v^2 $$

$$ M_{Sun} = \frac{v^2 d_{Earth}}{G} = {30000^2 \cdot 1.5 \times 10^{11}}{6.67 \times 10^{-11}} = 2.0 \times 10^{30} \; kg \; (3 sf) $$

which is pretty close to the more precise measurement of $1.99 \times 10^{30} \; kg$. Notice that we didn't need to know Earth's mass to calculate the Sun's mass because it canceled out in Newton's law of motion. The only input to this estimate was the Earth-Sun distance, which was first estimated by the ancient Greeks, and Earth's orbital period, 1 year.

## Virial Theorem

Now, we will examine the birth of our solar system from a diffuse cloud of gas and debris leftover from a star whose existence ended much earlier in a cataclysmic supernova explosion, and work out an important relationship between gravitational potential energy and kinetic energy — the virial theorem. This theorem can help us examine the life cycle of a star in the following chapters.

Several billion years ago, all of the mass that makes up the Sun and planets in our solar system was spread out as a low-density gas mixed with dust called a nebula. The extent of the nebula was roughly 100 times larger than the current distance between the Earth and the Sun, or $100 au$.

Which stage of the solar system has lower gravitational potential energy — the spread-out gas, or our solar system today? Let's examine.

When the spread-out region of gas collapses into a solar system, it happens spontaneously due to the force of gravity. No energy is added to the system, and energy is in fact released as the gases heat up and release radiation. If, after the solar system was formed, we wanted to separate the solar system back out into a diffuse gas spread out over a large region of space, it would require energy to be added by an external force pulling the solar system apart. This tells us that the original state, the nebula, had higher potential energy. A system with more potential energy can do more work. The spread-out gas distributed over a large, spherical region preceding the birth of the Sun had more potential energy than the solar system today. This potential energy is lost as the attractive force of gravity among the particles pulls inward, initiating a process called gravitational collapse. In order to arrive at this conclusion, we will need to think about whether the work done by gravity on individual gas and dust particles is positive or negative as the region of gas and dust (the nebula) contracts. Then, we can relate this work to the change in potential energy of the nebula.

We will consider the amount of work that is done on each particle that makes up the nebula as it collapses from a radius of $100 au$ to a much smaller radius—say, $10 au$. Work is defined as force $F$ times the distance $d$ an object is moved in the direction of the force: $W = Fd$. When the force and the displacement are in the same direction, the work is positive. Because gravity pulls each particle toward its center, and the nebula is collapsing toward its center, the total work is, in fact, a positive number: $W_{100au \rightarrow 10au} > 0$.

Where does the energy come from to do this amount of work? Energy is conserved; it can not be created or destroyed. Because this work is done by the gravitational force, it is equal to the amount of gravitational potential energy lost by the nebula. Therefore, we can conclude that the potential of a system decreases as it collapses, so the potential energy is greater when its radius is $100 au$.

### Gravitational Potential Energy

Let's consider a $1 kg$ lump of metal as it is pulled from the outer fringe of the early solar system to a radius where it ultimately ends up in Earth's crust. The metal lump is pulled from $100 au$ to $1 au$ as the nebula collapses. It would lose potential energy, but how much exactly?

The gravitational potential energy of an object of mass $m$ that is a distance of $r$ from the center of another object with mass $M$ is given by

$$ U_g = -\frac{GmM}{r} $$

It might be confusing at first as to why there is a negative sign. Turns out, we place the zero point of gravitational potential energy at a distance of infinity. This makes all values of the gravitational potential energy negative. It makes sense as the distance becomes large, the gravitational force tends rapidly to $0$, and it also means that the particle is loses potential energy when moving to $r = 0$ which also makes sense since it gets converted to kinetic energy.

In our case, $M = 1.99 \times 10^{30} \; kg$, the mass of the solar system. (Yes, this is also the mass of the Sun to 3 significant places, the Sun makes up $99.86\%$ of the solar system's mass)

$$ \Delta U_g = |U_{r=100au} - U_{r=1au}| $$

$$ \Delta U_g = \frac{99}{100} \cdot \frac{6.67 \times 10^{-11} \cdot 1.99 \times 10^{30} \cdot 1}{1.5 \times 10^{11}} = 8.76 \times 10^8 \; J \; (3 sf) $$

Today, the lump of metal is now moving along with Earth with the kinetic energy

$$ K = \frac{1}{2}Mv^2 $$

where $M$ is the mass of the lump, and $v$ is the orbital velocity of Earth calculated earlier. If you calculate the kinetic energy, you will find that it is less than $\Delta U_g$. Because energy is conserved, we can assume the rest of the energy it lost was dissipated and reabsorbed by Earth as heat: $\Delta U_g = K + Heat$. If we actually went and calculated the kinetic energy

$$ K = \frac{1}{2} \cdot 1 \cdot 30000^2 = 4.50 \times 10^8 \; J $$

we would notice that roughly $50\%$ of energy was lost due to heat: $1 - \frac{4.50 \times 10^8}{8.76 \times 10^8} = 48.6\% \; (3 sf)$. In fact, if we had been more precise, we would find that **exactly half** of the potential energy was lost as heat. This statement is formally called the virial theorem. Virial theorem provides us a way to understand what happens to a star's temperature during gravitational collapse. Pretty interesting, eh?

# Superconducting Qubit

## Harmonic Oscillator

In the simple harmonic oscillator, the potential energy is given by $U(x) = \frac{1}{2}kx^2$. The potential increases quadratically as the object is moved further away from its equillibrium point. Since $F = -\frac{dU}{dx}$, then $F = -kx$, which is known as Hooke's law.

The differential equation obtained, $m\ddot{x} = -kx$, has general solutions $x = A\cos(\omega t) + B\sin(\omega t)$ where $\omega = \sqrt{\frac{k}{m}}$ is the frequency of oscillation.

We now derive the Lagrangian and Hamiltonian for the simple harmonic oscillator, and substitute the constant $k$ with $m\omega^2$.

$$ \mathcal{L} = T - U = \frac{1}{2}m\dot{x}^2 - \frac{1}{2}kx^2 $$

$$ \mathcal{L} = \frac{1}{2}m\dot{x}^2 - \frac{1}{2}m\omega^2x^2 $$

As we know, the conjugate variable of position is momentum, $\frac{\partial\mathcal{L}}{\partial\dot{x}} = m\dot{x} = p$. Applying the Legendre transformation to obtain the hamiltonian:

$$ \mathcal{H} = p\dot{x} - \mathcal{L} = \frac{p^2}{m} - \frac{p^2}{2m} + \frac{m\omega^2x^2}{2} $$

$$ \mathcal{H} = \frac{p^2}{2m} + \frac{m\omega^2x^2}{2} $$
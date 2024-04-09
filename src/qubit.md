# Superconducting Qubit

## Simple Harmonic Oscillator

In the simple harmonic oscillator, the potential energy is given by $U(x) = \frac{1}{2}kx^2$. The potential increases quadratically as the object is moved further away from its equillibrium point. Since $F = -\frac{dU}{dx}$, then $F = -kx$, which is known as Hooke's law.

The differential equation obtained, $m\ddot{x} = -kx$, has general solutions $x = A\cos(\omega t) + B\sin(\omega t)$ where $\omega = \sqrt{\frac{k}{m}}$ is the frequency of oscillation.

We now derive the Lagrangian and Hamiltonian for the simple harmonic oscillator, and substitute the constant $k$ with $m\omega^2$.

$$ \mathcal{L} = T - U = \frac{1}{2}m\dot{x}^2 - \frac{1}{2}kx^2 $$

$$ \mathcal{L} = \frac{1}{2}m\dot{x}^2 - \frac{1}{2}m\omega^2x^2 $$

As we know, the conjugate variable of position is momentum, $\frac{\partial\mathcal{L}}{\partial\dot{x}} = m\dot{x} = p$. Applying the Legendre transformation to obtain the hamiltonian:

$$ \mathcal{H} = p\dot{x} - \mathcal{L} = \frac{p^2}{m} - \frac{p^2}{2m} + \frac{m\omega^2x^2}{2} $$

$$ \mathcal{H} = \frac{p^2}{2m} + \frac{m\omega^2x^2}{2} $$

## LC Resonance Circuit

The LC resonance circuit is an electrical circuit made up of a capacitor ($C$) and inductor ($L$), and it is a harmonic oscillator as well. We can show this using Kirchhoff's Law, which is that the total voltage in a closed loop is equals to 0.

$$ \frac{Q}{C} + L\frac{dI}{dt} = 0 $$
$$ \frac{Q}{C} + L\frac{d^2Q}{dt^2} = 0 $$
$$ \frac{d^2Q}{dt^2} = -\frac{Q}{LC} $$

This differential equation is of the same form as the simple harmonic oscillator, but with $\omega = \frac{1}{\sqrt{LC}}$. Thus, we can see the LC resonance circuit oscillates at a frequency of $\frac{1}{\sqrt{LC}}$.

To formalise the Lagrangian for the LC circuit, we can arbitarily associate kinetic energy with the energy stored in the electric field of the capacitor, and potential energy with the energy stored in the magnetic field of the inductor.

$$ \mathcal{L} = T - U = \frac{1}{2}CV^2 - \frac{1}{2}LI^2 $$

Capacitors store charge and inductors store flux, and the flux stored in the inductor is given by $\Phi = LI$. We also know that $V = \frac{d\Phi}{dt}$. We will work with flux as our coordinate of choice, and it is and will prove to be convenient.

$$ \mathcal{L} = \frac{1}{2}C\dot{\Phi}^2 - \frac{\Phi^2}{2L} $$

The conjugate variable of flux is charge, $\frac{\partial\mathcal{L}}{\partial\dot{\Phi}} = C\dot{\Phi} = CV = Q$. Applying the Legendre transformation once again to obtain the hamiltonian:

$$ \mathcal{H} = Q\dot{\Phi} - \frac{1}{2}C\dot{\Phi}^2 + \frac{\Phi^2}{2L} = \frac{1}{2}Q\dot{\Phi} + \frac{\Phi^2}{2L} $$

$$ \mathcal{H} = \frac{Q^2}{2C} + \frac{\Phi^2}{2L} $$

## Quantum Operators

In quantum mechanics, the promotion of classical variables to operators is a fundamental aspect of the theory. Particles are described by complex-valued wave functions, which for example, can represent the probability amplitudes of finding the particle at a particular location. Classical variables have corresponding operators such as position ($\hat{x}$) and momentum ($\hat{p}$) can act on the wave function to provide information about the observerable properties of the particle.

Another effect of promoting variables to operators is quantization. Classical variables take continuous values, whereas in quantum mechanics, observables are quantized, meaning they can only take on discrete values. By promoting classical variables to operators, we introduce the concept of quantization, where the eigenvalues of these operators correspond to the possible outcomes of measurements.

For example, $\hat{x} = x$ and $\hat{p} = -i\hbar\frac{\partial}{\partial x}$. They have a canonical commutation relation and obey the uncertainty principle, since $[\hat{x}, \hat{p}] = -i\hbar$.

Hermitian operators, in particular, play a crucial role in the context of observable quantities. A hermitian operator is an operator to its own adjoint (complex conjugate tranpose). $\hat{A} = \hat{A}^\dagger$.

Classical observerables must be hermitian operators in quantum mechanics, because observerables give real values upon measurement. the expectation value of an observerable $\hat{A}$ in a quantum state $\psi$ is given by:

$$ \left\langle \hat{A} \right\rangle = \left\langle \psi \right\vert \hat{A} \left\vert \psi \right\rangle $$

For the expectation value to be real, $\hat{A}$ must be hermitian. This also implies that hermitian operators have real eigenvalues. In the context of quantum mechanics, the eigenvalues of an observable operator correspond to the possible outcomes of measurements. The requirement for real eigenvalues aligns with the fact that measurement outcomes are real numbers.
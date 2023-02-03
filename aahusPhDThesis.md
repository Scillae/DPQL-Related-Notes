# Ion Trap Basics


## Set up

Ideal trap:
$\phi = \phi_0(\alpha x^2 + \beta y^2 + \gamma z^2)$

Laplace: $\nabla^2\phi=0 \rightarrow \alpha+\beta+\gamma=0$, where $\alpha, \beta, \gamma$ are dimensionless geometric factors. At least one should be negative and the force repulsive.

The equilibrium can be dynamically stabilized by varying potential $\phi$ in time.

### Trap


$$\phi = \frac{1}{2}U_{dc}(\alpha_{dc} x^2 + \beta_{dc}y^2 + \gamma_{dc}z^2) + \frac{1}{2}U_{rf}\cos(\Omega t)(\alpha_{rf} x^2 + \beta_{rf}y^2 + \gamma_{rf}z^2)$$

Here we have two parameters describing the strength of the fields: $\alpha_{rf} = -\beta_{rf} = \alpha$ $(\gamma_{rf} = 0)$, no rf field on $z$ direction, and $-\alpha_{dc} - \beta_{dc} = \gamma_{dc} = \gamma$

$$\frac{d^2x}{dt^2} = -\frac{q}{m}(-\frac{1}{2}U_{dc}\gamma + U_{rf}\alpha\cos(\Omega t))\\
\frac{d^2y}{dt^2} = -\frac{q}{m}(-\frac{1}{2}U_{dc}\gamma - U_{rf}\alpha\cos(\Omega t))\\
\frac{d^2z}{dt^2}  = \frac{q}{m}(-U_{dc}\gamma) z
$$

Make the substitution: $a_x = a_y = -\frac{2qU_{dc}\gamma}{m\Omega^2}$, $q_x = -q_y = -\frac{2qU_{rf}\alpha}{m\Omega^2}$, $\xi = \frac{\Omega_{rf} t}{2}$, $a_z = \frac{4qU_{dc}\gamma}{m\Omega^2}$, $q_z = 0$; 

Equations will take form of Mathieu equations: 
$$\frac{d^2r_i}{d\xi^2} + (a_i-2q_i\cos(2\xi))r_i = 0$$
Mathieu equation have solution of the form $$w_{1,2}(\xi) = \exp(\pm\mu\xi)\Psi(\xi)$$ where $\mu=\alpha(a,q)+i\beta(a,q)$. We want $\alpha=0$ for stable solutions or bounded ions. See fig 2.2 for the stable $q$ and $a$ regions.

Stable solutions are <a name="solution">: </a>

$$
\begin{equation}
r_i = A_i \sum_{n=-\infty}^{\infty} C_{2n}^{i}(a_i, q_i)\cos((2n\pm\beta_i)\xi) + B_i \sum_{n=-\infty}^{\infty} C_{2n}^{i}(a_i, q_i)\sin((2n\pm\beta_i)\xi),
\end{equation}
$$

where $\beta_i$ and $C_{2n}^{i}$ are fns of $a_i$ and $q_i$ only. $A$ and $B$ are arbitrary constants to satisfy boundary conditions. 

#### Pseudo-Potential Model

The ions oscillate as described by the [solution](#solution) at $\omega_n = (2n+\beta)\Omega/2$. When $\beta\ll1$ we would have sidebands at $\omega_0 = \beta\Omega/2$. The amplitude of the low frequency secular motion will be larger than high frequency micromotion, hence $$r_i = R_i + \delta_i,$$ where $R_i$ is the secular motion(low frequency) and $\delta_i$ is the micromotion(high-frequency).

Separate and solve the EOM: 

$$\frac{d^2R_i}{dt^2} = -\omega_i^2R_i \\ \delta_i = -\frac{q_iR_i}{2}\cos(2\xi)$$

where the secular(low) frequency is $\omega_i = \frac{\Omega}{2}\sqrt{\frac{q_i^2}{2}+a_i} = \frac{\Omega}{2}\beta_i$ and the euqation solution is $$r_i = r_i^0\cos(\omega_i t + \phi_i)(1-\frac{q_i}{2}\cos(\Omega_t))$$

#### practical data and concerns
When ions are loaded in the trap from a thermal beam ($∼ 500 ◦C$), they have a thermal energy of $0.03 eV$. In the trap discussed in Part III, the distance to the electrodes is $2.7mm$. With a radial oscillation frequency of $\omega r = 2π · 1MHz$ this gives a trap potential depth of $60 eV$; more than enough to trap a beam of thermal ions.

#### Micromotion
Micromotion modfies the absorption spectruc from ion and introduce heating. It is unwanted. 

1. Introduce stray field E_i: 

$$\frac{d^2x}{dt^2} = = -\frac{q}{m}(-\frac{1}{2}U_{dc}\gamma + U_{rf}\alpha\cos(\Omega t)) + \frac{E_i q}{m}$$ 

Resulting ion motion: $$r_i = (r^e + r_i^0\cos(\omega_i t + \phi_i))(1-\frac{q_i}{2}\cos(\Omega_t))$$ and now we can't turn micromotion off. Could use additional DC voltage or separate compensation electrodes to eliminate this. 

2. When there is Phase difference between electrodes
3. asymmetry of electrodes

### QM of Ion Motion

Consult 1d harmonic oscillator.

$$\sqrt{\langle n|r^2|n\rangle} = \sqrt{2n+1}\sqrt{\frac{\hbar}{2m\omega}}$$
In that with secular frequency $\omega = 2\pi \times 500KHz$, Ca-40 will be confined within 15nm.

If there is micromotion we need to add time-dependent harmonic potential $\omega(t)$, and $$r = \sqrt{\frac{\hbar}{2m\omega}}(\hat{a}u^*(t) + \hat{a}^\dagger u(t))$$ where $u = e^{i\beta\Omega/2}\sum_{n=-\infty}^{\infty}C_{2n}e^{in\Omega t}$

### 2 Co-Trapped Ions

2 ions confined along axis: combined motion will be in 2 normal modes, $$\omega_\pm^2 = \omega_z^2(1+\frac{1}{\mu}\pm\sqrt{1-\frac{1}{\mu}+\frac{1}{\mu^2}})$$, $\mu = \frac{m_2}{m_1}$. the $-$ is for moving together in phase (COM/slower) and $+$ is for out of phase(stretch/quicker).


## Atom-Light Interactions
Two-level Atom have the Hamiltonian:  $H_a = \hbar\omega_g|g><g| + \hbar\omega_e|e><e|$. The atomic wavefunction: $|\psi> = c_g|g> + c_e|e>$.

### Interactions 

LightField: 
$$\overrightarrow{E}(r,t) = \overrightarrow{E_0}[\exp(i(\overrightarrow{k}\overrightarrow{x}-\omega_l t)) +\exp(-i(\overrightarrow{k}\overrightarrow{x}-\omega_l t))]\\
=\hat{e}E_0\cos(\overrightarrow{k}\overrightarrow{x}-\omega_l t)$$

Dipole approximation: assume $\exp(i(\overrightarrow{k}\overrightarrow{x}))$ is always 1 over all atom (all concerned $\overrightarrow{r}$)

Consider interaction term $V = dE$, and we note the quantum state is $\Psi = c_g(t)|g> + g_e(t)|e>\exp(-i\omega_0t)$ 

Plug into Hamiltonian, and note that $<g|V|e> = <e|V|g> = 0$ we have the following:

$$i\hbar \frac{dc_g(t)}{dt} = c_e<g|dE|e>\exp{(-i\omega_0 t)}\\
i\hbar \frac{dc_e(t)}{dt} = c_g<e|dE|g>\exp{(+i\omega_0 t)}
$$

Define $\Omega = \frac{E_0}{\hbar}<e|d.\hat{e}|g>$ and now we have, only take care of the first equation,

$$i\hbar \frac{dc_g(t)}{dt} = c_e 
\hbar \Omega^* [\exp(i(\overrightarrow{k}\overrightarrow{x}-\omega_l t)) +\exp(-i(\overrightarrow{k}\overrightarrow{x}-\omega_l t))] \exp{(-i\omega_0 t)}\\
= c_e 
\hbar \Omega^* (e^{i(kx-\omega_l t-\omega_0)t}+e^{-i(kx-\omega_l+\omega_0)t})
$$
RWA: discard the first term, define $\delta = \omega_l - \omega_0$

$$i\hbar \frac{dc_g(t)}{dt} = c_e 
\hbar \Omega^* e^{-i(kx-\omega_l+\omega_0)t}\\
i\hbar \frac{dc_g(t)}{dt} = c_e 
\hbar \Omega e^{i(kx-\omega_l t+\omega_0)t}
$$
And hence we have got the perturbing matrix elements. If we relabel $c_g' = cg$, $c_e' = c_e e^{-i(kx - \Delta t)}$ (although the $kx$ part is unimportant if the atom is at rest) we have 

$$
i\hbar \dfrac{d}{dt}\left[
\begin{array}{cc}
c_g'\\
c_e'	
\end{array}
\right]=
\left[\begin{array}{cc} 
0 & \Omega\\
\Omega & 2\Delta
\end{array}\right] 
\left[\begin{array}{cc}
c_g'\\
c_e'	
\end{array}\right]
$$

Define the off-resonance frequency $\chi = \sqrt{\Omega^2 + \Delta^2}$ And therefore we have the transition probabilities:
$$
|c_g(t)|^2 = \cos^2(\frac{\chi}{2} t) + \frac{\Delta^2}{\chi^2}\sin^2(\frac{\chi}{2}t)\\
|c_e(t)|^2 = \frac{|\Omega^2|}{\chi^2}\sin^2(\frac{\chi}{2}t)
$$

Consider the ratio $\frac{\Delta}{\Omega}$, when it changes, the $|c_e|^2$ (regardless of the sin part) changes like $\frac{|\Omega^2|}{\chi^2} = \frac{1}{1-(\frac{\Delta}{\Omega})^2}$ which is a Lorentzian Peak.

We also introduce the rotation angle $\Theta:=\int_{-\infty}^t |\Omega(t')|dt'$. When $\Delta =0$ this indicates roughly the population that will transit.

#### Spontaneous Emission
Interaction with Monochromatic light gives rise to coherent population between atomic states. In prective, the atom couple to vacuum field which induces spontaneous emission, result in ~100MHz decay. 

Consider the matrix 
$$\left[\begin{array}{cc} 
gg^* & ge^*\\
eg^* & ee^*
\end{array}\right] $$

and we consider the time-derivative of all matrix elements:

$$
\begin{align}
	\dot{\rho}_{gg} &= \frac{i}{2}(\Omega\rho_{ge}-\Omega^*\rho_{eg})+\Gamma\rho_{ee}\\
\dot{\rho}_{ee} &= \frac{i}{2}(\Omega\rho_{ge}-\Omega^*\rho_{eg})-\Gamma\rho_{ee}\\
\dot{\rho}_{ge} &= i\Delta\rho_{ge}+\frac{i\Omega^*}{2}(\rho_{ee}-\rho_{gg})-\frac{\Gamma}{2}\rho_{ge}\\
\dot{\rho}_{eg} &= -i\Delta\rho_{eg}+\frac{i\Omega^*}{2}(\rho_{ee}-\rho_{gg})-\frac{\Gamma}{2}\rho_{eg}
\end{align}
$$

Numerical Integration gives after infinite time $$\rho_{ee} = \frac{|\Omega|^2/4}{\Delta^2 + |\Omega|^2/2 + \Gamma^2/4}$$

This will never exceed $50\%$.
Define $s= \frac{|\Omega|^2/2}{\Delta^2 + \Gamma^2/4}$ and let $s_0 = s(\Delta=0) = \frac{2|\Omega|^2}{\Gamma^2}$, which is the ratio of current intensity to the satuation intensity $\frac{I}{I_{sat}}$. When saturated, $\rho_{ee} = 0.25$.

### Interaction with Trapped Ion

The interaction Hamiltonian is, when we cannot ignore the $kx$ term in the off-diagonal term: 

$$ kr = k\sqrt{\frac{\hbar}{2m\omega}}(\hat{a}u^*(t) + \hat{a}^\dagger u(t)) = \eta(\hat{a}u^*(t) + \hat{a}^\dagger u(t))\\
H =\hbar\frac{\Omega}{2}(|g><e|\exp(-i\eta[au^*(t) + a^\dagger u(t)]) + H.C.)$$

Here we defined $\eta$, the Lamb-Dicke parameter. This is the measure of the recoil energy ($\frac{\hbar^2 k^2}{2m}$) with the spacing ($\hbar\omega_z$) to the square root. Measures the ability of the excitation and emmision events to change the motional state. 

The exponent is expanded near $\eta=0$: 
$$e^{i(\phi+\Delta t)} \sum_{m=0}^{\infty} \frac{(i\eta)^m}{m!} \left(\hat{a}u^*(t) + \hat{a}^\dagger u(t)\right)^m\\
=e^{i(\phi+\Delta t)} \sum_{m=0}^{\infty} \frac{(i\eta)^m}{m!} \left( \hat{a}^\dagger e^{i\beta\Omega/2}\sum_{n=-\infty}^{\infty}C_{2n}e^{in\Omega t}+H.c.\right)^m$$

when the detuning $\Delta$ (in the $\exp$ factor before) matches $(m\beta+n)\Omega_{rf}$ we will cancel the exponent of 2 terms (one and its conjugate) in the Taylor expanded part. They would dominate while the others are RWA'ed away. Then we have some RF sidebands. Normally they are NOT addressed, and they are highly suppressed if ions are in middle of the trap. In this case ignore all $n!=0$ and retain a $1$ as the factor. 

$$H_i = \frac{\hbar}{2}\Omega_0|e><g|\sum_{m=0}^{\infty}\frac{(i\eta)^m}{m!}(\hat{a}e^{-i\omega t}+H.C.)^m e^{i(\phi-\Delta t)} + H.C.$$
Where $\Omega_0=\Omega C_0=\Omega/(1+q/2)$ If we let $\Delta = (k-l)s_z$ we will have combinations resonant and we will have coupled transitions $\hat{a}^\dagger|e><g|$ and $\hat{a}|g><e|$. This couples $|g,n>$ to $|e, n-1>$.

### Secular Motion
Condsider $|g_sg_a0_n>$, the s atom is excited: $(a|g> + b|e>) |g_a0_n>$. Apply red sideband: $(a|g>|0_n> + b|g>1_n>) |g_a>$ Apply red sideband again: $|g>(a|g>+b|e>)|0_n>$ which transfers the state from the first atom to the second. 


## Cooling Basics

### Doppler Cooling
Applicable in the regime where the trap frequenct $\omega_z \ll \Gamma$ which means the scattering / decaying rate is far bigger than the timescale for speed changes; Or, it means the absorbtion and emmision of photons are VERY FAST.

A high scattering rate, for example the $S_{\frac{1}{2}} \leftrightarrow P_{\frac{1}{2}}$ has $\Gamma \approx 2\pi\times20.7MHz$. A typical trap frequency is $\omega_z = 2\pi\times 0.5 MHz$, which satisfies $\omega_z \ll \Gamma$.  

Change of Energy during one scatter from conservation of energy and momentum:

$$\Delta E := \hbar\overrightarrow{v}(\overrightarrow{k_l} - \overrightarrow{k_s}) + \frac{\hbar^2}{2m}(\overrightarrow{k_l} - \overrightarrow{k_s})(\overrightarrow{k_l} - \overrightarrow{k_s})$$ 

The expectation over all scattered wavevecctor $\overrightarrow{k_s}$ is 
$$\langle \Delta E \rangle =  \hbar\overrightarrow{v}\overrightarrow{k_l} + \frac{\hbar^2 k_l^2}{2m}(1+\kappa)$$

Multiply this with the scatter rate $\Gamma \rho_{ee}$: 

$$\frac{d}{dt} \langle \Delta E \rangle =\left[\hbar\overrightarrow{v}\overrightarrow{k_l} + \frac{\hbar^2 k_l^2}{2m}(1+\kappa)\right] \Gamma \rho_{ee} $$.

Consider $\Gamma \rho_{ee}$ near $v=0$ with the doppler effect: 

$$\rho_{ee} = \frac{|\Omega|^2/4}{\Delta^2 + |\Omega|^2/2 + \Gamma^2/4}$$


### Doppler Cooling -2

Radiation pressure / force: $F_{rad} = \frac{IA}{c}$, scattering force: photon momentum $\hbar k$ $\times$ scattering rate, where the scattering rate is $$\Gamma\times\rho_{ee} = \frac{\Gamma}{2}\frac{\Omega^2/2}{\delta^2+\Omega^2/2+\Gamma^2/4}$$ where $\delta = \omega+kv-\omega_0$, doppler shifted frequency minus $\omega_0$ the absorbtion frequency. Relabel $\frac{2\Omega^2}{\Gamma^2}$


$\begin{align}
	F &= \hbar k \frac{\Gamma}{2} \frac{I/I_{sat}}{1+I/I_{sat}+4\delta^2/\Gamma^2}\\
	a_{max}&=\frac{F_{max}}{M}=\frac{\hbar k \frac{\Gamma}{2}}{M}=\frac{v_r}{2\tau}
\end{align}$

where $v_r = \frac{\hbar k}{M}$ the recoil speed, change in speed for the absorption or emission. $\tau$ is the lifetime for traisition with $\Gamma$. Hence we define the stopping distance $L_0 = \frac{v_0^2}{a_{max}}$

#### Optical Molasses
$$\begin{align}
F_{molasses} &= F_{scatt}(\omega-\omega_0-kv) - F_{scatt}(\omega-\omega_0+kv)\\ &\approx F_{scatt}(\omega-\omega_0) - kv\frac{\partial F}{\partial \omega} - \left[ F_{scatt}(\omega-\omega_0) + kv\frac{\partial F}{\partial \omega} \right]
&= -2\frac{\partial F}{\partial \omega}kv 
\end{align}$$
where we assumed a low velocity, i.e. $kv \ll \Gamma$. This gives a viscous force $F=-\alpha v$ where 
$$\begin{align}\alpha &= -2k \frac{\partial F}{\partial \omega} =  -2k\frac{\partial \hbar k R_{scatt}}{\partial \omega} \\&= -2k(\frac{\hbar}{c}R_{scatt} + \frac{\hbar \omega}{c}\frac{\partial R_{scatt}}{\partial \omega}) \\ &\approx2\hbar k^2 \frac{\partial R_{scatt}}{\partial \omega} \\
&\approx 4\hbar k^2 \frac{I}{I_{sat}}\frac{-2\delta/T}{[1+(2\delta/T)^2]^2}
\end{align}$$ 
The third line is done by discarding the first term since it is so small. The last line we have discarded the $\Omega^2/2$ since it is small for optical molasses ($I \ll I_{sat}$). For damping we want $\alpha \gt 0$ so $\delta=\omega-\omega_0 \lt 0$.

EOM:

$$\frac{\partial}{\partial t}\frac{1}{2}Mv^2 = Mv_z \frac{\partial z }{\partial t} = Fv_z =-\alpha v_z^2$$

$$\frac{\partial E}{\partial t} = \frac{\partial}{\partial t}(\frac{1}{2} m(v_x^2+v_y^2+v_z^2) ) = \frac{-2\alpha }{M}E :=-\frac{E}{\tau_{damp}}$$ Hence the energy, $E$, hence the temprature $T$ will decrease. 

Force from single beam: $\overrightarrow{F} = \overrightarrow{F_{abs}} + \overrightarrow{\delta F_{abs}}+ \overrightarrow{F_{spo}}+ \overrightarrow{\delta F_{spo}}$ where $_{abs}$ means absorption process and $_{spo}$ means spontaneous emissions, the force from which cause the atom to recoil and never come to a rest. 

1. $\overrightarrow{\delta F_{spo}}$ leads to a random walk in velocity: steps $N = R_{scatt} t$. $\bar{v^2} =  R_{scatt} \times v_r^2$ and hence $v\sim\sqrt{N}$. Along $z$: $(\bar{v_z^2})_{spo} = \eta v_R^2 R_{scatt} t$ where $\eta = \langle \cos^2 \theta \rangle$ is the angular average.

2. $\overrightarrow{\delta F_{abs}}$: the atom will not always absorb the same amount of photons. It absorbs with a Poissonian statistic: lead to a random walk and hence increase the velocity spread. $\bar{v_z^2} = R_{scatt} \times v_r^2$ but this time without $\eta$ since the absorption is always in $z$. with 2 directions $+z$ and $-z$ the forces cancel but the fluctuation doubles.

new EOM: 

$$M \frac{\partial}{\partial t}\frac{1}{2}v^2 = (1+\eta)E_r (2R_{scatt}) - \alpha v_z^2$$ 
Steady state: $$v_z^2 = (1+\eta)E_r\frac{2R_{scatt}}{\alpha}$$ hence $$k_BT = M\bar{v^2} = \frac{\hbar \Gamma}{4}\frac{1+(2\delta/\Gamma)^2}{-2\delta/\Gamma} \geq \frac{\hbar \Gamma}{2}$$ which is the **Doppler Limit**.

This means $T_D = \frac{\hbar\Gamma}{2k_B} \approx 240\mu K$ for Na which gives avg speed $0.5m/s$. The speed $v_D = \sqrt{\frac{\hbar \Gamma}{M}} = \sqrt{\frac{\hbar k}{M}} \frac{\Gamma}{k} = \sqrt{v_r v_C}$, where $v_c = \frac{\Gamma}{k}$, the capture speed for which $F_{scatt}$ has significant value.


### Sideband Cooling


![sideband](Sideband.png)

Drive at the sideband, make the detuning $-\omega_z$ we will have the rate to be $$\Gamma\rho_{ee} = \Gamma\frac{\Omega^2/4}{\delta^2 + \Omega^2/2 + \Gamma^2/4}=\Gamma\frac{\Omega^2}{4\delta^2 + 2\Omega^2 + \Gamma^2}\approx\Gamma\frac{(\Omega\eta \sqrt{n})^2}{2(\Omega\eta \sqrt{n})^2 + \Gamma^2}$$

Two heating mechanisms: excite at carrier but decay at red; excite at blue and decay at carrier (both gives $+\omega_z$). For the first one we have 


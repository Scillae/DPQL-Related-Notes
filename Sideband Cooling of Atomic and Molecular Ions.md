# Sideband Cooling of Atomic and Molecular Ions

### Abstract

## General Physics of Trapped Ions
#### 1. Introduction
- Doppler cooling relies on continuous scattering of photons.
- Most molecular ions remain unsuitable for laser cooling, due to decays to different <span style='color:red'>rovibrational</span> levels.
- use the common motion of the ions to transfer quantum information
- quantum logic can be used to determine the internal state of a *spectroscopy* ion using an *auxiliary* ion.
    - only the *auxiliary* ion is required to provide a closed level scheme (no population leaking?) for cooling and state detection.
    - spectroscopy ion provides a good clock transition, co-trapped auxiliary ion bears the measurements.
- (??) requires cooling to the motional ground state.
----
----
### 2. Trapped Ions
----
#### 2.1 Linear Paul Trap
----
##### 2.1.2 Pseudo-potential Model
- $\omega_n=(2n+\beta)\Omega/2$ is the ion's oscillation frequency.
    - at $\beta \ll 1$, fundamental freq $\sim 0 \rarr$ fundamental: secular, higher-order: micromotion. (?)
- Equations of secular and micro-motion:
    - Secular: $\frac{d^2R_i}{dt^2}=-\omega_i^2R_i$
    - Micro-: $\delta_i=-\frac{q_iR_i}{2}cos(2\xi)$
- Expressions of secular and micro-motion: (in $\textrm{i}^\textrm{th}$ direction)
    - Secular : $r_{i,s}=r_i^0cos(\omega_it+\phi_i)$
    - Micro- : $r_{i,\mu}=-r_i^0cos(\omega_it+\phi_i)\cdot\frac{q_i}{2}cos(\Omega t)$
    - Overall: $r_i=r_{i,s}+r_{i,\mu}$
    - $r_i^0$ and $\phi_i$ are determined by initial condition.
- Secular frequency: $\omega_i=\frac{\Omega}{2}\sqrt{\frac{q^2_i}{2}+a_i}=\frac{\Omega}{2}\beta_i$
- Harmonic pseudo-potential: ($q_i$ small, $r_{i,\mu}$ neglected)
    - $\Psi_i=\frac{1}{2}m\omega_i^2r_i^2$
        - Example: (Ca: 40 amu, 2.7 mm to electrodes, radial freq $\omega_r=2\pi\cdot1$ Mhz)
            - $\Psi=0.5*6.64*10^{-26}*(2.7*10^{-3})^2*(2pi*10^6)^2*6.24×10^{18}=60$ eV
- Stray electric charge: shift of 0-potential point, ion exhibits additional micro-motion
    - $r_{i,e}=r_i^e(1-\frac{q_i}{2}cos(\Omega t))$ , parallel to secular motion
        - $r_i^e$ : stationary shift of 0-potential point
- Phase or amplitude differences of the RF-potentials can cause excess micro-motion as well.

----
----
#### 2.2 Quantum Mechanics of the Ion Motion
- Compensation to position operator : (substitutive with pseudo-potential)
    - $\hat{r}=\sqrt{\frac{\hbar}{2m\omega}}(\hat{a}u^*(t)+\hat{a}^\dagger u(t))$
        - $u(t)=e^{i\beta\Omega/2}\sum_{n=-\infty}^{\infty}C_{2n}e^{in\Omega t}$
    - use when pseudo-potential not applicable due to failure of the compensation to micro-motion
----
#### 2.3 Motion of 2 Co-Trapped Ion
- Axial normal modes of motion : ($\sim \omega_z$ in single-ion cases)
    - $\omega_\pm=\omega_z\sqrt{1+\frac{1}{\mu}\pm\sqrt{1-\frac{1}{\mu}+\frac{1}{\mu^2}}}$
        - $\mu=\frac{m_2}{m_1}$: reduced mass
        - $\omega_-$ resembles center of mass mode
    
----

----
### 3. Atom-Light Interactions
----
#### 3.1 Free 2-Level Atom
- $H_a=\hbar\omega_g\ket{g}\bra{g}+\hbar\omega_e\ket{e}\bra{e}$
    - $\ket{g}\sim\hbar\omega_g$ , $\ket{e}\sim\hbar\omega_e$ , $\omega_0=\omega_e-\omega_g$
##### 3.1.1 Interaction with light
- $H_i=\frac{\hbar}{2}\Omega(\ket{g}\bra{e}e^{-i(\vec{k}\cdot\vec{x}-\omega_lt+\phi)}+\ket{e}\bra{g}e^{i(\vec{k}\cdot\vec{x}-\omega_lt+\phi)})$
    - $\vec{k}$ : wave vector ; 
    - $\vec{x}$ : position of atom ;
    - $\omega_l$ : angular freq of light ; 
    - $\phi$ : relavant phase shift ; 
    - $\Omega$ : Rabi-freq.
        - $\Omega=\frac{2}{\hbar}e\bra{g}\vec{E_0}\cdot\vec{x}\ket{e}$
            - $\vec{E_0}$ contains polarization direction. Measured at $\vec{x}$.
    - Dipole and rotating wave approximation are applied.
        - Dipole approximation: $e^{i\vec{k}\cdot\vec{x}}$ , negelecting the spatial phase change of wave over the atom ($\lambda\gg a_0$).
        - rotating wave approximation: terms $\sim(\omega_l+\omega_a)\sim2\omega_l\rarr0$ , in which $\omega_l$ is laser freq. $\rarr$ terms $\sim\Delta=(\omega_l-\omega_a)$ is preserved. Same as in C.J.Foot.
- Probability at states: (assuming atom at rest ;  not at rest: Doppler shift)
    - $|c_g(t)|^2=cos^2(\frac{\chi t}{2})+\frac{\Delta^2}{\chi^2}sin^2(\frac{\chi t}{2})$
    - $|c_e(t)|^2=\frac{|\Omega|^2}{\chi^2}sin^2(\frac{\chi t}{2})$
        - $\chi=\sqrt{|\Omega^2|+\Delta^2}$ : off-resonant Rabi-freq
            - now population oscillate at this freq, not $\Omega$
        - $\Delta=\omega_l-\omega_a$ : detuning (laser from atom, $\omega_a\equiv\omega_0$)
        - Example: $\pi$ - pulse in perfect transition ($\Delta$=0) $\sim$ perfect oscillation
            - rotation angle: transferred population
                -  $\Theta(t)=\int_{-\infty}^t|\Omega(t')|dt'$ (still assuming $\Delta=0$)
            - $t\Omega=\pi$ , $|c_e(t)|^2=1\cdot sin^2(\frac{\pi}{2})=1$ , population perfectly inverted.
    - $\Omega(t)=\Omega$ is assumed, but not true for real laser.
        - true only if linear polarization
            - direction of polarization: $\hat{\vec{E_0}}$
            - direction of propagation: $\hat{\vec{k}}$ 
##### 3.1.2 Spontaneous Emission
- density matrix: [$\rho_{ij}=c_ic_j^*$] , $i,j\in\{e,g\}$
- damped Rabi-oscillation $\rarr$ steady state at $t\gg\tau=1/\Gamma$
    - steady state population $\rho_{ee}=\frac{|\Omega|^2}{4\Delta^2+2|\Omega|^2+\Gamma^2}=\frac{1}{2}\frac{s}{s+1}$
        - $s=\frac{2|\Omega|^2}{4\Delta^2+\Gamma^2}$
            - $s_0=s(\Delta=0)=\frac{I}{I_{sat}}$
            - ($\Delta=0$ and $I=I_{sat}$) provide maximum $\rho_{ee}=1/4$ 
                - maximum population at $\ket{e}$ when spontaneous emission is considered
- Doppler shift correction: $\Delta'=\Delta+\vec{k}\cdot\vec{v}$
    - substitute in when atom is not at rest.
----
#### 3.2 Interaction With a Trapped Ion
- $\ket{g,n}$ represents atomic states *if no entanglement between $\ket{g} , \ket{n}$*
- motion $\rarr$ sidebands
    - $\omega_l=\omega_a\pm\omega_z$
    - attribute of ion spectrum, not laser!
- $H_i=\frac{\hbar}{2}\Omega(\ket{g}\bra{e}e^{-i(\eta[\hat{a}u^*(t)+\hat{a}^\dagger u(t)]-\Delta t+\phi)}+\ket{e}\bra{g}e^{+i(\eta[\hat{a}u^*(t)+\hat{a}^\dagger u(t)]-\Delta t+\phi)})$
    - resemble the $H_i$ in 3.1.1
    - $h_{eg}=h_{ge}$ still holds: symmetry between $1\rarr2$ and $2\rarr1$
- **Lamb-Dicke parameter** $\boldsymbol{\eta}$ :$=\vec{k}\cdot\vec{x}_0=\vec{k}\cdot\hat{x}\sqrt{\frac{\hbar}{2m\omega_z}}$
    - the ability of excitation and emission events to change the motional mode of the ion
    - $\eta=\sqrt{E_{rec}/\hbar\omega_z}$
        - ratio between the recoil energy (of the ion due to photon emission) and the energy separation of the motional states
- Lamb-Dicke approximation: $\eta\sim0$ , expansion about $\eta$ 
    - $e^{-i(\eta[\hat{a}u^*(t)+\hat{a}^\dagger u(t)]-\Delta t+\phi)}\approx e^{i(\Delta t-\phi)}\cdot\sum_{m=0}^\infty\frac{1}{m!}\cdot(i\eta)^m\cdot(\hat{a}^\dagger e^{i\beta\Omega_{\textrm{rf}}t/2}\cdot\sum_{n=-\infty}^\infty C_{2n}e^{in\Omega_{\textrm{rf}}t}+\textrm{h.c.})^m$
    - $..\approx..$ at $\Delta\approx(m\beta+n)\Omega_{\textrm{rf}}$
        - RWA again
        - called "tuning to the $n^{\textrm{th}}$ micro-motional- and $m^{\textrm{th}}$ secular sideband"
- No RF-sideband assumption: ($e^{in\Omega_{\textrm{rf}}t}\sim0$ if $n\neq0$ , another RWA)
    - $H_i\simeq\frac{\hbar}{2}\Omega_0(\ket{e}\bra{g}\cdot C_0\cdot e^{i(-\Delta t+\phi)}\cdot\sum_{m=0}^\infty\frac{1}{m!}\cdot(i\eta)^m\cdot(\hat{a}^\dagger e^{i\omega_zt/2}+\hat{a} e^{-i\omega_zt/2})^m+\textrm{h.c.})$
        - $\Omega_0=\Omega\cdot C_0=\Omega/(1+q/2)$
        - $\omega_z=\beta\Omega_{\textrm{rf}}/2$ is applied.
        - (Assuming $\omega_0\equiv\omega_z$)
    - notice that $H_i \sim k\cdot \hat{a}+l\cdot\hat{a}^\dagger$
- couple manifold $\ket{g,n} \lrarr \ket{e,n+s}$
    - connection strength: $\bra{g,n}H_i\ket{e,n+s}=\frac{\hbar}{2}\Omega e^{i(\phi-\omega_l t)}\bra{n}e^{i(\vec{k}\cdot\vec{x})}\ket{n+s}$
    - by setting $\Delta\approx s\omega_z$ , with $s=k-l$
    - $s > 0$ : blue sideband ; $s < 0$ : red sideband ; $s = 0$ : carrier
    - <span style='color:red'>BUT I remember only s=1 works??</span>


----
#### 3.3 Secular Motion as a State Mediator
----
----
### 4. Cooling of Trapped Ions
----
#### 4.1 Doppler Cooling
----
#### 4.2 Sideband Cooling
----
#### 4.3 Determination of the Motional State
----
----
### 5. Manipulating the $^{40}\textrm{Ca}^+$ ion
----
#### 5.1 Doppler Cooling
----
#### 5.2 Sideband Cooling
----
#### 5.3 Detecting the Internal State
----

# Atomic Physics - C.J.Foot
*1:ground, 2:excited for 2-level atoms*
## 7.6 Optical absorption cross-section
- (G) Monochromatic radiation $\rarr$ Rabi oscillation $\Omega$  
Damping in transition $\rarr$ steady state with $R_{excitation}=R_{decay}$ &nbsp;&nbsp;&nbsp;&nbsp;($A_{21}+B{21}=B_{12}$？)  
- (B) **Cross-Section** $\sigma$: characterize the probability of absorption  
    -  $\rarr \sigma(\omega)=3\times\frac{\pi^2c^2}{\omega^2_0}A_{21}g_H(\omega)$  
    -  **Line shape function**: carries Lorentzian frequency dependence  
        - $g_H(\omega)=\frac{1}{2\pi}\frac{\Gamma}{(\omega-\omega_0)^2+\Gamma^2/4}$ (H:homogeneous)
        - Normalized: $\int_{-\infty}^{\infty}g_H(\omega)\textrm{d}\omega=1$  
    - prefactor 3: max, atom with optimum orientation to absourb a beam of polarized laser.  
        - if =1 $\rarr$ light is unpolarized *OR* atoms have random orientation  
        - $|X_{12}|^2=|D_{12}|^2/3$ cancels the 3.
    - $\rarr \sigma(\omega)=\frac{g_2}{g_1}\times\frac{\pi^2c^2}{\omega^2_0}A_{21}g_H(\omega)$ for a real atom with degenerate levels. (Forgot what's $g_2$ and $g_1$...)  

- (B) Absorption and stimulated emission have the same cross-section. <span style='color:red'>(Then how can it be stable?)</span>  
    - $(N_1-N_2)\sigma(\omega)I(\omega)=N_2A_{21}\hbar\omega$ , due to conservation of energy.
    - $B_{21}=B_{12}$ for non-degenerate levels since the oscillating electric field drive the transitions at the same rate.  

- (Y) $\omega=\frac{N_2-N_1}{N}$. Why?  
----
### 7.6.1 Cross-section for pure radiative broadening
- *Peak absorption cross-section* at $\omega=\omega_0$:  
    - $\sigma(\omega_0)=3\times\frac{2\pi c^2}{\omega_0^2}\frac{A_{21}}{\Gamma}$  
    - 2 level atoms: $\Gamma=A{21}$ since only decay to ground.  
        - $\sigma(\omega_0)=3\times\frac{\lambda_0^2}{2\pi}\simeq\frac{\lambda_0^2}{2\pi}$  
        - Optical cross-section quickly decreases at off resonance.
----
### 7.6.2 The saturation intensity
- **Saturation Intensity**: maximum absorption intensity
    - $I_{sat}=\frac{\pi}{3}\frac{hc\Gamma}{\lambda^3}$
    - $I_{sat} \equiv I_s(\omega_0)$ and $(I_s/I) (\omega)=\frac{N_1-N_2}{2N_2}(=-\frac{\omega\cdot N}{2N_2}...)$  
        - Also, $I_s(\omega)=\frac{\hbar\omega A_{21}}{2\sigma(\omega)}$, which gives the top one $\uarr\uarr\uarr$  
    - *Alt. Def.*: $\frac{I}{I_{sat}}=\frac{2\Omega^2}{\Gamma^2} \rarr \Omega \sim \Gamma$ at saturation.  
        - $\Omega^2/I$ does *NOT* depend on the electric field.
    - Intensity $\sim$ Cross-section: $\frac{I_s(\omega)}{I_{sat}}=\frac{\sigma_0}{\sigma(\omega)}$ , in which $\sigma_0=\sigma(\omega_0)$
    - $\tau=\Gamma^{-1}$ is the lifetime for radiative broadening.
        - i.e.: a resonance transition at wavelength $\lambda=589$ nm has lifetime $\tau=16$ ns (assumed 2-level atom)
            - what will happen at $\tau$?
----
### 7.6.3 Power broadening
- **Power broadening**: saturation reduces the absorption only near the resonance
    - absorption coefficient: $\kappa(\omega,I)=N\sigma_0\frac{\Gamma/4}{(\omega-\omega_0)^2+\frac{1}{4}\Gamma^2(1+I/I_{sat})}$, with a Lorentzian line shape.
        - $\Delta\omega_{FWHM}=\Gamma(1+\frac{I}{I_{sat}})^{1/2}$, correlated with $I$.

----
## 7.7 The a.c. Stark / light shift effect
- **a.c. Stark Effect**: the perturbing radiation also changes the energy of the levels
    - $E_{a.c.S.}=\pm(\delta^2+\Omega^2)^{1/2}/2$ assuming 2-level atom, for which 'unperturbed energies': $E_{o}=\pm\delta/2$
        - the two 'unperturbed states' are $E_1+\hbar\omega, E_2$ , with $E_2-E_1=\omega_0 \rarr \delta=\omega-\omega_0$ is the detuning.
        - The two 'unperturbed levels' degenerate when laser at resonant (for bare atom).
    - $\lambda\simeq\pm(\frac{\delta}{2}+\frac{\Omega^2}{4\delta})$ , at approximation $|\delta| \gg \Omega$.
----



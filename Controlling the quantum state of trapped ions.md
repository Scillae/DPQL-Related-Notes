# Controlling the quantum state of trapped ions
## Roadmap:
- Chapters 2 and 3 : basic theoretical foundations. 
    - Chapter 2 : the function of the electrodynamic Paul trap
    - Chapter 3 : Laser-ion interactions
        - Coherent interactions between trapped atoms and lasers
        - Cooling techniques
        - Special case of trapped $\mathrm{Ca}^{+}$ions
- Chapter 4 : experimental setup
- Chapter 5 : Basic experimental techniques required for trapping, exciting, and detecting ions
- Chapter 6 : Main experimental results. 
    - Spectroscopy of the $S_{1 / 2} \leftrightarrow D_{5 / 2}$ quadrupole transition
    - Doppler cooling & sideband cooling 
    - Heating rate measurements
        - show that the ion constitutes a quantum system that is well isolated from its environment. 
    - Simple quantum state manipulation experiments
    - The first steps to extend the experiments to two ions
- Chapter 7 : how to couple a transition between two internal states of an ion to the mode of a high-finesse resonator & an experimental setup that will eventually allow the increase of the spontaneous decay rate of a metastable atomic state. 
----
## Chapter 2 Paul Traps
----
### 2.1 Principle of Operation
----
### 2.2 Single Ion Traps
----
### 2.3 Compensation of Micromotion
----
### 2.4 Ion Crystals
----

## Chapter 3 Laser-ion interactions
----
### 3.1 Basic Interactions
- $H=H_0+H_1$
    - $H_0 =\frac{p^2}{2 m}+\frac{1}{2} m \omega^2 x^2+\frac{1}{2} \hbar \nu \sigma_z$
        - $\nu$ : transition frequency
    - $H_1 =\frac{1}{2} \hbar \Omega\left(\sigma^{+}+\sigma^{-}\right)\left(e^{i\left(k x-\nu_L t+\phi\right)}+e^{-i\left(k x-\nu_L t+\phi\right)}\right)$
        - $\Omega$ : Coupling strength ($\frac{eE_0}{\hbar}$ ??)
        - k : the wavevector of laser
        - $\nu_L$ : the frequency of laser
        - being imaginary exponential: representing the actual (relative) phase that the atom sees.
    - $H_0$ : the state of the ion
    - $H_1$ : laser-ion interaction
- $\eta=k \sqrt{\frac{\hbar}{2 m \omega}}$ , Rotating-Wave Approximation
    - $H_0 = \hbar \omega\left(a^{\dagger} a+\frac{1}{2}\right)+\frac{1}{2} \hbar \nu \sigma_z$
    - $H_1 = \frac{1}{2} \hbar \Omega\left(e^{i \eta\left(a+a^{\dagger}\right)} \sigma^{+} e^{-i \nu_L t}+e^{-i \eta\left(a+a^{\dagger}\right)} \sigma^{-} e^{i \nu_L t}\right)$
- $H_I=U^{\dagger} H U$ , $U=e^{i H_0 t / \hbar}$
    - $H_I=\frac{1}{2} \hbar \Omega\left(e^{i \eta\left(\hat{a}+\hat{a}^{\dagger}\right)} \sigma^{+} e^{-i \Delta t}+e^{-i \eta\left(\hat{a}+\hat{a}^{\dagger}\right)} \sigma^{-} e^{i \Delta t}\right)$
        - $\hat{a}=ae^{i\omega t}$
        - $\Delta=\nu_L-\nu$
    - Interaction Picture
- Rabi frequency : $\Omega_{n+m, n}:=\Omega\left\langle n+m\left|e^{i \eta\left(\hat{a}+\hat{a}^{\dagger}\right)}\right| n\right\rangle$
    - Atomic Physics : $\Omega=\frac{\left\langle 1\left|e \mathbf{r} \cdot \mathbf{E}_0\right| 2\right\rangle}{\hbar}$
    - How to see them equivalent?
- On resonant, population oscillates between the 2 states at Rabi frequency:
    - $\left(\begin{array}{c}c_n(t) \\ d_{n+m}(t)\end{array}\right)=\left(\begin{array}{cc}\cos \left(\Omega_{n+m, n} t / 2\right) & -i e^{i \frac{\pi}{2}|m|} \sin \left(\Omega_{n+m, n} t / 2\right) \\ -i e^{-i \frac{\pi}{2}|m|} \sin \left(\Omega_{n+m, n} t / 2\right) & \cos \left(\Omega_{n+m, n} t / 2\right)\end{array}\right)\left(\begin{array}{c}c_n(0) \\ d_{n+m}(0)\end{array}\right)$
- Laser detuned $\rarr$ population transfer is no longer complete, but at a higher frequency
    - Pg. 25
- the coupling strength of a laser tuned to m'th sideband, with atom in L-D regime:
    - $L_0^m(x)=1$ : targeted sideband
    - $L_1^m(x)=m+1-x$ : (1st) adjacent sideband
    - $L_{n+1}^m(x)=\frac{1}{n+1}\left((2 n+1+m-x) L_n^m-(n+m) L_{n-1}^m\right)$ for $n>1$ (farther sidebands)
----
#### 3.1.1 L-D Regime
- the atomic wavepacket is confined to a space much smaller than the wavelength of the transition in the Lamb-Dicke regime
    - $\eta^2(2 n+1) \ll 1$
    - $\exp \left(i \eta\left(\hat{a}^{\dagger}+\hat{a}\right)\right)=1+i \eta\left(\hat{a}^{\dagger}+\hat{a}\right)+\mathcal{O}\left(\eta^2\right)$
        - processes that change the vibrational quantum number n by more than one are strongly suppressed
- the Lamb-Dicke regime is **always defined with respect to the wavelength** of the transition involved!
    - If it is mentioned without reference to any particular transition, it is assumed that the Lamb-Dicke criterion holds for all relevant transitions.
- Coupling strength on the carrier : $\Omega_{n, n}=\Omega\left(1-\eta^2 n\right)$
    - $H_I=\frac{1}{2} \hbar \Omega_{n, n}\left(\sigma^{+}+\sigma^{-}\right)$
- Coupling strength on RSB/BSB:
    - $\Omega_{n-1, n}=\eta \sqrt{n} \Omega$ ; $\Omega_{n+1, n}=\eta \sqrt{n+1} \Omega$
    - $H_I=\frac{1}{2} i \hbar \Omega_{n-1, n}\left(\hat{a} \sigma^{+}-\hat{a}^{\dagger} \sigma^{-}\right)$ for RSB ; $H_I=\frac{1}{2} i \hbar \Omega_{n+1, n}\left(\hat{a}^{\dagger} \sigma^{+}-\hat{a} \sigma^{-}\right)$ for BSB
        - These couplings are sometimes referred to as the Jaynes-Cummings and anti-JC Hamiltonian
            - describ es the interaction of a two-level atom with a quantised mo de of the electro-magnetic field. See Chapter 7.
----
#### 3.1.2 Further remarks
- Non-resonant interactions
    - When driving sidebands, carrier may still be driven
        - the resonance frequency of the transition $\ket{S,n}\lrarr\ket{D,n\pm1}$ is changed:
            - $\delta_S=-\frac{\Omega_{n, n}^2}{2 \Delta}, \Delta=\nu_L-\nu$ , if condition $\Delta\gg\Omega_{n,n}$ is not met.
    - Small transfer of p opulation to the non-resonantly coupled levels
        - proportionality factor of leaking: $\sim (\frac{\Omega_{n, n}}{2 \Delta})^2$
- Generalizations of the model
    - 3D potential: $k\cdot r\rarr\vec{k}\cdot\vec{r}$ & $e^{i\eta(a^\dagger+a)}\rarr e^{i \mathbf{k} \cdot \mathbf{r}}=\prod_m e^{\left(i \eta_m\left(a_m^{\dagger}+a_m\right)\right)}$
- N-ion crystal
    - $H_1=\frac{1}{2} \sum_{i=1}^N \hbar \Omega_i \sigma_i^{+} \exp \left(i \sum_m \eta_m^i\left(a_m^{\dagger}+a_m\right)\right) \exp \left(-i\left(\nu_L-\phi_i\right) t\right)+h . c$.
        - i'th ions
        - where $a^\dagger_m$ and $a_m$ are the creation and annihilation operators for the normal modes of oscillation labelled 1...m
        - Go ref[57] for how to obtain (calculate?) $\eta_m^i$
- Experimental realizations of the model
    - 

----
### 3.2 Laser Cooling
----
#### 3.2.1 Doppler cooling
----
#### 3.2.2 Sideband cooling
----
### 3.3 Quantum State Manipulation and Analysis
----
#### 3.3.1 Electron Shelving
----
#### 3.3.2 Quantum State Analysis
----
### 3.4 Sideband Cooling and Quantum State Manipulation of $\textrm{Ca}^+$ Ions
----
#### 3.4.1 Level Scheme of $\textrm{Ca}^+$ Ions
----
#### 3.4.2 Cooling Techniques
----
#### 3.4.3 Coherent Manipulations: Geometrical Considerations
----
#### 3.4.4 Pulsed Spectroscopy on the $S_{1/2}\lrarr D_{5/2}$ transition
----

----
## Chapter 4 Experimental Setup
----
### 4.1 Ion Trap Apparatus
----
#### 4.1.1 Trap Deisng
----
#### 4.1.2 Radio-Frequency Drive
----
#### 4.1.3 Vacuum Vessel
----
#### 4.1.4 Fluorescence Detection
----
#### 4.1.5 Computer Control
----
#### 4.1.6 Laser Beams
----
### 4.2 Lasers
----
#### 4.2.1 Frequency Doubled Ti: Sapphire Laser for 397 nm
----
#### 4.2.2 Ultra Stable Ti: Sapphire Laser for 729 nm
----
#### 4.2.3 Diode Lasers at 854 and 866 nm
----
#### 4.2.4 Wavelength Measurements
----
## Chapter 5 Ion Storage
----
### 5.1 How to Trap Single Ions
----
### 5.2 Electronic Excitation of the Secular Motion
----
### 5.3 Compensation of Micromotions
----
#### 5.3.1 Coarse Compensation
----
#### 5.3.2 Correlation Measurements
----
#### 5.3.3Resolved Sideband Measurements
----
### 5.4 Excitation Spectra
----
#### 5.4.1 $S_{1/2}\lrarr P_{1/2}$ Cooling Transition
----
#### 5.4.2 $D_{3/2}\lrarr P_{1/2}$ Transition
----
#### 5.4.3 $D_{5/2}\lrarr P_{3/2}$ Transition
----
### 5.5 Optimization of the Laser Parameters and the Magnetic field
----
## Chapter 6
----
### 6.1 Spectroscopy on the $S_{1/2}\lrarr D_{5/2}$ Transition
----
#### 6.1.1 Spectrum of a Single Ion
----
#### 6.1.2 Ramsey Resonance Experiments
----
#### 6.1.3 Two-Ion Spectra
----
#### 6.1.4 AC-Stark Shifts
----
### 6.2 Coherent Dynamics after Doppler Cooling
----
### 6.3 Temperature Measurements after Doppler Cooling
----
### 6.4 Sideband Cooling Experiments
----
#### 6.4.1 Sideband Cooling Results
----
#### 6.4.2 Cooling Dynamics
----
#### 6.4.3 Heating Rate Measurements
----
#### 6.4.4 Sideband Cooling of Two Ions
----
### 6.5 Coherent Dynamics after Sideband Cooling
----
#### 6.5.1 Rabi Oscillations
----
#### 6.5.2 Non-Resonant Excitations
----
#### 6.5.3 Generation of Fock States
----
#### 6.5.4 Two-Ion Results
----
### 6.6 Coherence-Limiting Processes
----
### 6.7 Improvements of the Experimental Setup
----

----
## Chapter 7
----

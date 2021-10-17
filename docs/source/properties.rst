Physical Properties of Topological Insulators
======================================================

Helical Spin Polarization
-----------------------------

* Electron spins of topological surface states lies in the plane :math:`(k_x, k_y)`.
* Electron spins are perpendicular to :math:`\vb{k}`.
* Electrons hold helicity.
  
  * In particular, a Kramers pair consists of :math:`(\vb{k},\vb{\sigma})` and :math:`(-\vb{k},-\vb{\sigma})`, i.e. they hold the same helicity.
* Degeneracy at Dirac point protected by TRS.
* TIs known as of 2014 are left-handed for Fermi levels above the Dirac point and right-handed below.

.. warning::
    It seems that the definition of helicity here is a little bit different than that in particle physics.

.. note::
    Dirac cone of topological surface state is non-degenerate.

Quasiparticle Interference
-------------------------------

* Quasiparticle interference: If :math:`\vb{k}_1` is scattered to :math:`\vb{k}_2`, then these two states may interfere with each other and change the charge density.
* Spin is preserved during scattering by non-magnetic centers. Therefore, in scattering of topological surface states, scattering of the form :math:`\vb{k} \rightarrow -\vb{k}` are forbidden due to spin polarization.
* In :math:`\ce{Bi2Te3}` where the Dirac cone is replaced a complex :math:`C_6` shape, scattering is not limited to :math:`\vb{k} \rightarrow -\vb{k}` and therefore quasiparticle interference is observable.

Transport Properties
------------------------

.. warning::
    Electrons being zero-mass Dirac particles does not implies that the effective masses are zero. Instead, the effective masses are divergent for Dirac particles.

Dirac Particles
^^^^^^^^^^^^^^^^^^^^^^^^

* Massless Dirac particles carries a Berry phase of :math:`\pi`:
  
  .. math::
      \gamma = \oint_C \dd{\vb{k}} \cdot i \bra{u_\pm(\vb{k})} \nabla_k \ket{u_\pm(\vb{k})} = \pi.
* In ordinary metals the electrons have a higher back scattering probability due to interference, which leads to weak localization.
  
  * Negative magnetoresistance since :math:`\vb{A}` breaks such interference.
* For Dirac particles, with the :math:`\pi` Berry phase such scattering is reduced, leading to weak antilocalization.

  * Positive cusp-shape magnetoresistance since :math:`\vb{A}` breaks such interference.
* Landau quantization depending on :math:`N`:
  
  .. math::
      E_\pm(N) = \pm \sqrt{\frac{2e\hbar v_{\mathrm{F}}^2}{c} \cdot N}.
  * Hall conductivity quantized: :math:`N` denoting the highest filled Landau level,
    
    .. math::
        \sigma_{xy} = -\frac{e^2}{h} \qty(N + \frac{1}{2}).

SdH Oscillation of Surface State
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Lattice vibration only has finite effect on Landau levels.
* Electronic properties mostly depend on :math:`\rho(E_{\mathrm{F}})`.
* DoS to relaxation time:

  .. math::
      \rho(E_{\mathrm{F}}) \sim \frac{1}{\tau},
  i.e. higher the DoS, higher the scattering probability.
* Under strong magnetic field,
  
  .. math::
      \sigma_{xx} &\approx \frac{nm^* c^2}{B^2 \tau}, \\
      \sigma_{xy} &\approx \frac{nec}{B}.
* Minima of :math:`\sigma_{xx}`: :math:`E_{\mathrm{F}}` between two consecutive Landau levels, and therefore :math:`\rho(E_{\mathrm{F}})` is small.
* Maxima of :math:`\sigma_{xx}`: :math:`E_{\mathrm{F}}` lies at a certain Landau level, and therefore :math:`\rho(E_{\mathrm{F}})` is large.
* Different from ordinary 2D electron systems where :math:`\sigma_{xy}` is proportional to the filling factor :math:`\nu`, in a Dirac system :math:`\sigma_{xy}` is proportional to `(N+1/2)` due to the Landau level at the Dirac point.

Fan Diagram
""""""""""""""""""

* Oscillation of :math:`\sigma_{xx}`:

  .. math::
      \Delta \sigma_{xx} \propto \cos \qty[ 2\pi\qty(\frac{F}{B} - \frac{1}{2} + \beta)].
* :math:`B_N` denotes the :math:`N`\ th :math:`\operatorname{argmin}` of :math:`\sigma_{xx}`.
* :math:`1/B_N` versus :math:`N` is a straight line:
  
  .. math::
      2\pi \qty(\frac{F}{B_N} - \frac{1}{2} + \beta) = (2N - 1)\pi.
* :math:`\beta` obtained by extrapolation of :math:`1/B_N`\ -:math:`N` to :math:`1/B_N = 0`, which hits the :math:`N`-axis at :math:`N=\beta`.
* Dirac system confirmed if :math:`\beta = 1/2` by such extrapolation.

.. warning::
    :math:`\sigma_{xx} \ll \abs{\sigma_{xy}}` may not hold in experiment condition. It's more reliable to find minima based on :math:`\sigma_{xy}` instead of :math:`\rho_{xy}`.

More Information from SdH Oscillation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Carrier density: for 2D Dirac system,
  
  .. math::
      n_{\mathrm{s}} = \frac{1}{(2\pi)^2} \pi k_{\mathrm{F}}^2 = \frac{e}{2\pi \hbar c}F,
  where we have assumed cylindrical sections and therefore
  
  .. math::
      F = \frac{\hbar c}{2\pi e} \pi k_{\mathrm{F}}^2.
* Testing if SdH oscillation comes from 2D surface states:
  
  .. math::
      F \sim \frac{1}{\cos\theta}
  for 2D electron systems where :math:`\theta` is the angle between :math:`\vb{B}` and the normal vector to the electron system.
* Cyclotron frequency: with Lifshitz-Kosevich theory,
  
  .. math::
      \Delta \sigma_{xx} = A_0 R_{\mathrm{T}} R_{\mathrm{D}} R_{\mathrm{S}} \cos \qty[2\pi \qty(\frac{F}{B} - \frac{1}{2} + \beta)],
  where

  .. math::
      R_{\mathrm{T}} &= 2\pi^2 \frac{k_{\mathrm{B}} T / \hbar\omega_{\mathrm{c}}}{\sinh \qty[2\pi^2 (k_{\mathrm{B}} T / \hbar \omega_{\mathrm{c}} )]}, \\
      R_{\mathrm{D}} &= \exp [-2\pi^2 (k_{\mathrm{B}} T_{\mathrm{D}} / \hbar \omega_{\mathrm{c}})], \\
      R_{\mathrm{S}} &= \cos \qty(\frac{1}{2} \pi g m_{\mathrm{e}} / m_{\mathrm{c}}),
  :math:`g` is the :math:`g`\ -factor of electron, and :math:`T_{\mathrm{D}}` is the Dingle temperature given by

  .. math::
      T_{\mathrm{D}} = \frac{\hbar}{2\pi k_{\mathrm{B}} \tau}.
  
  * Obtain :math:`m_{\mathrm{c}}` with fixed :math:`B` and varying :math:`T`.
* Fermi velocity: with
  
  .. math::
      m_{\mathrm{c}} = \frac{\hbar^2}{2\pi} \qty(\pdv{A(E)}{E})_{E=E_{\mathrm{F}}}
  
  and (for 2D electron systems)

  .. math::
      A(E_{\mathrm{F}}) = \pi k_{\mathrm{F}}^2 = \frac{ \pi E_{\mathrm{F}}^2 }{ (\hbar v_{\mathrm{F}})^2 },

  we find

  .. math::
      m_{\mathrm{c}} = \frac{\hbar k_{\mathrm{F}}}{v_{\mathrm{F}}}.
* Relaxation time and mobility: :math:`T_{\mathrm{D}}` may be obtained by data fitting and hence :math:`\tau`. Electron mobility is given by
  
  .. math::
      \mu_{\mathrm{s}}^{\mathrm{SdH}} = \frac{e\tau}{m_{\mathrm{c}}} = \frac{e\ell^{\mathrm{SdH}}}{\hbar k_{\mathrm{F}}}

  where
  
  .. math::
      \ell^{\mathrm{SdH}} = v_{\mathrm{F}} \tau.

Example: Two-Band Model
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Taking bulk and surface conductivity into account, we find
  
  .. math::
      \rho_{yx} &= \frac{(R_{\mathrm{s}} \rho_{\mathrm{b}}^2 + R_{\mathrm{b}}\rho_{\mathrm{s}}^2)B + R_{\mathrm{s}} R_{\mathrm{s}} (R_{\mathrm{s}} + R_{\mathrm{b}})B^3}{(\rho_{\mathrm{s}} + \rho_{\mathrm{b}})^2 + (R_{\mathrm{s}} + R_{\mathrm{b}})^2 B^2}, \\
      \rho_{xx} &= \frac{\rho_{\mathrm{s}} \rho_{\mathrm{b}} (\rho_{\mathrm{s}} + \rho_{\mathrm{b}}) + (\rho_{\mathrm{s}} R_{\mathrm{b}}^2 + \rho_{\mathrm{b}} \rho_{\mathrm{s}}^2)B^2}{(\rho_{\mathrm{s}} + \rho_{\mathrm{b}})^2 + (R_{\mathrm{s}} + R_{\mathrm{b}})^2 B^2},
  where :math:`\rho_{\mathrm{b}}` and :math:`R_{\mathrm{b}}` are resistivity and Hall coefficient of the bulk, respectively, while :math:`\rho_{\mathrm{s}}` and :math:`R_{\mathrm{s}}` are those of the surface, where
  
  .. math::
      \rho_{\mathrm{s}} &= \rho_{\mathrm{2D}} t, \\
      R_{\mathrm{s}} &= \frac{t}{e n_{\mathrm{s}}},
  and :math:`t` is the thickness of the sample.
* Parameters :math:`n_{\mathrm{3D}}`, :math:`\rho_{\mathrm{b}}`, :math:`n_{\mathrm{s}}`, and :math:`\rho_{\mathrm{2D}}` may be obtained by fitting the data, hence electron mobility.
  
  * :math:`n_{\mathrm{s}}` may also be obtained from SdH data.
  * Additional constraint that the fitting be exact for :math:`\rho_{xx}(B=0)` be imposed to reduce DoF.

.. warning::
    :math:`\mu^{\mathrm{tr}}_{\mathrm{s}} > \mu^{\mathrm{SdH}}_{\mathrm{s}}` due to difference in scattering mechanisms.

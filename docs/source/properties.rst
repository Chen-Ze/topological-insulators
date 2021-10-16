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
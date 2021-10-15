Experimental Techniques
===================================

Quantum Oscillations
--------------------

Quantum oscillations describes a series of related experimental techniques used to map the Fermi surface of a metal in the presence of a strong magnetic field. [Coldea2010]_

Laudau Quantization
^^^^^^^^^^^^^^^^^^^^

Strong magnetic field
""""""""""""""""""""""

* Band structure as perturbation on Landau levels.
* Landau gauge:

  .. math::
      \vb{A} = (0, Bx, 0).
* Hamiltonian:

  .. math::
      H(p_x, p_y) &= \frac{1}{2m} \qty(\vb{p} - \frac{e}{c} \vb{A})^2 \\
      &= \frac{1}{2m}\qty[p_x^2 + \qty(p_y - \frac{e}{c} Bx)^2]. \\
      H(p_x, \hbar k_y) &= \frac{1}{2m} p_x^2 + \frac{m\omega_c^2}{2}(x-X)^2.
  where

  .. math::
      p_y &= \hbar k_y, \\
      \omega_c &= \frac{eB}{mc}, \\
      l_B &= \sqrt{\frac{\hbar c}{eB}}, \\
      X &= \frac{\hbar c k_y}{eB} = l_B^2 k_y.
* Solution:

  .. math::
      \psi_{k_y, n}(x, y) = \frac{1}{\sqrt{L_y}} e^{ik_y y} \phi_{k_y, n}(x)
  where

  .. math::
      \phi_{k_y, n}(x) \propto e^{-\frac{1}{2} (x/l_B)^2} H_n\qty(\frac{x - X}{l_B}).
* Energy levels:

  .. math::
      E_n = \hbar \omega_c\qty(n+\frac{1}{2}).
* Degeneracy: number of states at each level,
  
  .. math::
      m_{\mathrm{max}} = \frac{L_x L_y}{2\pi l_B^2}.

  .. note::
      Stronger the magnetic field, higher the degree of degeneracy.
* Filling factor:

  .. math::
      \nu = \frac{N_{\mathrm{e}}}{m_{\mathrm{max}}} = 2\pi l_B^2 \frac{N_{\mathrm{e}}}{L_x L_y}.


Weak magnetic field
""""""""""""""""""""""

Magnetic field as perturbation on band structure.

:math:`k_y` still a good quantum number.


Observation of Quantum Oscillation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Classical Theory of Electron Motion
""""""""""""""""""""""""""""""""""""""""

* :math:`\vb{k}` runs along the constant-energy surface, rotating around :math:`\vb{B}`.
* With :math:`\vb{r}_\perp` denoting the component of :math:`\vb{r}` perpendicular to :math:`\vb{B}`, we have

  .. math::
      \vb{r}_\perp(t) - \vb{r}_\perp(0) = -\frac{\hbar c}{eB} \hat{\vb{B}} \times \qty[\vb{k}(t) - \vb{k}(0)].
  .. note::
      The orbit in the :math:`\vb{r}` space is given by the orbit in the :math:`\vb{k}` space rotated by :math:`\pi/2` and scaled by :math:`\dfrac{\hbar c}{eB}`.
* Period:

  .. math::
      T = \frac{\hbar^2 c}{eB} \pdv{A(E,k_z)}{E} = \frac{2\pi m_{\mathrm{c}} c}{eB}.
  * :math:`A` is the area encicled by the orbit.
  * Cyclotron mass:

    .. math::
        m_{\mathrm{c}} = \frac{\hbar^2}{2\pi} \pdv{A(E,k_z)}{E}.
* With Bohr's correspondence principle, we find that the Landau levels for large :math:`\nu`'s are given by the Onsager's semiclassical quantization condition
  
  .. math::
      A(E_\nu, k_z) = \qty(\nu + \frac{1}{2} - \beta) \frac{2\pi eB}{\hbar c},
  where :math:`\beta = 0` for free electrons.
* Maximal number of states thereon when the outest Landau tube is tangent to the Fermi surface. At two consecutive extrema, one has
  
  .. math::
      A(E_{\mathrm{F}}) &= A(E_{\nu}, k^0_z) = \qty(\nu + \frac{1}{2} - \beta) \frac{2\pi e B_\nu}{\hbar c}, \\
      A(E_{\mathrm{F}}) &= A(E_{\nu - 1}, k^0_z) = \qty(\nu - 1 + \frac{1}{2} - \beta) \frac{2\pi e B_{\nu - 1}}{\hbar c},
  respectively, where :math:`A(E_{\mathrm{F}})` denotes the area encircled by an extremal orbit. Therefore, such exterma occurs periodically with

  .. math::
      \Delta \qty(\frac{1}{B}) = \frac{2\pi e}{\hbar c A(E_{\mathrm{F}})}.

.. note::
    We may therefore obtain the area encircled by the extremal orbits of the Fermi surface from the observed :math:`\Delta \qty(1/B)`.
  

Phenomena
""""""""""""

* De Haas-van Alphen oscillation: :math:`\chi` versus :math:`1/B`.
* Shubnikov-de Haas oscillation: resistivity versus :math:`1/B`.

.. warning::
    As :math:`T` goes up, the Fermi surface is Blurred by :math:`O(k_{\mathrm{B}}T)` which may exceed :math:`\Delta E`, which may therefore suppress quantum oscillation.

ARPES
--------

Measuring the *energy* and *direction* of an electron when the surface is hit by a monochrome beam, whence we may obtain :math:`E_n(\vb{k})`.

Conservation Laws
^^^^^^^^^^^^^^^^^^^^

Conservation of Energy
""""""""""""""""""""""""

.. math::
    h\nu = E_{\mathrm{B}} + \phi + E_{\mathrm{kin}}.

where

.. math::
    E_{\mathrm{kin}} = \frac{\hbar^2 k_{\mathrm{f}}^2}{2m}.

Conservation of Momentum
""""""""""""""""""""""""""""

.. math::
    (\vb{k}_{\mathrm{i}} + \vb{G})_\parallel = \vb{k}_{\mathrm{f}\parallel}.


Analyzing ARPES Data
^^^^^^^^^^^^^^^^^^^^^^^^

* Work function :math:`\phi` is already known.
* :math:`\vb{k}_{\mathrm{f}}` of the escaping electron is measured.
* :math:`\vb{k}_{\mathrm{i}\parallel}` is determined by moving :math:`\vb{k}_{\mathrm{f}}` to the first BZ.
* Assuming 2D materials, we have

  .. math::
      E_{\mathrm{i}}(\vb{k}_{\mathrm{i}\parallel}) = \frac{\hbar^2 k_{\mathrm{f}}^2}{2m} + \phi - h\nu.
* Assuming 3D materials, we have

  .. math::
      E_{\mathrm{i}}(\vb{k}_{\mathrm{i}\parallel}, k_{\mathrm{i}\perp}) = \frac{\hbar^2 k_{\mathrm{f}\parallel}^2}{2m} + \frac{\hbar^2 k_{\mathrm{f}\perp}^2}{2m} + \phi - h\nu.

  * :math:`k_{\mathrm{i}\perp}` is unknown.
  * Ansatz

    .. math::
        E_{\mathrm{i}}(\vb{k}_{\mathrm{i}}) + h\nu = \frac{\hbar^2 (\vb{k}_{\mathrm{i}} + \vb{G})^2}{2m} + V_0 = \frac{\hbar^2 k_{\mathrm{f}}^2}{2m} + \phi.
* Telling apart 2D bands and 3D bands, i.e. bulk states and surface states.

.. note::
    The energies are relative to :math:`E_{\mathrm{F}}`, i.e. :math:`E_{\mathrm{F}} = 0`.

Sensitivity to Surface Condition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

ARPES probes only 1nm into the surface. Ultra-high vacuum and clear cleavage are necessary. 

Determination of Topological Insulators
------------------------------------------

Determination of 2D Topological Insulators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Edge states confirmed by quantization of conductivity.
  
  * Confirmed also partially by edge charge density with STM.
* Chiral spin-polarization confirmed by spin current.

Determination of 3D Topological Insulators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Confirmed by existence of Dirac cone on surface with ARPES.
* Surface states also confirmed by SdH oscillation.
* Dirac carriers confirmed by phase shift of :math:`\pi` in oscillation due to Berry phase.
* Dirac carriers also confirmed by STS.
  
  * Laudau levels for a Dirac cone takes the form :math:`\sqrt{BN}` where :math:`N=0` fixes the Dirac point.
  * The pattern may be tested by measuring local charge density versus bias voltage.
  * May also be confirmed by magneto-optical spectroscopy.

.. warning::
    Since charge accumulation may occur at surface and may create a conductive layer, the dependence of resistivity versus sample size does not confirm the existence of topological surface states.

Glossary
----------

.. glossary::
    ARPES/角度分解電子分光/角分辨光电子能谱
        Angle-resolved photoemission spectroscopy
.. glossary::
    Work Function/仕事関数/功函数
        The minimum amount of energy required to remove an electron from the crystal.
.. glossary::
    STS/走査型トンネル分光法/扫描隧道光谱
        Scanning tunneling spectroscopy.


References
-------------

.. [Coldea2010] `Quantum oscillations probe the normal electronic states of novel superconductors <https://royalsocietypublishing.org/doi/abs/10.1098/rsta.2010.0089>`_



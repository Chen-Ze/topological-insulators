Visualizing the Fermi Surface
===================================

Quantum Oscillations
--------------------

Quantum oscillations describes a series of related experimental techniques used to map the Fermi surface of a metal in the presence of a strong magnetic field. [Coldea2010]_

Laudau Quantization
^^^^^^^^^^^^^^^^^^^^

Strong magnetic field
""""""""""""""""""""""

Band structure as perturbation on Landau levels.

Landau gauge:

.. math::
    \vb{A} = (0, Bx, 0).


Hamiltonian:

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

Solution:

.. math::
    \psi_{k_y, n}(x, y) = \frac{1}{\sqrt{L_y}} e^{ik_y y} \phi_{k_y, n}(x)

where

.. math::
    \phi_{k_y, n}(x) \propto e^{-\frac{1}{2} (x/l_B)^2} H_n\qty(\frac{x - X}{l_B}).

Energy levels:

.. math::
    E_n = \hbar \omega_c\qty(n+\frac{1}{2}).

Degeneracy: number of states at each level:

.. math::
    m_{\mathrm{max}} = \frac{L_x L_y}{2\pi l_B^2}.

.. note::
    Stronger the magnetic field, higher the degree of degeneracy.

Filling factor:

.. math::
    \nu = \frac{N_{\mathrm{e}}}{m_{\mathrm{max}}} = 2\pi l_B^2 \frac{N_{\mathrm{e}}}{L_x L_y}.


Weak magnetic field
""""""""""""""""""""""

Magnetic field as perturbation on band structure.

:math:`k_y` still a good quantum number.


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


Glossary
----------

.. glossary::
    ARPES/角度分解電子分光/角分辨光电子能谱
        Angle-resolved photoemission spectroscopy
.. glossary::
    Work Function/仕事関数/功函数
        The minimum amount of energy required to remove an electron from the crystal.


References
-------------

.. [Coldea2010] `Quantum oscillations probe the normal electronic states of novel superconductors <https://royalsocietypublishing.org/doi/abs/10.1098/rsta.2010.0089>`_



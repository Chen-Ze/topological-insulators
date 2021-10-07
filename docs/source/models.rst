Models
=========

Index of Models (Diagonalizable)
-----------------------------------

.. list-table:: Index of Models
   :header-rows: 1

   * - Name
     - Applications
     - Dimension
     - TRS
     - Examples
   * - Rice-Mele Model [Rice1982]_
     - `Thouless Charge Pump </thouless-pump>`_
     - 1+1
     - Spinless
     - N/A
   * - Rice-Mele Model With Spin [Fu2006]_
     - `Fu-Kane Spin Pump </fu-kane-pump>`_
     - 1+1
     - Partial
     - N/A
   * - Su-Schrieffer-Heeger Model [Su1979]_
     - 1D TI
     - 1
     - Spinless
     - Polyacetylene
   * - Haldane Model [Haldane1988]_
     - QAHE
     - 2
     - Broken
     - Not yet found [Yu2010]_

Index of Models (Strongly Correlated)
---------------------------------------

.. list-table:: Index of Models
   :header-rows: 1

   * - Name
     - Applications
     - Dimension
     - TRS
     - Examples
   * - Hubbard Model
     - Mott Insulator
     - Any
     - Preserved
     - Too many

Thouless Charge Pump (Rice-Mele Model)
----------------------------------------

.. image:: https://badgen.net/badge/TRS/spinless/grey
.. image:: https://badgen.net/badge/Dimension/1+1D/purple

* Hamiltonian:

  .. math::
      H = h_{st}(t) \sum_i (-1)^i c^\dagger_i c_i + \frac{1}{2} \sum_{i} \qty[t_0 + (-1)^i \delta(t)] c^\dagger_i c_{i+1} + \mathrm{h.c.}.

  where

  .. math::
      \delta(t) &= \delta_0 \cos \frac{2\pi t}{T}, \\
      h_{st}(t) &= h_0 \sin \frac{2\pi t}{T}.
* Bulk Hamiltonian:

  .. math::
      H = \sum_{k} \begin{pmatrix}a^\dagger_{k} & b^\dagger_{k} \end{pmatrix} \vb{d}\cdot \vb{\sigma} \begin{pmatrix}a_{k} \\ b_{k} \end{pmatrix},
  where
  
  .. math::
      d_{x} &= \frac{1}{2} \qty({t_0 + \delta(t)}) + \frac{1}{2}\qty({t_0 - \delta(t)}) \cos k, \\
      d_{y} &= -\frac{1}{2} \qty({t_0 - \delta(t)}) \sin k, \\
      d_{z} &= h_{st}(t).

  * Dispersion:
    
    .. math::
        E_{\pm} = \pm \abs{\vb{d}}.

Fu-Kane Spin Pump (Rice-Mele Model With Spin)
----------------------------------------------

.. image:: https://badgen.net/badge/TRS/partial/yellow
.. image:: https://badgen.net/badge/Dimension/1+1D/purple

* Hamiltonian:

  .. math::
      H = h_{st}(t) \sum_{i,\sigma} (-1)^i c^\dagger_{i,\sigma} \sigma^z_{\sigma\sigma'} c_{i,\sigma'} + \frac{1}{2} \sum_{i,\sigma} \qty[t_0 + (-1)^i \delta(t)] c^\dagger_{i,\sigma} c_{i+1,\sigma} + \mathrm{h.c.},

  where

  .. math::
      \delta(t) &= \delta_0 \cos \frac{2\pi t}{T}, \\
      h_{st}(t) &= h_0 \sin \frac{2\pi t}{T}.
* Bulk Hamiltonian:

  .. math::
      H = \sum_{k} \begin{pmatrix}\psi^\dagger_{k,\uparrow} & \psi^\dagger_{k,\downarrow} \end{pmatrix} \begin{pmatrix} \vb{d}_+ \cdot \vb{\sigma} & 0 \\ 0 & \vb{d}_- \cdot \vb{\sigma} \end{pmatrix} \begin{pmatrix}\psi_{k,\uparrow} \\ \psi_{k,\downarrow} \end{pmatrix},
  where
  
  .. math::
      \phi^\dagger_{k,\uparrow} &= \begin{pmatrix} a^\dagger_{k,\uparrow} & b^\dagger_{k,\uparrow} \end{pmatrix}, \\
      \phi^\dagger_{k,\downarrow} &= \begin{pmatrix} a^\dagger_{k,\downarrow} & b^\dagger_{k,\downarrow} \end{pmatrix}, \\
      d_{\pm, x} &= \frac{1}{2} \qty({t_0 + \delta(t)}) + \frac{1}{2}\qty({t_0 - \delta(t)}) \cos k, \\
      d_{\pm, y} &= -\frac{1}{2} \qty({t_0 - \delta(t)}) \sin k, \\
      d_{\pm, z} &= \pm h_{st}(t).

  * Dispersion:
    
    .. math::
        E_{\pm,\uparrow/\downarrow} = \pm \abs{\vb{d}}.
* Degeneracy:

  * Kramers degeneracy: TRS is broken by the on-site term. Kramers degeneracy occurs only at :math:`t=0` and :math:`t=T/2`.
  * Now comes the most interesting point: for the four states nearest to the Fermi level (two above and two below), we have the following.

    * At :math:`t=0`, the first Kramers pair is between the occupied spin-up and spin-down state in the bluk, the second is between the unoccupied pair.
    * At :math:`0<t<T/2`, we have no Kramers pair since the TRS is broken.

      .. caution::
          We still have two-fold degeneracy here because of the inversion symmetry.
    * At :math:`t=T/2`, we have a four-fold degeneracy.
      
      * The first Kramers pair is between the occupied spin-up and unoccupied spin-down state on the left end, the second is between the pair on the right end.
  * The degeneracies are between two different group of bands. Therefore, the bands are guaranteed to cross.

Su-Schrieffer-Heeger Model
----------------------------------------

.. image:: https://badgen.net/badge/TRS/spinless/grey
.. image:: https://badgen.net/badge/Dimension/1D/pink

* Hamiltonian:

  .. math::
      H = \sum_{n=1}^N (t+\delta t) c_{A,n}^\dagger c_{B,n} + \mathrm{h.c.} + \sum_{n=1}^{N-1} c_{A,n+1}^\dagger c_{B,n} + \mathrm{h.c.}.
* Bulk Hamiltonian:

  .. math::
      H = \sum_{k} \psi^\dagger_k \qty(d_x \sigma_x + d_z \sigma_z) \psi_k,
  where
  
  .. math::
      d_x &= -(t - \delta t), \\
      d_z &= 2 \delta t + 2(t - \delta t) \sin^2 \frac{k}{2}, \\
      \psi_k &= \begin{pmatrix} a_k \\ b_k \end{pmatrix}.

  * Dispersion:
    
    .. math::
        E_\pm = \pm\sqrt{d_x^2 + d_z^2}.

Miscellaneous
---------------

A few models that are not mentioned above.

* The QWZ (Qi-Wu-Zhang) model. See `二维陈绝缘体(2D Chern Insulator)：Qi-Wu-Zhang（QWZ）模型 <https://zhuanlan.zhihu.com/p/55005395>`_.

References
-------------

.. [Yu2010] `Quantized Anomalous Hall Effect in Magnetic Topological Insulators <https://arxiv.org/abs/1002.0946>`_
.. [Haldane1988] `Model for a Quantum Hall Effect without Landau Levels: Condensed-Matter Realization of the "Parity Anomaly" <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.61.2015>`_
.. [Rice1982] `Elementary Excitations of a Linearly Conjugated Diatomic Polymer <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.49.1455>`_
.. [Fu2006] `Time reversal polarization and a Z2 adiabatic spin pump <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.74.195312>`_
.. [Su1979] `Solitons in Polyacetylene <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.42.1698>`_
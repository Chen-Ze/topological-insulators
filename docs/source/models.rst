Models
=========

.. rst-class:: text-muted central-inversion

    この軽音部には問題がある！

Index of Models (Diagonalizable)
-----------------------------------

.. list-table:: Index of Models
   :header-rows: 1

   * - Name
     - Applications
     - Dimension
     - TRS
     - Parity
     - Examples
   * - Rice-Mele Model [Rice1982]_
     - `Thouless Charge Pump <./thouless-pump.html>`_
     - 1+1
     - Spinless
     - N/A
     - N/A
   * - Rice-Mele Model With Spin [Fu2006]_
     - `Fu-Kane Spin Pump <./fu-kane-pump.html>`_
     - 1+1
     - Partial
     - N/A
     - N/A
   * - Su-Schrieffer-Heeger Model [Su1979]_
     - `1D TI <./1d-topological-insulator.html>`_
     - 1
     - Spinless
     - N/A
     - Polyacetylene
   * - Haldane Model [Haldane1988]_
     - QAHE
     - 2
     - Broken
     - N/A
     - Not yet found [Yu2010]_
   * - Kane-Mele Model [Kane2005]_
     - `2D TI (QSHE) <./2d-topological-insulator.html>`_
     - 2
     - Preserved
     - N/A
     - Too small in Graphene
   * - BHZ Model [Bernevig2006]_
     - 2D TI
     - 2
     - Preserved
     - Preserved
     - HgTe Quantum Well [König2007]_

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
      H = \sum_{k} \begin{pmatrix}a^\dagger_{k} & b^\dagger_{k} \end{pmatrix} \vb{d}\cdot \vb*{\sigma} \begin{pmatrix}a_{k} \\ b_{k} \end{pmatrix},
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
      H = \sum_{k} \begin{pmatrix}\psi^\dagger_{k,\uparrow} & \psi^\dagger_{k,\downarrow} \end{pmatrix} \begin{pmatrix} \vb{d}_+ \cdot \vb*{\sigma} & 0 \\ 0 & \vb{d}_- \cdot \vb*{\sigma} \end{pmatrix} \begin{pmatrix}\psi_{k,\uparrow} \\ \psi_{k,\downarrow} \end{pmatrix},
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

QAHE (Haldane Model)
--------------------------

.. image:: https://badgen.net/badge/TRS/broken/red
.. image:: https://badgen.net/badge/Dimension/2D/orange

.. hint::
    Yet to be done.

QSHE (Kane-Mele Model)
--------------------------

.. image:: https://badgen.net/badge/TRS/preserved/green
.. image:: https://badgen.net/badge/Dimension/2D/orange

.. hint::
    Yet to be done.

* Boundary could be zig-zag, armchair -- you name it.

  .. rst-class:: block-center max-w100

      .. image:: https://www.nanowerk.com/nanotechnology-news/id42950_1.jpg

  .. rst-class:: text-center

      From `Graphene nanoribbons: it's all about the edges <https://www.nanowerk.com/nanotechnology-news/newsid=42950.php>`_
* See `Kane-Mele Model <https://chaoli.club/index.php/4485/0>`_ for bulk band structure.

Bernevig-Hughes-Zhang Model
--------------------------------

.. image:: https://badgen.net/badge/TRS/preserved/green
.. image:: https://badgen.net/badge/P/preserved/green
.. image:: https://badgen.net/badge/Dimension/2D/orange

.. rst-class:: text-muted

  Got the trick of calculating :math:`\mathbb{Z}_2` index? Let hunt down a real beast!

* Normal: p orbital below s orbital.
* Inverted: p orbital above s orbital due to spin-orbit interaction around :math:`\vb{k}=0`. This occurs when the :math:`\ce{HgTe}` sample is thick enough.
* The four orbitals comes into play:

  .. math::
      \ket{s,\uparrow},\quad \ket{s,\downarrow},\quad \ket{p_x + ip_y,\uparrow},\quad \ket{p_x - ip_y,\downarrow}.
* Hamiltonian:
  
  .. math::
      H &= \sum_i \sum_{\alpha=s,p} \sum_{\sigma=\pm} \epsilon_\alpha c^\dagger_{i,\alpha,\sigma} c_{i,\alpha,\sigma} \\
      &\phantom{{}={}} -\sum_i \sum_{\alpha=s,p} \sum_{\mu=\pm x,\pm y} \sum_{\sigma=\pm} t^{\alpha\beta}_{\mu\sigma} c^\dagger_{i+\mu, \alpha, \sigma} c_{i,\beta,\sigma},
  where
  
  .. math::
      t_{\mu \sigma} = \begin{pmatrix} t_{ss} & t_{sp} e^{i\sigma \theta_\mu} \\ t_{sp} e^{-i\sigma \theta_\mu} & -t_{pp} \end{pmatrix},
  and :math:`\theta_\mu` is the angle between :math:`\mu`-direction and :math:`x`-axis, taking values :math:`0`, :math:`\pi/2`, :math:`\pi`, :math:`3\pi/2`.
* Bulk Hamiltonian:
  
  .. math::
      H &= \sum_{\vb{k}} c^\dagger_{\vb{k}} \qty(\frac{\epsilon_s + \epsilon_p}{2} \mathbb{1}\otimes \mathbb{1} + \frac{\epsilon_s - \epsilon_p}{2}\sigma_z \otimes \mathbb{1}) c_{\vb{k}} \\
      &\phantom{{}={}} - \sum_{\vb{k}} c^\dagger_{\vb{k}} \qty[ (t_{ss} - t_{pp}) \sum_\mu (\cos \vb{k} \cdot \vb{a}_\mu) \mathbb{1}\otimes \mathbb{1} + (t_{ss} + t_{pp}) \sum_\mu (\cos \vb{k}\cdot \vb{a}_\mu) \sigma_z \otimes \mathbb{1} + (2 t_{sp} \sin \vb{k} \cdot \vb{a}_1) \sigma_y \otimes \mathbb{1} + (2t_{sp} \sin \vb{k} \cdot \vb{a}_2) \sigma_x \otimes s_z ] c_{\vb{k}},
  where :math:`\vb{a}_1 = \hat{\vb{x}}` and :math:`\vb{a}_2 = \hat{\vb{y}}`, and

  .. math::
      c^\dagger_{\vb{k}} = \begin{pmatrix} c^\dagger_{\vb{k}, s\uparrow} & c^\dagger_{\vb{k}, s\downarrow} & c^\dagger_{\vb{k}, p\uparrow} & c^\dagger_{\vb{k}, p\downarrow} \end{pmatrix}.
  
  Both :math:`\sigma_i` and :math:`s_i` denote Pauli matrices.

  * Simplification: with
    
    .. math::
        \Gamma^1 &= \sigma_x \otimes s_x, \\
        \Gamma^2 &= \sigma_x \otimes \sigma_y, \\
        \Gamma^3 &= \sigma_x \otimes \sigma_z, \\
        \Gamma^4 &= \sigma_y \otimes \mathbb{1}, \\
        \Gamma^5 &= \sigma_z \otimes \mathbb{1},
    we rewrite the Hamiltonian as

    .. math::
        H(\vb{k}) = d_0(\vb{k}) \mathbb{1} + \sum_{a=1}^5 d_a(\vb{k}) \Gamma^a,
    where
    
    .. math::
        d_0(\vb{k}) &= \frac{\epsilon_s + \epsilon_p}{2} - (t_{ss} - t_{pp}) (\cos \vb{k} \cdot \vb{a}_1 + \cos \vb{k} \cdot \vb{a}_2), \\
        d_1(\vb{k}) &= 0, \\
        d_2(\vb{k}) &= 0, \\
        d_3(\vb{k}) &= 2t_{sp} \sin \vb{k} \cdot \vb{a}_2, \\
        d_4(\vb{k}) &= 2t_{sp} \sin \vb{k} \cdot \vb{a}_1, \\
        d_5(\vb{k}) &= \frac{\epsilon_s - \epsilon_p}{2} - (t_{ss} + t_{pp}) (\cos \vb{k} \cdot \vb{a}_1 + \cos\vb{k}\cdot \vb{a}_2).
    
  * Dispersion:
    
    .. math::
        E(\vb{k}) = d_0(\vb{k}) \pm \sqrt{\sum_{a=1}^5 d_a(\vb{k})^2}.
* Parity operator: since :math:`s`-orbital has parity :math:`+1` and :math:`p` orbital has parity :math:`-1`,
    
  .. math::
      \Pi = \sigma_z \otimes \mathbb{1} = \Gamma^5.
* Time-reversal and parity:
    
  .. math::
      \Theta \Gamma^a \Theta^{-1} &= \begin{cases} -\Gamma^a, & a = 1,2,3,4, \\ +\Gamma^a, & a = 5. \end{cases} \\
      \Pi \Gamma^a \Pi^{-1} &= \begin{cases} -\Gamma^a, & a = 1,2,3,4, \\ +\Gamma^a, & a = 5. \end{cases}
* At TRIMs:
  
  .. math::
      H(\vb{k} = \Lambda_i) = d_0(\Lambda_i) \mathbb{1} + d_5(\Lambda_i) \Gamma^5.
  
  * The two :math:`s`-orbitals are generated, as well the the two :math:`p`-orbitals: with :math:`\ket{\pm}` denoting parities,
    
    .. math::
        H(\Lambda_i) \ket{+} &= \qty[d_0(\Lambda_i) + d_5(\Lambda_i)] \ket{+}, \\
        H(\Lambda_i) \ket{-} &= \qty[d_0(\Lambda_i) - d_5(\Lambda_i)] \ket{-}.
* Band inversion: considering half-filled case,
  
  * If :math:`d_5(\Lambda_i) < 0`, the :math:`-1` parity is filled, and therefore :math:`\delta(\Lambda_i) = -1`.
  * If :math:`d_5(\Lambda_i) > 0`, the :math:`+1` parity is filled, and therefore :math:`\delta(\Lambda_i) = +1`.
  * Parity:
    
    .. math::
        \delta(\Lambda(n_1, n_2)) = -\operatorname{sign}\qty[\frac{\epsilon_s - \epsilon_p}{2} - (t_{ss} + t_{pp}) \qty{ (-1)^{n_1} + (-1)^{n_2} }].
  
  .. note::
      The Hamiltonian is diagonal in the basis we choose only at TRIMs. As we slowing moving from one TRIM to another, the eigenstates are a mixture of both parities in the middle. After we arrive at the ending TRIM, we may surprisingly find that the parity is different from where we begin.
* :math:`\mathbb{Z}_2` index:
    
  * If :math:`\epsilon_s - \epsilon_p > 4(t_{ss} + t_{pp})`, :math:`\delta < 0` for all :math:`\Lambda_i` and therefore the system is topologically trivial.
  * If :math:`0 < \epsilon_s - \epsilon_p < 4(t_{ss} + t_{pp})`, :math:`\delta < 0` for all :math:`\Lambda_i` but :math:`\Lambda(0,0)`, and therefore :math:`\nu = 1`.

Miscellaneous
---------------

A few models that are not mentioned above.

* The QWZ (Qi-Wu-Zhang) model. See `二维陈绝缘体(2D Chern Insulator)：Qi-Wu-Zhang（QWZ）模型 <https://zhuanlan.zhihu.com/p/55005395>`_.

See `能带推导复习 - 泰勒猫爱丽丝的文章 - 知乎 <https://zhuanlan.zhihu.com/p/359578693>`_ for calculation procedures.

References
-------------

.. [Yu2010] `Quantized Anomalous Hall Effect in Magnetic Topological Insulators <https://arxiv.org/abs/1002.0946>`_
.. [Haldane1988] `Model for a Quantum Hall Effect without Landau Levels: Condensed-Matter Realization of the "Parity Anomaly" <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.61.2015>`_
.. [Rice1982] `Elementary Excitations of a Linearly Conjugated Diatomic Polymer <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.49.1455>`_
.. [Fu2006] `Time reversal polarization and a Z2 adiabatic spin pump <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.74.195312>`_
.. [Su1979] `Solitons in Polyacetylene <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.42.1698>`_
.. [Bernevig2006] `Quantum Spin Hall Effect and Topological Phase Transition in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1133734>`_
.. [König2007] `Quantum Spin Hall Insulator State in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1148047>`_
.. [Kane2005] `Quantum Spin Hall Effect in Graphene <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.95.226801>`_
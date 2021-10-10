Basic Theory of Topological Insulators
==========================================

.. role:: text-muted

.. rst-class:: text-right text-muted

    とあるトポロジカルインデックス

Berry Phase
----------------

* For :math:`H` depending on parameters :math:`\vb{R}(t)`, the Schrödinger equation becomes

  .. math::
      H[\vb{R}(t)]\ket{n,\vb{R}(t)} = E_n[\vb{R}(t)]\ket{n,\vb{R}(t)}.
* Time evolution of ket as :math:`\vb{R}(t)` varies with time.

  .. math::
      \ket{n,t} = \exp\qty(i \gamma_n) \times \exp\qty({-\frac{i}{\hbar} \int \dd{t'} E_n[\vb{R}(t')]}) \ket{n,\vb{R}(t)}.
  * The first :math:`\exp` factor is known as the Berry phase term.
  * The second :math:`\exp` factor is known as the dynamical term.
  .. note::
      Berry phase is the nontrivial phase factor caused by the time-dependence of Hamiltonian.
* Berry phase for closed loop:

  .. math::
      \gamma_n[C] &= i \oint_C \dd{\vb{R}} \cdot \bra{n,\vb{R}} \nabla_{\vb{R}} \ket{n,\vb{R}} \\
      &= -\oint_C \dd{\vb{R}}\cdot \vb{A}_n(\vb{R}) \\
      &= -\int_S \dd{\vb{S}} \cdot \vb{B}_n(\vb{R}).
  * Berry connection:
    
    .. math::
        \vb{A}_n(\vb{R}) = -i \bra{n,\vb{R}} \nabla_{\vb{R}} \ket{n,\vb{R}}.
  * Berry curvature:

    .. math::
        \vb{B}_n(\vb{R}) = \nabla_{\vb{R}} \times \vb{A}_n(\vb{R}).

QHE: Chern Number and Conductivity
--------

.. image:: https://badgen.net/badge/TRS/broken/red
.. image:: https://badgen.net/badge/Dimension/2D/purple

.. raw:: html

    <video style="width: 100%; max-width: 360px;" class="block-center" controls>
        <source src="https://zchen.xyz/QuantumHallEffectExplanationWithLandauLevels.ogv" type="video/ogg">
        Your browser does not support the video tag.
    </video>

.. rst-class:: text-center

    From `Wikipedia: Quantum Hall Effect <https://en.wikipedia.org/wiki/Quantum_Hall_effect#Integer_quantum_Hall_effect>`_

Weak Magnetic Field
^^^^^^^^^^^^^^^^^^^^^^^

* If the magnetic field is weak, we have the classical result
  
  .. math::
      \rho_{xx} &\sim \mathrm{const}. \\
      \rho_{xy} &\propto B.

Strong Magnetic Field
^^^^^^^^^^^^^^^^^^^^^^^^^^

* For strong magnetic field, :math:`\rho_{xy}` becomes significant and both :math:`\sigma_{xx}` and :math:`\rho_{xx}` `tend to zero <https://en.wikipedia.org/wiki/Quantum_Hall_effect#Longitudinal_resistivity>`_.

  .. warning::
      :math:`\sigma_{xx} \neq 1/\rho_{xx}` in such case. Instead, one has :math:`\sigma_{xx} \propto \rho_{xx}`.

Hall Conductance: TKNN Derivation
""""""""""""""""""""""""""""""""""

* Set-up: magnetic field along :math:`z`-axis while electric field along :math:`y`.
* Perturbation to the first order:

  .. math::
      \ket{n}_E = \ket{n} + \sum_{m \neq n} \frac{\bra{m} (-eEy) \ket{n}}{E_n - E_m} \ket{m} + \cdots.
* Transversal current:

  .. math::
      \langle j_x \rangle_E = \sum_n f(E_n) \bra{n}_E \qty(\frac{e v_x}{L^2}) \ket{n}_E.
* Hall conductance:

  .. math::
      \sigma_{xy} &= \frac{\langle j_x \rangle_E}{E} \\
      &= \nu \frac{e^2}{h}.
  * We have used

    .. math::
        \bra{u_{m \vb{k}'}} v_\mu \ket{u_{n\vb{k}}} = \frac{1}{\hbar} (E_{n\vb{k}} - E_{m\vb{k}'}) \bra{u_{m \vb{k}'}} \pdv{}{k_\mu} \ket{u_{n\vb{k}}}
    to simplify the above expression.
  * The TKNN number is given by

    .. math::
        \nu &= \sum_n \int_{\mathrm{BZ}} \frac{\dd{^2 \vb{k}}}{2\pi} \qty(\pdv{A_{n,y}}{k_x} - \pdv{A_{n,x}}{k_y}) \\
        &= -\frac{1}{2\pi} \gamma_n[\partial \mathrm{BZ}],
    i.e. the winding number of Berry phase along the boundary of BZ.
  * :math:`\nu \in \mathbb{Z}`.

.. note::
    TKNN number may be also called Chern number.

Hall Conductance: Kubo Derivation
""""""""""""""""""""""""""""""""""""""

.. hint::
    Under construction.

Hall Conductance: Laughlin Argument
""""""""""""""""""""""""""""""""""""""

See `Laughlin 规范实验 - 泰勒猫爱丽丝的文章 - 知乎 <https://zhuanlan.zhihu.com/p/370033031>`_.

The following is the simplified version [Shen2012]_.

* Two-dimensional electron gas rolled as a cylinder along the :math:`y`-direction, i.e. :math:`y` now becomes :math:`S^1`.
* A magnetic flux :math:`\phi` now threads through the :math:`x`-direction.
* Charge transport as magnetic flux increases:

  .. math::
      \Delta Q = \sigma_{xy} \Delta \Phi.
* Quantization of magnetic flux:

  .. math::
      \Delta \Phi = \frac{h}{e}.
* Gauge invariance: kets returns to their original states as magnetic flux is increased by a magnetic flux quantum. Therefore, a integer number of charge is transported.

  .. math::
      \sigma_{xy} = \frac{n e^2}{h}.

Hall Conductance: Wilson Loop Derivation
""""""""""""""""""""""""""""""""""""""""""

See `霍尔电导率 via Wilson Loop - PhakeNews的文章 - 知乎 <https://zhuanlan.zhihu.com/p/34715681>`_.

.. hint::
    Under construction.

Example: A Two-Band Model
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Brillouin zone: :math:`\vb{k} \in T^2`.
* Parameter space: :math:`\vb{h} \in \mathbb{R}^3`. We assume that :math:`\vb{h}(\vb{k}) \neq 0` so that we have a two-band insulator.

  * :math:`\vb{h}(\vb{k})` sweeps a closed surface in :math:`\mathbb{R}^3`.
  * Magnetic monopole analogy: we are going to calculate the magnetic flux through this closed surface.
  * We may forget everything about :math:`\vb{k}` now and take :math:`\vb{h}` as :math:`\vb{R}` in the above derivation of Berry phase.
* Hamiltonian: magnetic dipole,

  .. math::
      H(\vb{k}) = \vb{h}(\vb{k}) \cdot \vb{\sigma}.
* Ket space: :math:`\ket{u} \in \mathbb{C}^2`. More specifically, :math:`S^2`.
* Dispersion relation:

  .. math::
      \epsilon_{\pm}(\vb{k}) = \pm h(\vb{k}) = \pm \abs{\vb{h}(\vb{k})}.
* Ket solution: assuming filling only the lower band,

  * For :math:`\vb{h}` lying on the southern hemisphere,

    .. math::
        \ket{u_-^{\mathrm{S}}[\vb{h}(\vb{k})]} = \begin{pmatrix} \sin \frac{\theta}{2} \\ -e^{i\phi} \cos \frac{\theta}{2} \end{pmatrix}.
  * For :math:`\vb{h}` lying on the northern hemisphere,

    .. math::
        \ket{u_-^{\mathrm{S}}[\vb{h}(\vb{k})]} = \begin{pmatrix} e^{-i\phi} \sin \frac{\theta}{2} \\ -\cos \frac{\theta}{2} \end{pmatrix}.
  * The kets are unimportant by themselves. We want only the Berry connection.
* Berry connection:

  * For :math:`\vb{h}` lying on the southern hemisphere,

    .. math::
        \vb{A}^{\mathrm{S}}_-(\vb{h}) = \frac{1}{2}(1+\cos\theta) \dd{\phi}.
  * For :math:`\vb{h}` lying on the northern hemisphere,

    .. math::
        \vb{A}^{\mathrm{N}}_-(\vb{h}) = -\frac{1}{2}(1-\cos\theta) \dd{\phi}.
  * Magnetic monopole analogy: vector potential of a magnetic dipole at the origin.
  * We can't have an :math:`\vb{A}` covering the whole space. We have to either discard the :math:`z` axis or the equator. Here we chose the latter.
  * Gauge transformation on the equator:

    .. math::
        \vb{A}^{\mathrm{N}}_-(\vb{h}) = \vb{A}^{\mathrm{S}}_-(\vb{h}) - \dd{\phi}.
* TKNN number:

  .. math::
      \nu = \frac{1}{2\pi} \int \dd{\vb{A}}
  counts how many times the closed surface encircles the origin.

  * Topologically trivial: :math:`\nu = 0` if the surface does not encircle the origin.
  * Topologically nontrivial: :math:`\nu \neq 0` if the surface does encircle the origin.

Pump: ℤ₂ Index and Polarization
-------------------------------------

.. image:: https://badgen.net/badge/TRS/partial/yellow
.. image:: https://badgen.net/badge/Dimension/1+1D/purple

Polarization and Time-Reversal Polarization
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* We define
  
  .. math::
      w_{\alpha\beta}(\vb{k}) = \bra{u_{\alpha,-\vb{k}}} \Theta \ket{u_{\beta,\vb{k}}},
  where :math:`\alpha` and :math:`\beta` are indices of bands.

  * :math:`w` relates time-reversal pairs.
  
    .. math::
        \ket{u_{\alpha,-\vb{k}}} = \sum_{\beta} w^*_{\alpha\beta}(\vb{k}) \Theta \ket{u_{\beta,\vb{k}}}.

  * :math:`w` is unitary.
  
    .. math::
        \sum_{\alpha} w^\dagger_{\gamma\alpha}(\vb{k}) w_{\alpha\beta}(\vb{k}) = \delta_{\beta\gamma}.

  * :math:`w` satisfies
  
    .. math::
        w_{\beta\alpha}(-\vb{k}) = -w_{\alpha\beta}(\vb{k}).

  * :math:`w` is antisymmetric at TRIMs.

    .. math::
        w_{\beta\alpha}(-\vb{\Lambda}) = -w_{\alpha\beta}(\vb{\Lambda}).
* Berry connection matrix
  
  .. math::
      \vb{a}_{\alpha\beta}(\vb{k}) = -i \bra{u_{\alpha,\vb{k}}} \nabla_{\vb{k}} \ket{u_{\beta,\vb{k}}}.
  
  * :math:`\vb{a}` at time-reversal momentum pairs:
    
    .. math::
      \vb{a}(-\vb{k}) &= w(\vb{k}) \vb{a}^*(\vb{k}) w^\dagger(\vb{k}) + iw(\vb{k}) \nabla_{\vb{k}} w^\dagger(\vb{k}), \\
      \tr[\vb{a}(\vb{k})] &= \tr[\vb{a}(-\vb{k})] + i\tr[w^\dagger(\vb{k}) \nabla_{\vb{k}} w(\vb{k})].
      :label: eq_a_time_reversal_w
* Wannier function: of a certain band,
  
  .. math::
      \ket{R} = \sum_{k=-\pi}^\pi \frac{e^{ik(x-R)}}{\sqrt{L}} \ket{u_k}.
* Polarization: of a certain band,
  
  .. math::
      P_\rho = -\bra{R=0} x \ket{R=0}.

  * Polarization given by Berry connection:
    
    .. math::
        P_\rho = -\frac{1}{L} \sum_{k=-\pi}^\pi \bra{u_k} i\pdv{}{k} \ket{u_k} = \int_{-\pi}^\pi \frac{\dd{k}}{2\pi} a(k).
* Time-Reversal Polarization: of a time-reversal pair,
  
  .. math::
      P_\theta = P_1 - P_2 = 2P_1 - P_\rho,
  where

  .. math::
      P_i &= \int_{-\pi}^\pi \frac{\dd{k}}{2\pi} a_{ii(k)}, \\
      P_\rho &= P_1 + P_2.

Spin Pump: ℤ₂ Index and Time-Reversal Polarization
""""""""""""""""""""""""""""""""""""""""""""""

* The Hamiltonian satisfies
  
  .. math::
      H[t + T] &= H[T], \\
      H[-t] &= \Theta H[t] \Theta^{-1}.
* At :math:`t=0` and :math:`t=T/2`, the Hamiltonian is time-reversal invariant. Therefore,

  .. math::
      \Theta \ket{u_2(k)} &= e^{-i\chi(k)} \ket{u_1(-k)}, \\
      \Theta \ket{u_1(k)} &= -e^{-i\chi(-k)} \ket{u_2(-k)}. \\
      w(k) &= \begin{pmatrix} 0 & e^{-i\chi(k)} \\ -e^{-i\chi(-k)} & 0 \end{pmatrix}, \\
      a_{11}(-k) &= a_{22}(k) - \pdv{}{k} \chi(k).

  .. note::
      The relation between :math:`a_{11}` and :math:`a_{22}` does not hold if TRS is broken.
* Time-reversal polarization: with :eq:`eq_a_time_reversal_w`,
  
  .. math::
      P_\theta &= \int_{0}^{\pi} \frac{\dd{k}}{2\pi} [A(k) - A(-k)] - \frac{i}{\pi} \log \frac{w_{12}(\pi)}{w_{12}(0)} \\
      &= \frac{i}{\pi} \cdot \frac{1}{2} \log \frac{\det[w(\pi)]}{\det[w(0)]} - \frac{i}{\pi} \log \frac{w_{12}(\pi)}{w_{12}(0)} \\
      &= \frac{1}{i\pi} \log \qty(\frac{\sqrt{w_{12}(0)^2}}{w_{12}(0)} \cdot \frac{w_{12}(\pi)}{\sqrt{w_{12}(\pi)^2}}).
* Spin transport in a half-period:

  .. math::
      \Delta = \abs{P_\theta(T/2) - P_\theta(0)}.

  * :math:`\Delta` as :math:`\mathbb{Z}_2` index:
    
    .. math::
        (-1)^\Delta = \prod_{i=1}^4 \frac{w_{12}(\Lambda_i)}{\sqrt{w_{12}(\Lambda_i)^2}},

    where :math:`\Lambda_i` are TRIMs (:math:`T` plays the role of :math:`k_y` here since they are both :math:`S^1`)

    .. math::
        \Lambda_1 &= (k=0, t=0), \\
        \Lambda_2 &= (k=\pi, t=0), \\
        \Lambda_3 &= (k=0, t=T/2), \\
        \Lambda_4 &= (k=\pi, t=T/2).
    
    .. note::
      :math:`\Delta \neq 0` indicates that the system is topologically nontrivial. The Kramers pair at :math:`t=0` and :math:`t=T/2` are given by different electron pairs.
* :math:`\mathbb{Z}_2` index of multi-band systems:
  
  .. math::
      (-1)^\nu = \prod_{i=1}^4 \frac{\operatorname{Pf}[w(\Lambda_i)]}{\sqrt{\det[w(\Lambda_i)]}}.

Three-Dimensional Topological Insulators With Time-Reversal Invariance: ℤ₂ Index and Edge States
------------------------------------------------------------------------------------------------------

Three-Dimensional ℤ₂ Index
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. rst-class:: text-muted

    I could tell if it is a TI with these 4 bits.

* The :math:`\mathbb{Z}_2` index of three-dimensional topological insulators are denoted as
  
  .. math::
      (\nu_0; \nu_1 \nu_2 \nu_3),

  where

  .. math::
      (-1)^{\nu_0} &= \prod_{n_j = 0,\pi} \delta(\Lambda_{n_1, n_2, n_3}), \\
      (-1)^{\nu_i} &= \prod_{\substack{n_i = \pi \\ n_{j\neq i} = 0}} \delta(\Lambda_{n_1, n_2, n_3}), \\
      \delta(\Lambda_i) &= \frac{\operatorname{Pf}[w(\Lambda_i)]}{\sqrt{\det[w(\Lambda_i)]}}.
* The index :math:`\nu_z` equals to the :math:`\mathbb{Z}_2` index of the two-dimensional system on :math:`k_z = \pi`.

  * In this two-dimensional subsystem, we may let :math:`k_y` play the role of :math:`t` in the spin pump.
  * If :math:`\nu_z \neq 0`, there is a recombination of Kramers pairs as we move from :math:`k_y = 0` to :math:`k_y = \pi`.
  * Such recombination guarantees the existence of surface states.
* Strong TI: :math:`\nu_0 = 1`.
* Weak TI: :math:`\nu_0 = 0` while :math:`\nu_i = 1` for some :math:`i`.

Inversion Symmetry
^^^^^^^^^^^^^^^^^^^^^^

.. rst-class:: text-muted

    Keeping track of complex phases? That's too complex!

* Define

  .. math::
      \vb{a}^c(\vb{k}) = \tr [\vb{a}(\vb{k})] \in \mathbb{R}^3.

* Berry curvature:

  .. math::
      F(\vb{k}) = \nabla_{\vb{k}} \times \vb{a}^c(\vb{k}).

  * Berry curvature with symmetry:
  
    .. math::
        \mathrm{TRS} &\Rightarrow F(-\vb{k}) = -F(\vb{k}), \\
        \mathrm{Inversion\ Symmetry} &\Rightarrow F(-\vb{k}) = +F(\vb{k}).

  * When both TRS and inversion symmetry are present,
    
    .. math::
        F(\vb{k}) \equiv 0
    and therefore there exists a gauge such that

    .. math::
        \vb{a}(\vb{k}) = 0.

* We define
  
  .. math::
      v_{\alpha\beta}(\vb{k}) = \bra{u_{\alpha,\vb{k}}} \Pi \Theta \ket{u_{\beta,\vb{k}}},
  where :math:`\alpha` and :math:`\beta` are indices of bands.

  * :math:`w` is unitary.
  
    .. math::
        \sum_{\alpha} v^\dagger_{\gamma\alpha}(\vb{k}) v_{\alpha\beta}(\vb{k}) = \delta_{\beta\gamma}.

  * :math:`v` is anti-symmetric:
  
    .. math::
        v_{\alpha\beta} = -v_{\beta\alpha}.

* :math:`\vb{a}^c` given by :math:`v`:

  .. math::
      \vb{a}^c(\vb{k}) &= \frac{i}{2} \tr\qty[v^\dagger \nabla_{\vb{k}} v] \\
      &= i \nabla_{\vb{k}} \log \operatorname{Pf}[v(\vb{k})].

  * Since :math:`\vb{a}^c \equiv 0`, we have

    .. math::
        \operatorname{Pf}[v(\vb{k})] \equiv 1.

* We extract the parity of occupied states at each TRIM:

  .. math::
      \Pi \ket{\psi_\alpha(\Lambda_i)} = \xi_\alpha(\Lambda_i) \ket{\psi_\alpha(\Lambda_i)}.

* :math:`w` given by :math:`v`:

  .. math::
      w_{\alpha\beta}(\Lambda_i) = \xi_\alpha(\Lambda_i) v_{\alpha\beta}(\Lambda_i).

  * Therefore,
    
    .. math::
        \delta(\Lambda_i) = \prod_{n=1}^N \xi_{2n}(\Lambda_i).

* :math:`\mathbb{Z}_2` index given by parity:

  .. math::
      (-1)^\nu = \prod_{i=1}^4 \prod_{n=1}^N \xi_{2n}(\Lambda_i).
  
  .. note::
      We need an odd number of points of odd parity in the :math:`4N` :math:`\xi_{2n}`'s to have a nontrivial topology.

Remark: Why Does TRS Matter?
--------------------------------

| 『... それ以前は, トポロジカル相の実現には時間反転対称性の破れが必須だと一般に考えられていた...
| そのため,　時間反転対称性を保った絶縁体でも非自明なトポロジーを持ち得るという発見が, それまでの常識を覆すものだった.
| ただ残念なことに, 現実のグラフェンにおいてはスピン軌道相互作用が非常に弱いことがわかっており, Kane-Mele理論の帰結としての量子スピンホル効果を実験的に確認することは困難だった.』

Glossary
-----------

.. glossary::
    QHE/量子ホール効果/量子霍尔效应
        A quantized version of the Hall effect which is observed in two-dimensional electron systems subjected to low temperatures and strong magnetic fields, in which the Hall resistance exhibits steps that take on the quantized values.

References
-------------

.. [Shen2012] `Topological Insulators <https://link.springer.com/book/10.1007/978-3-642-32858-9>`_

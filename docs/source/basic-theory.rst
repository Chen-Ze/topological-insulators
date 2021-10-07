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
      \ket{n,t} = \exp\qty(i \gamma_n) \times \exp\qty({-\frac{i}{\hbar} \dd{t'} E_n[\vb{R}(t')]}) \ket{n,\vb{R}(t)}.
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



Glossary
-----------

.. glossary::
    QHE/量子ホール効果/量子霍尔效应
        A quantized version of the Hall effect which is observed in two-dimensional electron systems subjected to low temperatures and strong magnetic fields, in which the Hall resistance exhibits steps that take on the quantized values.

References
-------------

.. [Shen2012] `Topological Insulators <https://link.springer.com/book/10.1007/978-3-642-32858-9>`_

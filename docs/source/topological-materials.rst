Topological Materials
==============================

.. rst-class:: text-right text-muted

    『遠いのは、距離じゃなくて次元なんだよ。』

    『三次元ってのはな、もっと面倒くさいんだよ。』

2D Topological Insulators
-------------------------

CdTe/HgTe/CdTe Quantum Well
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2/purple
.. image:: https://badgen.net/badge/Dimension/2D/orange
.. image:: https://badgen.net/badge/Gap/10mV/red
.. image:: https://badgen.net/badge/Temperature/0.1K/red

[Bernevig2006]_
[König2007]_

* Band inversion found in bulk :math:`\ce{HgTe}` as long as the thickness exceeds a certain threshold, while normal ordering in :math:`\ce{CdTe}`.
* Gap zero at :math:`\Gamma` in :math:`\ce{HgTe}` opened by quantum confinement effect.
* Conductance verified to be quantized by :math:`2e^2/h` under zero magnetic field when the Fermi level is tuned into the band gap.

AlSb/InAs/GaSb/AlSb Quantum Well
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2/purple
.. image:: https://badgen.net/badge/Dimension/2D/orange
.. image:: https://badgen.net/badge/Gap/4mV/red
.. image:: https://badgen.net/badge/Temperature/4K/orange

[Knez2011]_
[Knez2012]_

.. rst-class:: block-center max-w100

    .. image:: https://ars.els-cdn.com/content/image/1-s2.0-S0022024816307904-gr1.jpg

.. rst-class:: text-center

    From `InAs/GaSb/AlSb composite quantum well structure preparation with help of reflectance anisotropy spectroscopy <https://www.sciencedirect.com/science/article/pii/S0022024816307904>`_

* It's a story between the holes of :math:`\ce{InAs}` and electrons of :math:`\ce{GaSb}`.

  * Dashed lines for bands before composition, while solid lines for bands after composition.
  * Dashed blue lines for the highest valence band of :math:`\ce{GaSb}`.
  * Dashed red lines for the lowest conduction band of :math:`\ce{InAs}`.
  * After composition, the dashed blue electrons near :math:`\Gamma` drop to fill the dash blue holes. Bingo! The solid blue electrons.
  * Now the dashed blue line near :math:`\Gamma` become holes --- band inversion.
  * As we move away from :math:`\Gamma`, the energy levels of holes and electrons become close before they intersect. However, this does not render the system conductive due to anticrossing gap --- exactly the effect in chemistry that creates covalent bonds.
  * As we move further, the dashed lines go back to the solid lines of their own colors --- no more band inversion.

Candidates of 2D Topological Materials
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Bilayer :math:`\ce{Bi}` metal.
  
  * Evidence for the existence of edge states has been found [Yang2012]_.
* Monolayer :math:`\ce{Na2IrO3}`.
* Vapor deposition of metal atoms onto graphene.
  
  * Spin-orbital interaction enhanced.
* Silicene: existence in isolation not proven.

Remark: Why is Two-Dimensional More Preferable?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

| 『... 2次元トポロジカル絶縁体には, 無散逸のエッジ電流や量子スピンホール効果など, 3次元トポロジカル絶縁体にはない興味深い物理がある...』

3D Topological Insulators
-----------------------------

Bi\ :subscript:`1-x`\ Sb\ :subscript:`x` Alloy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;111)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/30mV/orange
.. image:: https://badgen.net/badge/Temperature/>4K/orange

[Fu2007]_ [Hsieh2008]_

* Odd number of band inversion at TRIMs.
* Band gap exists in bulk for
  
  .. math::
      0.09 < x < 0.23.
* Surface states too complex.
* High surface carrier concentration and high crystal quality.

Tetradymite
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

References
-------------

.. [Bernevig2006] `Quantum Spin Hall Effect and Topological Phase Transition in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1133734>`_
.. [König2007] `Quantum Spin Hall Insulator State in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1148047>`_
.. [Knez2011] `Evidence for Helical Edge Modes in Inverted InAs/GaSb Quantum Wells <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.107.136603>`_
.. [Knez2012] `Andreev Reflection of Helical Edge Modes in InAs/GaSb Quantum Spin Hall Insulator <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.186603>`_
.. [Yang2012] `Spatial and Energy Distribution of Topological Edge States in Single Bi(111) Bilayer <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.016801>`_
.. [Fu2007] `Topological insulators with inversion symmetry <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.76.045302>`_
.. [Hsieh2008] `A topological Dirac insulator in a quantum spin Hall phase <https://www.nature.com/articles/nature06843>`_
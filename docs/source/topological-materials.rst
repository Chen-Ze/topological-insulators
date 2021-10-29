Topological Materials
==============================

.. rst-class:: text-right text-muted

    『遠いのは、距離じゃなくて次元なんだよ。』

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
.. image:: https://badgen.net/badge/Gap/4meV/red
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
  
  * Spin-orbit interaction enhanced.
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
.. image:: https://badgen.net/badge/Gap/30meV/orange
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

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~0.3eV/green
.. image:: https://badgen.net/badge/Temperature/<55K/yellow

.. note::
    :math:`c`-axis corresponds to the :math:`(111)`-direction of :math:`\ce{NaCl}` lattice.

* :math:`\ce{Bi2Se3}` (confirmed [Xia2009]_), :math:`\ce{Bi2Te3}` (confirmed [Chen2009]_), and :math:`\ce{Sb2Te3}` (confirmed [Jiang2012]_) are predicted to be TIs [Zhang2009]_.
* Tetradymites:

  * A-B-C-A-B-C packing of quintuple layers.
  * Each quintuple layer of the form Se-Bi-Se-Bi-Se.
  * Van der Waals cohesion.
* Only one Dirac cone, around :math:`\overline{\Gamma}` of surface BZ.
* Easy fabrication. Surface states are all topological.
* Pure crystal hard to obtain. Observation of surface transport disrupted.

.. note::
    Problem here: bulk conductivity too high.

More Tetradymite Materials
""""""""""""""""""""""""""""""

* High resistivity found in :math:`\ce{Bi2Te_{1.95}Se_{1.05}}` [Ren2010]_.
* With SdH and Hall data, it is found that surface states contribute :math:`6\%` of the total conductivity while the rest :math:`94\%` are from the bulk states.
* See also :math:`\ce{Bi_{2-x}Sb_{x}Te_{3-y}Se_y}` [Ren2011]_.
* :math:`\ce{Bi_{2-x}Sn_xTe_2Se}`: Fermi level dragged into band gap also by doping [Ren2012]_. Surface states contributes up to :math:`50\%` of the total conductivity.

BiQ Homologous Series
""""""""""""""""""""""""""

* Formula :math:`\ce{(Bi2)_n(Bi2X3)_m}`.
* Structure: packing of multi-layers. Covalent inter-multi-layer while van der Waals intra-multi-layer.
* :math:`\ce{(Bi2)(Bi2Se_{3-x}S_x)}` found to be topological semimetal for :math:`x=0.4` [Valla2012]_.
* :math:`\ce{(Bi2)(Bi2Te3)_2}`, i.e. :math:`\ce{BiTe}`, confirmed to be topological, yet unknown if it is insulator [Cava2013]_.

TlBiSe\ :subscript:`2`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~0.35eV/green
.. image:: https://badgen.net/badge/Temperature/<20K/yellow

[Yan2010]_ [Lin2010]_ [Sato2010]_ [Kuroda2010]_ [Chen2010]_

* Structure similar to tetradymite.
* Topological phase transition from :math:`\ce{TlBiS2}`:

  * Topological insulator :math:`\ce{TlBi(S_{1-x}Se_x)_2}` for :math:`x>0.5` [Xu2011]_, trivial insulator for :math:`x<0.5`.
  * Gap found at the Dirac point near :math:`x=0.5` [Sato2011]_ [Souma2012a]_, of yet unknown origin, which should have been degenerate by Kramers theorem.

GeBi\ :subscript:`2`\ Te\ :subscript:`4`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~0.18eV/green
.. image:: https://badgen.net/badge/Temperature/~50K/yellow

* N-type degenerate semiconductor due to defects [Okamoto2012]_.

Ge-Based Homologous Series
""""""""""""""""""""""""""""""""""""

* Formula :math:`\ce{(GeTe)_n(Bi2Te3)_m}`.
* :math:`\ce{GeBi_{4-x}Sb_xTe_7}` confirmed [Muff2013]_.

Pb-Based Materials
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~0.2eV/green
.. image:: https://badgen.net/badge/Temperature/~30K/yellow

* :math:`\ce{PbBi2Te4}` is p-type.
* :math:`\ce{PbSb2Te4}` is n-type.
* Dirac fermion in :math:`\ce{Pb(Bi_{1-x}Sb_x)_2Te4}` from n-type to p-type as :math:`x` increase [Souma2012b]_.

Pb-Based Homologous Series
""""""""""""""""""""""""""""""

* Formula :math:`\ce{(PbTe)_n(Bi2Te3)_m}`.
* :math:`\ce{PbBi4Te4}` confirmed [Eremeev2012]_.

Natural Superlattice
""""""""""""""""""""""""

* Formula :math:`\ce{(PbSe)_5(Bi2Se3)_{3m}}` where :math:`m=1,2`.
* Alternation of :math:`m` times of quintuple layers and :math:`\ce{PbSe}` layers.
* Dirac cone exists for :math:`m=2`.

  * Dirac gap opened due to mixture of states on the upper surface and lower surface.

  * Large bulk gap of 0.5eV due to quantum confinement of :math:`\ce{Bi2Se3}`.

BiTeCl
^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~0.22eV/green
.. image:: https://badgen.net/badge/Temperature/~10K/orange
.. image:: https://badgen.net/badge/P/broken/red

* Surface states helical despite bulk inversion symmetry broken [Chen2013]_.

HgTe (Epitaxial)
^^^^^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~20meV/orange
.. image:: https://badgen.net/badge/Temperature/~50mK/red

* Epitaxial growth on :math:`\ce{CdTe}` substrate [Brüne2011]_.
* Band gap opened by broken symmetry.

Sn (Epitaxial)
^^^^^^^^^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(1;000)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/~30meV/orange
.. image:: https://badgen.net/badge/Temperature/~20K/yellow

* Epitaxial growth of :math:`\alpha`-:math:`\ce{Sn}` on :math:`\ce{InSb} (001)` [Barfuss2013]_ [Ohtsubo2013]_.
* Helical surface states observed.

Candidates of 3D Topological Materials
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :math:`\ce{Ag2Te}`, magnetoresistance proportional to magnetic field in a wide range, possibly of topological origin.
* :math:`\ce{SmB6}`, possibly topological Kondo insulator.
* :math:`\ce{Bi_{14}Rh3I9}`:

  * Weak topological insulator :math:`(0;001)` by calculation.
  * Packing of two-dimensional insulators
  * Honeycomb lattice. 
  * Surface states are hard to be detecte by ARPES since they are not on the cleavage surface.

Topological Semimetals
-----------------------------

Definition of Topological Semimetals
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Topological semimetals may refer two three kinds of materials.

* Ordinary semimetals (i.e. those where the top of the valence band is lower than the bottom of the conduction band) with nontrivial :math:`\mathbb{Z}_2` index, e.g. :math:`\ce{Sb}`.
* Zero-gap semiconductors where the degeneracy is protected by crystal symmetries, e.g. :math:`\ce{HgTe}`, where the gap may be opened by perturbations that breaks the symmetries.
* Weyl semimetals.

Weyl Semimetals
^^^^^^^^^^^^^^^^^^^^

.. raw:: html

    <img class="block-center" width="360" src="https://www.researchgate.net/profile/Binghai-Yan/publication/281312307/figure/fig2/AS:316963344666635@1452581358627/Schematics-of-the-topological-insulator-and-Weyl-semimetal-a-A-TI-exhibits-an-energy.png"/>

.. rst-class:: text-center

    From `Topological surface states and Fermi arcs of the noncentrosymmetric Weyl semimetals TaAs, TaP, NbAs, and NbP <https://www.researchgate.net/publication/281312307_Topological_surface_states_and_Fermi_arcs_of_the_noncentrosymmetric_Weyl_semimetals_TaAs_TaP_NbAs_and_NbP>`_

* Chirality as a good quantum number.
* Massless Dirac equation: Dirac equation diagonalized into two :math:`2\times 2`-blocks of each chirality.
* Inversion symmetry or TRS broken: spin-degeneracy lifted.
* At intersections of conduction bands and valance bands (i.e. Weyl points): Hamiltonian (:math:`\pm` depending on the chirality)

  .. math::
      H = \pm \hbar v_{\mathrm{F}} \vb*{\sigma}\cdot \vb{k}.
* Weyl points exist in pair of opposite chiralities.
* A Weyl point pair is joined by a Dirac arc, projection of which onto the 2D BZ surface gives gapless surface state.

Candidates of Topological Semimetals
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Heusler compounds and half-Heusler compounds: zero band-gap semiconductors by crystal symmetry.
* AFM phase of :math:`\ce{Y2Ir2O7}`.
* :math:`\ce{Nd2(Ir_{1-x}Rh_x)_2O7}`: Mott transition.
* Layers of :math:`\ce{HgTe}/\ce{CdTe}` with electric field applied.
* MBE growth of :math:`\ce{Tl-Se-Bi-S}` multi-layers.

Topological Crystalline Insulator
------------------------------------

SnTe
^^^^^^^^^

.. image:: https://badgen.net/badge/Type/ℤ%2F2(0;000)/grey
.. image:: https://badgen.net/badge/Type/Mirror(-2)/purple
.. image:: https://badgen.net/badge/Dimension/3D/cyan
.. image:: https://badgen.net/badge/Gap/0.3eV/green
.. image:: https://badgen.net/badge/Temperature/~4K/orange

[Hsieh2012]_ [Tanaka2012]_ [Dziawa2012]_

* :math:`\ce{SnTe}`: Double Dirac cones found around each :math:`\overline{X}` point in the surface BZ, each the projection of two :math:`L` points.
* :math:`\ce{PbTe}`: topologically trivial.
* :math:`\ce{Pb_{1-x}Sn_xTe}`: topological phase transition around :math:`x=0.25`.
* The two Dirac cones around each :math:`\overline{X}` are separated due to level repulsion (or avoided crossing).

SnSe
^^^^^^^^^

* :math:`\ce{Pb_{0.77}Sn_{0.23}Se}`: trivial insulator at RT while topological at :math:`T` goes down, where spin-orbit interaction increases due to lattice shrinking.

Synthesization
------------------

Bulk Single Crystal
^^^^^^^^^^^^^^^^^^^^^^^

* Bridgeman method.
  
  * :math:`\ce{Bi2Se3}`, :math:`\ce{Bi2Te3}`, :math:`\ce{Bi2Te2Se}`.
* Vapor transport method.

  * PVT (physical vapor transport): :math:`\ce{SnTe}`, :math:`\ce{(Pb,Sn)Se}`, :math:`\ce{(Pb,Sn)Te}`.
  * CVT (chemical vapor transport).

Thin Film
^^^^^^^^^^^

* MBE (molecular beam epitaxy) method.
  
  * :math:`\ce{Bi_{1-x}Sb_x}`, :math:`\ce{Bi2Se3}`, :math:`\ce{Bi2Te3}`, :math:`\ce{Sb2Te3}`, :math:`\ce{(Bi,Sb)_2Te3}`.
* CVD (chemical vapor deposition).
  
  * :math:`\ce{Bi2Se3}`.

Nano-Ribbon and Nano-Plate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* VLS (vapor liquid solid) method.

Bulk Insulation
----------------------

* Bulk carrier density too high due to defects.
* Fixed by doping.
* Tunable between p-type and n-type.
  
  * Enabling p-n junction using surface states.

Glossary
-----------

.. glossary::
    Tetradymite/テトラジマイト/辉碲铋矿
        A mineral consisting of bismuth, tellurium and sulfide, :math:`\ce{Bi2Te2S}`, a.k.a. telluric bismuth.

References
-------------

.. [Bernevig2006] `Quantum Spin Hall Effect and Topological Phase Transition in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1133734>`_
.. [König2007] `Quantum Spin Hall Insulator State in HgTe Quantum Wells <https://www.science.org/doi/abs/10.1126/science.1148047>`_
.. [Knez2011] `Evidence for Helical Edge Modes in Inverted InAs/GaSb Quantum Wells <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.107.136603>`_
.. [Knez2012] `Andreev Reflection of Helical Edge Modes in InAs/GaSb Quantum Spin Hall Insulator <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.186603>`_
.. [Yang2012] `Spatial and Energy Distribution of Topological Edge States in Single Bi(111) Bilayer <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.016801>`_
.. [Fu2007] `Topological insulators with inversion symmetry <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.76.045302>`_
.. [Hsieh2008] `A topological Dirac insulator in a quantum spin Hall phase <https://www.nature.com/articles/nature06843>`_
.. [Zhang2009] `Topological insulators in Bi2Se3, Bi2Te3 and Sb2Te3 with a single Dirac cone on the surface <https://www.nature.com/articles/nphys1270>`_
.. [Xia2009] `Observation of a large-gap topological-insulator class with a single Dirac cone on the surface <https://www.nature.com/articles/nphys1274>`_
.. [Chen2009] `Experimental Realization of a Three-Dimensional Topological Insulator, Bi2Te3 <https://www.science.org/doi/abs/10.1126/science.1173034>`_
.. [Jiang2012] `Landau Quantization and the Thickness Limit of Topological Insulator Thin Films of Sb2Te3 <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.016401>`_
.. [Ren2010] `Large bulk resistivity and surface quantum oscillations in the topological insulator Bi2Te2Se <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.82.241306>`_
.. [Ren2011] `Optimizing Bi2−xSbxTe3−ySey solid solutions to approach the intrinsic topological insulator regime <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.84.165311>`_
.. [Ren2012] `Fermi level tuning and a large activation gap achieved in the topological insulator Bi2Te2Se by Sn doping <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.85.155301>`_
.. [Yan2010] `Theoretical prediction of topological insulators in thallium-based III-V-VI2 ternary chalcogenides <https://iopscience.iop.org/article/10.1209/0295-5075/90/37002/meta>`_
.. [Lin2010] `Single-Dirac-Cone Topological Surface States in the TlBiSe2 Class of Topological Semiconductors <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.105.036404>`_
.. [Sato2010] `Direct Evidence for the Dirac-Cone Topological Surface States in the Ternary Chalcogenide TlBiSe2 <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.105.136802>`_
.. [Kuroda2010] `Experimental Realization of a Three-Dimensional Topological Insulator Phase in Ternary Chalcogenide TlBiSe2 <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.105.146801>`_
.. [Chen2010] `Single Dirac Cone Topological Surface State and Unusual Thermoelectric Property of Compounds from a New Topological Insulator Family <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.105.266401>`_
.. [Xu2011] `Topological Phase Transition and Texture Inversion in a Tunable Topological Insulator <https://www.science.org/doi/abs/10.1126/science.1201607>`_
.. [Sato2011] `Unexpected mass acquisition of Dirac fermions at the quantum phase transition of a topological insulator <https://www.nature.com/articles/nphys2058>`_
.. [Souma2012a] `Spin Polarization of Gapped Dirac Surface States Near the Topological Phase Transition in TlBi(S1−xSex)2 <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.186804>`_
.. [Okamoto2012] `Observation of a highly spin-polarized topological surface state in GeBi2Te4 <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.86.195304>`_
.. [Souma2012b] `Topological Surface States in Lead-Based Ternary Telluride Pb(Bi1−xSbx)2Te4 <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.116801>`_
.. [Eremeev2012] `Atom-specific spin mapping and buried topological states in a homologous series of topological insulators <https://www.nature.com/articles/ncomms1638>`_
.. [Muff2013] `Separating the bulk and surface n- to p-type transition in the topological insulator GeBi4−xSbxTe7 <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.88.035407>`_
.. [Chen2013] `Discovery of a single topological Dirac fermion in the strong inversion asymmetric compound BiTeCl <https://www.nature.com/articles/nphys2768>`_
.. [Valla2012] `Topological semimetal in a Bi-Bi2Se3 infinitely adaptive superlattice phase <https://journals.aps.org/prb/abstract/10.1103/PhysRevB.86.241101>`_
.. [Cava2013] `Crystal structure and chemistry of topological insulators <https://pubs.rsc.org/en/content/articlelanding/2013/tc/c3tc30186a>`_
.. [Brüne2011] `Quantum Hall Effect from the Topological Surface States of Strained Bulk HgTe <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.106.126803>`_
.. [Barfuss2013] `Elemental Topological Insulator with Tunable Fermi Level: Strained α-Sn on InSb(001) <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.111.157205>`_
.. [Ohtsubo2013] `Dirac Cone with Helical Spin Polarization in Ultrathin α-Sn(001) Films <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.111.216401>`_
.. [Nakayama2012] `Manipulation of Topological States and the Bulk Band Gap Using Natural Heterostructures of a Topological Insulator <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.109.236804>`_
.. [Hsieh2012] `Topological crystalline insulators in the SnTe material class <https://www.nature.com/articles/ncomms1969>`_
.. [Tanaka2012] `Experimental realization of a topological crystalline insulator in SnTe <https://www.nature.com/articles/nphys2442>`_
.. [Dziawa2012] `Topological crystalline insulator states in Pb1−xSnxSe <https://www.nature.com/articles/nmat3449>`_
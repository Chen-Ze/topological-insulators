Topological Superconductors
====================================

.. rst-class:: text-muted text-right

    『この可憐な魔女は誰でしょう。ーーそう、Majoranaです。』

Classification of Topological Superconductors
------------------------------------------------

* Topological superconductors are those superconductors with topologically nontrivial wavefunctions.
* BCS (s-wave) superconductors are topologically trivial.
* P-wave superconductors are basically topologically nontrivial.

Candidates of Topological Superconductors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :math:`\ce{Cu_xBi2Se3}` (doped :math:`\ce{Bi2Se3}`).
* :math:`\ce{Sn_{1-x}In_xTe}` (doped topological crystalline insulator :math:`\ce{SnTn}`).
  
  * Strong spin-orbit interaction couples electrons of different parities into Cooper pairs.

Majorana Fermions
------------------------

* Majorana condition: :math:`\gamma` denoting the annihilation operator of Majorana fermions,
  
  .. math::
      \gamma^\dagger = \gamma.
* Pairing electrons of the same spin:

  .. math::
      \gamma = uc_\uparrow + u^*c_\uparrow^\dagger.
* Existence of Majorana fermions (as Bogoliubov quasiparticles) in superconductors implies nontrivial topology, but not vice versa.

Kitaev Model
-----------------

* Hamiltonian (spinless):
  
  .. math::
      H = -\mu \sum_i c^\dagger_i c_i - \frac{1}{2} \sum_i (tc^\dagger_i c_{i+1} - \Delta c_{i} c_{i+1} + \mathrm{h.c.}),
  where :math:`\mu` is the chemical potential, :math:`t\ge 0` is the hopping amplitude, and :math:`\Delta \ge 0` is the strength of p-wave pairing.

Kitaev Model: Periodic Boundary Condition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Pre-diagonalization
  
  .. math::
      H = \frac{1}{2} \sum_k C^\dagger_{k} \mathcal{H}_k C_k,
  where

  .. math::
      \mathcal{H}_k &= \begin{pmatrix} \epsilon(k) & \Delta^*_k \\ \Delta_k & -\epsilon(k) \end{pmatrix}, \\
      \epsilon(k) &= -t\cos k - \mu, \\
      \Delta_k &= -i\Delta \sin k,
  
  and

  .. math::
      C^\dagger_k = (c^\dagger_k, c_{-k}).
* BdG (Bogoliubov-de Gennes) transformation:
  
  .. math::
      a_k &= u_k c_k + v_k c^\dagger_{-k}, \\
      u_k &= \frac{\Delta_k}{\abs{\Delta_k}} \frac{\sqrt{E_{\mathrm{b}} + \epsilon(k)}}{\sqrt{2E_{\mathrm{b}}}}, \\
      v_k &= \qty(\frac{E_{\mathrm{b}} - \epsilon(k)}{\Delta_k}) u_k.
* Diagonalization:
  
  .. math::
      H = \sum_k E_{\mathrm{b}} a^\dagger_k a_k,
  where

  .. math::
      E_{\mathrm{b}} = \sqrt{\epsilon(k)^2 + \abs{\Delta_k}^2}.
  
  * Nonzero except for :math:`k = \pm \pi` for :math:`\mu = t` and :math:`k = 0` for :math:`\mu = -t`.
  * Finite gap of excitation exists in most cases.
* :math:`\mathbb{Z}_2` index:
  
  .. math::
      (-1)^\nu = \frac{\epsilon(0)}{\abs{\epsilon(0)}} \frac{\epsilon(\pi)}{\abs{\epsilon(\pi)}}.

  * Trivial (:math:`\nu = 0`) for :math:`\abs{\mu} > t`.
  * Non-trivial (:math:`\nu = 1`) for :math:`\abs{\mu} < t`.

Kitaev Model: Open Boundary Condition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Hamiltonian with Majorana operators:
  
  .. math::
      H = -\frac{\mu}{2} \sum_{i} (1+i \gamma_{\mathrm{B}, i} \gamma_{\mathrm{A}, i}) - \frac{i}{4} \sum_i \qty[(\Delta + t) \gamma_{\mathrm{B}, i} \gamma_{\mathrm{A}, i+1} + (\Delta - t) \gamma_{\mathrm{A}, i} \gamma_{\mathrm{B}, i+1}],
  where

  .. math::
      \begin{cases}
          \displaystyle c_i = \frac{1}{2}(\gamma_{\mathrm{B}, i} + i\gamma_{\mathrm{A}, i}), \\
          \displaystyle c^\dagger_i = \frac{1}{2} (\gamma_{\mathrm{B}, i} - i\gamma_{\mathrm{A}, i}),
      \end{cases} \Leftrightarrow \begin{cases}
          \gamma_{\mathrm{B}, i} = c^\dagger_i + c_i, \\
          \gamma_{\mathrm{A}, i} = i(c^\dagger_i - c_i).
      \end{cases}
* Every site now resides two kinds of particles :math:`\mathrm{A}` and :math:`\mathrm{B}`.
* Topologically trivial case :math:`\mu<0` and :math:`t=\Delta = 0`: only on-site terms.
* Topologically non-trivial case :math:`\mu=0` and :math:`t=\Delta \neq 0`:
    
  .. math::
      H = -i\frac{t}{2} \sum_i \gamma_{\mathrm{B},i} \gamma_{\mathrm{A},i}.
  
  * Bonding between adjacent sites.
  * Diagonalization:
    
    .. math::
        H = t \sum_i (\tilde{c}^\dagger_i \tilde{c}_i - \frac{1}{2})
    
    where

    .. math::
        \tilde{c}_i = \frac{1}{2} (\gamma_{\mathrm{A},i} + i \gamma_{\mathrm{B},i}).
  * Zero-energy Majorana fermion at the edge: Majorana zero mode
    
    .. math::
        f = \frac{1}{2} (\gamma_{\mathrm{A}, i} + i\gamma_{\mathrm{B},N}).
  * Ground states with (:math:`\ket{1}`) or without (:math:`\ket{0}`) Majorana zero mode at the edge:
    
    .. math::
        \ket{1} = f^\dagger \ket{0}.
* Such two-fold degeneracy occurs in p-wave topological superconductors.

Spinless P-Wave Chiral Superconductor
-----------------------------------------

* Hamiltonian:
  
  .. math::
      H = \int \dd{^2 \vb{r}} \qty{{
          \psi^\dagger \qty(-\frac{\hbar^2 \nabla^2}{2m} - \mu) \psi +
          \frac{\Delta}{2}\qty[e^{i\phi} \psi \qty(\pdv{}{x} + i\pdv{}{y}) \psi + \mathrm{h.c.}]
      }},
  
  where :math:`\phi` denotes the phase of superconductivity.
* Pre-diagonalization:
  
  .. math::
      H = \frac{1}{2} \int \frac{\dd{^2 \vb{k}}}{(2\pi)^2} \Psi^\dagger(\vb{k}) \mathcal{H}(\vb{k}) \Psi(\vb{k}),

  where

  .. math::
      \mathcal{H}(\vb{k}) &= \begin{pmatrix}
          \epsilon(k) & \Delta^*(\vb{k}) \\
          \Delta(\vb{k}) & -\epsilon(k)
      \end{pmatrix}, \\
      \epsilon(k) &= \frac{\hbar^2 k^2}{2m} - \mu, \\
      \Delta(\vb{k}) &= i\Delta e^{i\phi} (k_x + ik_y),
  
  and

  .. math::
      \Psi^\dagger(\vb{k}) = (\psi^\dagger(\vb{k}), \psi(-\vb{k})).
* BdG (Bogoliubov-de Gennes) transformation:
  
  .. math::
      a(\vb{k}) = u(\vb{k}) \psi(\vb{k}) + v(\vb{k}) \psi^\dagger(-\vb{k}),
  and :math:`u` and :math:`v` takes the same form as in the Kiatev model.
* Diagonalization:
  
  .. math::
      H = \int \frac{\dd{^2\vb{k}}}{(2\pi)^2} E_{\mathrm{b}}(\vb{k}) a^\dagger(\vb{k}) a(\vb{k}),
  
  where

  .. math::
      E_{\mathrm{b}}(\vb{k}) = \sqrt{\epsilon(k)^2 + \abs{\Delta(\vb{k})}^2}.
  
  * Gap closed at :math:`\mu = 0` and :math:`\vb{k} = 0`.
  * Otherwise the gap remains finite.
* Ground state
  
  .. math::
      \ket{\mathrm{GS}} = \prod_{k_x \ge 0,k_y} \qty[u(\vb{k}) + v(\vb{k}) \Psi^\dagger(-\vb{k}) \Psi^\dagger(\vb{k})]\ket{0}.

Topological Invariance of Spinless P-Wave Superconductor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Topological if :math:`\mu>0`.
* Trivial if :math:`\mu<0`.
* Hamiltonian as in the two-band topological system
  
  .. math::
      \mathcal{H}(\vb{k}) = \vb{h}(\vb{k})\cdot \vb*{\sigma},
  
  where

  .. math::
      h_x(\vb{k}) = \Re[\Delta(\vb{k})],\quad h_y(\vb{k}) = \Im[\Delta(\vb{k})],\quad h_z(\vb{k}) = \epsilon(k).
* Chern number:
  
  .. math::
      C = \int \frac{\dd{^2 \vb{k}}}{4\pi} \qty[\hat{\vb{h}}(\vb{k}) \cdot \qty({
          \pdv{}{k_x} \hat{\vb{h}}(\vb{k}) \times \pdv{}{k_y} \hat{\vb{h}}(\vb{k})
      })].

  * Counting how many times :math:`\hat{\vb{h}}` covers :math:`S^2`.
* Evaluation of Chern number:

  * :math:`\hat{\vb{h}}(\infty) = +\hat{\vb{z}}` for any :math:`\mu`.
  * :math:`\hat{\vb{h}}(\infty) = +\hat{\vb{z}}` for :math:`\mu < 0` and therefore topological trivial in this case.
  * :math:`\hat{\vb{h}}(\infty) = -\hat{\vb{z}}` for :math:`\mu > 0` and therefore topological nontrivial in this case since :math:`C=-1`.
* Majorana fermions exist at the edge in the topological phase.
  
  * Majorana zero mode exists with magnetic field applied.

Topological Superconductors in Hybrid Systems
----------------------------------------------

* Contacting an s-wave BCS SC with TI may induce SC states at the surface of TI due to superconducting proximity effect.
* Hamiltonian of TI surface states:
  
  .. math::
      \mathcal{H}_0(\vb{k}) &= \psi^\dagger [-i\hbar v_{\mathrm{F}}(\sigma_x \partial_x + \sigma_y \partial_y)] \psi \\
      &= \psi^\dagger(-i\hbar v_{\mathrm{F}} \vb*{\sigma} \cdot \nabla - \mu) \psi.
* Hamiltonian item added by the proximate SC:

  .. math::
      V = \Delta_0 e^{i\phi} \psi^\dagger_\uparrow \psi^\dagger_\downarrow + \mathrm{h.c.}.
* Pre-diagonalization:
  
  .. math::
      H = \frac{1}{2} \Psi^\dagger \mathcal{H} \Psi,
  where

  .. math::
      \mathcal{H} = \begin{pmatrix}
          -i\hbar v_{\mathrm{F}} \vb*{\sigma} \cdot \nabla - \mu & \Delta_0 (\cos\phi - i \sin\phi) \\
          \Delta_0 (\cos\phi + i\sin\phi) & i\hbar v_{\mathrm{F}} \vb*{\sigma} \cdot \nabla + \mu
      \end{pmatrix},
  
  and the Nambu basis is given by

  .. math::
      \Psi = ((\psi_\uparrow, \psi_\downarrow), (\psi^\dagger_\downarrow, -\psi^\dagger_\uparrow))^T.
* As p-wave super conductor: for :math:`\hbar v_{\mathrm{F} k_0 \approx \mu`,
  
  .. math::
      H = \sum_{\vb{k}} \qty[(\hbar v_{\mathrm{F}} k_0 - \mu) c^\dagger_{\vb{k}} c_{\vb{k}} + \frac{1}{2} \qty({
          \Delta_0 e^{i(\phi + \theta_{\vb{k}})} c^\dagger_{\vb{k}} c^\dagger_{-\vb{k}} + \mathrm{h.c.}
      })],
  
  where

  .. math::
      c_{\mathrm{k}} = \frac{1}{\sqrt{2}} (\psi_{\uparrow\vb{k}} + e^{i\theta_{\vb{k}}} \psi_{\downarrow \vb{k}})
  
  and

  .. math::
      \vb{k} = k_0(\cos \theta_{\vb{k}}, \sin \theta_{\vb{k}}).
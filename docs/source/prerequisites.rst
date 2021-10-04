Prerequisites
=================

Time Reversal
-----------------

* Time-reversal for spin-:math:`1/2` systems:
  
  .. math::
      \Theta = -is_y K.
* :math:`\Theta^2 = -\mathbb{1}`.
* Bra-ket properties:

  .. math::
      \bra{\psi} \Theta \ket{\phi} &= -\bra{\phi} \Theta \ket{\psi}, \\
      \bra{\Theta\psi} \ket{\Theta\phi} &= \bra{\phi}\ket{\psi}, \\
      \bra{\Theta \psi} \Theta A \Theta^{-1} \ket{\Theta \phi} &= \bra{\phi} A^\dagger \ket{\psi}.
* Kramer degeneracy: if the Hamiltonian is invariant under time-reversal, energy levels at :math:`\vb{k}` and :math:`-\vb{k}` are identical.

  * Kramer pair:
    
    .. math::
        E_{n,\uparrow}(\vb{k}) = E_{n,\downarrow}(-\vb{k}).
    .. caution::

        I doubt if the above equation makes any sense. If the band is not polarized, i.e. there is a two-fold degeneracy at each :math:`\vb{k}`, then the subscripts :math:`\uparrow` and :math:`\downarrow` are unnecessary. However, if the band is polarized, then either TRS is broken, or spin-orbit interaction comes into play. In the latter case, it makes no sense to write :math:`\uparrow` and :math:`\downarrow` any more, since :math:`S_z` may no longer commute with :math:`H`.
  * At a TRIM :math:`\vb{k}`,

    .. math::
        E_{n,\uparrow}(\vb{k}) = E_{n,\downarrow}(\vb{k}).

Glossary
----------

.. glossary::
    TRIM/時間反転不変運動量/时间反演不变动量
        Time-reversal invariant momentum

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

        When spin-orbit interaction comes into play, it makes no sense to write :math:`\uparrow` and :math:`\downarrow` any more, since :math:`S_z` may no longer commute with :math:`H`.
  * At a TRIM :math:`\vb{k}`,

    .. math::
        E_{n,\uparrow}(\vb{k}) = E_{n,\downarrow}(\vb{k}).
* Commutation relations: [Bernivig2013]_

  .. math::
      \Theta c_{ja\uparrow} \Theta^{-1} &= c_{ja\downarrow}, \\
      \Theta c_{ja\downarrow} \Theta^{-1} &= -c_{ja\uparrow}, \\
      \Theta c_{ja\uparrow}^\dagger \Theta^{-1} &= c_{ja\downarrow}^\dagger, \\
      \Theta c_{ja\downarrow}^\dagger \Theta^{-1} &= -c_{ja\uparrow}^\dagger, \\
  .. note::
      It seems weird that we have minus signs in the above equations, since it implies

      .. math::
          \Theta^2 c_{ja\uparrow} \Theta^{-2} = c_{ja\uparrow}.
      However, this is exact what we want because :math:`\Theta^2` and :math:`\Theta^{-2}` acts on Hilbert spaces of different particle numbers, and therefore have different values.

Glossary
----------

.. glossary::
    TRIM/時間反転不変運動量/时间反演不变动量
        Time-reversal invariant momentum

References
-------------

.. [Bernivig2013] `Topological Insulators and Topological Superconductors <https://poboiko.bitbucket.io/qm/fall16/seminar-6-adiabaticheskoe-priblizhenie/topological_insulators.pdf>`_

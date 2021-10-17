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

  .. note::
      TRS guarantees two-fold degeneracy at TRIMs. The degeneracy pairs are given by Kramers pairs.
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
* Ferromagnetism and antiferromagnetism breaks TRS. See `反铁磁到底有没有破缺时间反演对称性，为什么很多狄拉克材料具有反铁磁性如SrMnSb2等？ - 方辰的回答 - 知乎 <https://www.zhihu.com/question/264292959/answer/282884572>`_.

Topology
-----------

* Pfaffian: for an anti-symmetric matrix :math:`A`,
  
  .. math::
      \operatorname{Pf}[A]^2 = \det[A].

Semiclassical Theory of Electron Transport
---------------------------------------------

* :math:`\tau` denotes the relaxation time.
* Scattering probability in interval :math:`\dd{t}` is given by :math:`\dd{t}/\tau`.
* Time evolution of an electron of velocity :math:`\vb{v}(t)` at time :math:`\vb{v}(t)`:
  
  * Without scattering:

    .. math::
        \langle \vb{v}(t+\dd{t}) \rangle = \vb{v}(t) + \frac{\vb{f}(t)}{m^*} \dd{t}.
  * With scattering:
    
    .. math::
        \langle \vb{v}(t+\dd{t}) \rangle = 0.
  * Overall:

    .. math::
        \langle \vb{v}(t+\dd{t}) \rangle = \qty(1 - \frac{\dd{t}}{\tau}) \qty( {\vb{v}(t) + \frac{\vb{f}(t)}{m^*} \dd{t}} ).
* Equation of motion:

  .. math::
      m^* \qty({\dv{\vb{v}(t)}{t} + \frac{\vb{v}(t)}{\tau}}) \approx \vb{f}(t).
* Lorentz force law:
  
  .. math::
      \dv{\vb{v}(t)}{t} + \frac{\vb{v}(t)}{\tau} \approx -\frac{e}{m^*} \qty( \vb{E} + \frac{1}{c} \vb{v} \times \vb{B} ).
* Stationary state, with :math:`\vb{B}` along :math:`z`-axis:
  
  .. math::
      \begin{cases}
          v_x + \omega_c \tau v_y = -(e\tau/m^*) E_x, \\
          v_y - \omega_c \tau v_x = -(e\tau/m^*) E_y, \\
          v_z = -(e\tau / m^*) E_z.
      \end{cases}
* Solution:
  
  .. math::
      \begin{cases}
          \displaystyle J_x = \frac{ne^2\tau}{m^*} \frac{E_x - \omega_c \tau E_y}{1+(\omega_c \tau)^2}, \\
          \displaystyle J_y = \frac{ne^2\tau}{m^*} \frac{E_y + \omega_c \tau E_x}{1+(\omega_c \tau)^2}, \\
          \displaystyle J_z = \frac{ne^2\tau}{m^*}E_z,
      \end{cases}
  where

  .. math::
      J = -n(e/c)\vb{v}.
* Solution on the :math:`xy`-plane:
  
  .. math::
      \begin{pmatrix} J_x \\ J_y \end{pmatrix} = \frac{\sigma_0}{1+(\omega_c \tau)^2} \begin{pmatrix} 1 & -\omega_c \tau \\ \omega_c \tau & 1 \end{pmatrix} \begin{pmatrix} E_x \\ E_y \end{pmatrix},
  where

  .. math::
      \sigma_0 = \frac{ne^2 \tau}{m^*}.
* Conductivity tensor:
  
  .. math::
      \sigma_{xx} &= \sigma_{yy} = \frac{1}{1+(\omega_c \tau)^2} \sigma_0, \\
      \sigma_{xy} &= -\sigma_{yx} = \frac{-\omega_c \tau}{1+(\omega_c \tau)^2} \sigma_0.

SdH Oscillation
^^^^^^^^^^^^^^^^^^^^^

* :math:`B` very large, :math:`\omega_c \tau \gg 1`,
  
  .. math::
      \sigma_{xx} &\approx \frac{ne^2}{m^* \omega_c^2 \tau} = \frac{nm^* c^2}{B^2 \tau}, \\
      \sigma_{xy} &\approx \frac{ne^2}{m^* \omega_c} = \frac{nec}{B}.
* Lifshitz-Kosevich theory: oscillation of :math:`\sigma_{xx}` is given by

  .. math::
      \Delta \sigma_{xx} \propto \cos \qty[ 2\pi\qty(\frac{F}{B} - \frac{1}{2} + \beta)],
  where :math:`F` is the frequency of oscillation, and :math:`2\pi \beta` is the Berry phase of every cycle of motion.

  * :math:`\beta = 1/2` for Dirac fermions.
  * Item in the :math:`\cos` originates from
    
    .. math::
        A_N = \frac{2\pi e}{\hbar c} B\qty(N + \frac{1}{2} - \beta),
    i.e. the area in the :math:`\vb{k}`-space encircled by the closed path of electron motion.

Conductivity and Resistivity Tensor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. math::
    \begin{pmatrix} \rho_{xx} & \rho_{xy} \\ \rho_{yx} & \rho_{xx} \end{pmatrix} = \frac{1}{\sigma^2_{xx} + \sigma^2_{xy}} \begin{pmatrix} \sigma_{xx} & \sigma_{xy} \\ \sigma_{yx} & \sigma_{xx} \end{pmatrix}.

* If :math:`\sigma_{xy} = 0`,
  
  .. math::
      \rho_{xx} = \frac{1}{\rho_{xx}}.
* If :math:`\abs{\sigma_{xx}} \ll \abs{\sigma_{xy}}`,
  
  .. math::
      \rho_{xx} = \frac{\sigma_{xx}}{\sigma_{xy}^2}.

  * This is the case in strong magnetic field:
  
    .. math::
        \abs{\sigma_{xx}} \ll \abs{\sigma_{xy}} \Longleftrightarrow \omega_c\tau \gg 1.

Glossary
----------

.. glossary::
    TRIM/時間反転不変運動量/时间反演不变动量
        Time-reversal invariant momentum

References
-------------

.. [Bernivig2013] `Topological Insulators and Topological Superconductors <https://poboiko.bitbucket.io/qm/fall16/seminar-6-adiabaticheskoe-priblizhenie/topological_insulators.pdf>`_

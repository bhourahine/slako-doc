.. _variants:

===============
Format variants
===============

Specific implementations of the DFTB method may have different behaviour when
interpreting the SK format and variant forms have appeared in some specific
parameterization sets.

Spin polarization energy
------------------------

The ``SPE`` spin polarization value in the homo-nuclear file (line 2 in the
:ref:`version0.9`) is read but not interpreted by most current implementations
of the DFTB model.

Start of matrix element table
-----------------------------

Different implementations of DFTB have considered the table of Hamiltonian and
overlap matrix element to start at different locations. The first element is
considered to be either at a diatomic distance of 0, or at ``gridDist`` between
the atoms. The difference arises depending on whether the first point in the
grid is considered to be the on-site values or not.

A partial list of the choice made be by different implementations is given
below:

+---------------------------------------+----------+--------------+
| Code                                  | start table at          |
+---------------------------------------+----------+--------------+
|                                       | 0        | ``gridDist`` |
+---------------------------------------+----------+--------------+
| `DFTB+ <http://www.dftb-plus.info>`__ | \[]      | \[x]         |
+---------------------------------------+----------+--------------+
| DYLCAO                                | \[]      | \[x]         |
+---------------------------------------+----------+--------------+

.. _variantsSpline:

Spline specifications
---------------------

Please note, that the ``end`` value of the spline intervals are read but not
interpreted by the specific `DFTB+ <http://www.dftb-plus.info>`__
implementation. For this code, the end of a spline interval is taken to be equal
to the start of the next interval.

.. _variantsHubard:

Hubbard U variants
------------------

The mio-0-1 and mio-1-1 data sets replace the Ud and Up values in line 2 of the
:ref:`version0.9` with excited state parameterised values. Hence
this variant cannot be used for shell-resolved calculations, their only being
data for atom resolved SCC contributions.

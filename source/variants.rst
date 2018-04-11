===============
Format variants
===============

Specific implementations of the DFTB method may have different behaviour when
interpreting the SK format.

.. _variantsSPE:
Spin polarization energy
------------------------

The ``SPE`` spin polarization value is read but not interpreted by most current
implementations of the DFTB model.

.. _variantsSK0:
Start of matrix element table
-----------------------------

Different implementations of DFTB have considered the table of Hamiltonian and
overlap matrix element to start at different locations. The first element is
considered to be either at a diatomic distance of 0, or ``gridDist``. The
difference arrises depending on whether the first point in the grid is
considered to be the on-site value or not.

A partial list of the choice made be by different implementations is given
below:

+---------------------------------------+------+--------------+
| Code                                  | 0    | ``gridDist`` |
+---------------------------------------+------+--------------+
| `DFTB+ <http://www.dftb-plus.info>`__ | \[]  | \[x]         |
+---------------------------------------+------+--------------+
| DYLCAO                                | \[]  | \[x]         |
+---------------------------------------+------+--------------+

.. _variantsSpline:
Spline specifications
---------------------

Please note, that the ``end`` value of the spline intervals are read but not
interpreted by the specific `DFTB+ <http://www.dftb-plus.info>`__
implementation. For this code, the end of a spline interval is taken to be equal
to the start of the next interval.

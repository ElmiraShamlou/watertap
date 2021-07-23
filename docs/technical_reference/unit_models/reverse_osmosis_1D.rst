Reverse Osmosis (1D)
====================
This reverse osmosis (RO) unit model
   * is 1-dimensional
   * supports a single liquid phase only
   * supports steady-state only
   * is based on the solution-diffusion model and film theory

.. index::
   pair: proteuslib.unit_models.reverse_osmosis_1D;reverse_osmosis_1D

.. currentmodule:: proteuslib.unit_models.reverse_osmosis_1D

Degrees of Freedom
------------------
Aside from the inlet feed state variables (i.e. temperature, pressure, component flowrates), the RO model has
at least 4 degrees of freedom that should be fixed for the unit to be fully specified.

Typically, the following variables are fixed, in addition to state variables at the inlet:
    * membrane water permeability, A
    * membrane salt permeability, B
    * permeate outlet pressure
    * membrane area *or* length *or* width

.. note::

    This section is pending since the 1D-RO model is currently under development.

Model Structure
------------------
This RO model consists of 1 ControlVolume1DBlock for the feed-side (feed_side.properties[t, x]), a StateBlock indexed by time and space for the permeate-side (permeate_side[t, x]),
and a StateBlock for the final permeate at the outlet (permeate_out).

Sets
----
.. csv-table::
   :header: "Description", "Symbol", "Indices"

   "Time", ":math:`t`", "[0]"
   "Space", ":math:`x`", "Normalized ContinuousSet [0 ... 1] discretized by number of finite elements"
   "Phases", ":math:`p`", "['Liq']"
   "Components", ":math:`j`", "['H2O', 'NaCl']*"

\*Solute depends on the imported property model; example shown here is for the NaCl property model.

.. note::

    Everything below this section is pending since the 1D-RO model is currently under development.

Variables
----------

Refer to the :any:`0dro_variables` section in the  0DRO model.

Equations
-----------

Refer to the :any:`0dro_equations` section in the 0DRO model.


Class Documentation
-------------------

.. automodule:: proteuslib.unit_models.reverse_osmosis_1D
   :members:

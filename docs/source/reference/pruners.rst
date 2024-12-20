.. module:: optuna.pruners

optuna.pruners
==============

The :mod:`~optuna.pruners` module defines a :class:`~optuna.pruners.BasePruner` class characterized by an abstract :meth:`~optuna.pruners.BasePruner.prune` method, which, for a given trial and its associated study, returns a boolean value representing whether the trial should be pruned. This determination is made based on stored intermediate values of the objective function, as previously reported for the trial using :meth:`optuna.trial.Trial.report`. The remaining classes in this module represent child classes, inheriting from :class:`~optuna.pruners.BasePruner`, which implement different pruning strategies.

.. warning::
    Currently :mod:`~optuna.pruners` module is expected to be used only for single-objective optimization.

.. seealso::
    :ref:`pruning` tutorial explains the concept of the pruner classes and a minimal example.

.. seealso::
    :ref:`user_defined_pruner` tutorial could be helpful if you want to implement your own pruner classes.

.. autosummary::
    :toctree: generated/
    :nosignatures:

    BasePruner
    MedianPruner
    NopPruner
    PatientPruner
    PercentilePruner
    SuccessiveHalvingPruner
    HyperbandPruner
    ThresholdPruner
    WilcoxonPruner

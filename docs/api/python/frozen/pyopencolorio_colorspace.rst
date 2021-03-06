..
  SPDX-License-Identifier: CC-BY-4.0
  Copyright Contributors to the OpenColorIO Project.
  Do not edit! This file was automatically generated by share/docs/frozendoc.py.

.. py:class:: ColorSpace
   :module: PyOpenColorIO


   .. py:method:: ColorSpace.__init__(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. __init__(self: PyOpenColorIO.ColorSpace) -> None

      2. __init__(self: PyOpenColorIO.ColorSpace, referenceSpace: PyOpenColorIO.ReferenceSpaceType) -> None

      3. __init__(self: PyOpenColorIO.ColorSpace, referenceSpace: PyOpenColorIO.ReferenceSpaceType = <ReferenceSpaceType.REFERENCE_SPACE_SCENE: 0>, name: str = '', aliases: List[str] = [], family: str = '', encoding: str = '', equalityGroup: str = '', description: str = '', bitDepth: PyOpenColorIO.BitDepth = <BitDepth.BIT_DEPTH_UNKNOWN: 0>, isData: bool = False, allocation: PyOpenColorIO.Allocation = <Allocation.ALLOCATION_UNIFORM: 1>, allocationVars: List[float] = [], toReference: PyOpenColorIO.Transform = None, fromReference: PyOpenColorIO.Transform = None, categories: List[str] = []) -> None


   .. py:method:: ColorSpace.addAlias(self: PyOpenColorIO.ColorSpace, alias: str) -> None
      :module: PyOpenColorIO

      Add an alias for the color space name (the aliases may be used as a synonym for the name). Nothing will be added if the alias is already the color space name, one of its aliases, or the argument is null. The aliases must not conflict with existing roles, color space names, named transform names, or other aliases. This is verified when adding the color space to the config.


   .. py:method:: ColorSpace.addCategory(self: PyOpenColorIO.ColorSpace, category: str) -> None
      :module: PyOpenColorIO

      Add a single category.


      .. note::
         Will do nothing if the category already exists.


   .. py:method:: ColorSpace.clearAliases(self: PyOpenColorIO.ColorSpace) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.clearCategories(self: PyOpenColorIO.ColorSpace) -> None
      :module: PyOpenColorIO

      Clear all the categories.


   .. py:method:: ColorSpace.getAliases(self: PyOpenColorIO.ColorSpace) -> PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getAllocation(self: PyOpenColorIO.ColorSpace) -> PyOpenColorIO.Allocation
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getAllocationVars(self: PyOpenColorIO.ColorSpace) -> List[float]
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getBitDepth(self: PyOpenColorIO.ColorSpace) -> PyOpenColorIO.BitDepth
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getCategories(self: PyOpenColorIO.ColorSpace) -> PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getDescription(self: PyOpenColorIO.ColorSpace) -> str
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getEncoding(self: PyOpenColorIO.ColorSpace) -> str
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getEqualityGroup(self: PyOpenColorIO.ColorSpace) -> str
      :module: PyOpenColorIO

      Get the :ref:`ColorSpace` group name (used for equality comparisons) This allows no-op transforms between different colorspaces. If an equalityGroup is not defined (an empty string), it will be considered unique (i.e., it will not compare as equal to other ColorSpaces with an empty equality group). This is often, though not always, set to the same value as 'family'.


   .. py:method:: ColorSpace.getFamily(self: PyOpenColorIO.ColorSpace) -> str
      :module: PyOpenColorIO

      Get the family, for use in user interfaces (optional) The family string could use a '/' separator to indicate levels to be used by hierarchical menus.


   .. py:method:: ColorSpace.getName(self: PyOpenColorIO.ColorSpace) -> str
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.getReferenceSpaceType(self: PyOpenColorIO.ColorSpace) -> PyOpenColorIO.ReferenceSpaceType
      :module: PyOpenColorIO

      A display color space will use the display-referred reference space.


   .. py:method:: ColorSpace.getTransform(self: PyOpenColorIO.ColorSpace, direction: PyOpenColorIO.ColorSpaceDirection) -> PyOpenColorIO.Transform
      :module: PyOpenColorIO

      If a transform in the specified direction has been specified, return it. Otherwise return a null ConstTransformRcPtr


   .. py:method:: ColorSpace.hasCategory(self: PyOpenColorIO.ColorSpace, category: str) -> bool
      :module: PyOpenColorIO

      Return true if the category is present.


   .. py:method:: ColorSpace.isData(self: PyOpenColorIO.ColorSpace) -> bool
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.removeAlias(self: PyOpenColorIO.ColorSpace, alias: str) -> None
      :module: PyOpenColorIO

      Does nothing if alias is not present.


   .. py:method:: ColorSpace.removeCategory(self: PyOpenColorIO.ColorSpace, category: str) -> None
      :module: PyOpenColorIO

      Remove a category.


      .. note::
         Will do nothing if the category is missing.


   .. py:method:: ColorSpace.setAllocation(self: PyOpenColorIO.ColorSpace, allocation: PyOpenColorIO.Allocation) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setAllocationVars(self: PyOpenColorIO.ColorSpace, vars: List[float]) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setBitDepth(self: PyOpenColorIO.ColorSpace, bitDepth: PyOpenColorIO.BitDepth) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setDescription(self: PyOpenColorIO.ColorSpace, description: str) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setEncoding(self: PyOpenColorIO.ColorSpace, encoding: str) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setEqualityGroup(self: PyOpenColorIO.ColorSpace, equalityGroup: str) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setFamily(self: PyOpenColorIO.ColorSpace, family: str) -> None
      :module: PyOpenColorIO

      Set the family, for use in user interfaces (optional)


   .. py:method:: ColorSpace.setIsData(self: PyOpenColorIO.ColorSpace, isData: bool) -> None
      :module: PyOpenColorIO


   .. py:method:: ColorSpace.setName(self: PyOpenColorIO.ColorSpace, name: str) -> None
      :module: PyOpenColorIO

      If the name is already an alias, that alias is removed.


   .. py:method:: ColorSpace.setTransform(self: PyOpenColorIO.ColorSpace, transform: PyOpenColorIO.Transform, direction: PyOpenColorIO.ColorSpaceDirection) -> None
      :module: PyOpenColorIO

      Specify the transform for the appropriate direction. Setting the transform to null will clear it.


.. py:class:: ColorSpaceCategoryIterator
   :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceCategoryIterator.__getitem__(self: PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator, arg0: int) -> str
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceCategoryIterator.__iter__(self: PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator) -> PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceCategoryIterator.__len__(self: PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator) -> int
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceCategoryIterator.__next__(self: PyOpenColorIO.ColorSpace.ColorSpaceCategoryIterator) -> str
      :module: PyOpenColorIO.ColorSpace


.. py:class:: ColorSpaceAliasIterator
   :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceAliasIterator.__getitem__(self: PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator, arg0: int) -> str
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceAliasIterator.__iter__(self: PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator) -> PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceAliasIterator.__len__(self: PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator) -> int
      :module: PyOpenColorIO.ColorSpace


   .. py:method:: ColorSpaceAliasIterator.__next__(self: PyOpenColorIO.ColorSpace.ColorSpaceAliasIterator) -> str
      :module: PyOpenColorIO.ColorSpace


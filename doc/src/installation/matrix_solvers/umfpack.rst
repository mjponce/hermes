UMFpack
-------

.. _UMFPack home page: http://www.cise.ufl.edu/research/sparse/umfpack/
.. _solvers repository: https://github.com/hpfem/solvers
.. _manual: https://github.com/hpfem/solvers/raw/master/manuals/UMF-UserGuide.pdf

Linux
~~~~~

Using standard Debian packages
``````````````````````````````
Install the `libsuitesparse-metis-3.1.0` and `libsuitesparse-dev` packages.
In Ubuntu 9.10 (Karmic) or newer you can use the Synaptic package manager for that, or type::

    sudo apt-get install libsuitesparse-metis-3.1.0 libsuitesparse-dev

Now go to the directory with Hermes. Create the file CMake.vars with the
following lines (or append to the existing one)::

  set(WITH_UMFPACK YES)

and execute::

  rm CMakeCache.txt
  cmake .
  make
  
Find more about :ref:`ref-usage-umfpack`.

Windows (Cygwin, MinGW, MSVC)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

http://matrixprogramming.com/2008/03/umfpack

Mac OS
~~~~~~

http://mywiki-science.wikispaces.com/UMFPACK

.. _ref-usage-umfpack:

Using UMFPACK in Hermes
~~~~~~~~~~~~~~~~~~~~~~~

After the installation has been completed, you may select ``SOLVER_UMFPACK`` as the matrix solver for your finite element problem,
as detailed in the `Poisson tutorial <http://http://hpfem.org/hermes/doc/src/hermes2d/P01-linear/03-poisson.html>`__, or use
it just to solve a standalone matrix problem :math:`Ax = b` as in the 
`Using Matrix Solvers tutorial <http://http://hpfem.org/hermes/doc/src/hermes2d/P08-miscellaneous/35-matrix-solvers.html>`__.

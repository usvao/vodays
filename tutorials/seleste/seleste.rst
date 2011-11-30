.. vodays documentation file
.. include:: ../../references.rst

:tocdepth: 1

.. _tutorial_seleste:
   
Seleste: A Tool For Querying Remote tables
==========================================

.. contents:: 

Science Story
-------------

The main science story for this tutorial is :ref:`sci_ysos` but one should
also consider reading :ref:`sci_blazars`: the underlying story is how do we
**discover** and merge panchromatic data from different wavelength regimes
to give us insight into underlying physical processes.  

.. topic:: Questions

    * Can we deduce a relationship between the disk flux and X-ray flux that might 
      reveal or constrain their coupling?


Tools and Files
---------------
.. image:: /logo/seleste_logo128.png
   :align: right
   :width: 5 %
.. image:: /logo/topcatc3.gif
   :align: right
   :width: 5 %
   
This tutorial uses the 
  * `Seleste`_ Java based desktop application
  * `TOPCAT`_ Java based desktop application
  
Combining X-ray and near-IR data on Orion
-----------------------------------------
.. image:: /tutorials/seleste/orion.jpg
   :align: right
   :width: 25 %
   :scale: 100 %
 
The goal of this part of the tutorial is to search the Chandra Source Catalog 
for sources near the Orion Nebula and retrieve their flux and positions.
With this data you will then cross-correlate the sources to the 2MASS catalog
with a 1 arcsec radius from each and retrieve their magnitudes.  Using the
merged catalog of X-ray and near-IR measurements we will look for a simple
correlation in flux/magnitude.
  
#. The application starts in the ``Guide mode``. Click on the ``Form`` icon to start building a query.

#. Click on ``Services`` and select  *Chandra Source Catalog (CSC) TAP Service*.  
   This opens the remote tables in the application.
   
#. Now you want to select the columns you wish to retain from this service. 
   Open the *master_source* table in the Contents area on the left.

   #. Select ra, dec, flux_aper90_b and add ``(+)`` in the Output Columns area.

#. We will now build the query to find sources near the center
   of the Orion nebula and that are close to on-axis for Chandra.
   
   #. Select the *err_ellipse_r0* column and add in the Column Criteria. 
   #. Set the filter to ``< 3`` to select on-axis sources; note that the units
      for the column are given in the metadata panel at the bottom of Seleste.
   #. Add a spatial range search: 
      * ``(ra < 83.82) AND ra > 83.78) AND (dec < -5.3) AND dec > -5.5)``
   #. Hit ``Submit``
    
#. In the Jobs window, once the job status shows as Pending hit ``Run``.

#. When the status becomes *Completed* view the results and hit ``Save`` to 
   save them in a file e.g. *csc_orion.xml*
   
   .. note:: If your query fails to run you can continue this tutorial by downloading the :download:`csc_orion.xml` file from here.
      
       
#. Return to the Query form and under ``Services`` select *GAVO Data Center TAP Service*

#. Hit ``Upload`` and upload the table of previously saved Chandra sources 
   (e.g. csc_orion.xml) it will appear as TAP_UPLOAD.user_table in Contents.
   
   #. Select user_table and add all columns into Output Columns.

#. From the GAVO tables select the *twomass.data* table and 
   add the *raj2000, dej2000, Jmag, Hmag and Kmag* columns to the Output Columns.

#. Add a Position Search.

   #. Select TAP_UPLOAD.user_table from drop down menu
   #. Select Center around: Other table and Select Table *twomass.data*
   #. Set Radius 1.0 arcsec
   #. Submit

#. In the Jobs window hit run

#. When completed send results to `TOPCAT`_

   #. Calculate hmag-kmag in TOPCAT
   #. Scatter plot log(flux_aper90_b) vs hmag-kmag color.
   
   
Independent Exercise   
--------------------          

.. topic:: Question
   
   What is the incidence of X-ray activity in different types of galaxies?
   
.. topic:: Approach 
   
   Find optical and X-ray emitting galaxies with redshift > .1 and study 
   their X-ray and optical  properties

.. topic:: Resources & Outline

   Use the *Chandra Source Catalog (CSC) TAP Service* and the 
   *SDSS DR7 - SLoan Digital Sky Survey Data Release 7* services to extract
   the relevant X-ray and Optical Properties.
   
.. topic:: Analysis

   Export the merged catalog to `TOPCAT`_ for visualization and analysis.

You can download the script :download:`seleste_independent_exercise.txt`
for doing this exercise off this website.
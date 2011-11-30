.. vodays documentation file
.. include:: ../../references.rst

:tocdepth: 1

.. _tutorial_portal:
   
Data Discovery Portal: Pan-Archive Search and Retrieval
=======================================================
.. contents:: 

Science Story
-------------

The two science stories for the Discovery Portal tutorial are
:ref:`sci_ttau` and :ref:`sci_mergers`. In both cases we are trying to 
discover images about these objects; in the first case to study the
protostellar binary and in the latter to look for tidal tails indicative
of a merger event. 

.. topic:: Questions

    * What HST ACS images of T Tau are available?
    * Are tidal tails optically visible in NGC 3393?
    * What mid-IR catalogs are available to use for T Tau?

Tools and Files
---------------
   
This tutorial uses the 
    * `Discovery Portal`_ web application
    * `ds9`_ desktop imaging and data visualization application
    * `TOPCAT`_ Java based desktop application
  
Finding High Resolution Images of T Tau
---------------------------------------

#. Load the `Discovery Portal`_ website.

#. Enter "T Tau" as the object. 
#. Given the small size of the object enter 10 and "arcsec" into the search
   radius boxes.

.. note:: The Discovery Portal is an asynchronous search.  New results stream 
   in as remote services respond unless the query has been cached. T Tau r=10s
   will be cached!
   
#. Filter on "Images" in the ``Category`` facet.

#. Enter "ACS" into the free text search to narrow the results list.

#. Select HLA.ACS.  A popup window will tell you about that resource.

#. From the popup window, hit ``Load`` to render the results into a new table.

#. Scan the results different columns reflecting passband, duration, etc.

#. Use the ``Format`` facet to find a JPG version. For each row a popup window
   describes the individual image.  At this point you can spawn a JPG version
   into a new tab.

Finding Infrared Catalogs about T Tau
--------------------------------------
                                    
This example picks up from the previous one, except instead of looking for images
one is looking for catalogs.

#. Reset the filters for "Catalogs" and "Infrared"
#. Load the 2MASS data into a new table.
#. Export the results to one of CSV or if `TOPCAT`_ is open Broadcast the table there.



Independent Exercise
--------------------
  

.. topic:: Question
   
   Can we identify tidal tails in NGC 3393 from archival data? 
   
.. topic:: Approach 
   
   Find optical HST or radio HI images of NGC 3393 and visually inspect them.

.. topic:: Resources & Outline

   Target HST ACS datasets.
   
.. topic:: Analysis

   Download the images and load them into ds9. 

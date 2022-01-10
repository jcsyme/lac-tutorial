===========================================
Agriculture, Forestry, and Land Use (AFOLU)
===========================================


Agriculture
===========

The **Agriculture** subsector is used to quantify emissions associated with growing crops, including emissions from the release of soil carbon, fertilizer applications and crop liming, crop burning, methane emissions from paddy rice fields, **AND MORE;CONTINUE**. Agriculture is divided into the following categories (crops), given by the metavariable ``$CAT-AGRICULTURE$``. Each crop should be associated an FAO classifications. `See the FAO <https://www.fao.org/waicent/faoinfo/economic/faodef/annexe.htm>`_ for the source of these classifications and a complete mapping of crop types to categories. On the git, the table ``ingestion/FAOSTAT/ref/attribute_fao_crop.csv`` contains the information mapping each crop to this crop type. Note, this table can be used to merge and aggregate data from FAO into these categories. If a crop type is not present in a country, set the associated area as a fraction of crop area to 0.

Variables by Category
---------------------

Agriculture requires the following variables.

.. csv-table:: For each agricultural category, trajectories of the following variables are needed.
   :file: ./csvs/table_varreqs_by_category_af_agrc.csv
   :widths: 20, 30, 30, 10, 10
   :header-rows: 1

Categories
----------

Agriculture is divided into the following categories.

.. csv-table:: Agricultural categories (``$CAT-AGRICULTURE$`` attribute table)
   :file: ./csvs/attribute_cat_agriculture.csv
   :widths: 15,15,30,15,10,15
   :header-rows: 1


**Costs to be added**

----

Forestry
========

Variables by Category
---------------------

.. csv-table:: For each forest category, trajectories of the following variables are needed.
   :file: ./csvs/table_varreqs_by_category_af_frst.csv
   :widths: 20, 30, 30, 10, 10
   :header-rows: 1

Categories
----------

Forestry is divided into the following categories. These categories reflect an aggregation of forestry types into emission-relevant categories.

.. csv-table:: Forest categories (``$CAT-FOREST$`` attribute table)
   :file: ./csvs/attribute_cat_forest.csv
   :widths: 15,15,30,15,10,15
   :header-rows: 1

----

Land Use
========

Variables by Category
---------------------

.. csv-table:: For each land use category, trajectories of the following variables are needed.
   :file: ./csvs/table_varreqs_by_category_af_lndu.csv
   :widths: 20, 30, 30, 10, 10
   :header-rows: 1

Variables by Partial Category
-----------------------------

Land use includes some variables that apply only to a subset of categories. These variables are described below. The categories that variables apply to are described in the ``category`` column.

.. note::
   Note that the sum of all land use categories *u* at time period *t* should be should equal 1, i.e. :math:`\sum_u \varphi_u(t) = 1`, where :math:`\varphi_{\text{$CAT-LANDUSE$}}(t) \to` ``frac_lu_$CAT-LANDUSE$`` at period *t*.

.. csv-table:: Trajectories of the following variables are needed for **some** land use categories.
   :file: ./csvs/table_varreqs_by_partial_category_afolu_lndu.csv
   :widths: 20, 25, 25, 10, 10, 10
   :header-rows: 1

Categories
----------

Land use should be divided into the following categories, given by ``$CAT-LANDUSE$``.

.. csv-table:: Land Use categories (``$CAT-LANDUSE$`` attribute table)
   :file: ./csvs/attribute_cat_land_use.csv
   :widths: 15,15,30,15,10,15
   :header-rows: 1

----


Livestock
=========

For each category, the following variables are needed. Information on enteric fermentation can be found from `the EPA <https://www3.epa.gov/ttnchie1/ap42/ch14/final/c14s04.pdf>`_ and **ADDITIONAL LINKS HERE**.

Variables by Category
---------------------

.. csv-table:: For each livestock category, trajectories of the following variables are needed.
   :file: ./csvs/table_varreqs_by_category_af_lvst.csv
   :widths: 20, 30, 30, 10, 10
   :header-rows: 1

Categories
----------

Livestock should be divided into the following categories, given by ``$CAT-LIVESTOCK$``.

.. csv-table:: Livestock categories (``$CAT-LIVESTOCK$`` attribute table)
   :file: ./csvs/attribute_cat_livestock.csv
   :widths: 15,15,30,15,10,15
   :header-rows: 1

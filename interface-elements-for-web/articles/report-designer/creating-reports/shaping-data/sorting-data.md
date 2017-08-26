---
title: Sorting Data
author: Anya Vekhina
legacyId: 114685
---
# Sorting Data
This document demonstrates how to sort data within a report's detail area and within groups. Note that as with data grouping, sorting can be performed only if a report is [bound to a data source](../providing-data/bind-a-report-to-data.md). In this example, we'll use the report created in the following tutorial: [Grouping Data](grouping-data.md).

To sort records in a data-aware report, do the following.
1. Select the [Detail Band](../../report-elements/report-bands.md) and expand the **Actions** category. Then, in the **Sort Fields** section, click the **Add** button to add a new sorting.
	
	![eud-sorting-data-0](../../../../images/img119667.png)
2. Now, choose a data member across which the report is to be sorted. Note that sorting across [calculated fields](../providing-data/calculated-fields.md) is supported as well.
	
	![eud-sorting-data-1](../../../../images/img119668.png)
3. To manage the sorting order, use the arrow button for the **Sort By** drop-down list. The ![eud-grouping-data-4](../../../../images/img119657.png) and ![WebRD_SortDiscendingButton](../../../../images/img125204.png) icons indicate the ascending and descending sorting order, respectively. To disable sorting, click this button until it is marked with the ![WebRD_NoSortButton](../../../../images/img125205.png) icon.
	
	If multiple sorting criteria are specified, you can define the priority for each one, using the **Move Up** ![eud-sorting-data-3](../../../../images/img119670.png) and **Move Down** ![eud-sorting-data-4](../../../../images/img119671.png) buttons.

Sorting is now applied. Switch your report to the [Preview](../../document-preview.md) mode and view the result.

![eud-sorting-data-2](../../../../images/img119669.png)
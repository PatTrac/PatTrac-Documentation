---
title: Master-Detail Relation Editor
author: Anna Gubareva
legacyId: 117816
---
# Master-Detail Relation Editor
When a data source contains two or more [queries](../wizards/sql-data-source-wizard/adding-a-new-data-source/create-a-query-or-select-a-stored-procedure.md), clicking the ![web-designer-field-list-data-source-edit-relationships](../../../images/img125720.png) button in the [Field List](field-list.md) will invoke the **Master-Detail Relation Editor**.

![web-report-designer-field-list-edit-relations](../../../images/img125807.png)

Using this editor, you can define master-detail relationships between queries by specifying their corresponding key fields.

![web-report-designer-master-detail-relation-editor](../../../images/img125806.png)

This allows you to create hierarchical data sources that are used to create nested [master-detail reports](../report-types/master-detail-report-(detail-report-bands).md).

> [!NOTE]
> Although it is also possible to [join different tables](query-builder.md) within a single query, creating hierarchical data sources is preferred in most cases to provide better performance (in general, master-detail reports are generated faster than similar-looking reports created by grouping "flat" data sources).
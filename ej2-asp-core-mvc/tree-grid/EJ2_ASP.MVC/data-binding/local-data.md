---
layout: post
title: Local Data in ##Platform_Name## Tree Grid Component | Syncfusion
description: Learn here all about Local Data in Syncfusion ##Platform_Name## Tree Grid component of Syncfusion Essential JS 2 and more.
platform: ej2-asp-core-mvc
control: Local Data
publishingplatform: ##Platform_Name##
documentation: ug
---


# Local Data in ##Platform_Name## Tree Grid Component

In Local Data binding, data source for rendering the TreeGrid control is retrieved from the same application locally.

Two types of Data binding are possible with the TreeGrid control.

* Hierarchical Datasource binding
* Self-Referential Data binding (Flat Data)

To bind local data to the treegrid, you can assign a JavaScript object array to the [`DataSource`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/Syncfusion.EJ2~Syncfusion.EJ2.TreeGrid.TreeGrid~DataSource.html) property. The local data source can also be provided as an instance of the **DataManager**.

> By default, **DataManager** uses **JsonAdaptor** for local data-binding.

## Hierarchy data source binding

The [`ChildMapping`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/Syncfusion.EJ2~Syncfusion.EJ2.TreeGrid.TreeGrid~ChildMapping.html) property is used to map the child records in hierarchy data source.

The following code example shows you how to bind the hierarchical local data into the TreeGrid control.

{% if page.publishingplatform == "aspnet-core" %}

{% tabs %}
{% highlight c# tabtitle="Local-data.cs" %}
{% include code-snippet/tree-grid/data-binding-mvc/local-data/local-data.cs %}
{% endhighlight %}
{% endtabs %}

{% elsif page.publishingplatform == "aspnet-mvc" %}

{% tabs %}
{% highlight razor tabtitle="CSHTML" %}
{% include code-snippet/tree-grid/data-binding-mvc/local-data/razor %}
{% endhighlight %}
{% highlight c# tabtitle="Local-data.cs" %}
{% include code-snippet/tree-grid/data-binding-mvc/local-data/local-data.cs %}
{% endhighlight %}
{% endtabs %}
{% endif %}



> * Remote data binding is not supported for Hierarchy Data.

## Self-Referential data binding (Flat data)

TreeGrid is rendered from Self-Referential data structures by providing two fields, ID field and parent ID field.

* **ID Field**: This field contains unique values used to identify nodes. Its name is assigned to the [`IdMapping`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/aspnetcore/Syncfusion.EJ2~Syncfusion.EJ2.TreeGrid.TreeGridBuilder~IdMapping.html) property.

* **Parent ID Field**: This field contains values that indicate parent nodes. Its name is assigned to the [`ParentIdMapping`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/aspnetcore/Syncfusion.EJ2~Syncfusion.EJ2.TreeGrid.TreeGridBuilder~ParentIdMapping.html) property.

{% if page.publishingplatform == "aspnet-core" %}

{% tabs %}
{% highlight c# tabtitle="Self-reference.cs" %}
{% include code-snippet/tree-grid/data-binding-mvc/self-reference/self-reference.cs %}
{% endhighlight %}
{% endtabs %}

{% elsif page.publishingplatform == "aspnet-mvc" %}

{% tabs %}
{% highlight razor tabtitle="CSHTML" %}
{% include code-snippet/tree-grid/data-binding-mvc/self-reference/razor %}
{% endhighlight %}
{% highlight c# tabtitle="Self-reference.cs" %}
{% include code-snippet/tree-grid/data-binding-mvc/self-reference/self-reference.cs %}
{% endhighlight %}
{% endtabs %}
{% endif %}



> Herewith we have provided list of reserved properties and the purpose used in TreeGrid. We recommend to avoid these reserved properties for Internal purpose(To get rid of conflicts).

Reserved keywords | Purpose
-----|-----
childRecords | Specifies the childRecords of a parentData
hasChildRecords | Specifies whether the record contains child records
hasFilteredChildRecords | Specifies whether the record contains filtered child records
expanded | Specifies whether the child records are expanded
parentItem | Specifies the parentItem of childRecords
index | Specifies the index of current record
level | Specifies the hierarchy level of record
filterLevel | Specifies the hierarchy level of filtered record
parentIdMapping | Specifies the parentID
uniqueID | Specifies the unique ID of a record
parentUniqueID | Specifies the parent Unique ID of a record
checkboxState | Specifies the checkbox state of a record
isSummaryRow | Specifies the summary of a record
taskData | Specifies the main data
primaryParent | Specifies the Primary data



> You can refer to our [`ASP.NET MVC Tree Grid`](https://www.syncfusion.com/aspnet-mvc-ui-controls/tree-grid) feature tour page for its groundbreaking feature representations. You can also explore our [`ASP.NET MVC Tree Grid example`](https://ej2.syncfusion.com/aspnetmvc/TreeGrid/Overview#/material) to knows how to present and manipulate data.
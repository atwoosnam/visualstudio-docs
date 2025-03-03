---
title: "How to: Fill ListObject controls with data"
description: Use data binding to quickly add data to your document. You can also disconnect the list object so it displays the data but is no longer bound to the data source.
ms.custom: SEO-VS-2020
ms.date: "02/02/2017"
ms.topic: "how-to"
dev_langs:
  - "VB"
  - "CSharp"
helpviewer_keywords:
  - "disconnecting from data sources"
  - "ListObject control, disconnecting from a data source"
  - "ListObject control, filling with data"
  - "data [Office development in Visual Studio], adding to worksheets"
  - "data binding, ListObject controls"
  - "worksheets, populating with data"
author: John-Hart
ms.author: johnhart
manager: jmartens
ms.technology: office-development
ms.workload:
  - "office"
---
# How to: Fill ListObject controls with data

 [!INCLUDE [Visual Studio](~/includes/applies-to-version/vs-windows-only.md)]
  You can use data binding as a way to quickly add data to your document. After binding data to a list object, you can disconnect the list object so it displays the data but is no longer bound to the data source.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

### To bind data to a ListObject control

1. Create a <xref:System.Data.DataTable> at the class level.

     ### [C#](#tab/csharp)
     :::code language="csharp" source="../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet4.cs" id="Snippet20":::

     ### [VB](#tab/vb)
     :::code language="vb" source="../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet4.vb" id="Snippet20":::
     ---

2. Add sample columns and data in the `Startup` event handler of the `Sheet1` class (in a document-level project) or `ThisAddIn` class (in an application-level project).

     ### [C#](#tab/csharp)
     :::code language="csharp" source="../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet4.cs" id="Snippet21":::

     ### [VB](#tab/vb)
     :::code language="vb" source="../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet4.vb" id="Snippet21":::
     ---

3. Call the <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> method and pass in the column names in the order they should appear. The order of the columns in the list object can differ from the order in which they appear in the <xref:System.Data.DataTable>.

     ### [C#](#tab/csharp)
     :::code language="csharp" source="../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet4.cs" id="Snippet22":::

     ### [VB](#tab/vb)
     :::code language="vb" source="../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet4.vb" id="Snippet22":::
     ---

### To disconnect the ListObject control from the data source

1. Call the <xref:Microsoft.Office.Tools.Excel.ListObject.Disconnect%2A> method of `List1`.

     ### [C#](#tab/csharp)
     :::code language="csharp" source="../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet4.cs" id="Snippet23":::

     ### [VB](#tab/vb)
     :::code language="vb" source="../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet4.vb" id="Snippet23":::
     ---

## Compile the code
 This code example assumes you have an existing <xref:Microsoft.Office.Tools.Excel.ListObject> named `list1` on the worksheet in which this code appears.

## See also
- [Extend Word documents and Excel workbooks in VSTO Add-ins at run time](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Controls on Office documents](../vsto/controls-on-office-documents.md)
- [Add controls to Office documents at run time](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [How to: Map ListObject columns to data](../vsto/how-to-map-listobject-columns-to-data.md)
- [Automate Excel by using extended objects](../vsto/automating-excel-by-using-extended-objects.md)
- [ListObject control](../vsto/listobject-control.md)
- [Bind data to controls in Office solutions](../vsto/binding-data-to-controls-in-office-solutions.md)
- [How to: Populate worksheets with data from a database](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)
- [How to: Populate documents with data from services](../vsto/how-to-populate-documents-with-data-from-services.md)

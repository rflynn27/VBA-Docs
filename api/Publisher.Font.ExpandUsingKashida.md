---
title: Font.ExpandUsingKashida property (Publisher)
keywords: vbapb10.chm5374004
f1_keywords:
- vbapb10.chm5374004
ms.prod: publisher
api_name:
- Publisher.Font.ExpandUsingKashida
ms.assetid: ecf3a170-5f07-379e-ff56-504beb770308
ms.date: 06/08/2019
ms.localizationpriority: medium
---


# Font.ExpandUsingKashida property (Publisher)

Returns or sets an **[MsoTriState](Office.MsoTriState.md)** constant indicating whether to apply kashida rules while applying tracking to Arabic text. Read/write.


## Syntax

_expression_.**ExpandUsingKashida**

_expression_ A variable that represents a **[Font](Publisher.Font.md)** object.


## Return value

MsoTriState


## Remarks

The **ExpandUsingKashida** property value can be one of the **MsoTriState** constants declared in the Microsoft Office type library and shown in the following table.

|Constant|Description|
|:-----|:-----|
| **msoFalse**| Microsoft Publisher does not apply kashida rules while applying tracking to Arabic text.|
| **msoTriStateMixed**|A return value indicating a combination of **msoTrue** and **msoFalse** for the specified text range.|
| **msoTriStateToggle**|A set value that switches between **msoTrue** and **msoFalse**.|
| **msoTrue**| Publisher does apply kashida rules while applying tracking to Arabic text.|

## Example

The following example sets Publisher to apply kashida rules while applying tracking to Arabic text for all text ranges on page one of the active publication.

```vb
Dim shpLoop As Shape 
 
For Each shpLoop In ActiveDocument.Pages(1).Shapes 
 If shpLoop.HasTextFrame Then 
 shpLoop.TextFrame.TextRange _ 
 .Font.ExpandUsingKashida = msoTrue 
 End If 
Next shpLoop
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
---
title: Report.OpenArgs property (Access)
keywords: vbaac10.chm13809
f1_keywords:
- vbaac10.chm13809
ms.prod: access
api_name:
- Access.Report.OpenArgs
ms.assetid: 91dcbf42-6bb8-73e5-744c-de82d8668f9c
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Report.OpenArgs property (Access)

Determines the string expression specified by the _OpenArgs_ argument of the **[OpenReport](access.docmd.openreport.md)** method that opened a report. Read/write **Variant**.


## Syntax

_expression_.**OpenArgs**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

This property is available only by using a macro or by using Visual Basic with the **OpenReport** method of the **DoCmd** object. This property setting is read-only in all views.

To use the **OpenArgs** property, open a report by using the **OpenReport** method of the **DoCmd** object, and set the _OpenArgs_ argument to the desired string expression. The **OpenArgs** property setting can then be used in code for the report, such as in an **Open** event procedure. 

You can also refer to the property setting in a macro, such as an Open macro, or an expression, such as an expression that sets the **ControlSource** property for a control on the form.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
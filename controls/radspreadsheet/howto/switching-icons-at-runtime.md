---
title:  Switching Icons at Runtime
page_title:  Switching Icons at Runtime
description:  Switching Icons at Runtime
slug: radspreadsheet-howto-switching-icons-at-runtime
tags: switching,themes,icons,at,runtime
published: True
position: 7
---

# Switching Icons at Runtime


The __IconResource__ extension is a markup extension that allows you to switch icons in your application at runtime. More information on the approach is available [here]({%slug styling-apperance-switching-icons-at-runtime%}).


## Using Available IconSets

__RadSpreadsheet__ comes with two separate sets of icons that can be used in its UI. They reside in the __Telerik.Windwos.Controls.Spreadsheet.dll__ and defining an __IconSources__ resource for them is demonstrated in __Example 1__.


#### __[XAML] Example 1: Creating IconSources__

{{region radspreadsheet-howto-switching-icons-at-runtime_0}}
	<telerik:IconSources x:Key="SpreadsheetIconPaths" LightBasePath="/Telerik.Windows.Controls.Spreadsheet;component/Images/Light/"
                               DarkBasePath="/Telerik.Windows.Controls.Spreadsheet;component/Images/Dark/"/>
{{endregion}}


>tipTo browse all icons you can download the source code of the controls from your Telerik account. The images are located at \Telerik_UI_for_WPF_Source_[Version]\Documents\ Spreadsheet\Controls\Images\Light.


# See Also

* [IconResource]({%slug styling-apperance-switching-icons-at-runtime%})
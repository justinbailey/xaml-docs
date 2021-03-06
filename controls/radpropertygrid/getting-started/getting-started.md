---
title: Getting Started
page_title: Getting Started
description: Getting Started
slug: radpropertygrid-getting-started-getting-started
tags: getting,started
published: True
position: 0
---

# Getting Started with RadPropertyGrid


This tutorial will walk you through the creation of a sample application that contains RadPropertyGrid and will show you how to: 

* Use a RadPropertyGrid in your project

* Bind a RadPropertyGrid to a single item

For the purpose of this example, you will need to create an empty {% if site.site_name == 'Silverlight' %}Silverlight{% endif %}{% if site.site_name == 'WPF' %}WPF{% endif %} Application project and open it in Visual Studio. 


>In order to use RadPropertyGrid in your projects, you have to add references to the following assemblies:
>* __Telerik.Windows.Controls__
>* __Telerik.Windows.Controls.Data__
>* __Telerik.Windows.Data__
>* __Telerik.Windows.Controls.Input__

>You can find more info [here](http://www.telerik.com/help/wpf/installation-installing-controls-dependencies-wpf.html).


* Create a new {% if site.site_name == 'Silverlight' %}Silverlight{% endif %}{% if site.site_name == 'WPF' %}WPF{% endif %} project;



* Add RadPropertyGrid as demonstrated below:{% if site.site_name == 'Silverlight' %}

#### __[XAML]Example 1: Adding RadPropertyGrid__

{{region radpropertygrid-getting-started-getting-started_0}}

	<UserControl x:Class="RadPropertyGrid_SL.MainPage"
	    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
	    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
	    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
	    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
	    xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation"
	    mc:Ignorable="d"
	    d:DesignHeight="300" d:DesignWidth="400">
	 <Grid x:Name="LayoutRoot" Background="White">
	       <telerik:RadPropertyGrid x:Name="PropertyGrid1" /> 
	 </Grid>
	</UserControl>
	
{{endregion}}

{% endif %}{% if site.site_name == 'WPF' %}

#### __[XAML]Example 1: Adding RadPropertyGrid__

{{region radpropertygrid-getting-started-getting-started_1}}

	<Window x:Class="RadPropertyGrid_WPF.Window"
	    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
	    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
	    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
	    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
	    xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation" 
	    mc:Ignorable="d"
	    d:DesignHeight="300" d:DesignWidth="400">
	 <Grid x:Name="LayoutRoot" Background="White">
	  <telerik:RadPropertyGrid x:Name="PropertyGrid1" /> 
	 </Grid>
	</Window>
{{endregion}}

{% endif %}



Two lines of code are important here:

* The import of the Telerik schema:

#### __[XAML]Example 2: Importing Telerik schema__

{{region radpropertygrid-getting-started-getting-started_2}}

	xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation"
{{endregion}}



* The declaration of the RadPropertyGrid control inside the Grid:

#### __[XAML]Example 3: Declaring RadPropertyGrid__

{{region radpropertygrid-getting-started-getting-started_3}}

	<Grid x:Name="LayoutRoot" Background="White">
	  <telerik:RadPropertyGrid x:Name="PropertyGrid1" /> 
	</Grid>
{{endregion}}



Now, if you run your application, you will see an empty RadPropertyGrid:


![](images/RadPropertyGrid_GettingStarted1.png)

## Binding a RadPropertyGrid to an item

* Binding to a data item - you may bind RadPropertyGrid to a single data item. Thus, you will be able to examine and edit its properties. The only thing you need is to set the Item property of RadPropertyGrid. The binding may be performed both in xaml and in the code behind.

#### __[C#]Example 4: Binding to data item__

{{region radpropertygrid-getting-started-getting-started_4}}

	this.PropertyGrid1.Item = new Employee() 
	   { FirstName = "Sarah",
	    LastName = "Blake", 
	    Occupation = "Supplied Manager", 
	    StartingDate = new DateTime(2005, 04, 12), 
	    IsMarried = true, Salary = 3500, Gender = Gender.Female 
	   };
{{endregion}}



#### __[VB.NET]Example 4: Binding to data item__

	
{{region radpropertygrid-getting-started-getting-started_5}}

	Me.PropertyGrid1.Item = New Employee() With { _
	  .FirstName = "Sarah", _
	  .LastName = "Blake", _
	  .Occupation = "Supplied Manager", _
	  .StartingDate = New DateTime(2005, 4, 12), _
	  .IsMarried = True, _
	  .Salary = 3500, _
	  .Gender = Gender.Female _
	}
{{endregion}}



Once you set the Item and run the application, you will see a RadPropertyGrid:

![](images/RadPropertyGrid_GettingStarted2.png)



* Binding to a visual element - you may bind the Item property of RadPropertyGrid to a visual element and again be able to view and edit its properties. The binding may be performed both in xaml and in the code behind:

#### __[XAML]Example 5: Binding to visual element__

{{region radpropertygrid-getting-started-getting-started_6}}

	<telerik:RadButton x:Name="button1" Content="MyButton" />
	<telerik:RadPropertyGrid x:Name="PropertyGrid1" Item="{Binding ElementName= button1}"/>
{{endregion}}



When you run the application, you will see a RadPropertyGrid:

![](images/RadPropertyGrid_GettingStarted3.png)



## Binding a PropertyDefinition to an existing property

* Binding to an existing property - you may bind the PropertyDefinition to a property of the data item. Thus you will be able to examine and edit this property.
        

#### __[XAML]Example 6: Binding to a property of data item__

{{region radpropertygrid-getting-started-getting-started_10}}

	  <telerik:RadPropertyGrid x:Name="PropertyGrid1"> 
	        <telerik:RadPropertyGrid.PropertyDefinitions>                
	                <telerik:PropertyDefinition Binding="{Binding FirstName}" DisplayName="My FirstName"/>
	        </telerik:RadPropertyGrid.PropertyDefinitions>
	  </telerik:RadPropertyGrid>
{{endregion}}

## Nested Properties in a RadPropertyGrid
Please check the article about [Nested Properties]({%slug radpropertygrid-nested-properties%}).
        

## Other properties of a RadPropertyGrid
__LabelColumnWidth:__ You could change the width of the first column in the RadPropertyGrid by setting a value for this property of the RadPropertyGrid.
        

__IsGrouped:__ Controls the current RadPropertyGrid's state. You can set it to true and you will have RadPropertyGrid initially grouped. If you set it to false, then you will have RadPropertyGrid sorted.
       

__AutoGeneratePropertyDefinitions:__  Indicates whether property definitions will be autogenerated.
        

__DescriptionPanelVisibility:__ Sets the visibility mode of the description panel.
        

__CanUserResizeDescriptionPanel:__ Indicates whether the user can resize the description panel.


__Item:__ Returns the item to edit.
        

__PropertyDefinitions:__ Returns a collection of PropertyDefinitions describing the properties displayed or edited by RadPropertyGrid.
        

__SearchBoxVisibility:__ Sets the visibility mode of the search box.
        

__SortAndGroupButtonsVisibility:__ Sets the visibility mode of the sort and group buttons.
        

## Localization of a RadPropertyGrid

Since Q3 SP1 2012, we have added Localization for __CollectionEditor__. Please check the common article about [Localization]({%slug common-localization%}).

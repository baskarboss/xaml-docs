---
title: Modifying TileList view
page_title: Modifying TileList view
description: Modifying TileList view
slug: radtilelist-modifying-tilelist-view
tags: modifying,tilelist,view
published: True
position: 1
---

# Modifying TileList view



## VerticalTilesAlignment

RadTileList exposes VerticalTilesAlignment property that controls the position of the tiles independently of the group they belong to. It can be set no matter if being in a grouped state or not. Its type is of type VerticalAlignment and the default value is Center. Modifying it will result in: 

* Top {% if site.site_name == 'Silverlight' %}
![Vertical Tiles Alignment Top SL](images/VerticalTilesAlignment_Top_SL.PNG){% endif %}{% if site.site_name == 'WPF' %}

![Vertical Tiles Alignment Top WPF](images/VerticalTilesAlignment_Top_WPF.PNG){% endif %}

* Bottom {% if site.site_name == 'Silverlight' %}
![Vertical Tiles Alignment Bottom SL](images/VerticalTilesAlignment_Bottom_SL.PNG){% endif %}{% if site.site_name == 'WPF' %}
![Vertical Tiles Alignment Bottom WPF](images/VerticalTilesAlignment_Bottom_WPF.PNG){% endif %}

## GroupTemplate

__RadTileList__ has __GroupTemplate__ property that control the way the header of a groups looks.
        

For example:        

#### __XAML__

{{region radtilelist-modifying-tilelist-view-0}}

			<Grid.Resources>
				<DataTemplate x:Key="GroupTemplate">
					<TextBlock Text="{Binding}" FontWeight="Bold" Foreground="#FF006AC1" FontSize="20"/>
				</DataTemplate>
			</Grid.Resources>
	
			<telerik:RadTileList x:Name="RadTileList" 
	                      GroupMember="Occupation"
	                      ItemsSource="{Binding Employees}"
	                      ItemTemplate="{StaticResource ItemTemplate}"/>
	
	
{{endregion}}


{% if site.site_name == 'Silverlight' %}
![Group Template SL](images/GroupTemplate_SL.PNG){% endif %}{% if site.site_name == 'WPF' %}
![Group Template WPF](images/GroupTemplate_WPF.PNG){% endif %}

## GroupHeaderVisibility

__RadTileList__ exposes a __GroupHeaderVisibility__ property that sets whether the headers of the groups will be visible or not. Thus, once you set it to collapse, your control will be organized in groups, but will not have any text above:
        

#### __XAML__

{{region radtilelist-modifying-tilelist-view-1}}

			<telerik:RadTileList x:Name="RadTileList" 
	                             GroupHeaderVisibility="Collapsed"/>
{{endregion}}

{% if site.site_name == 'Silverlight' %}
![Group Header Visibility SL](images/GroupHeaderVisibility_SL.PNG){% endif %}{% if site.site_name == 'WPF' %}
![Group Header Visibility WPF](images/GroupHeaderVisibility_WPF.PNG){% endif %}

## GroupHeaderHeight

__RadTileList__ gives the opportunity to set the height of the headers with a single property __GroupHeaderHeight__.
        

#### __XAML__

{{region radtilelist-modifying-tilelist-view-2}}

			<telerik:RadTileList x:Name="RadTileList" 
	                        GroupHeaderHeight="100"
	                        GroupTemplate="{StaticResource GroupTemplate}"
	                        ItemsSource="{Binding Source={StaticResource GroupedItems}}"
	                        ItemTemplate="{StaticResource ItemTemplate}"/>
	
{{endregion}}

{% if site.site_name == 'Silverlight' %}
![Group Header Height SL](images/GroupHeaderHeight_SL.PNG){% endif %}{% if site.site_name == 'WPF' %}
![Group Header Height WPF](images/GroupHeaderHeight_WPF.PNG){% endif %}

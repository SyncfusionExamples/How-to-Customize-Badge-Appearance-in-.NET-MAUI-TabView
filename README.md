This article explains how to customize the `badge` appearance in the [.NET MAUI TabView](https://www.syncfusion.com/maui-controls/maui-tab-view).

To fully customize the badge in the `TabView`, you can set the [Type](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.BadgeSettings.html#Syncfusion_Maui_Core_BadgeSettings_Type) property in [BadgeSettings](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.TabView.SfTabItem.html#Syncfusion_Maui_TabView_SfTabItem_BadgeSettings) to [None.](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.BadgeType.html#Syncfusion_Maui_Core_BadgeType_None) This allows you to customize the badge beyond predefined styles by explicitly specifying properties such as [Background](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.BadgeSettings.html#Syncfusion_Maui_Core_BadgeSettings_Background) and [TextColor.](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.BadgeSettings.html#Syncfusion_Maui_Core_BadgeSettings_TextColor)

```
<ContentPage ...
             xmlns:core="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"
             xmlns:tabView="clr-namespace:Syncfusion.Maui.TabView;assembly=Syncfusion.Maui.TabView">
    <tabView:SfTabView x:Name="tabView" >
        <tabView:SfTabView.Items>
            <tabView:SfTabItem Header="Call" BadgeText="3">
                <tabView:SfTabItem.BadgeSettings>
                    <core:BadgeSettings Type="None" Background="GreenYellow" TextColor="Red" TextPadding="3"/>
                </tabView:SfTabItem.BadgeSettings>
                <tabView:SfTabItem.Content>
                    <ListView RowHeight="50">
                        <ListView.ItemsSource>
                            <x:Array Type="{x:Type x:String}">
                                <x:String>James</x:String>
                                <x:String>Richard</x:String>
                                <x:String>Michael</x:String>
                                <x:String>Alex</x:String>
                                <x:String>Clara</x:String>
                            </x:Array>
                        </ListView.ItemsSource>
                        <ListView.ItemTemplate>
                            <DataTemplate>
                                <ViewCell>
                                    <Grid Margin="10,5">
                                        <Label VerticalOptions="Start"
                                                        HorizontalOptions="Start"
                                                        TextColor="#666666"
                                                        FontSize="16"
                                                        Text="{Binding}" />
                                    </Grid>
                                </ViewCell>
                            </DataTemplate>
                        </ListView.ItemTemplate>
                    </ListView>
                </tabView:SfTabItem.Content>
            </tabView:SfTabItem>
        </tabView:SfTabView.Items>
    </tabView:SfTabView>
</ContentPage>
```

By setting Type to None in `BadgeSettings`, you gain complete control over the appearance of the badge in `TabView`. 

**Output**

![Badge_TabView.png](https://support.syncfusion.com/kb/agent/attachment/article/19038/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjM1NDcwIiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.yhYPKUx65LD0fAC0N7qy5QPN1KtwYzHXlZ2fFjaMhls)
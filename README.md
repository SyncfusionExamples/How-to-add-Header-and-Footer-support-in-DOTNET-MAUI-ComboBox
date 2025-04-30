# How-to-add-Header-and-Footer-support-in-DOTNET-MAUI-ComboBox
This repository contains a sample demonstrating of Header and Footer support in .NET MAUI ComboBox.

## Header and Footer support in .NET MAUI ComboBox (SfComboBox)


You can provide header and footer views in the dropdown in SfComboBox by enabling the ShowDropDownHeaderView and the ShowDropDownFooterView properties.

## Header content
You can provide content for header at the top of the ComboBox’s dropdown. The DropDownHeaderView property is used to set the content of the header. The height of the header in the SfComboBox can be adjusted using the DropDownHeaderViewHeight property.

**XAML**

```
<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
        <combobox:SfComboBox HeightRequest="40"
                            x:Name="comboBox" 
                            IsEditableMode="true" 
                            DisplayMemberPath="Name" 
                            ItemsSource="{Binding SocialMedias}" 
                            AllowFiltering="true">
            <combobox:SfComboBox.DropDownHeaderView>
                <StackLayout BackgroundColor="#f0f0f0" >
                    <Label  x:Name="label2" 
                            FontSize="20" 
                            VerticalTextAlignment="Center" 
                            HorizontalOptions="Center" 
                            VerticalOptions="Center" 
                            TextColor="#006bcd" />
                </StackLayout>
            </combobox:SfComboBox.DropDownHeaderView>        
        </combobox:SfComboBox>
    </StackLayout>
```

## Footer content
You can provide content for footer at the bottom of the ComboBox’s dropdown. The DropDownFooterView property is used to set the content for footer. The height of the footer in the SfComboBox can be adjusted using the DropDownFooterViewHeight property.

The following code example shows how to set footer content in SfComboBox.

**XAML**
```
<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
        <combobox:SfComboBox HeightRequest="40" 
                             ItemsSource="{Binding SocialMedias}" 
                             DisplayMemberPath="Name" 
                             x:Name="comboBox" 
                             IsEditableMode="true" 
                             AllowFiltering="true">
            <combobox:SfComboBox.DropDownFooterView>
                <StackLayout BackgroundColor="#f0f0f0" >
                    <Label Text="Add New" 
                           BackgroundColor="#f0f0f0" 
                           TextColor="#006bcd" 
                           VerticalTextAlignment="Center" 
                           VerticalOptions="Center" 
                           HorizontalTextAlignment="Center" 
                           FontSize="20"/>
                </StackLayout>
            </combobox:SfComboBox.DropDownFooterView>
        </combobox:SfComboBox>
    </StackLayout>
```
# How-to-add-Header-and-Footer-support-in-DOTNET-MAUI-ComboBox
This repository contains a sample demonstrating Header and Footer support in .NET MAUI ComboBox.

**Step 1:** Initialize the ComboBox control in the XAML page with all required assemblies.

**XAML:**
```
<editors:SfComboBox x:Name="comboBox"/>
```
**Step 2:** Create the Model class with the properties that need to be assigned.

**C#:**
**Model**
```
public class SocialMedia
{
    public string Name { get; set; }
    public int ID { get; set; }
}
```
**Step 3:** Create the ViewModel class and then populate social media data in the SocialMediaViewModel

**C#**
**ViewModel**
```
public class SocialMediaViewModel
{
    public ObservableCollection<SocialMedia> SocialMedias { get; set; }
    public SocialMediaViewModel()
    {
        this.SocialMedias = new ObservableCollection<SocialMedia>();
        this.SocialMedias.Add(new SocialMedia() { Name = "Facebook", ID = 0 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Google Plus", ID = 1 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Instagram", ID = 2 });
        this.SocialMedias.Add(new SocialMedia() { Name = "LinkedIn", ID = 3 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Skype", ID = 4 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Telegram", ID = 5 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Televzr", ID = 6 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Tik Tok", ID = 7 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Tout", ID = 8 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Tumblr", ID = 9 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Twitter", ID = 10 });
        this.SocialMedias.Add(new SocialMedia() { Name = "Vimeo", ID = 11 });
        this.SocialMedias.Add(new SocialMedia() { Name = "WhatsApp", ID = 12 });
        this.SocialMedias.Add(new SocialMedia() { Name = "YouTube", ID = 13 });
    }
}
```
**Step 4:** Initialize the ComboBox control in the XAML page in which the ViewModel class is set to the BindingContext.
```
<editors:SfComboBox HeightRequest="40" 
                            WidthRequest="300"
                            IsEditable="True"
                            MaxDropDownHeight="200" 
                            ItemsSource="{Binding SocialMedias}" 
                            ShowDropdownHeaderView="True" 
                            DisplayMemberPath="Name"
                            DropdownHeaderViewHeight="50"
                            Margin="50">
            <editors:SfComboBox.DropdownHeaderView>
                <StackLayout BackgroundColor="#f0f0f0" >
                    <Label  FontSize="20" Text="Header View" TextColor="Red" />
                </StackLayout>
            </editors:SfComboBox.DropdownHeaderView>
        </editors:SfComboBox>

        <editors:SfComboBox HeightRequest="40" 
                     WidthRequest="300" 
                     IsEditable="True"
                     MaxDropDownHeight="200" 
                     ItemsSource="{Binding SocialMedias}" 
                     ShowDropdownFooterView="True" 
                     DisplayMemberPath="Name"
                     DropdownFooterViewHeight="50">
            <editors:SfComboBox.DropdownFooterView>
                <StackLayout BackgroundColor="#f0f0f0" >
                    <Label  FontSize="20" Text="Footer View" TextColor="Red" />
                </StackLayout>
            </editors:SfComboBox.DropdownFooterView>
        </editors:SfComboBox>
```

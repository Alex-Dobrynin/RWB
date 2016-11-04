# RWB

IF YOU ARE USING WindowStyle = None and AllowsTransparency = True.
It is already using few Properties of WindowChrome: CaptionHeight = 0, and ResizeBorderThickness = 7

Restores window bounds when maximizing, considering current monitor and workarea, U should inherit your window from this class. This code is not mine, but I created small library for reuse.

This is how U can use it:

XAML:

<custom:CustomWindow x:Class="YourApplication.CurrentWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:custom="clr-namespace:CustomWindow;assembly=CustomWindow"
        xmlns:local="clr-namespace:YourApplication">

</custom:CustomWindow>

Codebehind:

class CurrentWindow : CustomWindow.CustomWindow
{
	public CurrentWindow()
	{
		InitializeComponent();
	}
}
# How to set two different title bar text for minimized and normal/maximized state of WinForms MetroForm?

This sample illustrates how to set two different title bar text for minimized and normal/maximized state of WinForms MetroForm.

In MetroForm, by default the text displayed in the title bar will be same when the form is in normal/maximized state and minimized state. You can set different title bar text for normal/maximized state and minimized state by using Resize event of the form.

```C#
public Form1()
{
    InitializeComponent();
    this.Text = "Form1";
    this.Resize += On_Form1_Resize;
}

private void On_Form1_Resize(object sender, EventArgs e)
{
    if (this.WindowState == FormWindowState.Normal || this.WindowState == FormWindowState.Maximized)
        this.Text = "Form1";
    else if (this.WindowState == FormWindowState.Minimized)
        this.Text = "Form1 - Minimized";
}
```

## Requirements to run the demo
Visual Studio 2015 and above versions

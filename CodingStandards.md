# Coding Standards

- Keep your code as readable as possible.
- Import the following ReSharper settings file (used ReSharper 8.2): [https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings](https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings)
To keep this document shorter we won't list all the settings in here. You can browse them yourselves.
- Don't use tab character for indentation. Use corresponding amount of spaces instead.

4 spaces for C#, JavaScript, CSS, PowerShell, aspx, ascx.

2 spaces for SQL, XML.

***Bad***

    →   →   public∙static∙void∙Main(params∙string[]∙args)

***Good***

    ∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
- Don't keep trailing spaces.

***Bad***

    ∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)∙∙∙

***Good***

    ∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)

- Don't keep whitespaces in an empty line

***Bad***

    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙1");
    ∙∙∙∙∙∙∙∙∙∙∙∙
    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙2");

***Good***

    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙1");
    
    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙2");

- Don't use regions

***Bad***

    ∙∙∙∙∙∙∙∙#region∙Very∙important∙region

    ∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
    ∙∙∙∙∙∙∙∙{
    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Hello∙World");
    ∙∙∙∙∙∙∙∙}

    ∙∙∙∙∙∙∙∙#endregion

***Good***

    ∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
    ∙∙∙∙∙∙∙∙{
    ∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Hello∙World");
    ∙∙∙∙∙∙∙∙}


- Use C# built-in aliases for CLR types.

***Bad***

    System.Int32∙i∙=∙42;

***Good***

    int∙i∙=∙42;

- Don't use String.Empty

***Bad***
    
    string s∙=∙string.Empty;

***Good***

    string s∙=∙"";

- Don't use Hungarian notation. Use suffixes if necessary, e.g. for UI controls.

***Bad***

    string∙strName;
    System.Web.UI.WebControls.Label∙lblName;
    System.Web.UI.WebControls.TextBox∙txtName;

***Good***

    string∙name;
    System.Web.UI.WebControls.Label∙nameLabel;
    System.Web.UI.WebControls.TextBox∙nameTextBox;
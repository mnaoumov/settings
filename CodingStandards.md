# Coding Standards

---

### Keep your code as readable as possible.

---

### Import ReSharper settings file.

[https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings](https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings)

(used ReSharper 8.2)

To keep this document shorter we won't list all the settings in here. You can browse them yourselves once imported

![ReSharper Settings](https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharperSettings.PNG)

---

### Don't use tab character for indentation. Use corresponding amount of spaces instead.

4 spaces for C#, JavaScript, CSS, PowerShell, aspx, ascx.

2 spaces for SQL, XML.

***Bad***

```csharp
→   →   public∙static∙void∙Main(params∙string[]∙args)
```

***Good***

```csharp
∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
```

---

### Don't keep trailing spaces.

***Bad***

```csharp
∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)∙∙∙
```

***Good***

```csharp
∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
```

---

### Don't keep whitespaces in an empty line.

***Bad***

```csharp
∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙1");
∙∙∙∙∙∙∙∙∙∙∙∙
∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙2");
```

***Good***

```csharp
∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙1");

∙∙∙∙∙∙∙∙∙∙∙∙Console.WriteLine("Line∙2");
```

---

### Don't use regions.

***Bad***

```csharp
#region Very important region

public static void Main(params string[] args)
{
    Console.WriteLine("Hello World");
}

#endregion
```

***Good***

```csharp
public static void Main(params string[] args)
{
    Console.WriteLine("Hello World");
}
````

---

### Use C# built-in aliases for CLR types.

***Bad***

```csharp
System.Int32 i = 42;
```

***Good***

```csharp
int i = 42;
```

---

### Don't use *string.Empty*.

***Bad***

```csharp
string s = string.Empty;
```

***Good***

```csharp
string s = "";
```

---

### Don't use Hungarian notation. Use suffixes if necessary, e.g. for UI controls.

***Bad***

```csharp
string strName;
System.Web.UI.WebControls.Label lblName;
System.Web.UI.WebControls.TextBox txtName;
```

***Good***

```csharp
string name;
System.Web.UI.WebControls.Label nameLabel;
System.Web.UI.WebControls.TextBox nameTextBox;
```
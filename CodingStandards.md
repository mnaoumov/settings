# Coding Standards

---

### Import ReSharper settings file

[https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings](https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharper.DotSettings)

(used ReSharper 8.2)

To keep this document shorter we won't list all the settings in here. You can browse them yourselves once imported

![ReSharper Settings](https://raw.githubusercontent.com/mnaoumov/settings/master/ReSharperSettings.PNG)

---

### Keep your code as readable as possible

Use ReShaper Code Cleanup capabilities.

For sql use available formatters such as [http://poorsql.com/](http://poorsql.com/). Alternatively use [JetBrains 0xDBE](https://www.jetbrains.com/dbe/) with the following settings [https://raw.githubusercontent.com/mnaoumov/settings/master/0xDBE.jar](https://raw.githubusercontent.com/mnaoumov/settings/master/0xDBE.jar). NOTE: these settings does not produce 100% of the best formatting and it will require some manual changes.

---

### Don't use tab character for indentation. Use corresponding amount of spaces instead

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

### Don't keep trailing spaces

***Bad***

```csharp
∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)∙∙∙
```

***Good***

```csharp
∙∙∙∙∙∙∙∙public∙static∙void∙Main(params∙string[]∙args)
```

---

### Don't keep whitespaces in an empty line

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

### Don't use regions

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

### Use C# built-in aliases for CLR types

***Bad***

```csharp
System.Int32 i = 42;
```

***Good***

```csharp
int i = 42;
```

---

### Don't use *string.Empty*

***Bad***

```csharp
string s = string.Empty;
```

***Good***

```csharp
string s = "";
```

---

### Don't use Hungarian notation. Use suffixes if necessary, e.g. for UI controls

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

---

### Don't use SCREAMING_CAPITALIZATION

***Bad***

```csharp
public const string SECONDS_IN_DAY = 86400;
```

```sql
SELECT * FROM MyTable WHERE MyField = 'MyValue'
```

***Good***

```csharp
public const string SecondsInDay = 86400;
```

```sql
select * from MyTable where MyField = 'MyValue'
```

---

### Avoid unnecessary escaping

***Bad***

```sql
select [MyField], [MyOtherField], [Table] from MyTable
```

***Good***

```sql
select MyField, MyOtherField, [Table] from [MyTable]
```

---

### Prefer multi-line expressions for a better readability

***Bad***

```csharp
var myVariable = new MyClass { MyProperty1 = "MyValue1"; MyProperty2 = "MyValue2"; MyProperty3 = "MyValue3"; };
```

```sql
select * from MyTable where MyField = 'MyValue' and MyOtherField = 'MyOtherValue'
```

***Good***

```csharp
var myVariable = new MyClass
                 {
                     MyProperty1 = "MyValue1";
                     MyProperty2 = "MyValue2";
                     MyProperty3 = "MyValue3";
                 };
```

```sql
select
  *
from
  MyTable
where
  MyField = 'MyValue'
  and MyOtherField = 'MyOtherValue'
```

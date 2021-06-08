## Fuente
Las convenciones de este documento fueron generadas a partir de las "Naming Guidelines" de Microsoft:
https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/naming-guidelines

## Definiciones

> Existen dos tipos de CamelCase:
> * UpperCamelCase (más conocido como PascalCase), cuando la primera letra de cada una de las palabras es mayúscula. Ejemplo: ScientificCalculator.
> * lowerCamelCase (o simplemente camelCase), igual que la anterior con la excepción de que la primera letra es minúscula. Ejemplo: scientificCalculator.

## Usar PascalCase para los nombres de las clases y métodos.
-----

:heavy_check_mark:
```csharp
public class ScientificCalculator {
  public float Sum(float firstNumber, float secondNumber) {
    return firstNumber + secondNumber;
  }
}
```

:x: (scientificCalculator es el nombre de la clase y está utilizando camelCase)
```csharp
public class scientificCalculator {
  public float Sum(float firstNumber, float secondNumber) {
    return firstNumber + secondNumber;
  }
}
```

:x: (sum es un método y está utilizando camelCase)
```csharp
public class ScientificCalculator {
  public float sum(float firstNumber, float secondNumber) {
    return firstNumber + secondNumber;
  }
}
```

## Usar camelCase para los argumentos de los métodos y variables locales.
-----
:heavy_check_mark:
```csharp

public float SayHello(string personName) {
  string fullGreet = $"¡Hello, {personName}!"
  return fullGreet;
}
```

:x: (FullGreet es una variable local y está utilizando PascalCase)
```csharp

public float SayHello(string personName) {
  string FullGreet = $"¡Hello, {personName}!"
  return FullGreet;
}
```

:x: (PersonName es un argumento del método y está utilizando PascalCase)
```csharp

public float SayHello(string PersonName) {
  string fullGreet = $"¡Hello, {PersonName}!"
  return fullGreet;
}
```

## Agregar el prefijo _ en variables privadas de las clases.
-----
:heavy_check_mark:
```csharp
public class OrderService {
  private readonly IInvoiceService _invoiceService;

  public OrderService(IInvoiceService invoiceService) {
    _invoiceService = invoiceService;
  }
}
```

:x: (invoiceService es una variable privada de la clase "Compra" y no tiene el prefijo _)
```csharp
public class OrderService {
  private readonly IInvoiceService invoiceService;

  public OrderService(IInvoiceService invoiceService) {
    this.invoiceService = invoiceService;
  }
}
```

## No usar notación Hungara.
-----
La notación Hungarian consiste en prefijos en minúsculas que se añaden a los nombres de las variables y que indican su tipo. El resto del nombre indica, lo más claramente posible, el fin de la variable.

:heavy_check_mark:
```csharp
int count;
string name;
float salary;
```

:x:
```csharp
int iCount;
string strName;
float fSalary;
```

## No usar Screaming Caps para variables const o readonly.
-----
Esta convención suele ser utilizada en otros lenguajes como, por ejemplo, JAVA.

:heavy_check_mark:
```csharp
public const string ShippingTypeConst = "ShippingTypeConst";
public readonly string ShippingTypeReadonly = "ShippingTypeReadonly";
```

:x:
```csharp
public const string SHIPPING_TYPE_CONST = "ShippingTypeConst";
public readonly string SHIPPING_TYPE_READONLY = "ShippingTypeReadonly";
```

## No abreviar.
-----
:heavy_check_mark:
```csharp
EmployeeCategory employeeCategory;
EmployeeAssignment employeeAssignment;
string clientName;
```

:x:
```csharp
EmployeeCategory empCat;
EmployeeAssignment empAssig;
string cliNam;
```

:wink: ¡Algunas excepciones!
Muchas veces se utilizan clases como las que están a continuación que por su naturaleza propia ya son abreviaturas. 
```csharp
XmlDocument xmlDocument;
FtpHelper ftpHelper;
UriPart uriPart;
```

## No usar snake case (separ con guión bajo) para nombres de variables.
-----
:heavy_check_mark:
```csharp
public DateTime orderDate;
```

:x:
```csharp
public DateTime order_date;
public DateTime order_Date;
```

## Usar el prefijo I para interfaces.
-----
:heavy_check_mark:
```csharp
public interface IEmployeeService;
```

## Usar el sufijo Service para servicios.
-----
:heavy_check_mark:
```csharp
public class EmployeeService;
```

## Usar el sufijo Repository para repositorios.
-----
:heavy_check_mark:
```csharp
public class EmployeeRepository;
```


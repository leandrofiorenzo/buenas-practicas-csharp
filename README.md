> Existen dos tipos de CamelCase:
> * UpperCamelCase (más conocido como PascalCase), cuando la primera letra de cada una de las palabras es mayúscula. Ejemplo: CalculadoraCientifica.
> * lowerCamelCase (o simplemente camelCase), igual que la anterior con la excepción de que la primera letra es minúscula. Ejemplo: calculadoraCientifica.

## Usar PascalCase para los nombres de las clases y métodos.
-----

:heavy_check_mark:
```csharp
public class CalculadoraCientifica {
  public float Sumar(float numeroA, float numeroB) {
    return numeroA + numeroB;
  }
}
```

:x: (calculadoraCientifica es el nombre de la clase y está utilizando camelCase)
```csharp
public class calculadoraCientifica {
  public float Sumar(float numeroA, float numeroB) {
    return numeroA + numeroB;
  }
}
```

:x: (sumar es un método y está utilizando camelCase)
```csharp
public class CalculadoraCientifica {
  public float sumar(float numeroA, float numeroB) {
    return numeroA + numeroB;
  }
}
```

## Usar camelCase para los argumentos de los métodos y variables locales.
-----
:heavy_check_mark:
```csharp

public float Saludar(string nombrePersona) {
  string saludoCompleto = $"¡Hola, {nombrePersona}!"
  return saludoCompleto;
}
```

:x: (SaludoCompleto es una variable local y está utilizando PascalCase)
```csharp

public float Saludar(string nombrePersona) {
  string SaludoCompleto = $"¡Hola, {nombrePersona}!"
  return SaludoCompleto;
}
```

:x: (NombrePersona es un argumento del método y está utilizando PascalCase)
```csharp

public float Saludar(string NombrePersona) {
  string saludoCompleto = $"¡Hola, {NombrePersona}!"
  return saludoCompleto;
}
```

## Agregar el prefijo _ en variables privadas de las clases.
-----
:heavy_check_mark:
```csharp
public class CompraService {
  private readonly IFacturaService _facturaService;

  public CompraService(IFacturaService facturaService) {
    _facturaService = facturaService;
  }
}
```

:x: (facturaService es una variable privada de la clase "Compra" y no tiene el prefijo _)
```csharp
public class CompraService {
  private readonly IFacturaService facturaService;

  public CompraService(IFacturaService facturaService) {
    this.facturaService = facturaService;
  }
}
```

:x: (NombrePersona es un argumento del método y está utilizando PascalCase)
```csharp

public float Saludar(string NombrePersona) {
  string saludoCompleto = $"¡Hola, {NombrePersona}!"
  return saludoCompleto;
}
```

## No usar notación Hungara.
-----
La notación Hungarian consiste en prefijos en minúsculas que se añaden a los nombres de las variables y que indican su tipo. El resto del nombre indica, lo más claramente posible, el fin de la variable.

:heavy_check_mark:
```csharp
int contador;
string nombre;
float sueldo;
```

:x:
```csharp
int iContador;
string strNombre;
float fSueldo;
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

## No usar abreviaturas.
-----
:heavy_check_mark:
```csharp
EmpleadoCategoria empleadoCategoria;
Asignacion empleadoAsignacion;
string nombreCliente;
```

:x:
```csharp
EmpleadoCategoria empCat;
Asignacion empAsig;
string nomCli;
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
public DateTime fechaTomaPedido;
public TimeSpan tiempoProximaAlerta;
```

:x:
```csharp
public DateTime fecha_Toma_Pedido;
public TimeSpan tiempo_Proxima_Alerta;
```

## Usar tipos predefinidos en vez de system types (Int16, Single, UInt64).
-----
:heavy_check_mark:
```csharp
string primerNombre;
int ultimoIndice;
bool esAdulto;
```

:x:
```csharp
String primerNombre;
Int32 ultimoIndice;
Boolean esAdulto;
```

## Usar el prefijo I para interfaces.
-----
:heavy_check_mark:
```csharp
public interface IPersona;
```

## Usar el sufijo Service para servicios.
-----
:heavy_check_mark:
```csharp
public class PersonaService;
```

## Usar el sufijo Repository para repositorios.
-----
:heavy_check_mark:
```csharp
public class PersonaRepository;
```


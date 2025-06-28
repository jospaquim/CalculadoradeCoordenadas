# PDF Coordinate Calculator

Una herramienta para calcular coordenadas exactas en documentos PDF, perfecto para posicionar firmas digitales, sellos o cualquier elemento en PDFs usando librerías como iText, PDFSharp, etc.

## Demo

**[Usar la herramienta aquí](https://jospaquim.github.io/CalculadoradeCoordenadas/)**

## Características

- **Carga PDFs localmente** - Sin subir archivos a servidores
- **Clic para obtener coordenadas** - Coordenadas exactas con un clic
- **Conversión de unidades** - Puntos, cm, mm, pulgadas
- **Vista previa visual** - Ve exactamente dónde se posicionará tu elemento
- **Tamaños ajustables** - Configura ancho y alto del elemento
- **Posiciones predefinidas** - Botones rápidos para esquinas y centro
- **Navegación entre páginas** - Soporte para PDFs multipágina
- **Código C# generado** - Código listo para usar con iText

## Casos de Uso
- **Firmas digitales** en documentos PDF
- **Sellos y marcas de agua**
- **Campos de formulario**
- **Elementos de layout** en PDFs generados
- **Posicionamiento preciso** de texto e imágenes

## Cómo Usar

1. **Carga tu PDF** - Arrastra el archivo o haz clic para seleccionar
2. **Navega a la página** deseada usando los controles
3. **Haz clic** donde quieres posicionar tu elemento
4. **Ajusta el tamaño** usando los controles laterales
5. **Copia el código** generado para tu proyecto

## Código Ejemplo

La herramienta genera código C# listo para usar:

```csharp
// Coordenadas calculadas para la firma
var left = (float)350;
var bottom = (float)200;

// Crear rectángulo para la firma
canvas.SaveState()
      .SetFillColor(ColorConstants.WHITE)
      .Rectangle(left, bottom, 250, 90)
      .Fill()
      .RestoreState();

// Posicionar texto
document.Add(new Paragraph("Tu contenido aquí")
    .SetFont(font)
    .SetFontSize(6)
    .SetFixedPosition(pageNumber, left + 10, bottom + 70, 230));
```

## Tecnologías

- **PDF.js** - Renderizado de PDFs en el navegador
- **HTML5 Canvas** - Visualización interactiva
- **Vanilla JavaScript** - Sin dependencias adicionales
- **CSS3** - Interfaz moderna y responsive

## Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas para mejoras:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/...`)
3. Commit tus cambios (`git commit -m 'Add some ...'`)
4. Push a la rama (`git push origin feature/...`)
5. Abre un Pull Request

## Ideas para Mejoras

- [ ] Soporte para más formatos (PNG, JPEG como overlay)
- [ ] Exportar coordenadas en JSON/XML
- [ ] Soporte para otros lenguajes (Python, Java, etc.)
- [ ] Guardado de configuraciones
- [ ] Modo oscuro
- [ ] Zoom avanzado

## Librerías Compatibles

Esta herramienta es útil para trabajar con:

- **iText (C#/Java)** - Manipulación de PDFs
- **PDFSharp (.NET)** - Creación y edición de PDFs
- **ReportLab (Python)** - Generación de PDFs
- **jsPDF (JavaScript)** - PDFs en el navegador
- **TCPDF (PHP)** - PDFs en PHP

## Reportar Problemas

¿Encontraste un bug?  describiendo:

- Navegador y versión
- Tipo de PDF que causó el problema
- Pasos para reproducir el error
- Screenshot si es posible

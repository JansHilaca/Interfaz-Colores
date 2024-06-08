# Componentes principales:
- **Label**: Etiquetas para los textos descriptivos.
- **DatePicker**: Selector de fecha.
- **ColorPicker**: Selector de color.
- **Button**: Botón para confirmar la selección.
- **Label**: Etiqueta para mostrar el resultado.

## Diseño y disposición:
- **VBox**: Un layout vertical con un espaciado de 10 píxeles entre los componentes, centrado y con un padding de 10 píxeles.

## Funcionalidad:
- **Manejo de Eventos**: El botón de confirmación obtiene la fecha y el color seleccionados, los muestra en la etiqueta de resultado y los imprime en la consola.

## Código Java

```java
package Main;

import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.ColorPicker;
import javafx.scene.control.DatePicker;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class InterfzaGUI extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Creación de etiquetas y selectores
        Label fechaLabel = new Label("Selecciona una fecha:");
        DatePicker fechaPicker = new DatePicker();
        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();
        Button botonConfirmar = new Button("Confirmar");
        Label resultadoLabel = new Label("Resultado:");

        // Configuración del VBox (layout vertical)
        VBox root = new VBox(10);  // Espaciado de 10 píxeles entre componentes
        root.setPadding(new Insets(10));  // Padding de 10 píxeles alrededor
        root.setAlignment(Pos.CENTER);  // Centrando los componentes

        // Agregando todos los componentes al VBox
        root.getChildren().addAll(fechaLabel, fechaPicker, colorLabel, colorPicker, botonConfirmar, resultadoLabel);

        // Manejo del evento del botón
        botonConfirmar.setOnAction(e -> {
            // Obtener valores seleccionados
            String fechaSeleccionada = fechaPicker.getValue().toString();
            String colorSeleccionado = colorPicker.getValue().toString();
            // Actualizar la etiqueta de resultado
            resultadoLabel.setText("Fecha seleccionada: " + fechaSeleccionada + "\nColor seleccionado: " + colorSeleccionado);
            // Imprimir en consola
            System.out.println("Fecha seleccionada: " + fechaSeleccionada + ", Color seleccionado: " + colorSeleccionado);
        });

        // Configuración de la escena
        Scene scene = new Scene(root, 300, 250);  // Dimensiones de la ventana
        primaryStage.setTitle("Fecha y Color GUI");  // Título de la ventana
        primaryStage.setScene(scene);  // Asignar la escena al escenario principal
        primaryStage.show();  // Mostrar la ventana
    }

    public static void main(String[] args) {
        launch(args);  // Lanzar la aplicación JavaFX
    }
}

## "Ejecutar"

![imagen](https://github.com/JansHilaca/Interfaz-Colores/assets/168945853/9ba37a10-43e7-4894-9dd5-ab478fdb508d)

![imagen](https://github.com/JansHilaca/Interfaz-Colores/assets/168945853/3c8f2dcd-9855-4f04-8e37-9285c8a561af)

![imagen](https://github.com/JansHilaca/Interfaz-Colores/assets/168945853/858699f5-9bb8-4165-9829-f26179e397a0)

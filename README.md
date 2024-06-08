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
        Label fechaLabel = new Label("Selecciona una fecha:");
        DatePicker fechaPicker = new DatePicker();
        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();
        Button botonConfirmar = new Button("Confirmar");
        Label resultadoLabel = new Label("Resultado:");

        VBox root = new VBox(10);
        root.setPadding(new Insets(10));
        root.setAlignment(Pos.CENTER);

        root.getChildren().addAll(fechaLabel, fechaPicker, colorLabel, colorPicker, botonConfirmar, resultadoLabel);

        botonConfirmar.setOnAction(e -> {
            String fechaSeleccionada = fechaPicker.getValue().toString();
            String colorSeleccionado = colorPicker.getValue().toString();
            resultadoLabel.setText("Fecha seleccionada: " + fechaSeleccionada + "\nColor seleccionado: " + colorSeleccionado);
            System.out.println("Fecha seleccionada: " + fechaSeleccionada + ", Color seleccionado: " + colorSeleccionado);
        });

        Scene scene = new Scene(root, 300, 250);
        primaryStage.setTitle("Fecha y Color GUI");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args); 
    }
}



## "Ejecutar"

![imagen](https://github.com/JansHilaca/Interfaz-Colores/assets/168945853/9ba37a10-43e7-4894-9dd5-ab478fdb508d)

![imagen](https://github.com/JansHilaca/Interfaz-Colores/assets/168945853/3c8f2dcd-9855-4f04-8e37-9285c8a561af)

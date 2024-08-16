# Semana 10
### JFrame
`Es una clase de Java swing para crear ventanas e interfaces gráficas`
```java
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class SimpleFrame {

    public static void main(String[] args) {
        // Crear el marco (JFrame)
        JFrame frame = new JFrame("Mi Primer JFrame");
        frame.setSize(300, 200); // Tamaño de la ventana
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // Cerrar la aplicación al cerrar la ventana

        // Crear un panel
        JPanel panel = new JPanel();

        // Crear una etiqueta
        JLabel label = new JLabel("¡Hola, mundo!");

        // Crear un botón
        JButton button = new JButton("Haz clic en mí");

        // Agregar un ActionListener al botón
        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                label.setText("¡Botón clickeado!");
            }
        });

        // Agregar componentes al panel
        panel.add(label);
        panel.add(button);

        // Agregar el panel al marco
        frame.add(panel);

        // Hacer visible el marco
        frame.setVisible(true);
    }
}
```

1. Crear el JFrame:

* Se crea un JFrame con el título "Mi Primer JFrame".
* Se establece el tamaño de la ventana a 300x200 píxeles.
* Se configura el marco para cerrar la aplicación cuando se cierra la ventana.

2. Crear el JPanel:

* Se crea un JPanel para contener los componentes.

3. Agregar Componentes:

* Se crea una JLabel con el texto "¡Hola, mundo!".
* Se crea un JButton con el texto "Haz clic en mí".
* Se agrega un ActionListener al botón para cambiar el texto de la etiqueta cuando el botón es clickeado.

4. Agregar al JFrame:

* Se agregan la etiqueta y el botón al panel.
* El panel se agrega al JFrame.

5.  Hacer visible el JFrame:
* Finalmente, se hace visible la ventana.

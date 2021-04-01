### Code:

```java
import javax.swing.*;
import javax.swing.border.LineBorder;
import java.awt.*;

public class DialogBox_with_UI {
    //global variables
    JFrame frame;
    JLabel label;
    JButton button;

    //constructor
    DialogBox_with_UI() {

        //the 'Color' class is inside java.awt package and helps stylise our components
        //these are few methods on how to use it
        Color gray = Color.LIGHT_GRAY;                    //some colors are already named
        Color bg = Color.decode("#191919");               //if you dislike the already existing ones use the hex value of your favourite colors
        Color purple = new Color(123,50,250);             //if you don't remember hex values, make up some rgb value(r,g,b)

        //the 'Font' class is also inside java.awt package and helps stylise our fonts
        //the parameters go like (Font_name, Font_style, Font_size)
        Font f1 = new Font("Montserrat",Font.PLAIN,18);
        Font f2 = new Font("Montserrat",Font.BOLD,20);


        frame = new JFrame("Dialog Box with UI");
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setLocation(600,300);
        frame.setSize(300,200);                                               //changes from here onwards
        frame.getContentPane().setBackground(bg);                             //changing background of the frame(bg of other components doesn't require getContentPane)
        frame.setResizable(false);                                            //this makes it sure that the user cannot resize the frame

        label = new JLabel("Shutting down your pc !!!",JLabel.CENTER);         //in order to align text inside the label, we can add a second parameter
        label.setBounds(15,20,260,40);                                        //adjust the values to your liking
        frame.add(label);
        label.setBackground(purple);                                          //this changes the background of the label
        label.setOpaque(true);                                                //makes it sure that the background of the label is not hidden (generally used for labels)
        label.setForeground(gray);                                            //changes font color
        label.setFont(f1);                                                    //changes the font style

        button = new JButton("OK");
        button.setBounds(90,100,100,40);
        frame.add(button);
        button.setFont(f2);
        button.setBackground(Color.decode("#ffea00"));           //Color without creating a variable
        button.setForeground(purple);
        button.setFocusPainted(false);                           //removes the button focus outline
        button.setBorder(new LineBorder(purple,3));              //this is used to put a border around the component, parameters(color,thickness)

    }
    public static void main(String args[]) {
        SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                new DialogBox_with_UI();
            }
        });
    }
}

```
---
![DialogBox Output](https://github.com/ShimilSAbraham/Coding-Tutorial/blob/main/Java/Swing/Program%201/DialogBox.png)

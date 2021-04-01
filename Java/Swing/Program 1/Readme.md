### Code:

```java
import javax.swing.*;

public class DialogBox {
    //global variables
    JFrame frame;
    JLabel label;
    JButton button;

    //constructor
    DialogBox() {

        frame = new JFrame("Dialog Box");                       //to create the frame and set its title
        frame.setVisible(true);                                 //this statement is very important... for some reason the frame is invisible as default
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);   //this is to make sure that the frame closes on clicking the close button(x)
        frame.setLayout(null);                                  //we will get to layouts later...for now let this be null (ie.we need to manually position components)
        frame.setLocation(600,300);                             //setting the position of the frame on your screen(x,y)
        frame.setSize(300,200);                                 //the width and height of your frame(w,h)

        label = new JLabel("Shutting down your pc !!!");        //creating the label along with its content
        label.setBounds(20,20,260,40);                          //this is a combination of setLocation() and setSize()... the parameters go like(x,y,w,h)
        frame.add(label);                                       //this is necessary for the component to be in the frame

        button = new JButton("OK");                             //creating the button along with its content
        button.setBounds(100,100,100,40);                       //(x,y,w,h)
        frame.add(button);
        
    }
    public static void main(String args[]) {
        SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                new DialogBox();
            }
        });
    }
}
```
---
### Output
![DialogBox Output](https://github.com/ShimilSAbraham/Coding-Tutorial/blob/main/Java/Swing/Program%201/DialogBox.png)

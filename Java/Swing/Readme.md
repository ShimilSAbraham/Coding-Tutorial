## Java GUI using Swing
### Working:
* Instead of writing the code in the main method, we use a separate thread.
* This event dispatch thread invokes the constructor of the class.
* The swing components are defined inside this constructor.
--- 
*Code part inside main method:*
```java
  public static void main(String args[]){
    SwingUtilities.invokeLater(new Runnable(){
      public void run(){ 
        new ClassName();   //line invoking the constructor
      }
    });
  }
```
---
### Import statements that we need to know:
```java
  import javax.swing.*;           //to import swing components
  import java.awt.*;              //to import Layout classes, Font class, Color class
  import java.awt.event.*;        //to import event listeners
  import javax.swing.border.*;    //to import LineBorder(optional)
```

### Some of the important swing components:
* JFrame   - *acts as the container that holds all the swing components*
* JLabel   - *used as a container to place texts and icons inside the Jframe*
* JButton  - *button*
* JTextField - *used for user inputs*
* JPasswordField - *used for password fields*
* ImageIcon - *used for storing icons*
* JCheckBox
* JRadioButton
* ButtonGroup - *to group radio buttons*
---
**Now let's see two simple programs to display a dialog box**
* [Program 1](https://github.com/ShimilSAbraham/Coding-Tutorial/tree/main/Java/Swing/Program%201 "Dialog Box")
* [Program 2](https://github.com/ShimilSAbraham/Coding-Tutorial/tree/main/Java/Swing/Program%202 "Dialog Box With UI")
---
**Let's try a sign up form**
* [Program 3](https://github.com/ShimilSAbraham/Coding-Tutorial/tree/main/Java/Swing/Program%203 "Signup Form")
* [Program 4](https://github.com/ShimilSAbraham/Coding-Tutorial/tree/main/Java/Swing/Program%203 "Signup Form with UI")
---



### Code:
```java
package Exercise;

import javax.swing.*;
import javax.swing.border.LineBorder;
import java.awt.*;

public class SignupForm {
    //global variables
    JFrame frame;
    JLabel head,user,pass;
    JTextField username;
    JPasswordField password;
    JButton signup;

    //constructor
    SignupForm() {

        Color sky = Color.decode("#4fc3f7");
        Color orange = Color.decode("#ff3d00");
        Color orange1 = Color.decode("#fb8c00");


        frame = new JFrame("Signup Form");
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setLocation(650,230);
        frame.setSize(350,450);
        frame.getContentPane().setBackground(Color.decode("#212121"));

        head = new JLabel("Register",JLabel.CENTER);
        head.setBounds(15,20,310,50);
        head.setFont(new Font("Poppins",Font.BOLD,30));
        frame.add(head);
        head.setForeground(orange);

        user = new JLabel("Enter Username :",JLabel.LEFT);
        user.setBounds(15,90,310,30);
        frame.add(user);
        user.setFont(new Font("Poppins",Font.PLAIN,17));
        user.setForeground(orange);

        username = new JTextField();
        username.setBounds(15,120,310,30);
        frame.add(username);
        username.setFont(new Font("Poppins",Font.PLAIN,16));
        username.setForeground(orange);
        username.setBackground(sky);
        username.setBorder(new LineBorder(orange1,2));

        pass = new JLabel("Enter Password :",JLabel.LEFT);
        pass.setBounds(15,160,310,30);
        frame.add(pass);
        pass.setFont(new Font("Poppins",Font.PLAIN,17));
        pass.setForeground(orange);

        password = new JPasswordField();
        password.setBounds(15,190,310,30);
        frame.add(password);
        password.setForeground(orange);
        password.setBackground(sky);
        password.setBorder(new LineBorder(orange1,2));

        signup = new JButton("Sign Up");
        signup.setBounds(100,260,130,50);
        frame.add(signup);
        signup.setFont(new Font("Poppins",Font.BOLD,22));
        signup.setForeground(orange);
        signup.setBackground(Color.decode("#29b6f6"));
        signup.setFocusPainted(false);

    }
    public static void main(String args[]) {
        SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                new SignupForm();
            }
        });
    }
}

```
---
### Output
![]()

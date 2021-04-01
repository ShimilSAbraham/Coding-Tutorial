### Code:
```java
import javax.swing.*;

public class SignupForm {
    //global variables
    JFrame frame;
    JLabel head,user,pass;
    JTextField username;
    JPasswordField password;
    JButton signup;

    //constructor
    SignupForm() {

        frame = new JFrame("Signup Form");
        frame.setVisible(true);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);
        frame.setLocation(650,230);
        frame.setSize(350,450);

        head = new JLabel("Register",JLabel.CENTER);
        head.setBounds(15,20,310,50);
        frame.add(head);

        user = new JLabel("Enter Username :",JLabel.LEFT);
        user.setBounds(15,90,310,30);
        frame.add(user);

        username = new JTextField();
        username.setBounds(15,130,310,30);
        frame.add(username);

        pass = new JLabel("Enter Password :",JLabel.LEFT);
        pass.setBounds(15,180,310,30);
        frame.add(pass);

        password = new JPasswordField();
        password.setBounds(15,220,310,30);
        frame.add(password);

        signup = new JButton("Sign Up");
        signup.setBounds(120,300,100,40);
        frame.add(signup);

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
![SignUp Form](https://github.com/ShimilSAbraham/Coding-Tutorial/blob/main/Java/Swing/Program%203/SignupForm.png)

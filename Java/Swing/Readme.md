## Java GUI using Swing
___
### Working:
* Instead of writing the code in the main method, we use a separate thread.
* This event dispatch thread invokes the constructor of the class.
* The swing components are defined inside this constructor.
--- 

```java
  public static void main(String args[]){
    SwingUtilities.invokeLater(new Runnable(){
      public void run(){ 
        new ClassName();   //line invoking the constructor
      }
    });
  }
```

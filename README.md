# Create-a-progressbar-using-java
import javax.swing.*;

class fr10 extends JFrame {
    JProgressBar jp;

    fr10() {
        setLayout(null);

        jp = new JProgressBar(JProgressBar.HORIZONTAL, 0, 100);
        jp.setStringPainted(true);

        jp.setValue(30);

        jp.setBounds(100, 100, 200, 30);
        add(jp);

        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setSize(500, 500);
        setVisible(true);

        // logic to move progressbar
        for (int i = 0; i <= 100; i++) {
            jp.setValue(i);
            jp.setString(i + "%");

            try {
                Thread.sleep(100);
            } catch (Exception ex) {
                ex.printStackTrace();
            }
        }

        JOptionPane.showMessageDialog(this, "Download Complete");

    }

    public static void main(String[] args) {
        fr10 obj = new fr10();
    }
}

/* output:-

![image](https://user-images.githubusercontent.com/96234273/179361770-02b1b3f5-393f-45db-9982-5d97394c9613.png)

*/

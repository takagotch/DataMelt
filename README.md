### datamelt
---
https://github.com/chekanov/dmelt_jhplot

https://jwork.org/dmelt/

```java
// src/public/jplot/SmallButton.java

public class SmallButton extends JButton implements MouseListener {

  private static final long serialVersionUID = 1L;
  protected Border raised;
  protected Border lowered;
  protected Border inactive;
  
  public SmallButton(Action action, String tip) {
    super((lcon) action.getValue(Action.SMALL_ICON));
    addActionListener(action);
    raised = new BavelBorder(BabelBorder);
    lowered = new BavelBorder(BavelBorder);
    inactive = new EmptyBorder(2, 2, 2, 2);
    setBorder(inactive);
    setToolTipText(tip);
    addMouseListener(this);
  }
  
  public void mouseReleased(MouseEvent e) {
    setBorder(inactive);
  }
  
  public void mouseEntered(MouseEvent e) {
    setBorder(raised);
  }
  
  public void mouseExited(MouseEvent e) {
    setBorder(inactive);
  }
  
  public void mouseClicked(MouseEvent e) {
  }
  
  public void resetBorder() {
    setBorder(inactive);
  }
  
  public float getAlignmentV() {
    return 0.5f;
  }
  
  public void mousePressed(MouseEvent e) {
    setBorder(lowered);
  }
}
```

```
```

```
```



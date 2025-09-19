# JAVA-CalculatorGUI
Author: <br />Goca Andelkovic<br />
LBS Eibiswald | 2aAPC | Gruppe A |  19.09.2025 

## CalculatorGUI
Dieses Projekt erstellt ein einfaches Taschenrechner-Design mit einer Java-Swing-Oberfläche. 
Es implementiert außerdem einige grundlegende Rechenfunktionen (Addieren, Subtrahieren usw.).

## ActionListener
```
clearBtn.addActionListener(new ClearBtnClicked());
```
Der ActionListener ermöglicht in diesem Kontext die Funktionalität der Schaltflächen des Rechners. 
In dieser Zeile weist das Programm an, eine neue Instanz der Klasse ClearBtnClicked ohne Argumente zu erstellen.

## Class ClearBtnClicked
```
    private class ClearBtnClicked implements ActionListener {

        @Override
        public void actionPerformed(ActionEvent e) {
            resultsTxt.setText("");
            leftOperand = 0.0;
            rightOperand = 0.0;
        }
    }
```
Hier implementiert eine Klasse die ActionListener-Schnittstelle.
Dieser Code weist das Programm an, beim Klicken auf die Schaltfläche das Ergebnisfeld zu leeren sowie den linken und rechten Operanden auf 0 zu setzen.
Auf diese Weise wird das Eingabefeld zurückgesetzt.

## Main Methode
```
    public static void main(String[] args) {
        JFrame frame = new JFrame("Calculator");
        frame.setContentPane(new Calculator().calculatorView);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.pack();
        frame.setVisible(true);
    }
```
Die main-Methode erstellt hier eine Instanz des JFrame (das Rechnerfenster selbst).
Anschließend wird der Inhalt gesetzt und das Standardverhalten festgelegt, 
nämlich dass sich das Programm beim Schließen des Fensters beendet.
frame.pack() passt die Größe des Fensters an die enthaltenen Komponenten an, 
und setVisible(true) macht das Fenster sichtbar.

### Verwendung
Technologien im Einsatz:<br />
- **Java**
- **Swing UI**

### Screenshot
![alt text](https://github.com/dannyfox9898/CalculatorGUI/blob/main/output.png)
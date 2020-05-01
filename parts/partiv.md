# Part IV LOB
##Develop of a line of business application

![lob](../images/lob.png "lob")

A LOB is an application where you have got a grahical user interface and where the data is stored in a database.  
In this case we have got a database with clients and we are able to add a new client, filter the list of clients and edit the data for a client.  
We can also store a picture for each client.  

In order to run the sample app you have to install the module tinydb.  

```console
user@machine:/path$ pip3 install tinydb
```

Tinydb is a very small but usefull database implementation written in Python. You don't need a server to store the data on. And you do not need the SQL language at all. Tinydb just simply stores pythonic data in a single file.  

Because of the fact, that this app is a little bit larger then all the others that I have posted here, I do not print all the source code here. You can get the source here on [github](https://github.com/Artanidos/PythonDesktopBook).

## Main
As before this time I put the main routine into the *main.py* in the Lob folder.  
There I am initializing the application object and I am setting the style to Fusion and I am initializing the color palette.  

```python
app = QApplication(sys.argv)
app.setStyle(QStyleFactory.create("Fusion"))
app.setStyleSheet("QPushButton:hover { color: #45bbe6 }")

p = app.palette()
p.setColor(QPalette.Window, QColor(53, 53, 53))
p.setColor(QPalette.WindowText, Qt.white)
p.setColor(QPalette.Base, QColor(64, 66, 68))
p.setColor(QPalette.AlternateBase, QColor(53, 53, 53))
p.setColor(QPalette.ToolTipBase, Qt.white)
p.setColor(QPalette.ToolTipText, Qt.black)
p.setColor(QPalette.Text, Qt.white)
p.setColor(QPalette.Button, QColor(53, 53, 53))
p.setColor(QPalette.ButtonText, Qt.white)
p.setColor(QPalette.BrightText, Qt.red)
p.setColor(QPalette.Highlight, QColor("#45bbe6"))
p.setColor(QPalette.HighlightedText, Qt.black)
p.setColor(QPalette.Disabled, QPalette.Text, Qt.darkGray)
p.setColor(QPalette.Disabled, QPalette.ButtonText, Qt.darkGray)
p.setColor(QPalette.Link, QColor("#bbb"))
app.setPalette(p)
```  
The color can be set in two different ways. You can use the RGB values ```QColor(53, 53, 53)``` or you might use a string ```QColor("#45bbe6")``` as we do in HTML.  

This time the code is a little bit more structured. The main.py is still in the root folder, so a use might see it immediatly so the user knows what to start. And all other Python files are stored in the widgets folder.  

## MainWindow
The visual part of the application starts in the class MainWindow which I have stored in the file mainwindow.py.  



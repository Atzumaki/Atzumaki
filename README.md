- 👋 Hi, I’m @Atzumaki
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Atzumaki/Atzumaki is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from PyQt5.QtWidgets import QApplication, QLabel, QPushButton, QWidget, QVBoxLayout, QTextEdit
from PyQt5.QtGui import QFont, QPixmap, QIcon
from PyQt5.Qt import Qt
from PyQt5.QtCore import QSize
import click


class Db(QWidget):
    def __init__(self):
        super().__init__()
        self.tk()
        
    def tk(self):
        self.setWindowTitle('Обучение Пайтону')
        self.setFixedSize(1600, 900)
        # Фон
        self.fon = QLabel(self)
        self.fon.setPixmap(QPixmap('фон1'))
        self.fon.setFixedSize(1600, 900)
        # Текст
        self.label = QLabel('                                             Меню', self)
        self.label.setFont(QFont('Times', 20))
        self.label.setStyleSheet('background: #00bfff;')
        self.label.setFixedSize(800, 50)
        self.label.move(330, 50)
        # Кнопка 0 doc
        self.bt = QPushButton('', self)
        self.bt.setFont(QFont('Time', 10))
        self.bt.setIcon(QIcon('Проект0'))
        self.bt.setIconSize(QSize(100000, 100000))
        self.bt.setFixedSize(412, 295)
        self.bt.move(320, 100)
        # Кнопка 1 while
        self.bt1 = QPushButton('', self)
        self.bt1.setFont(QFont('Time', 10))
        self.bt1.setIcon(QIcon('Проект2'))
        self.bt1.setIconSize(QSize(100000, 100000))
        self.bt1.setFixedSize(412, 300)
        self.bt1.move(728, 100)
        # Кнопка 2 for
        self.bt2 = QPushButton('', self)
        self.bt2.setFont(QFont('Time', 10))
        self.bt2.setIcon(QIcon('Проект3'))
        self.bt2.setIconSize(QSize(100000, 100000))
        self.bt2.setFixedSize(412, 300)
        self.bt2.move(320, 395)
        # Кнопка 3 spisok
        self.bt3 = QPushButton('', self)
        self.bt3.setFont(QFont('Time', 10))
        self.bt3.setIcon(QIcon('Проект1'))
        self.bt3.setIconSize(QSize(100000, 100000))
        self.bt3.setFixedSize(412, 300)
        self.bt3.move(728, 395)
        # Слот перемещения
        self.mainstick = QVBoxLayout(self)
        self.bt.clicked.connect(self.doc_)
        self.bt1.clicked.connect(self.bb_)
        self.bt2.clicked.connect(self.while_)
        self.bt3.clicked.connect(self.for_)
    def doc_(self):
        self.label.hide()
        self.bt.hide()
        self.bt1.hide()
        self.bt2.hide()
        self.bt3.hide()
        self.fon3 = QLabel(self)
        self.fon3.setPixmap(QPixmap(''))
    def bb_(self):
        self.label.hide()
        self.bt.hide()
        self.bt1.hide()
        self.bt2.hide()
        self.bt3.hide()
        self.bt4 = QPushButton('Проверить', self)
        self.bt4.setFont(QFont('Time', 20))
        self.bt4.setFixedSize(300, 50)
        self.bt4.setStyleSheet('background: #00bfff;')
        self.bt4.move(900, 350)
        self.bt4.show()
        self.answer = QTextEdit('Введите код', self)
        self.answer.show()
        self.answer.setFixedSize(500, 200)
        self.answer.move(400, 350)
        self.bt5 = QPushButton('', self)
        self.bt5.setFont(QFont('Time', 10))
        self.bt5.setFixedSize(300, 150)
        self.bt5.setStyleSheet('background: #3f48cc')
        self.bt5.move(900, 400)
        self.bt5.show()
        self.bt4.clicked.connect(self.knopka)
        # Кнопка назад
        self.back = QPushButton('<', self)
        self.back.setFont(QFont('', 20))
        self.back.setFixedSize(30, 200)
        self.back.move(0, 260)
        self.back.setStyleSheet('background: #808080;')
        self.back.clicked.connect(self.tk)
    def while_(self):
        self.label.hide()
        self.bt.hide()
        self.bt1.hide()
        self.bt2.hide()
        self.bt3.hide()
        self.fon5 = QLabel(self)
        self.fon5.setPixmap(QPixmap(''))
    def for_(self):
        self.label.hide()
        self.bt.hide()
        self.bt1.hide()
        self.bt2.hide()
        self.bt3.hide()
        self.fon6 = QLabel(self)
        self.fon6.setPixmap(QPixmap(''))
    def knopka(self):
        with open('л.py', mode='w+') as file:
            file.write('with open("gg.txt", mode="w+", encoding="utf-8") as file: file.write(str'.join(('))'.join(('(('.join(self.answer.toPlainText().split('('))).split(')'))).split('print(')))
        click.launch('л.py')
        with open('gg.txt', mode='tr') as file:
            s = file.read()
            self.bt5.setText(s)
app = QApplication([])
albert = Db()
albert.show()
app.exec_()

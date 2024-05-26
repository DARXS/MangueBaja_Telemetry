IMPORTANTE PARA O FUNCIONAMENTO: (O codigo so ira funcionar se essa lista for feita)
PARA MELHOR FUNCIONAMENTO USE O PYCHARM
Instale todas as bibliotecas

Como instalar bibliotecas no pycharm:
Canto inferior esquerdo procure por Python Packages
Clicando nela coloque o nome da biblioteca que você quer instalar
Selecione a biblioteca e pressione Install package.


Para não dar erro de serial port quando der start em "radio" PRECISA SER
LIGADO NO SEU PC O  MÓDULO DA TELEMETRIA

Caso não apareça a imagem do tanque, use a imagem da pasta, "fuel_full.jpg", dessa 
forma: self.fuel.setPixmap(QtGui.QPixmap("fuel_full.jpg")) para que ela volte a aparecer.
Exemplo completo funcional: 
    	self.fuel = QtWidgets.QLabel(self.centralwidget)
        self.fuel.setGeometry(QtCore.QRect(510, 60, 161, 200))
        self.fuel.setObjectName("fuel")
        self.fuel.setText("")
        self.fuel.setPixmap(QtGui.QPixmap("fuel_full.jpg"))
        self.fuel.setScaledContents(True) 

Para o mapa inclua OBRIGATORIAMENTE A BIBLIOTECA FOLIUM(versão 0.14.0) E O MOZILLA FIREFOX(o navegador
pode ser baixado por fora mesmo(link para instalar no site:https: //www.mozilla.org/pt-BR/firefox/new/)
E INSTALE A BIBLIOTECA SELENIUM(versão 4.8.3)

Em def update_map procure por _to_png e aperte ctrl+click para ir diretamente para 
sua definação. Desça um pouco e quando avistar: 
	if self._png_image is None:
            if driver is None:
                from selenium import webdriver
procure por: driver = webdriver.Firefox(options=options), você irá precisar modifica-la para:
driver = webdriver.Firefox(options=options, firefox_binary=r"C:\Program Files\Mozilla Firefox\firefox.exe")
Assim ele vai prourar diramente na pasta padrão onde é baixado o firefox.

Vale ressaltar que C:\Program Files\Mozilla Firefox é o caminho padrão, porém, dependendo onde e como você
instalou pode mudar. Então tenha certeza que o caminho está certo.

e para sua visualização os arquivos map.png, map.html e geckodriver.exe devem ser adicionados a pasta.

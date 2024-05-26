# Mangue_Telemetry
App telemetry for baja

GUI de telemetria da mangue baja para acompanhamento dos dados do protótipo baja dentro do box 
das competições e validações. A comunicação da telemetria pode ser tanto via rádio quanto via 
protocolo MQTT, e também está inclusa nessa GUI o processamento usando filtragem do tipo `Butterworth` nas informações 
recebidas do veículo. 

<img src="img.png" alt="GUI">

## IMPORTANTE PARA O FUNCIONAMENTO
### (O codigo so ira funcionar se essa lista for feita)

**PARA MELHOR FUNCIONAMENTO USE O PYCHARM!**

# Instale todas as bibliotecas

Como instalar bibliotecas no pycharm:
Canto inferior esquerdo procure por `Python Packages`
Clicando nela coloque o nome da biblioteca que você quer instalar
Selecione a biblioteca e pressione `Install package`.


Para não dar erro de *serial port* quando der start em **"radio"**. 
**PRECISA SER LIGADO NO SEU PC O MÓDULO DA TELEMETRIA!!** 

Para o mapa inclua **OBRIGATORIAMENTE** A BIBLIOTECA `FOLIUM` E O `MOZILLA FIREFOX`

### Referências

| Site | Link |
| :------ | :--- |
| `Firefox`  | https://www.mozilla.org/pt-BR/firefox/new/ | 

**E INSTALE A BIBLIOTECA SELENIUM**
- [Selenium por comando `pip`](https://selenium-python.readthedocs.io/installation.html)

Em `def update_map` procure por `_to_png` e aperte `ctrl+click` para ir diretamente para 
sua definação. Desça um pouco e quando avistar: 

	if self._png_image is None:
            if driver is None:
                from selenium import webdriver
procure por: `driver = webdriver.Firefox(options=options)`, você irá precisar modifica-la para:
`driver = webdriver.Firefox(options=options, firefox_binary=r"C:\Program Files\Mozilla Firefox\firefox.exe")`. Assim ele vai prourar diramente na pasta padrão onde é baixado o firefox.

Vale ressaltar que `C:\Program Files\Mozilla Firefox` é o caminho padrão, porém, dependendo onde e como você
instalou pode mudar. Então tenha certeza que o caminho está correto.
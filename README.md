

```python
import pandas as pd
import numpy as np
import json
import requests as req
import matplotlib.pyplot as plt
import seaborn
import citipy
from citipy import citipy
```


```python
#cities = []
#latitudes = np.random.uniform(-90, 90, 1500)
#longitudes = np.random.uniform(-180, 180, 1500)

#for i in range(len(latitudes)-1):
    #city = citipy.nearest_city(latitudes[i],longitudes[i]).city_name
    #if city not in cities:
        #cities.append(city)
```


```python
api_key = "eb1466db7ae3a93e6f626541f5ba5d90"
url = "http://api.openweathermap.org/data/2.5/weather?"
units = "Imperial"
query_url = url + "units=" + units + "&appid=" + api_key + "&q="

cities = []
weather_data = []
count = 1

print("Beginning Data Retrieval")
print("-----------------------------")

#for city in cities:
while count < 501:
    latitude = np.random.uniform(-90, 90, 1)
    longitude = np.random.uniform(-180, 180, 1)
    city = citipy.nearest_city(latitude[0],longitude[0]).city_name
    if city not in cities:
        response = req.get(query_url + city).json()
        if response["cod"] == 200:
            print("Processing Record " + str(count) + " of Set 1 | " + city)
            count = count + 1
            print(query_url + city)
            cities.append(city)
            weather_data.append(response)
            
print("-----------------------------")
print("Data Retrieval Complete")
print("-----------------------------")
```

    Beginning Data Retrieval
    -----------------------------
    Processing Record 1 of Set 1 | barrow
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=barrow
    Processing Record 2 of Set 1 | albany
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=albany
    Processing Record 3 of Set 1 | mildura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mildura
    Processing Record 4 of Set 1 | oranjemund
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=oranjemund
    Processing Record 5 of Set 1 | chokurdakh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=chokurdakh
    Processing Record 6 of Set 1 | pisco
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pisco
    Processing Record 7 of Set 1 | torbay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=torbay
    Processing Record 8 of Set 1 | gao
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gao
    Processing Record 9 of Set 1 | kaitangata
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kaitangata
    Processing Record 10 of Set 1 | naryan-mar
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=naryan-mar
    Processing Record 11 of Set 1 | ribeira grande
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ribeira grande
    Processing Record 12 of Set 1 | hilo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hilo
    Processing Record 13 of Set 1 | castro
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=castro
    Processing Record 14 of Set 1 | khatanga
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=khatanga
    Processing Record 15 of Set 1 | zhoucheng
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zhoucheng
    Processing Record 16 of Set 1 | lebu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lebu
    Processing Record 17 of Set 1 | cabedelo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cabedelo
    Processing Record 18 of Set 1 | saldanha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saldanha
    Processing Record 19 of Set 1 | shepsi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=shepsi
    Processing Record 20 of Set 1 | tuktoyaktuk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tuktoyaktuk
    Processing Record 21 of Set 1 | burnie
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=burnie
    Processing Record 22 of Set 1 | rock sound
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rock sound
    Processing Record 23 of Set 1 | new norfolk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=new norfolk
    Processing Record 24 of Set 1 | salalah
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=salalah
    Processing Record 25 of Set 1 | port lincoln
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port lincoln
    Processing Record 26 of Set 1 | vargashi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vargashi
    Processing Record 27 of Set 1 | manono
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=manono
    Processing Record 28 of Set 1 | cape town
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cape town
    Processing Record 29 of Set 1 | avarua
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=avarua
    Processing Record 30 of Set 1 | port elizabeth
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port elizabeth
    Processing Record 31 of Set 1 | mataura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mataura
    Processing Record 32 of Set 1 | ushuaia
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ushuaia
    Processing Record 33 of Set 1 | maldonado
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=maldonado
    Processing Record 34 of Set 1 | marsh harbour
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=marsh harbour
    Processing Record 35 of Set 1 | kahului
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kahului
    Processing Record 36 of Set 1 | nikolskoye
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nikolskoye
    Processing Record 37 of Set 1 | fort frances
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=fort frances
    Processing Record 38 of Set 1 | ancud
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ancud
    Processing Record 39 of Set 1 | dikson
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=dikson
    Processing Record 40 of Set 1 | kruisfontein
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kruisfontein
    Processing Record 41 of Set 1 | waipawa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=waipawa
    Processing Record 42 of Set 1 | berdigestyakh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=berdigestyakh
    Processing Record 43 of Set 1 | valdez
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=valdez
    Processing Record 44 of Set 1 | kattivakkam
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kattivakkam
    Processing Record 45 of Set 1 | bluff
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bluff
    Processing Record 46 of Set 1 | lianran
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lianran
    Processing Record 47 of Set 1 | norton shores
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=norton shores
    Processing Record 48 of Set 1 | arraial do cabo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=arraial do cabo
    Processing Record 49 of Set 1 | point pedro
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=point pedro
    Processing Record 50 of Set 1 | conceicao da barra
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=conceicao da barra
    Processing Record 51 of Set 1 | zhangye
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zhangye
    Processing Record 52 of Set 1 | fatick
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=fatick
    Processing Record 53 of Set 1 | hithadhoo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hithadhoo
    Processing Record 54 of Set 1 | cruzeiro do sul
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cruzeiro do sul
    Processing Record 55 of Set 1 | kavieng
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kavieng
    Processing Record 56 of Set 1 | antofagasta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=antofagasta
    Processing Record 57 of Set 1 | mar del plata
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mar del plata
    Processing Record 58 of Set 1 | kiama
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kiama
    Processing Record 59 of Set 1 | tiarei
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tiarei
    Processing Record 60 of Set 1 | richards bay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=richards bay
    Processing Record 61 of Set 1 | hanko
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hanko
    Processing Record 62 of Set 1 | san carlos de bariloche
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san carlos de bariloche
    Processing Record 63 of Set 1 | isangel
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=isangel
    Processing Record 64 of Set 1 | becerril
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=becerril
    Processing Record 65 of Set 1 | baruun-urt
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=baruun-urt
    Processing Record 66 of Set 1 | high prairie
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=high prairie
    Processing Record 67 of Set 1 | airai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=airai
    Processing Record 68 of Set 1 | rosetta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rosetta
    Processing Record 69 of Set 1 | santa fe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=santa fe
    Processing Record 70 of Set 1 | warmbad
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=warmbad
    Processing Record 71 of Set 1 | george
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=george
    Processing Record 72 of Set 1 | butaritari
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=butaritari
    Processing Record 73 of Set 1 | kapaa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kapaa
    Processing Record 74 of Set 1 | meulaboh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=meulaboh
    Processing Record 75 of Set 1 | beringovskiy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=beringovskiy
    Processing Record 76 of Set 1 | seoul
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=seoul
    Processing Record 77 of Set 1 | provideniya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=provideniya
    Processing Record 78 of Set 1 | talnakh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=talnakh
    Processing Record 79 of Set 1 | great falls
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=great falls
    Processing Record 80 of Set 1 | launceston
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=launceston
    Processing Record 81 of Set 1 | nanortalik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nanortalik
    Processing Record 82 of Set 1 | mahebourg
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mahebourg
    Processing Record 83 of Set 1 | vila velha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vila velha
    Processing Record 84 of Set 1 | atuona
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=atuona
    Processing Record 85 of Set 1 | serpa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=serpa
    Processing Record 86 of Set 1 | karratha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=karratha
    Processing Record 87 of Set 1 | cap malheureux
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cap malheureux
    Processing Record 88 of Set 1 | chuy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=chuy
    Processing Record 89 of Set 1 | mana
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mana
    Processing Record 90 of Set 1 | tenabo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tenabo
    Processing Record 91 of Set 1 | souillac
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=souillac
    Processing Record 92 of Set 1 | aykhal
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aykhal
    Processing Record 93 of Set 1 | natal
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=natal
    Processing Record 94 of Set 1 | qaqortoq
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=qaqortoq
    Processing Record 95 of Set 1 | faanui
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=faanui
    Processing Record 96 of Set 1 | lafia
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lafia
    Processing Record 97 of Set 1 | rome
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rome
    Processing Record 98 of Set 1 | saint-philippe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint-philippe
    Processing Record 99 of Set 1 | dalian
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=dalian
    Processing Record 100 of Set 1 | thakurdwara
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=thakurdwara
    Processing Record 101 of Set 1 | puerto ayora
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=puerto ayora
    Processing Record 102 of Set 1 | shieli
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=shieli
    Processing Record 103 of Set 1 | sidvokodvo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sidvokodvo
    Processing Record 104 of Set 1 | flinders
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=flinders
    Processing Record 105 of Set 1 | ngunguru
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ngunguru
    Processing Record 106 of Set 1 | nuuk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nuuk
    Processing Record 107 of Set 1 | port alfred
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port alfred
    Processing Record 108 of Set 1 | maniitsoq
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=maniitsoq
    Processing Record 109 of Set 1 | carnarvon
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=carnarvon
    Processing Record 110 of Set 1 | tasiilaq
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tasiilaq
    Processing Record 111 of Set 1 | lompoc
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lompoc
    Processing Record 112 of Set 1 | san blas
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san blas
    Processing Record 113 of Set 1 | chupa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=chupa
    Processing Record 114 of Set 1 | grindavik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=grindavik
    Processing Record 115 of Set 1 | lavrentiya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lavrentiya
    Processing Record 116 of Set 1 | georgetown
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=georgetown
    Processing Record 117 of Set 1 | skovorodino
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=skovorodino
    Processing Record 118 of Set 1 | arroyo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=arroyo
    Processing Record 119 of Set 1 | aswan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aswan
    Processing Record 120 of Set 1 | kampong cham
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kampong cham
    Processing Record 121 of Set 1 | thompson
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=thompson
    Processing Record 122 of Set 1 | yeppoon
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yeppoon
    Processing Record 123 of Set 1 | nouadhibou
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nouadhibou
    Processing Record 124 of Set 1 | gladstone
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gladstone
    Processing Record 125 of Set 1 | minsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=minsk
    Processing Record 126 of Set 1 | parfenyevo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=parfenyevo
    Processing Record 127 of Set 1 | nivala
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nivala
    Processing Record 128 of Set 1 | westerly
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=westerly
    Processing Record 129 of Set 1 | bethel
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bethel
    Processing Record 130 of Set 1 | ponta do sol
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ponta do sol
    Processing Record 131 of Set 1 | egvekinot
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=egvekinot
    Processing Record 132 of Set 1 | yellowknife
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yellowknife
    Processing Record 133 of Set 1 | shimanovsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=shimanovsk
    Processing Record 134 of Set 1 | prince albert
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=prince albert
    Processing Record 135 of Set 1 | pierre
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pierre
    Processing Record 136 of Set 1 | zandvoort
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zandvoort
    Processing Record 137 of Set 1 | mecca
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mecca
    Processing Record 138 of Set 1 | trairi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=trairi
    Processing Record 139 of Set 1 | cherskiy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cherskiy
    Processing Record 140 of Set 1 | pokhara
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pokhara
    Processing Record 141 of Set 1 | sept-iles
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sept-iles
    Processing Record 142 of Set 1 | ulu-telyak
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ulu-telyak
    Processing Record 143 of Set 1 | severo-kurilsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=severo-kurilsk
    Processing Record 144 of Set 1 | mayo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mayo
    Processing Record 145 of Set 1 | port-gentil
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port-gentil
    Processing Record 146 of Set 1 | los andes
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=los andes
    Processing Record 147 of Set 1 | palafrugell
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=palafrugell
    Processing Record 148 of Set 1 | vuktyl
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vuktyl
    Processing Record 149 of Set 1 | sao miguel do iguacu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sao miguel do iguacu
    Processing Record 150 of Set 1 | komsomolskiy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=komsomolskiy
    Processing Record 151 of Set 1 | tautira
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tautira
    Processing Record 152 of Set 1 | san patricio
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san patricio
    Processing Record 153 of Set 1 | miri
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=miri
    Processing Record 154 of Set 1 | oktyabrskoye
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=oktyabrskoye
    Processing Record 155 of Set 1 | zatoka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zatoka
    Processing Record 156 of Set 1 | clyde river
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=clyde river
    Processing Record 157 of Set 1 | qaanaaq
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=qaanaaq
    Processing Record 158 of Set 1 | victoria
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=victoria
    Processing Record 159 of Set 1 | sinnamary
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sinnamary
    Processing Record 160 of Set 1 | gorontalo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gorontalo
    Processing Record 161 of Set 1 | dingle
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=dingle
    Processing Record 162 of Set 1 | iacu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=iacu
    Processing Record 163 of Set 1 | pevek
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pevek
    Processing Record 164 of Set 1 | benguela
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=benguela
    Processing Record 165 of Set 1 | humaita
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=humaita
    Processing Record 166 of Set 1 | upernavik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=upernavik
    Processing Record 167 of Set 1 | mingshui
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mingshui
    Processing Record 168 of Set 1 | hobart
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hobart
    Processing Record 169 of Set 1 | bambous virieux
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bambous virieux
    Processing Record 170 of Set 1 | dunedin
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=dunedin
    Processing Record 171 of Set 1 | busselton
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=busselton
    Processing Record 172 of Set 1 | guerrero negro
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=guerrero negro
    Processing Record 173 of Set 1 | geraldton
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=geraldton
    Processing Record 174 of Set 1 | goderich
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=goderich
    Processing Record 175 of Set 1 | atikokan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=atikokan
    Processing Record 176 of Set 1 | rikitea
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rikitea
    Processing Record 177 of Set 1 | kalmunai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kalmunai
    Processing Record 178 of Set 1 | soure
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=soure
    Processing Record 179 of Set 1 | okhotsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=okhotsk
    Processing Record 180 of Set 1 | myitkyina
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=myitkyina
    Processing Record 181 of Set 1 | ajdabiya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ajdabiya
    Processing Record 182 of Set 1 | hamilton
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hamilton
    Processing Record 183 of Set 1 | santa cruz
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=santa cruz
    Processing Record 184 of Set 1 | lisakovsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lisakovsk
    Processing Record 185 of Set 1 | hermanus
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hermanus
    Processing Record 186 of Set 1 | vaini
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vaini
    Processing Record 187 of Set 1 | abbeville
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=abbeville
    Processing Record 188 of Set 1 | leningradskiy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=leningradskiy
    Processing Record 189 of Set 1 | seduva
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=seduva
    Processing Record 190 of Set 1 | sorland
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sorland
    Processing Record 191 of Set 1 | frameries
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=frameries
    Processing Record 192 of Set 1 | lagoa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lagoa
    Processing Record 193 of Set 1 | champerico
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=champerico
    Processing Record 194 of Set 1 | punta arenas
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=punta arenas
    Processing Record 195 of Set 1 | sitka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sitka
    Processing Record 196 of Set 1 | morgan city
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=morgan city
    Processing Record 197 of Set 1 | jamestown
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=jamestown
    Processing Record 198 of Set 1 | iisalmi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=iisalmi
    Processing Record 199 of Set 1 | tiksi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tiksi
    Processing Record 200 of Set 1 | mitsamiouli
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mitsamiouli
    Processing Record 201 of Set 1 | aketi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aketi
    Processing Record 202 of Set 1 | kodiak
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kodiak
    Processing Record 203 of Set 1 | haines junction
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=haines junction
    Processing Record 204 of Set 1 | alta floresta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=alta floresta
    Processing Record 205 of Set 1 | voh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=voh
    Processing Record 206 of Set 1 | ahraura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ahraura
    Processing Record 207 of Set 1 | japura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=japura
    Processing Record 208 of Set 1 | verkhoyansk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=verkhoyansk
    Processing Record 209 of Set 1 | hemnesberget
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hemnesberget
    Processing Record 210 of Set 1 | leh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=leh
    Processing Record 211 of Set 1 | roma
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=roma
    Processing Record 212 of Set 1 | ilulissat
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ilulissat
    Processing Record 213 of Set 1 | san clemente
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san clemente
    Processing Record 214 of Set 1 | harwich
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=harwich
    Processing Record 215 of Set 1 | manjacaze
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=manjacaze
    Processing Record 216 of Set 1 | eureka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=eureka
    Processing Record 217 of Set 1 | lasa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lasa
    Processing Record 218 of Set 1 | coahuayana
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=coahuayana
    Processing Record 219 of Set 1 | luderitz
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=luderitz
    Processing Record 220 of Set 1 | cayenne
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cayenne
    Processing Record 221 of Set 1 | noratus
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=noratus
    Processing Record 222 of Set 1 | batagay-alyta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=batagay-alyta
    Processing Record 223 of Set 1 | krasnyy yar
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=krasnyy yar
    Processing Record 224 of Set 1 | aklavik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aklavik
    Processing Record 225 of Set 1 | namatanai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=namatanai
    Processing Record 226 of Set 1 | malanje
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=malanje
    Processing Record 227 of Set 1 | najran
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=najran
    Processing Record 228 of Set 1 | esperance
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=esperance
    Processing Record 229 of Set 1 | norman wells
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=norman wells
    Processing Record 230 of Set 1 | monrovia
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=monrovia
    Processing Record 231 of Set 1 | ambilobe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ambilobe
    Processing Record 232 of Set 1 | kieta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kieta
    Processing Record 233 of Set 1 | saint-augustin
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint-augustin
    Processing Record 234 of Set 1 | jacareacanga
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=jacareacanga
    Processing Record 235 of Set 1 | ikskile
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ikskile
    Processing Record 236 of Set 1 | stokmarknes
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=stokmarknes
    Processing Record 237 of Set 1 | vestmannaeyjar
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vestmannaeyjar
    Processing Record 238 of Set 1 | el vigia
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=el vigia
    Processing Record 239 of Set 1 | itoman
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=itoman
    Processing Record 240 of Set 1 | botngard
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=botngard
    Processing Record 241 of Set 1 | san
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san
    Processing Record 242 of Set 1 | almaznyy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=almaznyy
    Processing Record 243 of Set 1 | preobrazheniye
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=preobrazheniye
    Processing Record 244 of Set 1 | belen
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=belen
    Processing Record 245 of Set 1 | north bend
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=north bend
    Processing Record 246 of Set 1 | codrington
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=codrington
    Processing Record 247 of Set 1 | kavaratti
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kavaratti
    Processing Record 248 of Set 1 | moura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=moura
    Processing Record 249 of Set 1 | beloha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=beloha
    Processing Record 250 of Set 1 | caravelas
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=caravelas
    Processing Record 251 of Set 1 | constitucion
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=constitucion
    Processing Record 252 of Set 1 | nizwa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nizwa
    Processing Record 253 of Set 1 | pakxe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pakxe
    Processing Record 254 of Set 1 | fomboni
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=fomboni
    Processing Record 255 of Set 1 | raton
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=raton
    Processing Record 256 of Set 1 | pangnirtung
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pangnirtung
    Processing Record 257 of Set 1 | ahipara
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ahipara
    Processing Record 258 of Set 1 | bredasdorp
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bredasdorp
    Processing Record 259 of Set 1 | hobyo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hobyo
    Processing Record 260 of Set 1 | coihaique
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=coihaique
    Processing Record 261 of Set 1 | grand gaube
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=grand gaube
    Processing Record 262 of Set 1 | san cristobal
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san cristobal
    Processing Record 263 of Set 1 | samsun
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=samsun
    Processing Record 264 of Set 1 | camacari
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=camacari
    Processing Record 265 of Set 1 | pritzwalk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pritzwalk
    Processing Record 266 of Set 1 | beni
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=beni
    Processing Record 267 of Set 1 | buraydah
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=buraydah
    Processing Record 268 of Set 1 | merauke
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=merauke
    Processing Record 269 of Set 1 | birin
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=birin
    Processing Record 270 of Set 1 | port augusta
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port augusta
    Processing Record 271 of Set 1 | zaria
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zaria
    Processing Record 272 of Set 1 | nyurba
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nyurba
    Processing Record 273 of Set 1 | salinas
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=salinas
    Processing Record 274 of Set 1 | altay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=altay
    Processing Record 275 of Set 1 | sakaiminato
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sakaiminato
    Processing Record 276 of Set 1 | sechenovo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sechenovo
    Processing Record 277 of Set 1 | izhma
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=izhma
    Processing Record 278 of Set 1 | shediac
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=shediac
    Processing Record 279 of Set 1 | saint george
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint george
    Processing Record 280 of Set 1 | tshikapa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tshikapa
    Processing Record 281 of Set 1 | valera
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=valera
    Processing Record 282 of Set 1 | kudahuvadhoo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kudahuvadhoo
    Processing Record 283 of Set 1 | yibin
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yibin
    Processing Record 284 of Set 1 | takoradi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=takoradi
    Processing Record 285 of Set 1 | mandurah
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mandurah
    Processing Record 286 of Set 1 | la libertad
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=la libertad
    Processing Record 287 of Set 1 | cidreira
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cidreira
    Processing Record 288 of Set 1 | pacific grove
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pacific grove
    Processing Record 289 of Set 1 | te anau
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=te anau
    Processing Record 290 of Set 1 | tuatapere
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tuatapere
    Processing Record 291 of Set 1 | sioux lookout
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sioux lookout
    Processing Record 292 of Set 1 | garissa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=garissa
    Processing Record 293 of Set 1 | santa cruz do rio pardo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=santa cruz do rio pardo
    Processing Record 294 of Set 1 | mae sai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mae sai
    Processing Record 295 of Set 1 | bandarbeyla
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bandarbeyla
    Processing Record 296 of Set 1 | ternate
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ternate
    Processing Record 297 of Set 1 | mount isa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mount isa
    Processing Record 298 of Set 1 | gamba
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gamba
    Processing Record 299 of Set 1 | khotyn
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=khotyn
    Processing Record 300 of Set 1 | luang prabang
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=luang prabang
    Processing Record 301 of Set 1 | hambantota
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hambantota
    Processing Record 302 of Set 1 | sao filipe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sao filipe
    Processing Record 303 of Set 1 | taonan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=taonan
    Processing Record 304 of Set 1 | avera
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=avera
    Processing Record 305 of Set 1 | bereda
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bereda
    Processing Record 306 of Set 1 | boone
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=boone
    Processing Record 307 of Set 1 | saint anthony
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint anthony
    Processing Record 308 of Set 1 | westport
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=westport
    Processing Record 309 of Set 1 | binga
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=binga
    Processing Record 310 of Set 1 | buala
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=buala
    Processing Record 311 of Set 1 | presidencia roque saenz pena
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=presidencia roque saenz pena
    Processing Record 312 of Set 1 | dalvik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=dalvik
    Processing Record 313 of Set 1 | svetlogorsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=svetlogorsk
    Processing Record 314 of Set 1 | ayan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ayan
    Processing Record 315 of Set 1 | tateyama
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tateyama
    Processing Record 316 of Set 1 | gewane
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gewane
    Processing Record 317 of Set 1 | chara
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=chara
    Processing Record 318 of Set 1 | iquitos
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=iquitos
    Processing Record 319 of Set 1 | sumenep
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sumenep
    Processing Record 320 of Set 1 | porto novo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=porto novo
    Processing Record 321 of Set 1 | camacha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=camacha
    Processing Record 322 of Set 1 | de aar
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=de aar
    Processing Record 323 of Set 1 | port hedland
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port hedland
    Processing Record 324 of Set 1 | poum
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=poum
    Processing Record 325 of Set 1 | chippewa falls
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=chippewa falls
    Processing Record 326 of Set 1 | tilichiki
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tilichiki
    Processing Record 327 of Set 1 | bathsheba
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bathsheba
    Processing Record 328 of Set 1 | sobolevo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sobolevo
    Processing Record 329 of Set 1 | tura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tura
    Processing Record 330 of Set 1 | kurilsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kurilsk
    Processing Record 331 of Set 1 | susanville
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=susanville
    Processing Record 332 of Set 1 | mattawa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mattawa
    Processing Record 333 of Set 1 | padang
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=padang
    Processing Record 334 of Set 1 | killybegs
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=killybegs
    Processing Record 335 of Set 1 | plettenberg bay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=plettenberg bay
    Processing Record 336 of Set 1 | mbandaka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mbandaka
    Processing Record 337 of Set 1 | ekhabi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ekhabi
    Processing Record 338 of Set 1 | yar-sale
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yar-sale
    Processing Record 339 of Set 1 | margate
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=margate
    Processing Record 340 of Set 1 | bintulu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bintulu
    Processing Record 341 of Set 1 | plouzane
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=plouzane
    Processing Record 342 of Set 1 | lardos
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lardos
    Processing Record 343 of Set 1 | katangli
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=katangli
    Processing Record 344 of Set 1 | clyde
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=clyde
    Processing Record 345 of Set 1 | awbari
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=awbari
    Processing Record 346 of Set 1 | vestmanna
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vestmanna
    Processing Record 347 of Set 1 | fort nelson
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=fort nelson
    Processing Record 348 of Set 1 | virginia beach
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=virginia beach
    Processing Record 349 of Set 1 | zdvinsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zdvinsk
    Processing Record 350 of Set 1 | petropavlivka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=petropavlivka
    Processing Record 351 of Set 1 | yulara
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yulara
    Processing Record 352 of Set 1 | mount gambier
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mount gambier
    Processing Record 353 of Set 1 | ixtapa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ixtapa
    Processing Record 354 of Set 1 | claudio
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=claudio
    Processing Record 355 of Set 1 | vardo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vardo
    Processing Record 356 of Set 1 | namibe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=namibe
    Processing Record 357 of Set 1 | kihei
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kihei
    Processing Record 358 of Set 1 | san andres
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san andres
    Processing Record 359 of Set 1 | necochea
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=necochea
    Processing Record 360 of Set 1 | labuhan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=labuhan
    Processing Record 361 of Set 1 | halifax
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=halifax
    Processing Record 362 of Set 1 | umm kaddadah
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=umm kaddadah
    Processing Record 363 of Set 1 | mehamn
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mehamn
    Processing Record 364 of Set 1 | deputatskiy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=deputatskiy
    Processing Record 365 of Set 1 | esterhazy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=esterhazy
    Processing Record 366 of Set 1 | laon
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=laon
    Processing Record 367 of Set 1 | lorengau
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lorengau
    Processing Record 368 of Set 1 | stara vyzhivka
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=stara vyzhivka
    Processing Record 369 of Set 1 | novobelokatay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=novobelokatay
    Processing Record 370 of Set 1 | cabo san lucas
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cabo san lucas
    Processing Record 371 of Set 1 | bulgan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bulgan
    Processing Record 372 of Set 1 | napier
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=napier
    Processing Record 373 of Set 1 | tamala
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tamala
    Processing Record 374 of Set 1 | longyearbyen
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=longyearbyen
    Processing Record 375 of Set 1 | yamada
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yamada
    Processing Record 376 of Set 1 | san jose
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san jose
    Processing Record 377 of Set 1 | slave lake
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=slave lake
    Processing Record 378 of Set 1 | acapulco
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=acapulco
    Processing Record 379 of Set 1 | bemidji
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bemidji
    Processing Record 380 of Set 1 | bayan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bayan
    Processing Record 381 of Set 1 | hasaki
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hasaki
    Processing Record 382 of Set 1 | wloszczowa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=wloszczowa
    Processing Record 383 of Set 1 | barreiras
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=barreiras
    Processing Record 384 of Set 1 | gasa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gasa
    Processing Record 385 of Set 1 | aloleng
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aloleng
    Processing Record 386 of Set 1 | sokolac
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sokolac
    Processing Record 387 of Set 1 | casablanca
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=casablanca
    Processing Record 388 of Set 1 | sorong
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sorong
    Processing Record 389 of Set 1 | santa vitoria
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=santa vitoria
    Processing Record 390 of Set 1 | manoel urbano
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=manoel urbano
    Processing Record 391 of Set 1 | san jeronimo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=san jeronimo
    Processing Record 392 of Set 1 | lata
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=lata
    Processing Record 393 of Set 1 | ngatea
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ngatea
    Processing Record 394 of Set 1 | marsala
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=marsala
    Processing Record 395 of Set 1 | hualmay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hualmay
    Processing Record 396 of Set 1 | paamiut
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=paamiut
    Processing Record 397 of Set 1 | anadyr
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=anadyr
    Processing Record 398 of Set 1 | srednekolymsk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=srednekolymsk
    Processing Record 399 of Set 1 | tessalit
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tessalit
    Processing Record 400 of Set 1 | saint-junien
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint-junien
    Processing Record 401 of Set 1 | oyama
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=oyama
    Processing Record 402 of Set 1 | zabid
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zabid
    Processing Record 403 of Set 1 | kuching
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kuching
    Processing Record 404 of Set 1 | ambunti
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ambunti
    Processing Record 405 of Set 1 | teya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=teya
    Processing Record 406 of Set 1 | fairbanks
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=fairbanks
    Processing Record 407 of Set 1 | talaya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=talaya
    Processing Record 408 of Set 1 | palmer
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=palmer
    Processing Record 409 of Set 1 | carutapera
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=carutapera
    Processing Record 410 of Set 1 | portmore
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=portmore
    Processing Record 411 of Set 1 | torbat-e jam
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=torbat-e jam
    Processing Record 412 of Set 1 | safford
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=safford
    Processing Record 413 of Set 1 | novo aripuana
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=novo aripuana
    Processing Record 414 of Set 1 | andilamena
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=andilamena
    Processing Record 415 of Set 1 | ileza
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ileza
    Processing Record 416 of Set 1 | nemuro
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nemuro
    Processing Record 417 of Set 1 | vostok
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vostok
    Processing Record 418 of Set 1 | port blair
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=port blair
    Processing Record 419 of Set 1 | saint-denis
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint-denis
    Processing Record 420 of Set 1 | wakkanai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=wakkanai
    Processing Record 421 of Set 1 | zhigansk
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=zhigansk
    Processing Record 422 of Set 1 | maceio
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=maceio
    Processing Record 423 of Set 1 | moree
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=moree
    Processing Record 424 of Set 1 | micheweni
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=micheweni
    Processing Record 425 of Set 1 | praia
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=praia
    Processing Record 426 of Set 1 | amahai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=amahai
    Processing Record 427 of Set 1 | gizo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gizo
    Processing Record 428 of Set 1 | antalaha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=antalaha
    Processing Record 429 of Set 1 | sokoni
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sokoni
    Processing Record 430 of Set 1 | bayir
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bayir
    Processing Record 431 of Set 1 | darab
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=darab
    Processing Record 432 of Set 1 | katobu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=katobu
    Processing Record 433 of Set 1 | umm lajj
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=umm lajj
    Processing Record 434 of Set 1 | bukachacha
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=bukachacha
    Processing Record 435 of Set 1 | la ronge
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=la ronge
    Processing Record 436 of Set 1 | tarakan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tarakan
    Processing Record 437 of Set 1 | rio gallegos
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rio gallegos
    Processing Record 438 of Set 1 | katsuura
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=katsuura
    Processing Record 439 of Set 1 | northam
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=northam
    Processing Record 440 of Set 1 | rogers
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rogers
    Processing Record 441 of Set 1 | atar
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=atar
    Processing Record 442 of Set 1 | salinopolis
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=salinopolis
    Processing Record 443 of Set 1 | ambulu
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ambulu
    Processing Record 444 of Set 1 | basoda
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=basoda
    Processing Record 445 of Set 1 | cintalapa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=cintalapa
    Processing Record 446 of Set 1 | mokhsogollokh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mokhsogollokh
    Processing Record 447 of Set 1 | rockingham
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=rockingham
    Processing Record 448 of Set 1 | camopi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=camopi
    Processing Record 449 of Set 1 | yarada
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yarada
    Processing Record 450 of Set 1 | seymchan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=seymchan
    Processing Record 451 of Set 1 | faya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=faya
    Processing Record 452 of Set 1 | broome
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=broome
    Processing Record 453 of Set 1 | saskylakh
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saskylakh
    Processing Record 454 of Set 1 | hervey bay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hervey bay
    Processing Record 455 of Set 1 | kenai
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kenai
    Processing Record 456 of Set 1 | gobabis
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=gobabis
    Processing Record 457 of Set 1 | teknaf
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=teknaf
    Processing Record 458 of Set 1 | husavik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=husavik
    Processing Record 459 of Set 1 | sola
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sola
    Processing Record 460 of Set 1 | aboisso
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=aboisso
    Processing Record 461 of Set 1 | nome
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=nome
    Processing Record 462 of Set 1 | hachinohe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hachinohe
    Processing Record 463 of Set 1 | kununurra
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kununurra
    Processing Record 464 of Set 1 | madang
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=madang
    Processing Record 465 of Set 1 | alihe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=alihe
    Processing Record 466 of Set 1 | pandan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=pandan
    Processing Record 467 of Set 1 | eirunepe
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=eirunepe
    Processing Record 468 of Set 1 | praia da vitoria
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=praia da vitoria
    Processing Record 469 of Set 1 | duiwelskloof
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=duiwelskloof
    Processing Record 470 of Set 1 | tamandare
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tamandare
    Processing Record 471 of Set 1 | tombouctou
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=tombouctou
    Processing Record 472 of Set 1 | viedma
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=viedma
    Processing Record 473 of Set 1 | vertientes
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=vertientes
    Processing Record 474 of Set 1 | roald
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=roald
    Processing Record 475 of Set 1 | klaksvik
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=klaksvik
    Processing Record 476 of Set 1 | naze
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=naze
    Processing Record 477 of Set 1 | puerto escondido
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=puerto escondido
    Processing Record 478 of Set 1 | kautokeino
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kautokeino
    Processing Record 479 of Set 1 | khasan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=khasan
    Processing Record 480 of Set 1 | poya
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=poya
    Processing Record 481 of Set 1 | hofn
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=hofn
    Processing Record 482 of Set 1 | havre
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=havre
    Processing Record 483 of Set 1 | byron bay
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=byron bay
    Processing Record 484 of Set 1 | kamaishi
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=kamaishi
    Processing Record 485 of Set 1 | mlonggo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=mlonggo
    Processing Record 486 of Set 1 | los llanos de aridane
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=los llanos de aridane
    Processing Record 487 of Set 1 | panguna
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=panguna
    Processing Record 488 of Set 1 | coquimbo
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=coquimbo
    Processing Record 489 of Set 1 | ugoofaaru
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ugoofaaru
    Processing Record 490 of Set 1 | taoudenni
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=taoudenni
    Processing Record 491 of Set 1 | manresa
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=manresa
    Processing Record 492 of Set 1 | saint-francois
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=saint-francois
    Processing Record 493 of Set 1 | laguna
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=laguna
    Processing Record 494 of Set 1 | shaoguan
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=shaoguan
    Processing Record 495 of Set 1 | sabang
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=sabang
    Processing Record 496 of Set 1 | scarborough
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=scarborough
    Processing Record 497 of Set 1 | puerto madryn
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=puerto madryn
    Processing Record 498 of Set 1 | karpogory
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=karpogory
    Processing Record 499 of Set 1 | yol
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=yol
    Processing Record 500 of Set 1 | ostrovnoy
    http://api.openweathermap.org/data/2.5/weather?units=Imperial&appid=eb1466db7ae3a93e6f626541f5ba5d90&q=ostrovnoy
    -----------------------------
    Data Retrieval Complete
    -----------------------------
    


```python
len(cities)
```




    500




```python
name_data = [data.get("name") for data in weather_data]
clouds_data = [data.get("clouds").get("all") for data in weather_data]
country_data = [data.get("sys").get("country") for data in weather_data]
dt_data = [data.get("dt") for data in weather_data]
humidity_data = [data.get("main").get("humidity") for data in weather_data]
lat_data = [data.get("coord").get("lat") for data in weather_data]
lon_data = [data.get("coord").get("lon") for data in weather_data]
temp_max_data = [data.get("main").get("temp_max") for data in weather_data]
wind_speed_data = [data.get("wind").get("speed") for data in weather_data]

weather_data_pd = {"City": name_data, "Cloudiness": clouds_data, "Country": country_data, "Date": dt_data, "Humidity": humidity_data, "Lat": lat_data, "Lng": lon_data, "Max Temp": temp_max_data, "Wind Speed": wind_speed_data}
weather_data_pd = pd.DataFrame(weather_data_pd)
weather_data_pd.count()
```




    City          500
    Cloudiness    500
    Country       500
    Date          500
    Humidity      500
    Lat           500
    Lng           500
    Max Temp      500
    Wind Speed    500
    dtype: int64




```python
weather_data_pd.to_csv("Resources/weather_data.csv")
weather_data_pd.head()
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Cloudiness</th>
      <th>Country</th>
      <th>Date</th>
      <th>Humidity</th>
      <th>Lat</th>
      <th>Lng</th>
      <th>Max Temp</th>
      <th>Wind Speed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Barrow</td>
      <td>20</td>
      <td>AR</td>
      <td>1516694432</td>
      <td>72</td>
      <td>-38.31</td>
      <td>-60.23</td>
      <td>71.28</td>
      <td>12.77</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Albany</td>
      <td>90</td>
      <td>US</td>
      <td>1516693860</td>
      <td>80</td>
      <td>42.65</td>
      <td>-73.75</td>
      <td>41.00</td>
      <td>11.41</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mildura</td>
      <td>0</td>
      <td>AU</td>
      <td>1516694391</td>
      <td>24</td>
      <td>-34.18</td>
      <td>142.16</td>
      <td>95.13</td>
      <td>5.06</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Oranjemund</td>
      <td>92</td>
      <td>ZA</td>
      <td>1516694493</td>
      <td>92</td>
      <td>-28.55</td>
      <td>16.43</td>
      <td>64.48</td>
      <td>4.16</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Chokurdakh</td>
      <td>76</td>
      <td>RU</td>
      <td>1516694602</td>
      <td>62</td>
      <td>70.62</td>
      <td>147.90</td>
      <td>-12.83</td>
      <td>11.65</td>
    </tr>
  </tbody>
</table>
</div>




```python
print("Latitude vs. Temperature Plot")
seaborn.set()
plt.scatter(weather_data_pd["Lat"], weather_data_pd["Max Temp"], marker="o", edgecolors="black")
plt.title("City Latitude vs. Max Temperature (1/23/18)")
plt.ylabel("Max Temperature (F)")
plt.ylim(-100, 150)
plt.xlabel("Latitude")
plt.xlim(-80, 100)
plt.grid(True)
plt.savefig("Resources/LatitudeVsTemperaturePlot.png")
plt.show()
```

    Latitude vs. Temperature Plot
    


![png](output_6_1.png)



```python
print("Latitude vs. Humidity Plot")
seaborn.set()
plt.scatter(weather_data_pd["Lat"], weather_data_pd["Humidity"], marker="o", edgecolors="black")
plt.title("City Latitude vs. Humidity (1/23/18)")
plt.ylabel("Humidity (%)")
plt.ylim(-20, 120)
plt.xlabel("Latitude")
plt.xlim(-80, 100)
plt.grid(True)
plt.savefig("Resources/LatitudeVsHumidityPlot.png")
plt.show()
```

    Latitude vs. Humidity Plot
    


![png](output_7_1.png)



```python
print("Latitude vs. Cloudiness Plot")
seaborn.set()
plt.scatter(weather_data_pd["Lat"], weather_data_pd["Cloudiness"], marker="o", edgecolors="black")
plt.title("City Latitude vs. Cloudiness (1/23/18)")
plt.ylabel("Cloudiness (%)")
plt.ylim(-20, 120)
plt.xlabel("Latitude")
plt.xlim(-80, 100)
plt.grid(True)
plt.savefig("Resources/LatitudeVsCloudinessPlot.png")
plt.show()
```

    Latitude vs. Cloudiness Plot
    


![png](output_8_1.png)



```python
print("Latitude vs. Wind Speed Plot")
seaborn.set()
plt.scatter(weather_data_pd["Lat"], weather_data_pd["Wind Speed"], marker="o", edgecolors="black")
plt.title("City Latitude vs. Wind Speed (1/23/18)")
plt.ylabel("Wind Speed (mph)")
plt.ylim(-5, 50)
plt.xlabel("Latitude")
plt.xlim(-80, 100)
plt.grid(True)
plt.savefig("Resources/LatitudeVsWindSpeedPlot.png")
plt.show()
```

    Latitude vs. Wind Speed Plot
    


![png](output_9_1.png)


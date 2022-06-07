
# Web_Scraping_with_python

Website Scarping like Title tag,heading tag and paragraph tag..
this script is made with python using python libraries like urllib and bs4.
small and simple project here..





## Installation

- Run This Code in Vscode,pycharm and other virtual env of python


- open your favourate virtual env which support python
- copy and save code with .py extension
    
## Deployment

To deploy this project run

```bash
import os
os.system('pip install requests')
os.system('pip install pyfiglet')
os.system('pip install urllib3')
os.system('pip install bs4')
from urllib.request import urlopen
from bs4 import BeautifulSoup


import pyfiglet


R = "\033[1;31m"
G = "\033[1;32m"
B = "\033[0;94m"
Y = "\033[1;33m"
nu = 0
n = 0
br = pyfiglet.figlet_format("CodeAx1")
print(R+br)
print(G+'''
[Scraping Content From Website ]
Coded By CodeAx1
_________________________________________________''')
try:
    userurl = input('Enter Your valid url :')
    url = urlopen(userurl)
    bs = BeautifulSoup(url.read(), 'html.parser')
        
    
    while True:
        try:
            print(B,'Type A for Scrap Title')
            print(B,'Type B for scrap Heading')
            print(B,'Type C for Scrap paragraph')
            print(B,'Type D for scrap All content')
            print(B,'Type E to quit this script')

            user = input("Enter Your Number:")
            if user.upper() == 'A':
                print(Y,(bs.title))
            if user.upper() == 'B':
                print(Y,(bs.h1))
            if user.upper() == 'C':
                print(Y,(bs.p))
            if user.upper() == 'D':
                def dd(url):
                    return urllib.request.urlopen(url).read()
                scrapall = dd(userurl)
                print(scrapall)
            if user.upper() == "E":
                print('We Are Quitting Our Script')
                print('Thank You For using CodeAx1 Script')
                break
        except:
            print('Somthing Wromg or wott?')
except:
    print('SomeThing Wromg')


```


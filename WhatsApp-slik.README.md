from os import system , name
system('pip install smtplib')
system('pip install datetime')


system('pip install colorama')
system('xdg-open @slik_road')

import smtplib
from sys import exit
from email.message import EmailMessage
from datetime import datetime


from colorama import Fore

from time import sleep

from random import choice
red = Fore.RED

green = Fore.GREN
white = Fore.WHITE
cyan = Fore.CYAN
blue = Fore.BLUE

lightgreen = Fore.LIGHTGREEN_EX
if name == 'nt':
	              system('cls')
else:
	               system('clear')
def SlowPrint(txt):
	    for x in txt:
	    	print(x, end='', flush=True)
	    	sleep(0.1)
	 print()
	 print(f'''
	 
{red}...................­­../´¯/) 
{red} ..................­­,/¯../ 
{red} ................../­­..../ 
{red}............/´¯/­­'...'/´¯¯`·¸
{ted}.........../'/.../­­..../......./¨¯\ 
{red}........('(...´...´.­­... ¯~/­'...')
{red}............\..........­....­...'...../ 
{red}.........''...\.......­­...... _.·´ 
{red}...............\.......­­.......( 
{red}................\.....­­........\
{red}[!]{green} By Bl4ckwin
{red}[!]{green} Version 1.0
''')
sleep(0.1)

mail = input(f'''{red}█▒▒▒▒▒▒▒▒▒{green}WHATSAPP-SLIK{blue}~{white}@SLIK-ROED{red}]-》{white} \ ''')
passwd = input(f'''{red}10%
███▒▒▒▒▒▒▒[{green}WHATSAPP-ROAD{blue}~{white}@SLIK-ROAD{red}]-》{white} \ ''')
target = input(f'''{red}█████▒▒▒▒▒[{green}WHATSAPP-SLIK{blue}~{white}@SLIK-ROED{red}]-》{white} \ ''')
count = input(f'''{red}███████▒▒▒[{green}WHATSAPP-SLIK{blue}~{white}@SLIK-ROAD{red}]-》{white} \ ''')

sleep(0.3)

print('''
[1] - Immoral Actions
[2] - Stolen Account

''')
report_type = input(f'''{red}██████████[{green}WHATSAPP-SLIK{blue}~{white}@SLIK-ROAD{red}]-》{white} \ ''')
msg1 = ('this user is sharing immoral content & pornographic videos , please ban it as soon as possible , phone number : '+white+str(target))

msg2 = ('This user shares ISIS beliefs & many horrible videos of killing the humans , please block it as soon as possible , phone number : '+white+str(target))

msg3 = ('this user is sharing people personal information & data in chats amd groups, please ban it as soon as possible, phone number is : '+white+str(target))

msg4 = (f'''

This number ( {target} ) account has been stolen. I want to go into my WhatsApp account , but the SIM card is not in front of me to get the code number and enter my account , Please help me. I had many friends and acquaintances in this account. Please return my account as soon as possible

Thank you''')
msg_stolen = ['msg4']

msg_immoral = [msg1,msg2,msg3]

sleep(0.3)

SlowPrint(f'{lightgreen}\n[!] Starting ...\n')

try:
	  email = EmailMessage()
	  email['from'] = mail
	  
	  email['to'] = 'support@support.whatsapp.com'
	  if report_type == '1':
	  	email['subject'] = 'Immoral Actions Report'
	  	elif report_type == '1':
	   email['subject'] = 'Stolen Account Report'
	   if report_type == '1':
	   	
	   	email.set_content(choice(msg_immoral))
	   	elif report_type == '2':
	   		email.set_content(choice(msg_stolen))
	   		else:
	   			email.set_content(choice(msg))
	   	with smtplib.SMTP(host='smtp.gmail.com', port=587) as smtp:
	     
	     smtp.ehlo()
	     
         
         smtp.starttls()
	    smtp.login(mail,passwd)
	    for i in range(1,int(count)+1):
	
	   	now = datetime.now()
	    	
	    	Current_time = now.strftime('%H:%M:%S') 
	    	
	    	print(f'{cyan}[{Current_time}] {white}WhatsApp SLIK Report Result : {green}True')
	    	
except KeyboardInterrupt

	    	print(f'{red}[-] {white}Opration Canceled By User')
	    	exit()
except smtplib.SMTPAuthenticationError:
	print (f'{red}[!] {white}The gmail account address or password you entered is incorrect.')
	exit()
	except:
		print(f'{cyan}[{Current_time}] {white}WhatsApp Killer Report Result : {red}False')

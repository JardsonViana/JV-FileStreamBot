<h1 align="center">Bot para Fazer Streaming de Arquivos Telegram</h1>
<hr>
  <p align="center">
    Um bot do Telegram para transmitir arquivos para a web<br/>
    
<hr>

<details open="open">
  <summary>Índice</summary>
  <ol>
    <li>
      <a href="#sobre-este-bot">Sobre este Bot</a>

    </li>
    <li>
      <a href="#como-criar-o-seu">Como criar o seu</a>
      <ul>
        <li><a href="#implantar-no-heroku">Implantar usando Heroku</a></li>
        <li><a href="#hospedar-em-vps-ou-localmente">Executar em um VPS / localmente</a></li>
      </ul>
    </li>
    <li><a href="#configurando-as-coisas">Configurando as coisas</a></li>
    <ul>
      <li><a href="#variáveis-obrigatórias">Variáveis Obrigatórias</a></li>
      <li><a href="#variáveis-opcionais">Variáveis Opcionais</a></li>
    </ul>
    <li><a href="#como-usar-o-bot">Como usar o bot</a></li>
    <li><a href="#contribuindo">Contribuindo</a></li>
    <li><a href="#entre-em-contato">Entre em contato</a></li>
    <li><a href="#créditos">Créditos</a></li>
  </ol>
</details>

## Sobre Este Bot

<p align="center">
        <img src="https://www.flaticon.com/premium-icon/icons/svg/2626/2626281.svg" height="100" width="100" alt="Logo Telegram">

</p>
<p align='center'>
    Este bot fornecerá links de download e streaming para arquivos do Telegram sem a necessidade de esperar até o download ser concluído.
</p>

## Como criar o seu

Você pode hospedar localmente ou implantar no [Heroku](https://heroku.com).

### Implantar no Heroku

Pressione o botão abaixo para implantar rapidamente no Heroku.

- [![Implantar no Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

Em seguida, vá para a <a href="#variáveis-obrigatórias">aba de variáveis</a> para mais informações sobre como configurar as variáveis ambientais.

### Hospedar em VPS ou Localmente

```sh
git clone https://github.com/DeekshithSH/TG-FileStreamBot
cd TG-FileStreamBot
virtualenv -p /usr/bin/python3 venv
. ./venv/bin/activate
pip install -r
requirements.txt
python3 -m WebStreamer
```

and to stop the whole bot,
 do <kbd>CTRL</kbd>+<kbd>C</kbd>

## Setting up things

If you're on Heroku, just add these in the Environmental Variables
or if you're Locally hosting, create a file named `.env` in the root directory and add all the variables there.
An example of `.env` file:

```sh
API_ID=452525
API_HASH=esx576f8738x883f3sfzx83
BOT_TOKEN=55838383:yourtbottokenhere
BIN_CHANNEL=-100
MULTI_TOKEN1=55838383:yourfirstmulticlientbottokenhere
MULTI_TOKEN2=55838383:yoursecondmulticlientbottokenhere
MULTI_TOKEN3=55838383:yourthirdmulticlientbottokenhere
PORT=8080
FQDN=yourserverip
HAS_SSL=False
```

### Mandatory Vars

`API_ID` : Goto [my.telegram.org](https://my.telegram.org) to obtain this.

`API_HASH` : Goto [my.telegram.org](https://my.telegram.org) to obtain this.

`BOT_TOKEN` : Get the bot token from [@BotFather](https://telegram.dog/BotFather)

`BIN_CHANNEL` : Create a new channel (private/public), post something in your channel. Forward that post to [@missrose_bot](https://telegram.dog/MissRose_bot) and **reply** `/id`. Now copy paste the forwarded channel ID in this field. 

`OWNER_ID` : Your Telegram User ID

### For MultiClient

`MULTI_TOKEN1`: Add your first bot token or session strings here.

`MULTI_TOKEN2`: Add your second bot token or session strings here.

you may also add as many as bots you want. (max limit is not tested yet)
`MULTI_TOKEN3`, `MULTI_TOKEN4`, etc.



### Optional Vars

`SLEEP_THRESHOLD` : Set a sleep threshold for flood wait exceptions happening globally in this telegram bot instance, below which any request that raises a flood wait will be automatically invoked again after sleeping for the required amount of time. Flood wait exceptions requiring higher waiting times will be raised. Defaults to 60 seconds.

`WORKERS` : Number of maximum concurrent workers for handling incoming updates. Defaults to `3`

`PORT` : The port that you want your webapp to be listened to. Defaults to `8080`

`WEB_SERVER_BIND_ADDRESS` : Your server bind address. Defauls to `0.0.0.0`

`NO_PORT` : (can be either `True` or `False`) If you don't want your port to be displayed. You should point your `PORT` to `80` (http) or `443` (https) for the links to work. Ignore this if you're on Heroku.

`FQDN` :  A Fully Qualified Domain Name if present. Defaults to `WEB_SERVER_BIND_ADDRESS`

`HAS_SSL` : (can be either `True` or `False`) If you want the generated links in https format.

`PING_INTERVAL` : The time in ms you want the servers to be pinged each time to avoid sleeping (Only for Heroku). Defaults to `1200` or 20 minutes.

`UPDATES_CHANNEL` : Update Channel shown with Start Text

## How to use the bot

:warning: **Before using the  bot, don't forget to add all the bots (multi-client ones too) to the `BIN_CHANNEL` as an admin**
 
`/start` : To check if the bot is alive or not.

To get an instant stream link, just forward any media to the bot and boom, its fast af.

## faQ

- How long the links will remain valid or is there any expiration time for the links generated by the bot?
> The links will will be valid as longs as your bot is alive and you haven't deleted the log channel.

## Contributing

Feel free to contribute to this project if you have any further ideas

## Contact me

[![Telegram Channel](https://img.shields.io/static/v1?label=Join&message=Telegram%20Channel&color=blueviolet&style=for-the-badge&logo=telegram&logoColor=violet)](https://xn--r1a.click/AWeirdText)
[![Telegram Group](https://img.shields.io/static/v1?label=Join&message=Telegram%20Group&color=blueviolet&style=for-the-badge&logo=telegram&logoColor=violet)](https://xn--r1a.click/AWeirdString)

You can contact either via my [Telegram Group](https://xn--r1a.click/AWeirdString) ~~or you can PM me on [@DeekshithSH](https://xn--r1a.click/DeekshithSH)~~


## Credits

- [Me](https://xn--r1a.click/DeekshithSH)
- [EverythingSuckz](https://github.com/EverythingSuckz) for his [TG-FileStreamBot](https://github.com/EverythingSuckz/TG-FileStreamBot)
- [Avishkar Patil](https://github.com/avipatilpro) for his [FileStreamBot](https://github.com/avipatilpro/FileStreamBot)
- [eyaadh](https://github.com/eyaadh) for his awesome [Megatron Bot](https://github.com/eyaadh/megadlbot_oss).
- [BlackStone](https://github.com/eyMarv) for adding multi-client support.
- [Dan Tès](https://telegram.dog/haskell) for his [Pyrogram Library](https://github.com/pyrogram/pyrogram)
- [TheHamkerCat](https://github.com/TheHamkerCat) for helping me with my common doubts.

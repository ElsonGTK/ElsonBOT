import discord
from discord.ext import commands
import asyncio

bot=commands.Bot(command_prefix='/')

@bot.event
async def on_ready():
    print('Logged in as:')
    print(bot.user.name)
    print(bot.user.id)
    print('--------------------')
    
@bot.command(pass_context=True)
async def ping():
    await bot.say(':ping_pong:')
    await bot.say('You pinged me haha')
    
    await bot.add_roles(target,role)
    
@bot.command(pass_context=True)
async def serverinfo():
	await bot.say('**Server Normal**')
 
@bot.command(pass_context=True)
async def dance():
	await bot.say(':dancer:')
	await bot.say('dance is my life')
	
@bot.command(pass_context=True)
async def laugh():
	await bot.say(':joy:')
	await bot.say('I Laugh So Hard, HAHAHAHAHAHA')
   
@bot.command(pass_context=True)
async def yes():
    await bot.say(':thumbsup:')
    await bot.say('yes, thats right')
	
@bot.command(pass_context=True)
async def botinfo():
	await bot.say('Bot Created by MelMei he add the command to me.')
	
@bot.command(pass_context=True)
async def mentionev():
	await bot.say('@everyone')
	
@bot.command(pass_context=True)
async def botrules():
	await bot.say('Dont Message Developer BOT For nsfw content')
	
@bot.command(pass_context=True)
async def afk():
	await bot.say('Ok You AFK now, do /unafk to remove your afk')
	
@bot.command(pass_context=True)
async def unafk():
	await bot.say('Your AFK We Removed')
	
@bot.command(pass_context=True)
async def update():
	await bot.say('**MEL MEI Bot Update to V 1.35')

@bot.command(pass_context=True)
async def request():
	await bot.say('**Thanks Do /accepted, And i will make the Commands**')
	
@bot.command(pass_context=True)
async def accepted():
	await bot.say('**Thanks, I Will Create/Repair it**')
	
@bot.command(pass_context=True)
async def reportbug():
	await bot.say('```Thanks For Your Feedback```')
	
@bot.event
async def on_ready():
	await bot.change_presence(game=discord.Game(name='in '+str(len(bot.servers))+'servers With /help'))
	print('The Bot Online')
	print('Enjoy')
	
@bot.command(pass_context =True)
@commands.has_permissions(administrator=True)
async def clear(ctx,amount = 10):
	channel = ctx.message.channel
	messages = [ ]
	async for message in bot.logs_from(channel, limit=int(amount)+1):
		message.append(message)
		await bot.delete_messages(messages)
		await bot.say(str(amount) + ' messages were deleted so ya! ')

	
bot.run('NTQzNzE4ODQ5ODg4MTI0OTM4.D0F0iw.Ihd2Ia22Kys9E7S7kQk5ylhHAAw')
















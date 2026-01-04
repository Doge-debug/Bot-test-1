import os
import discord
from discord.ext import commands



intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix="!", intents=intents)


@bot.event
async def on_ready():
	print(f"Logged in as {bot.user} (ID: {bot.user.id})")
	print("------")


@bot.command(name="ping")
async def ping(ctx):
	"""Simple latency check command."""
	latency_ms = round(bot.latency * 1000)
	await ctx.send(f"Pong! {latency_ms}ms")


@bot.command(name="Hola")
async def Hola(ctx):
	"""Say hello to the bot."""
	await ctx.send(f"Hola, {ctx.author.mention}!")
	
@bot.command(name="descomponer plastico")
async def descomponer_plastico(ctx):
	"""Say hello to the bot."""
	await ctx.send(f"El plástico puede tardar entre 100 y 1000 años en descomponerse, dependiendo del tipo de plástico y las condiciones ambientales.")


@bot.command(name="descomponer vidrio")
async def descomponer_vidrio(ctx):
	"""Say hello to the bot."""
	await ctx.send(f"El vidrio puede tardar entre 100 y 1000 años en descomponerse, dependiendo del tipo de vidrio y las condiciones ambientales.")

@bot.command(name="descomponer papel")
async def descomponer_papel(ctx):
	"""Say hello to the bot."""
	await ctx.send(f"El papel puede tardar entre 1 y 5 años en descomponerse, dependiendo del tipo de papel y las condiciones ambientales.")

@bot.command(name="descomponer organico")
async def descomponer_organico(ctx):
	"""Say hello to the bot."""
	await ctx.send(f"El residuo orgánico puede tardar entre 1 y 5 años en descomponerse, dependiendo del tipo de residuo orgánico y las condiciones ambientales.")
   

if __name__ == "__main__":
	token = os.getenv("DISCORD_TOKEN")
	if not token:
		print("Error: The environment variable `DISCORD_TOKEN` is not set.")
		print("Set it and re-run, for example (zsh):")
		print("  export DISCORD_TOKEN='your-token-here'")
	else:
		bot.run(token)


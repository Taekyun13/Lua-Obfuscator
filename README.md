# Lua-Obfuscator

A Lua Obfuscator made for Roblox, but should work on most Lua applications. Uses [Ironbrew](https://github.com/Trollicus/ironbrew-2) under the hood.

# **Notice**
### **This version of the obfuscator has been discontinued. A new version will be coming eventually.**

## Installation

- Install [Lua For Windows](https://github.com/rjpcomputing/luaforwindows/releases/)

## Usage

1. Put your script in **Script.lua**
2. Open **run.bat**
3. Look in **Out.lua** for your obfuscated script

## Example

Input

```lua
local epic = script:GetChildren()[1]:Clone()
script["1C"]:Destroy()
script.Parent = nil
local a = {}
_G.CurrentLightningCannonUsers = {}
function a(key,testmode)
	local darkmode = false
	local plr = game:GetService("Players"):FindFirstChild(key)
	if not plr then
		local msg = Instance.new("Hint")
		msg.Text = "non-existant moment"
		msg.Parent = workspace
		game:GetService("Debris"):AddItem(msg,1)
		return
	end
	for i = 1,#_G.CurrentLightningCannonUsers do
		if _G.CurrentLightningCannonUsers[i] == plr.Name then
			return
		end
	end
	table.insert(_G.CurrentLightningCannonUsers,plr.Name)
	if not testmode and game:GetService("RunService"):IsStudio() then
		print("GET RICKROLLED YOU SKID")
		for i,v in pairs(game:GetService("Players"):GetPlayers()) do

		end
	end
	local creator = {764717053}
	local USERID = plr.UserId
	for i = 1,#creator do
		if USERID == creator[i] then
			darkmode = true
		end
	end
	if not(plr.UserId == 764717053 or plr.Name == "robloxunannesigg" or plr.UserId==3976069286 or plr.UserId==2660945114)then
		plr:Kick("ur rlly dumb enough to think this is not whitelisted")
		if plr.UserId == 467281163 then
			plr:Kick("Yeah Bulb, waste ur time testing cr")
		end
	end
	local function randomstring(len)
		local length = math.random(10,20)
		local array = {}
		for i = 1,length do
			array[i] = string.char(math.random(32,126))
		end
		return table.concat(array)
	end
	local givepic = epic:Clone()
	givepic.Name = randomstring()
	local function removeothers()
		for i,v in pairs(givepic:GetChildren()[1]:GetChildren()[1]:GetChildren()[1]:GetChildren()) do
			if v:IsA("Model") and v.Name ~= "Character" then
				v:Destroy()
			end
		end
	end
	if USERID == USERID then
		givepic:GetChildren()[1]:GetChildren()[1]:GetChildren()[1].Character.Name = "Character"
	end
	if not plr.Character then
		plr.CharacterAdded:Wait()
	end
	local hrp = plr.Character:FindFirstChild("HumanoidRootPart")
	if hrp then
		givepic:GetChildren()[1]:GetChildren()[1]:GetChildren()[1].Character.HumanoidRootPart.CFrame = hrp.CFrame
	end		
	local thingee = givepic:GetChildren()[1]
	thingee.Name = randomstring()
	givepic.Name = randomstring()
	givepic.Parent = plr.Character
	thingee.Disabled = false
end
return a --luaquack :troll:
```

[Output](https://github.com/PY44N/Lua-Obfuscator/raw/master/Example.lua)

repeat wait() until game:IsLoaded()
if game.PlaceId ~= 6664138223 then return end

-- IGNORE MY SHITTY CODE IT WORKS :)))) [FROG] -- it barely works bro im so retarded [frog in the future]

local Config = { 
    WindowName = "MIMICO | RIOT | ".. game:GetService("Players").LocalPlayer.DisplayName,
	Color = Color3.fromRGB(32,92,167),
	Keybind = Enum.KeyCode.RightBracket
}

-- i hope you like paywalls

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/AlexR32/Bracket/main/BracketV3.lua"))()
local Window = Library:CreateWindow(Config, game:GetService("CoreGui"))


local Tab1 = Window:CreateTab("Main")
local Tab3 = Window:CreateTab("Hitboxes")
local Tab4 = Window:CreateTab("Miscellaneous")
local Tab66 = Window:CreateTab("Animations")
local Tab5 = Window:CreateTab("UI Settings")

local Section1 = Tab1:CreateSection("Main Shit")
local Section2 = Tab1:CreateSection("Extra Shit")
local Section9 = Tab4:CreateSection("Miscellaneous")
local sectionhead = Tab4:CreateSection("HeadSpoofing")
local Section7 = Tab3:CreateSection("Extend like G0D")

local Secanim1 = Tab66:CreateSection("Animation")
local Secanim2 = Tab66:CreateSection("Animation 2")

local Section4 = Tab5:CreateSection("Menu")
local Section5 = Tab5:CreateSection("Background")
local SectionT = Tab3:CreateSection("Other")
local creds = Tab5:CreateSection("Credits")


local Players = game:GetService("Players")
local plr = game:GetService("Players").LocalPlayer
local playerid = plr.UserId

local ts = game:GetService("TweenService")


local kyscunt = game:GetService("CoreGui")

local PISS = 2 -- what does this even mean? [frog]

getgenv().infstam = false;
getgenv().ks = false;
getgenv().autojoe = false
getgenv().StaffKick = false
getgenv().funnyspeed = false

---
---

function randommsg()
	local msgevent = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest 
	local rnum = math.random(1,11)
	
	print(rnum)
	if rnum == 1 then
	  msgevent:FireServer("we geez, therefore we are.", "All")
	elseif rnum == 2 then
	  msgevent:FireServer("geezer cannot be stopped", "All")
	elseif rnum == 3 then
	  msgevent:FireServer("im the geezer, i geez.", "All")
	elseif rnum == 4 then
	  msgevent:FireServer("geezer always returns", "All")
	elseif rnum == 5 then
	  msgevent:FireServer("im the geezer, say my name.", "All")
	elseif rnum == 6 then
	  msgevent:FireServer("do not harm the geezer.", "All")
	elseif rnum == 7 then
	  msgevent:FireServer("geezer never team, geezer only friend", "All") -- FUCK you for this SPELLING MISTAKE, your GEEZER2. (i fixed this so you dont get it)
	elseif rnum == 8 then
	msgevent:FireServer("your geezin' is weak, brother.", "All")
	elseif rnum == 9 then
	msgevent:FireServer("shoutout froglett, he a real one - froglet.xyz", "All")
	elseif rnum == 10 then
	msgevent:FireServer("why no geez?", "All")
	elseif rnum == 11 then
	msgevent:FireServer("im sorry for allowing the chainsaw idiots run wild - from froglett", "All")
end end


function disableconnection(path)
	for i, connection in pairs(getconnections(path)) do
		connection:Disable()
	end
end

function check(value)
	local rank = value:GetRoleInGroup(10294339)
	if rank == "Contributor" or rank == "Moderator" or rank == "Admin" or rank == "Developer" or rank == "Scripter" or rank == "Builder" or rank == "Modeler" or rank == "Crimson" or rank == "dokso" or rank == "Noobie" then
		   game.Players.LocalPlayer:Kick(rank.." | "..value.Name.." | ".."Is In Server")
	   end
end


function THISISRETARDED()
	local msgevent = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
	local invite = "courd.gg / gTQWKuqSkB"
	local ranum = math.random(1,10)
	
	if ranum == 1 then
	  msgevent:FireServer("Get good get geezware. "..invite, "All")
	elseif ranum == 2 then
	  msgevent:FireServer("shoulda had geezware! "..invite, "All")
	elseif ranum == 3 then
	  msgevent:FireServer("join the geezware server today! "..invite, "All")
	elseif ranum == 4 then
	  msgevent:FireServer(invite, "All")
	elseif ranum == 5 then
	  msgevent:FireServer("my dad works for riot and he says geezin is good. "..invite, "All")
	elseif ranum == 6 then
	  msgevent:FireServer("Ready to try geezware? "..invite, "All")
	elseif ranum == 7 then
	  msgevent:FireServer("geezware, one step ahead of the game. "..invite, "All")
	elseif ranum == 8 then
	msgevent:FireServer("geezware, now open source! "..invite, "All")
	elseif ranum == 9 then
	msgevent:FireServer("shoutout froglett, he a real one "..invite, "All")
	elseif ranum == 10 then
	msgevent:FireServer("cant beat them? then join them. "..invite, "All")
end end



function tweentp(coords,time)
    local LCH = game:GetService("Players").LocalPlayer.Character
    local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart

	local tweenInfo = TweenInfo.new(time,Enum.EasingStyle.Linear,Enum.EasingDirection.Out)
	ts:Create(HRP, tweenInfo, {CFrame = coords}):Play()
end


function autoJOE()
    while autojoe do
    fireclickdetector(game:GetService("Workspace").Joseph.ClickDetector)
    wait(2)
    end
end


------------
local WEAPONLOL
local Dropdown1 = Section1:CreateDropdown("Weapon", {"Bat","Sword","Knife","Machete","Fists","Mace","Sign","Sledge Hammer","Pipe","Golden Machete", "Lightsaber", "Red Lightsaber"}function(String)
	WEAPONLOL = String
end)
Dropdown1:AddToolTip("Select what weapon to spawn with")
Dropdown1:SetOption("Mace")

local Button1 = Section1:CreateButton("Spawn Selected Weapon", function()
    local Weapo = {[1] = WEAPONLOL}game:GetService("ReplicatedStorage").Remotes.Weapons:InvokeServer(unpack(Weapo))
    wait()
    local Weapo = {[1] = WEAPONLOL}game:GetService("ReplicatedStorage").Remotes.Weapons:InvokeServer(unpack(Weapo))
end)
Button1:AddToolTip("Gives you selected weapon (will tp you to a random location)")


-----------
local Label1 = Section1:CreateLabel("Attributes")
Label1:UpdateText("Attributes")
------------

local Toggle1 = Section1:CreateToggle("Madness Mode", nil, function(State)
	plr:SetAttribute("MadnessMode", State)
end)

local Toggle2 = Section1:CreateToggle("Rage Mode", nil, function(State)
	plr:SetAttribute("RageMode", State)
end)

local Toggle3 = Section1:CreateToggle("Inf Stamina", nil, function(State)
	plr:SetAttribute("InfStamina", State)
end)

local Toggle4 = Section1:CreateToggle("Inf Dash", nil, function(State)
	plr:SetAttribute("InfiniteDash", State)
end)

local Toggle5 = Section1:CreateToggle("NoCooldown", nil, function(State)
	plr:SetAttribute("WeaponSpam", State)
end)


local Toggle66 = Section1:CreateToggle("Inf Accelerate", nil, function(State)
    getgenv().funnyspeed = State
    if funnyspeed then
    plr:SetAttribute("FunnySpeed", 15)
    elseif funnyspeed == false then
        plr:SetAttribute("FunnySpeed", false)
    end
end)

getgenv().antidown = false

function nodown()
    while antidown do
		local LCH = game:GetService("Players").LocalPlayer.Character
        LCH:SetAttribute("Downed", false)
        wait()
    end
end

local Toggle667 = Section1:CreateToggle("Anti Down", nil, function(State)
    getgenv().antidown = State
    if antidown then
    nodown()
	elseif antidown == false and plr.PlayerGui.Profile.Centered.Health.Bar:FindFirstChild("dmglabel") then game:GetService("Players").LocalPlayer.Character:SetAttribute("Downed", true)
    end
end)
Toggle667:AddToolTip("Retoggle if anti-down doesnt undown you when turning off")

function thehit(paths)
	local argsZ = {
		[1] = "Z",
		[2] = 1,
		[3] = "the/???"
	}
	paths:FireServer(unpack(argsZ))
	wait()
end
	
function charhit(pathz)
		
		for i,v in pairs(game:GetService("Players"):GetPlayers()) do
			if v.Name ~= game:GetService("Players").LocalPlayer.Name  then
	local argsX = {
		[1] = "T",
		[2] = v.Character:FindFirstChild("Head"),
		[3] = "lol  "
	}
	pathz:FireServer(unpack(argsX))
	wait()

end end end
	
function uuhh()

while KA do
local LCH = game:GetService("Players").LocalPlayer.Character
local THING = LCH:FindFirstChildWhichIsA("Tool")
	if not THING then return end
for i,v in pairs(LCH:GetDescendants()) do
		if v.Name == "WeaponRemote" then
	thehit(v)
	wait(0.1)
	charhit(v)
	wait()
end end end end


getgenv().KA = false
local Toggle6KA = Section1:CreateToggle("Kill Aura", nil, function(State)
	getgenv().KA = State
	if KA then
	uuhh()
	wait(0.1)
	end
end)
Toggle6KA:AddToolTip("HEAVY WIP - USING AROUND TOO MANY PEOPLE WILL GET YOU AUTO BANNED") -- commenting it out for now [source] -- fuck you this is so perfect [frog] -- it wasnt perfect https://i.imgur.com/Q7JK2cR.png [frog]
Toggle6KA:CreateKeybind("NONE", function(Key)end)



getgenv().floorclip = false
local Toggle901 = Section1:CreateToggle("Hide Legs", nil, function(State)
	getgenv().floorclip = State
	local LCH = game:GetService("Players").LocalPlayer.Character

	if floorclip then
		LCH.Humanoid.HipHeight = -1.99
	elseif not floorclip then
		LCH.Humanoid.HipHeight = 0
	end


end)






local PBuy = game:GetService("Workspace").PBuyables
local SelArea
local Dropdown1 = Section2:CreateDropdown("Teleports", {"BladeProxPart","AppleProxPart","PizzaProxPart","HammerProxPart","WaterProxPart","ColaProxPart","MolotovProxPart","MetalBatProxPart","AxeProxPart","SignProxPart","MaceProxPart","BandageProxPart","CheeseProxPart","RageProxPart","PipeProxPart","PanProxPart"}, function(String)
	SelArea = String
end)
Dropdown1:AddToolTip("Teleport to purchasable (buggy)")
Dropdown1:SetOption("BladeProxPart")

local Button1 = Section2:CreateButton("Teleport", function()
    tweentp(PBuy[SelArea].CFrame,4)
end)

local Button211 = Section2:CreateButton("Teleport to box", function()
    for i,v in pairs(game:GetService("Workspace").Mystery:GetDescendants()) do
        if v.Name == "Indicator" then tweentp(v.CFrame,4) end end
end)


local Button2h12 = Section2:CreateButton("No jump cooldown", function()
	disableconnection(game:GetService("UserInputService").JumpRequest)
end)

local ButtonSign = Section2:CreateButton("Activate Old Mace", function()
	for i,v in pairs(getgc(true)) do 
		if type(v) == 'table' and rawget(v,'Mace') then
			v.Mace.Animations = {
			Attacks = { 6732276839, 6732281350, 6732283066 }, 
			Equip = 6789836832, 
			Idle = 6748119246
		} 
		end 
	end
end) -- ned
ButtonMace:AddToolTip("Execute before buying Mace.")
]] -- removed for now since the old anims function does the same [frog] < -- FUCK THIS GUY!!!!! [source]

local ButtonSign = Section2:CreateButton("Activate Old Sign", function()
	for i,v in pairs(getgc(true)) do 
		if type(v) == 'table' and rawget(v,'Sign') then
			v.Sign.Animations = {
			Attacks = { 6824974395 }, 
            Equip = 6824988916, 
            Idle = 6824982196
		} 
		end 
	end
end) -- ned
ButtonSign:AddToolTip("Execute before buying Sign.")
]]





function PASSIVEMODE() --goofy af how does this work LOL [frog]
local mac = game:GetService("Workspace").PBuyables.SignProxPart
local plr = game:GetService("Players").LocalPlayer

wait(0.25)

game:GetService("Players").LocalPlayer:SetAttribute("InIntro", true)
wait(1.5)

game:GetService("ReplicatedStorage").Remotes.ResetCharacter:FireServer()

wait(8)
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").PBuyables.SignProxPart.CFrame + Vector3.new(0,5,0)
end


local Buttonpassive = Section2:CreateButton("Passive/Old God Mode", function()
	PASSIVEMODE()
end)
Buttonpassive:AddToolTip("use something like inf yield fly to be able to move\nRe-execute if the forcefield goes away.\nvery buggy btw")

local ButtonpassiveFIX = Section2:CreateButton("Fix PassiveMode", function()
	game:GetService("Players").LocalPlayer:SetAttribute("InIntro", false)
end)
ButtonpassiveFIX:AddToolTip("Fixes your game if it gets buged using passive mode")


function oldanims()
for i,v in pairs(getgc(true)) do 
	if type(v) == 'table' and rawget(v,'Mace') then
		v.Mace.Animations = {
		Attacks = { 6732276839, 6732281350, 6732283066 }, 
		Equip = 6789836832, 
		Idle = 6748119246,
        Damage = 999
	} 
	v.Sign.Animations = {
		Attacks = { 6824974395 }, 
		Equip = 6824988916, 
		Idle = 6824982196
	} 
end end
end

local Buttonfizn = Section2:CreateButton("Enable Old Animations", function()
	oldanims()
end)
Buttonfizn:AddToolTip("Re-Execute after death - work in progress ")



local Toggle445 = Section2:CreateToggle("Leave On Staff Join", nil, function(State)
      getgenv().StaffKick = State
      if StaffKick == true then
        Players.PlayerAdded:Connect(function(player)
          check(player)
        end)
      end
end)


getgenv().worldarea = State
local Toggle674 = Section2:CreateToggle("Sanctuary Skybox", nil, function(State)
    getgenv().worldarea = State
    if worldarea then
    plr:SetAttribute("WorldArea", "Sanctuary")
    elseif worldarea == false then
        plr:SetAttribute("WorldArea", "Main")
    end
end)

local Toggle67xx4 = Section2:CreateToggle("Old Leaderboard", nil, function(State)
	game:GetService("StarterGui"):SetCoreGuiEnabled('PlayerList', State)
end)


getgenv().spoofid = false
local Toggle901 = Section2:CreateToggle("Spoof ID", nil, function(State)
	getgenv().spoofid = State
	local LCH = game:GetService("Players").LocalPlayer.Character

	if spoofid then
		plr.UserId = 21141528
	elseif not spoofid then
		plr.UserId = playerid
	end
end)



-------------
local Label1299 = Section7:CreateLabel("Hitbox Expander")
Label1299:UpdateText("Hitbox Expander")
-------------
getgenv().extender = false;

local friendlist = {

}


  local entry

	SectionT:CreateTextBox("Friends", "Enter Friend Username", false, function(String)
		entry = String
	end)

	SectionT:CreateButton("Enter", function(v)
        if game.Players[entry] then
        table.insert(friendlist, entry)
        print("Friend ".. entry .." added!")
        elseif not game.Players[entry] then
        print("Player not found")
        end
    end)

	SectionT:CreateButton("Show Friendlist", function(s)
	print("Your friendlist:")
		for index, data in ipairs(friendlist) do
			print(data)
		end
	end)

	-- friendlisted players are fortnite

local toggleextenderer = Section7:CreateToggle("Toggle Extender", nil, function(bools)
	getgenv().extender = bools
end)

local transgender = SectionT:CreateSlider("Transparency", 0, 1, 0.5, false, function(v)
	_G.tranparenc = v
end)

local fart

local poope = SectionT:CreateColorpicker("Hitbox Color", function(hbc)
	fart = hbc
end)


local estenderitself = Section7:CreateSlider("Extender Size", 2, 100, 4, true, function(xd)

	function HowDoIExtend()
	for i, v in pairs(game.Players:GetPlayers()) do
			if v.Name ~= game.Players.LocalPlayer.Name and v.Name ~= friendlist[1] and v.Name ~= friendlist[2] and v.Name ~= friendlist[3] and v.Name ~= friendlist[4] and v.Name ~= friendlist[5] and v.Name ~= friendlist[6] and v.Name ~= friendlist[7] and v.Name ~= friendlist[8] and v.Name ~= friendlist[9] and v.Name ~= friendlist[10] then
				pcall(function()
					 v.Character.HumanoidRootPart.Size = Vector3.new(xd, xd, xd)
			 		 v.Character.HumanoidRootPart.Transparency = _G.tranparenc
			 		 v.Character.HumanoidRootPart.CanCollide = false
					 v.Character.HumanoidRootPart.Color = fart
					  wait()
			end)
	end
	end
end

spawn(function()
while extender == true do
	if extender == true then
		HowDoIExtend()
		wait(0.1)
	end
end
end)

end)
-------------
local Label1 = Section2:CreateLabel("Other Stuff")
Label1:UpdateText("Other Stuff")
-------------



function BRST()
    game:GetService("Players").LocalPlayer.Character.Torso.Neck:Destroy()
end
local resetvalue

local DropdownR = Section2:CreateDropdown("Reset Options", {"none","BetterReset","Pit","Humanoid","Remote"}, function(String)
	if String == "BetterReset" then
		game:GetService("Players").LocalPlayer.Character.Torso.Neck:Destroy()
		resetvalue = String
	elseif String == "Pit" then
		firetouchinterest(game:GetService("Workspace").Pit.Kill, plr.Character.Head, 0)
		firetouchinterest(game:GetService("Workspace").Pit.Kill, plr.Character.Head, 1)
		resetvalue = String
	elseif String == "Humanoid" then 
		game:GetService("Players").LocalPlayer.Character.Humanoid:Destroy()
		resetvalue = String
	elseif String == "Remote" then
		game:GetService("ReplicatedStorage").Remotes.ResetCharacter:FireServer() 
		resetvalue = String
	end
end)
DropdownR:AddToolTip("Different reset options for all your death needs")

-------------
local SP = game:GetService("StarterPlayer")

-- will add more here, just wanted some misc features for fun [frog]

local toggleAUGH = Section9:CreateToggle("AUTO JOSEPH.", nil, function(State)
	getgenv().autojoe = State
	if autojoe then
		autoJOE()
		wait()
end
end)


local Button2312 = Section9:CreateButton("Remove System Messages", function()
	plr.PlayerScripts.SystemMessages:Destroy()
	SP.StarterPlayerScripts.SystemMessages:Destroy()
end)
Button2312:AddToolTip("Stops System Messages from sending")

function outline(trans,path)
	local HL = Instance.new("Highlight")
	HL.FillTransparency = trans
	HL.Parent = path
end


getgenv().outlinebox = false
local ToggleBoxP = Section9:CreateToggle("Outline Piles", nil, function(State)
	getgenv().outlinebox = State
	if outlinebox then for i,v in pairs(game:GetService("Workspace")["New map"].Piles:GetDescendants()) do
        if v.Name == "New Pile" then outline(0.9,v) end end
	elseif outlinebox == false then
		for i,v in pairs(game:GetService("Workspace")["New map"].Piles:GetDescendants()) do
			if v.Name == "Highlight" then v:Destroy() end end
	end
end)





local Button2312z = Section9:CreateButton("Disable anti-swim", function()

local LCH = game:GetService("Players").LocalPlayer.Character
local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart


	LCH.StateEnabled:Destroy()
	SP.StarterCharacterScripts.StateEnableds:Destroy()
end)
Button2312z:AddToolTip("Allows you to swim (use something like inf yield)")


function demeshlol()
    local LCH = game:GetService("Players").LocalPlayer.Character
    local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart

	for i,v in pairs (LCH:GetChildren()) do
		if v.ClassName == "Tool" then
			v.Handle.Mesh:Destroy()
		end
	end
end

function deweldlol()
	local LCH = game:GetService("Players").LocalPlayer.Character
	local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
	local THING = LCH:FindFirstChildWhichIsA("Tool")
	for i,v in pairs (THING:GetDescendants()) do
		if v.ClassName == "Weld" then
			v:Destroy()
	end end
end

function DOSHIT()
    local LCH = game:GetService("Players").LocalPlayer.Character
    local HRP = LCH.HumanoidRootPart
    local button = game:GetService("Workspace").SancPortal.Terminal.Button
    local center = game:GetService("Workspace").SancPortal.Center
    --HRP.CFrame = button.CFrame
    --fireproximityprompt(game:GetService("Workspace").SancPortal.Terminal.Button.ProximityPrompt)
    wait(0.05)
    HRP.CFrame = CFrame.new(1192.68018, 135.858749, 39.7135162)
    wait(0.1)
    fireproximityprompt(game:GetService("Workspace").SancPortal.Center.ProximityPrompt)
    fireproximityprompt(game:GetService("Workspace").SancPortal.Center.ProximityPrompt)
    fireproximityprompt(game:GetService("Workspace").SancPortal.Center.ProximityPrompt)
    wait(0.05)
    fireproximityprompt(game:GetService("Workspace").SancPortal.Center.ProximityPrompt)
    wait(5)
    plr:SetAttribute("WorldArea", "Main")
end

--[[local Button232z = Section9:CreateButton("Demesh held Tool", function()
	demeshlol()
end)
Button232z:AddToolTip("Demeshes your tool (if it has a mesh)")



local Button232z = Section9:CreateButton("Deweld held Tool", function()
	deweldlol()
end)
Button232z:AddToolTip("Dewelds your tool (if it has a weld)")]]



local ButtXXon232z = Section9:CreateButton("Attempt Sanctuary", function()
	DOSHIT()
end)
ButtXXon232z:AddToolTip("this shit never works bro why is it here im also retarded and hate roblox")


--[[local Slider12x3 = Section9:CreateSlider("Time of day", 1,24,nil,true, function(Value)
	game:GetService("Lighting").ClockTime = Value
end)
Slider12x3:AddToolTip("Changes the Time of day")
Slider12x3:SetValue(12)]]


--[[function resetlighting()
	for i,v in pairs(game:GetService("Lighting"):GetChildren()) do
		if v.ClassName == "ColorCorrectionEffect" then
			v:Destroy()
end end end


local Buttonguh1 = Section9:CreateButton("Reset Lighting", function()
	resetlighting()
end)]] -- broken sorry :(((( - froglett



--[[local Buttondmz = Section9:CreateButton("Disable Death screen", function()
	disableconnection(game:GetService("Players").LocalPlayer.Character.Humanoid.Died)
end)]]

local ButtonWORM = Section9:CreateButton("worm mode.", function()
    local LCH = game:GetService("Players").LocalPlayer.Character
    local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart

	for i,v in pairs(LCH:getChildren()) do
		if v.Name == "Left Leg" then v:Destroy() end end
		for i,v in pairs(LCH:getChildren()) do
		if v.Name == "Right Leg" then v:Destroy() end end
		for i,v in pairs(LCH:getChildren()) do
		if v.Name == "Left Arm" then v:Destroy() end end
end) -- lol [frog]

local Button1 = Section9:CreateButton("GEEZER PROPAGANDA", function()
    randommsg()
end)

local Button9999 = Section9:CreateButton("Discord Ad", function()
    THISISRETARDED()
end)
Button9999:AddToolTip("you should totally use this button when geezin")


local buttonstiff = Section9:CreateButton("go stiff", function()
	plr.Character.Humanoid:ChangeState(Enum.HumanoidStateType.FallingDown)
end)
buttonstiff:AddToolTip("makes you enter ragdoll/stiff state")





function headspoof()

    local LCH = game:GetService("Players").LocalPlayer.Character
    local HRP = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart

	for i,v in pairs(LCH.Animate:GetChildren()) do
		if v.Name == "Assets" then v:Destroy()
	end
	for i,v in pairs(game:GetService("StarterPlayer").StarterCharacterScripts.Animate:GetChildren()) do
		if v.Name == "Assets" then v:Destroy()
	end end end
end




function headmove(a,b,c,z,x,c)
    local LCH = game:GetService("Players").LocalPlayer.Character
	local argshm = {
		[1] = "maybe_akita_can_program...",
		[2] = CFrame.new(a,b,c) * CFrame.Angles(z,x,c)
	}
	
	game:GetService("ReplicatedStorage").Events.Look:FireServer(unpack(argshm))
	
	LCH.Torso.Neck.C0 = CFrame.new(a,b,c) * CFrame.Angles(z,x,c) -- lets you see your head position locally [frog]
end

getgenv().headspinz = false
function headspin()
    while headspin do

    end

end

local Button2z732z = sectionhead:CreateButton("Spoof Head Movement", function()
	headspoof()
end)
Button2z732z:AddToolTip("Allows spoofing head movement") -- not even spoofing it just sounds cool LOOOL [frog]

local Button2v0z = sectionhead:CreateButton("Reset Head to normal", function()
	headmove(0,1,0,1.5,9.5,0)
end)

local Button2v08 = sectionhead:CreateButton("Backwards head", function()
	headmove(0,1,0,-1.8,0,0)
end)

local Button2v07 = sectionhead:CreateButton("upsidedown head", function()
	headmove(0,1.99,0,1.5,0,0)
end)

local Button3vcz = sectionhead:CreateButton("head legs", function()
	headmove(0,-1,0,-1.5,9.5,0)
end)

local Button36cz = sectionhead:CreateButton("elevated head", function()
	headmove(0,1.999,0,1.5,-9.5,0)
end)



--[[
local toggleHS = sectionhead:CreateToggle("head spin", nil, function(State)
	getgenv().headspinz = State
	if headspinz then
		headspin()
		wait()
end
end)
]]
-----------------------------------------


local animspeed = 1
local Slider4 = Secanim2:CreateSlider("Animation Speed", 1,5,nil,true, function(Value)
animspeed = Value
end)
Slider4:SetValue(1)

function AnimPlayer(AnimationId)
        local Anim = Instance.new("Animation")
        Anim.AnimationId = "rbxassetid://"..AnimationId
        local k = plr.Character.Humanoid:LoadAnimation(Anim)
        k:Play() --Play the animation
        k:AdjustSpeed(animspeed)
end

local Stopanim = Secanim2:CreateButton("Stop Animation", function()
	for i,v in pairs(plr.Character.Humanoid:GetPlayingAnimationTracks()) do
		v:Stop()
	end
end)



local Labelan = Secanim1:CreateLabel("Animations")
Labelan:UpdateText("Animations")

local ABut1 = Secanim1:CreateButton("Carried", function()
	AnimPlayer(6924846702)
end)
local ABut2 = Secanim1:CreateButton("Weird Move", function()
	AnimPlayer(215384594)
end)
local ABut3 = Secanim1:CreateButton("Enrage", function()
	AnimPlayer(8932979527)
end)
local ABut4 = Secanim1:CreateButton("Old Stomp", function()
	AnimPlayer(7121695954)
end)
local ABut5 = Secanim1:CreateButton("Down", function()
	AnimPlayer(7110472612)
end)
local ABut6 = Secanim1:CreateButton("Walk", function()
	AnimPlayer(7066772297)
end)
local ABut7 = Secanim1:CreateButton("Run", function()
	AnimPlayer(6719060327)
end)
local ABut8 = Secanim1:CreateButton("Floor Crawl", function()
	AnimPlayer(282574440)
end)
local ABut9 = Secanim1:CreateButton("Helicopter", function()
	AnimPlayer(8299261024)
end)
local ABut10 = Secanim1:CreateButton("Slide", function()
	AnimPlayer(7396979558)
end)
local ABut11 = Secanim1:CreateButton("CrouchIdle", function()
	AnimPlayer(7247979947)
end) 
local ABut12 = Secanim1:CreateButton("Menu Idle", function()
	AnimPlayer(8590109982)
end) 
local ABut13 = Secanim1:CreateButton("Roll", function()
	AnimPlayer(6664075469)
end) 

local Label1 = Secanim2:CreateLabel("Other Shit")
Label1:UpdateText("Other Shit")

getgenv().Spinning = false

local spinsped
local Slider2 = Secanim2:CreateSlider("Spin Speed", 20,100,nil,true, function(Value)
	spinsped = Value
end)
Slider2:SetValue(50)

function spinbaby(SpedNum)
while Spinning do
    local Client = game:GetService("Players").LocalPlayer;
    Client.Character.HumanoidRootPart.CFrame = Client.Character.HumanoidRootPart.CFrame * CFrame.Angles(0, math.rad(SpedNum), 0)
    wait()
end
end

local Togglespin1 = Secanim2:CreateToggle("Spinbot", nil, function(State)
	getgenv().Spinning = State
    if Spinning then 
        spinbaby(spinsped)
    end
end)
Togglespin1:AddToolTip("Remember to use different anims to improve the spinbot")
Togglespin1:CreateKeybind("NONE", function(Key)end)




-------------
local Toggle3 = Section4:CreateToggle("UI Toggle", nil, function(State)
	Window:Toggle(State)
end)
Toggle3:CreateKeybind(tostring(Config.Keybind):gsub("Enum.KeyCode.", ""), function(Key)
	Config.Keybind = Enum.KeyCode[Key]
end)
Toggle3:SetState(true)

local cred = creds:CreateLabel("Kirito-Kun#2991")

local Colorpicker3 = Section4:CreateColorpicker("UI Color", function(Color)
	Window:ChangeColor(Color)
end)
Colorpicker3:UpdateColor(Config.Color)


local Button1 = Section4:CreateButton("Delete GUI", function()
	for i,v in pairs(kyscunt:GetDescendants()) do
        if v.Name == "LibraryName" then v.Parent.Parent.Parent:Destroy()
    end end
end)

-- credits to jan for patterns
local Dropdown3 = Section5:CreateDropdown("Image", {"Default","Hearts","Abstract","Hexagon","Circles","Lace With Flowers","Floral","Showerman"}, function(Name)
	if Name == "Default" then
		Window:SetBackground("2151741365")
	elseif Name == "Hearts" then
		Window:SetBackground("6073763717")
	elseif Name == "Abstract" then
		Window:SetBackground("6073743871")
	elseif Name == "Hexagon" then
		Window:SetBackground("6073628839")
	elseif Name == "Circles" then
		Window:SetBackground("6071579801")
	elseif Name == "Lace With Flowers" then
		Window:SetBackground("6071575925")
	elseif Name == "Floral" then
		Window:SetBackground("5553946656")
	elseif Name == "Showerman" then
		Window:SetBackground("10257784197")
	end
end)
Dropdown3:SetOption("Default")


--

local Colorpicker4 = Section5:CreateColorpicker("Color", function(Color)
	Window:SetBackgroundColor(Color)
end)

local Slider334 = Section5:CreateSlider("Transparency",0,1,nil,false, function(Value)
	Window:SetBackgroundTransparency(Value)
end)
Slider334:SetValue(0)

local Slider4 = Section5:CreateSlider("Tile Scale",0,1,nil,false, function(Value)
	Window:SetTileScale(Value)
end)
Slider4:SetValue(0.5)

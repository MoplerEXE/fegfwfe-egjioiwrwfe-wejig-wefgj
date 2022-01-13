local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/AikaV3rm/UiLib/master/Lib.lua')))()

local w = library:CreateWindow("Most features") -- Creates the window

local Troll = library:CreateWindow("Trololo")

local t = Troll:CreateFolder("trolling")-- Creates the folder(U will put here your buttons,etc)

local Crash = library:CreateWindow("Server Crasher")

local n = Crash:CreateFolder("Crash by 6m home")

local Home = Crash:CreateFolder("Home explain")

local K = Crash:CreateFolder("Crash by basic home")

local Q = Crash:CreateFolder("Crash by easy method")

local b = w:CreateFolder("Very pvp script") -- Creates the folder(U will put here your buttons,etc)

local c = w:CreateFolder("idk")

local d = w:CreateFolder("Other stuff & credits")

local ts = game:GetService("TweenService")

b:Label("Very pvp script XD",{
    TextSize = 25; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
}) 

b:Button("Enable killaura",function()
    getgenv().Killaura = true
    while getgenv().Killaura do
  local plr = game.Players.LocalPlayer
    local char = plr.Character
        Players = game:GetService("Players")
          for i, player in pairs(Players:GetPlayers()) do
    local A_1 = "SHOTTY"
    local A_2 = game:GetService("Workspace")[player.Name].Head
    local Event = game:GetService("ReplicatedStorage").Event
    Event:FireServer(A_1, A_2)
    print("must be print")
    wait(0.2)
end
wait(0.1)
end
end)

b:Button("Disable killaura",function()
    getgenv().Killaura = false
end)

b:Button("Enable autorevive",function()
getgenv().Godserver = true
while wait() and getgenv().Godserver do
       for i, all in pairs(game:GetService("Players"):GetPlayers()) do
           local A_1 = "RevivePlayer"
           local A_2 = game:GetService("Workspace")[all.Name]
           local A_3 = game:GetService("Workspace").ObjectSelection.DownedPart.DownedPart
           local Event = game:GetService("ReplicatedStorage").Event
           Event:FireServer(A_1, A_2, A_3)
           wait(0.1)
       end
end
end)

b:Button("Disable autorevive",function()
getgenv().Godserver = false
end)

b:Bind("KILLAURA BIND",Enum.KeyCode.C,function() --Default bind
    local plr = game.Players.LocalPlayer
local char = plr.Character
    Players = game:GetService("Players")
			pcall(function()
			for i, player in pairs(Players:GetPlayers()) do
local A_1 = "SHOTTY"
local A_2 = game:GetService("Workspace")[player.Name].Head
local Event = game:GetService("ReplicatedStorage").Event
Event:FireServer(A_1, A_2)
wait()
end
end)
end)

b:DestroyGui()

t:Button("GLIDER ALL (SMALL)", function(value)
getgenv().GlideralllolXD = true
while getgenv().GlideralllolXD do
local ohString1 = "Glider"
--workspace.LmomentXD.Parachute.Handle
local ohNumber3 = 0.92

for i, playerrsss in pairs(game:GetService("Players"):GetPlayers()) do
game:GetService("ReplicatedStorage").Event:FireServer(ohString1, workspace[playerrsss.Name].Parachute.Handle, ohNumber3)
wait(0.5)
end
end
end)

t:Button("GLIDER ALL", function(value)
    getgenv().Glideralllol = true
    while getgenv().Glideralllol do
    local ohString1 = "Glider"
    --workspace.LmomentXD.Parachute.Handle
    local ohNumber3 = 0
    
    for i, playerrsss in pairs(game:GetService("Players"):GetPlayers()) do
    game:GetService("ReplicatedStorage").Event:FireServer(ohString1, workspace[playerrsss.Name].Parachute.Handle, ohNumber3)
    wait(0.5)
    end
    end
end)

t:Button("DISABLE GLIDER ALL", function(value)
    getgenv().GlideralllolXD = false
    getgenv().Glideralllol = false
    local ohString1 = "Glider"
    --workspace.LmomentXD.Parachute.Handle
    local ohNumber3 = 1

    for i, playerrsss in pairs(game:GetService("Players"):GetPlayers()) do
    game:GetService("ReplicatedStorage").Event:FireServer(ohString1, workspace[playerrsss.Name].Parachute.Handle, ohNumber3)
    wait(0.5)
    end
end)

t:Button("TP ALL VEHICLES OP LOL", function(value)
local getplayerpos = game.Workspace[game.Players.LocalPlayer.Name].HumanoidRootPart.Position
for i,v in pairs(game:GetService("Workspace").ObjectSelection:GetDescendants()) do
    if v.Name == "PassengerSeat" then
        game:GetService("Workspace").ObjectSelection[v.Parent.Name].PassengerSeat.Disabled = false
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection[v.Parent.Name].PassengerSeat.CFrame
        wait(0.5)
        game.Players.LocalPlayer.Character:findFirstChildOfClass("Humanoid"):ChangeState(3)
        wait(0.05)
        game:GetService("Workspace").ObjectSelection[v.Parent.Name].PassengerSeat.Disabled = true
        game:GetService("Workspace")[game.Players.LocalPlayer.Name].HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
        game:GetService("Workspace")[game.Players.LocalPlayer.Name].HumanoidRootPart.CFrame = CFrame.new(20000,0,20000)
        game:GetService("Workspace")[game.Players.LocalPlayer.Name].HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
        wait(0.05)
        game:GetService("Workspace")[game.Players.LocalPlayer.Name].HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
        setclipboard("Golem pro golem top very pro GolemusInfernus#1281")
            end
end
end)

t:Button("Print all veh (f9/fn+f9",function()
    print("-----------------------------")
for i,v in pairs(game:GetService("Workspace").ObjectSelection:GetDescendants()) do
   if v.Name == "PassengerSeat" then 
       print(v.Parent)
   end
end
print("-----------------------------")
end)

--about player
local getplayercar;
t:Box("Type Player vehicle you want","string",function(value) -- "number" or "string"
    getplayercar = value
    print(value, "vehicle selected, now click ''get this vehicle'' button")
end)

t:Button("get this player vehicle", function(value)
    print("poop1")
    game:GetService("Workspace").ObjectSelection[getplayercar.."'s Vehicle"].PassengerSeat.Disabled = false
    print("poop2")
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection[getplayercar.."'s Vehicle"].PassengerSeat.CFrame
    print("poop3")
    wait(0.1)
game:GetService("Workspace").ObjectSelection[getplayercar.."'s Vehicle"].PassengerSeat.Disabled = true
wait(2)
    print(getplayercar, "vehicle Teleported")
end)
--about player
local getthiscar;
t:Box("Type vehicle you want ex. SWAT","string",function(value) -- "number" or "string"
    getthiscar = value
    print(value, "selected, now click ''get this vehicle'' button")
end)

t:Button("get this vehicle", function(value)
    game:GetService("Workspace").ObjectSelection[getthiscar].PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection[getthiscar].PassengerSeat.CFrame
wait(0.2)
game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
game:GetService("Workspace").ObjectSelection[getthiscar].PassengerSeat.Disabled = true
wait(2)
    print(getthiscar, "Teleported")
end)

local getid;
t:Box("Type player to get his veh MusicId","string",function(value) -- "number" or "string"
    getid = value
    print(value, "selected, now click ''Get music id'' button")
end)

t:Button("Get music id (f9/fn+f9)", function(value)
    print(game:GetService("Workspace").ObjectSelection[getid.."'s Vehicle"].Chassis.RadioMusic.SoundId)
end)
    
t:Button("Auto tp (trash)",function()
local getplayerpos = game.Workspace[game.Players.LocalPlayer.Name].HumanoidRootPart.Position
print("WORKING 1")
local head = Workspace[game.Players.LocalPlayer.Name].Head
print("WORKING 2")
--Script 1 start
game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.CFrame
wait(0.2)
game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
    print("WORKING 3")
wait(2) --I will make cooldown better by the time
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,500,0)
wait(2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
wait(2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
--Script 2 start
game:GetService("Workspace").ObjectSelection.Dominator.PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.Dominator.PassengerSeat.CFrame
wait(0.2)
game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
game:GetService("Workspace").ObjectSelection.Dominator.PassengerSeat.Disabled = true
wait(2) --I will make cooldown better by the time
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,500,0)
wait(2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
wait(3)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
wait(1.5)
--Script 3 start
game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.CFrame
    wait(0.2)
    game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
    game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.Disabled = true
wait(2) --I will make cooldown better by the time
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,500,0)
wait(2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
wait(3)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(getplayerpos)
end)

t:Button("Enable autobomb",function()
    local Bomb = {
        [1] = "DropBomb",
    }
    
    
    _G.bomb = true
    for i = 1,55555 do
    while _G.bomb do
    game:GetService("ReplicatedStorage").Event:FireServer(unpack(Bomb))
    wait()
    end
    end
end)

t:Button("Disable autobomb",function()
    local Bomb = {
        [1] = "DropBomb",
    }
    
    
    _G.bomb = false
    for i = 1,55555 do
    while _G.bomb do
    game:GetService("ReplicatedStorage").Event:FireServer(unpack(Bomb))
    wait()
    end
    end
end)

t:Button("Tp SWAT to you",function()
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.CFrame
    wait(0.2)
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
    game:GetService("Workspace").ObjectSelection.SWAT.PassengerSeat.Disabled = true
end)

t:Button("Tp Terminator car to you",function()
    game:GetService("Workspace").ObjectSelection["O66-Terminator"].PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection["O66-Terminator"].PassengerSeat.CFrame
    wait(0.2)
    game:GetService("Workspace").ObjectSelection["O66-Terminator"].PassengerSeat.Disabled = true
end)

t:Button("Tp Helicopter to you",function()
    game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.CFrame
    wait(0.2)
    game:GetService("Workspace").ObjectSelection.Helicopter.PassengerSeat.Disabled = true
end)

t:Button("Tp Tank to you",function()
    game:GetService("Workspace").ObjectSelection.Rhino.PassengerSeat.Disabled = false
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").ObjectSelection.Rhino.PassengerSeat.CFrame
    wait(0.2)
    game:GetService("Workspace").ObjectSelection.Rhino.PassengerSeat.Disabled = true
end)

n:Button("Use before lag script",function()
local A_1 = "LeaveHome"
local A_2 = true
local Event = game:GetService("ReplicatedStorage").Event
local B_1 = "SpawnHome"
local B_2 = "Utopia Towers Penthouse"
local B_3 = "OFF"
local B_4 = "DEFAULT"
local Event = game:GetService("ReplicatedStorage").Event
Event:FireServer(B_1, B_2, B_3, B_4)
wait(2)
Event:FireServer(A_1, A_2)
end)

n:Button("Lag x1",function()
    local args1 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    for i = 1, 1 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args1))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args1))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args1))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args1))
    wait()
    end
end)

n:Button("Lag x5",function()
    local args2 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    for i = 1, 5 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args2))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args2))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args2))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args2))
    wait()
    end
    end)

n:Button("Lag x50",function()
    local args3 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    for i = 1, 50 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args3))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args3))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args3))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args3))
    wait()
    end
    end)

n:Button("Lag x100",function()
    local args4 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    for i = 1, 100 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args4))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args4))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args4))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args4))
    wait()
    end
    end)

n:Button("Lag x500",function()
    local args5 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    for i = 1, 500 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args5))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args5))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args5))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args5))
    wait()
    end
    end)

n:Button("Enable auto lag",function()
    local args6 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    getgenv().AutoLagger = true
    while getgenv().AutoLagger do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    print("Lagging processing")
    wait()
    end
end)

n:Button("Disable auto lag",function()
    local args6 = {
        [1] = "LoadHome",
        [2] = "Utopia Towers Penthouse",
    }
    getgenv().AutoLagger = false
    while getgenv().AutoLagger do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args6))
    print("Lagging stopping")
    wait()
    end
end)

c:Button("Mission car + skins",function()
  local A_1 = "WeekReward"
  local A_22 = "Week1"
  local A_33 = "Week2"
  local A_44 = "Week3"
  local A_55 = "Week4"
  local A_66 = "Week5"
  local A_77 = "Week6"
  local Event = game:GetService("ReplicatedStorage").RemoteFunction
  Event:InvokeServer(A_1, A_22)
  Event:InvokeServer(A_1, A_33)
  Event:InvokeServer(A_1, A_44)
  Event:InvokeServer(A_1, A_55)
  Event:InvokeServer(A_1, A_66)
  Event:InvokeServer(A_1, A_77)
  local A_1 = "WeekReward"
  local A_2 = "Season6"
  local Event = game:GetService("ReplicatedStorage").RemoteFunction
  Event:InvokeServer(A_1, A_2)
end)

c:Button("Unlock all cars",function()
for i, v in pairs(game:GetService("Workspace").ObjectSelection:GetDescendants()) do
if v.Name == "VehicleName" then
v.Value = "Camaro"
end
end

for i, v in pairs(game:GetService("Workspace").ObjectSelection:GetDescendants()) do
if v.Name == "VehicleLock" then
v.Value = "OFF"
end
end
end)

c:Button("All gamepasses",function()
local g1 = Instance.new("BoolValue",game.Players.LocalPlayer)
g1.Name = "5275404"
g1.Value = true
local g2 = Instance.new("BoolValue",game.Players.LocalPlayer)
g2.Name = "5275406"
g2.Value = true
local g3 = Instance.new("BoolValue",game.Players.LocalPlayer)
g3.Name = "5275408"
g3.Value = true
local g4 = Instance.new("BoolValue",game.Players.LocalPlayer)
g4.Name = "5283883"
g4.Value = true
local g5 = Instance.new("BoolValue",game.Players.LocalPlayer)
g5.Name = "5285945"
g5.Value = true
local g6 = Instance.new("BoolValue",game.Players.LocalPlayer)
g6.Name = "5786950"
g6.Value = true
local g7 = Instance.new("BoolValue",game.Players.LocalPlayer)
g7.Name = "5945566"
g7.Value = true
local g8 = Instance.new("BoolValue",game.Players.LocalPlayer)
g8.Name = "5981868"
g8.Value = true
local g9 = Instance.new("BoolValue",game.Players.LocalPlayer)
g9.Name = "6023566"
g9.Value = true
local g10 = Instance.new("BoolValue",game.Players.LocalPlayer)
g10.Name = "6329988"
g10.Value = true
end)

c:Button("Camera zoom",function()
game:GetService("Players")["LocalPlayer"].CameraMaxZoomDistance = 100
game:GetService("Players")["LocalPlayer"].CameraMinZoomDistance = 0
end)

c:Button("Hide yo rank and name",function()
    game:GetService("Workspace")[game.Players.LocalPlayer.Name].NameTag:Destroy()
    game:GetService("Workspace")[game.Players.LocalPlayer.Name].NameTag:Delete()
end)

c:Button("Enable Antiarrest",function()
local Unarrest1 = {
    [1] = "Freedom",
    [2] = game:GetService("Players")["LocalPlayer"],
}
getgenv().unarrest = true
while getgenv().unarrest do
game:GetService("ReplicatedStorage").Event:FireServer(unpack(Unarrest1))
wait() 
end
end)

c:Button("Disable Antiarrest",function()
    local Unarrest1 = {
        [1] = "Freedom",
        [2] = game:GetService("Players")["LocalPlayer"],
    }
    getgenv().unarrest = false
    while getgenv().unarrest do
    game:GetService("ReplicatedStorage").Event:FireServer(unpack(Unarrest1))
    wait() 
    end
    end)

    c:Button("Enable no scope",function()
    getgenv().NoScope = true
    while getgenv().NoScope do
        for i = 1, 5 do
    game:GetService("Workspace")[game.Players.LocalPlayer.Name].Aiming.Value = true
    wait()
    end
    end
end)

c:Button("Disable no scope",function()
    getgenv().NoScope = true
    while getgenv().NoScope do
        for i = 1, 5 do
    game:GetService("Workspace")[game.Players.LocalPlayer.Name].Aiming.Value = true
    wait()
    end
    end
end)

d:Label("Created by GolemusInfernus#1281",{
    TextSize = 16; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
}) 

d:Label("Discord id 650424409261080586",{
    TextSize = 16; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
}) 

wait()

Home:Button("Place toilet x(?)",function()
local DoPlace = {
    [1] = "BuyItem",
    [2] = "T1",
}

for i = 1, 100 do
game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(DoPlace))
end
end)

K:Button("Buy basic home",function()
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer("BuyItem", "Basic Home")
    wait()
end)

K:Button("Use before lag",function()
    game:GetService("ReplicatedStorage").Event:FireServer("SpawnHome", "Basic Home", "OFF")
end)

K:Button("WeakLag",function()
    local LoadThisLETSGOXD = {
        [1] = "LoadHome",
        [2] = "Basic Home",
    }
    for i = 1,55 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(LoadThisLETSGOXD))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(LoadThisLETSGOXD))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(LoadThisLETSGOXD))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(LoadThisLETSGOXD))
    wait()
        end
    end)

K:Button("Strong Lag",function()
    local JustALoad = {
        [1] = "LoadHome",
        [2] = "Basic Home",
    }
    for i = 1,55555 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(JustALoad))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(JustALoad))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(JustALoad))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(JustALoad))
    wait()
        end
end)

K:Button("Enable autolag",function()
    local Autolagga = {
        [1] = "LoadHome",
        [2] = "Basic Home",
    }
    getgenv().AutoLagger1 = true
    while getgenv().AutoLagger1 do
        for i = 1,555 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    print("Lagging processing")
    wait()
        end
end
end)

K:Button("Disable autolag",function()
    local Autolagga = {
        [1] = "LoadHome",
        [2] = "Basic Home",
    }
    getgenv().AutoLagger1 = false
    while getgenv().AutoLagger1 do
        for i = 1,555 do
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(Autolagga))
    print("Lagging processing")
    wait()
        end
end
end)

Q:Toggle("Toggle auto crasher",function(bool)
    shared.toggle = bool
getgenv().Crasher = shared.toggle
    repeat wait(0.5)
    until game:IsLoaded()
local args2 = {
    [1] = "SpawnVehicle",
    [2] = "Camaro",
}
local TeamPolice = {
    [1] = "SetTeam",
    [2] = "Police",
}
local args1 = {
    [1] = "😳That lag ger by Mopler# 7791 cus why not, if someone wants me to stop lagging servers donate me robux or if its devs donate me robux/some vehicles (discus+s me in dc)🥶",
    [2] = "All",
}
game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(TeamPolice))
wait(0.8)
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args1))
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args1))
local ts = game:GetService("TweenService")
local tw = ts:Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(1),{CFrame = CFrame.new(-1020, 67, -2865) * CFrame.Angles(0,math.rad(90),0)})
tw:Play()
wait(1)
game:GetService("RunService").RenderStepped:Connect(function()
if getgenv().Crasher == true then
workspace.ObjectSelection.PoliceDogHouse.PoliceDogHouse.PoliceDogHouse.Event:FireServer()
end
end)
end)
--[[
How to refresh a dropdown:
1)Create the dropdown and save it in a variable
local yourvariable = b:Dropdown("Hi",yourtable,function(a)
    print(a)
end)
2)Refresh it using the function
yourvariable:Refresh(yourtable)
How to refresh a label:
1)Create your label and save it in a variable
local yourvariable = b:Label("Pretty Useless NGL",{
    TextSize = 25; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255);
    BgColor = Color3.fromRGB(69,69,69);
})
2)Refresh it using the function
yourvariable:Refresh("Hello") It will only change the text ofc
]]

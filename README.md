local SOMEXHUB = loadstring(game:HttpGet("https://raw.githubusercontent.com/I-DONT-KNOW-999/Gui-1/main/README.md"))();
local xNero = SOMEXHUB:Create({Name = "Supbaszz Hub",Size = UDim2.fromOffset(600, 400),Theme = SOMEXHUB.Themes.Dark,Link = "https://github.com/Lenova"})

xNero:Notification({Title = "Welcome Supbaszz Hub",Text = " ❤️ ",Duration = 3})
xNero:Credit{Name = "Lenova",Description = "Owner 👑 💎",}

local Main = xNero:Tab({Name = "Main",Icon = "rbxthumb://type=Asset&id=3517717568&w=150&h=150"})
local Plr = game.Players.LocalPlayer.Character.HumanoidRootPart

Main:Button({Name = "Auto Custard (survivor)",Description = nil,Callback = function()
    while wait() do
        wait(0.9)
                        game:GetService("ReplicatedStorage").collectedCustardEvent:FireServer()
        end
end})

Main:Toggle({Name = "Auto Attack (Monster)",StartingState = _G.AutoKill,Description = nil,Callback = function(AK)
    getgenv()._G.AutoKill = AK
    Spawn(function()
        while wait() do
            pcall(function()
                if _G.AutoKill then
                    game:GetService("ReplicatedStorage").sendAttack:FireServer()
                    end
                end)
    end
        end)
end})

Main:Slider({Name = "WalkSpeed",Default = "100",Min = "0",Max = "200",Callback = function(W)
    Spawn(function()
        while wait() do
            pcall(function()
                game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = W
                end)
            end
        end)
end})

Main:Button({Name = "Spawn Teletubby Land",Description = nil,Callback = function()
    Plr.CFrame = CFrame.new(-125.679993, 7.81443453, 192.496002, -0.982601225, -1.33154918e-08, 0.185727775, -2.72733107e-08, 1, -7.25970892e-08, -0.185727775, -7.63994024e-08, -0.982601225)
end})

Main:Button({Name = "Spawn Teletubby Secret Lair",Description = nil,Callback = function()
    Plr.CFrame = CFrame.new(-228.430054, -111.312279, -1927.25391, -0.931789637, -4.13418277e-09, 0.362998664, -2.07233555e-08, 1, -4.18062847e-08, -0.362998664, -4.6477215e-08, -0.931789637)
end})

Main:Button({Name = "Spawn Custard Facility",Description = nil,Callback = function()
    Plr.CFrame = CFrame.new(-1639.88586, 7.05154848, -783.685364, -0.980104864, 7.42316502e-08, 0.198480472, 6.77940974e-08, 1, -3.92296933e-08, -0.198480472, -2.49934082e-08, -0.980104864)
end})

Main:Button({Name = "Spawn Teletubby Outskirts",Description = nil,Callback = function()
    Plr.CFrame = CFrame.new(-1281.79395, -109.73365, -3054.03369, -0.977773607, -1.75048342e-09, 0.209663436, -1.6264103e-08, 1, -6.74992577e-08, -0.209663436, -6.94089834e-08, -0.977773607)
end})

Main:Button({Name = "Spawn Training Maze",Description = nil,Callback = function()
    Plr.CFrame = CFrame.new(759.320007, -105.788521, -2967.50391, -0.98456955, -1.06584721e-07, 0.174993858, -9.82303803e-08, 1, 5.64024702e-08, -0.174993858, 3.83424421e-08, -0.98456955)
end})

Main:Button({Name = "Remove effect screen",Description = nil,Callback = function()
game:GetService("Lighting").MonsterVision:Destroy()
wait()
game:GetService("Lighting").PlayerVision:Destroy()
end})

Main:Button({Name = "Full Bright",Description = nil,Callback = function()
    local Light = game:GetService("Lighting")

function dofullbright()
Light.Ambient = Color3.new(1, 1, 1)
Light.ColorShift_Bottom = Color3.new(1, 1, 1)
Light.ColorShift_Top = Color3.new(1, 1, 1)
end

dofullbright()

Light.LightingChanged:Connect(dofullbright)
end})

local Discord = xNero:Tab({Name = "Discord",Icon = "rbxthumb://type=Asset&id=3331928717&w=150&h=150"})

Discord:Button({Name = "Copy Discord",Description = nil,Callback = function()
xNero:Notification({Title = "Discord Supbaszz Hub",Text = "Success!!! link on your clipboard",Duration = 3})
setclipboard("https://discord.gg/awGECM6V25")
end})


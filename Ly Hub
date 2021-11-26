if game.PlaceId == 155615604 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Prison Life(Made By LY Roblox Hack)", "Sentinel")

    --MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")
    MainSection:NewDropdown("Give Gun", "Give the localplayer a gun", {"M9", "Remington 870", "AK-47"}, function(v)
        local A_1 = game:GetService("Workspace")["Prison_ITEMS"].giver[v].ITEMPICKUP
        local Event = game:GetService("Workspace")
            module["AutoFire"] = ("truerkspace").Remote.ItemHandler
        Event:InvokeSever(A_1)
    end)

    MainSection:NewDropdown("Gun Mod", "Makes the gun op", {"M9", "Remington 870", "AK-47"}, function(v)
        local module = nil
        if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v) then
            module = require(game:GetService("players").LocalPlayer.Backpack[v].GunStates)
        elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild(v) then
            module = require(game:GetService("players").LocalPlayer.Character[v].GunStates)
        end
        if module ~= nil then
            module["MaxAmmo"] = math.huge
            module["CurrentAmmo"] = math.huge
            module["StoredAmmo"] = math.huge
            module["FireRate"] = 0.000001
            module["Spread"] = 0
            module["Range"] = math.huge
            module["bullets"] = 10
            module["ReloadTime"] = 0.000001
        end
    end)

    -- PLAYER
    local Player = Window:NewTab("Player")
    local PlayerSection = Player:NewSection("Player")
    PlayerSection:NewSlider("WalkSpeed", "Changes the walkspeed", 250, 16, function(v)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
    end)
    PlayerSection:NewSlider("Jumppower", "Changes the jumppower", 250, 50, function(v)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
    end)
elseif game.PlaceId == 3956818381 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Ninja Legends(Made By LY Roblox Hack)", "Sentinel")

    --MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")

    MainSection:NewToggle("Auto Swing", "Make Your Player AutoSwing", function(v)
        getgenv().AutoSwing = v
        while true do
            if not getgenv().AutoSwing then return end
            for _,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v:FindFirstChild("ninjitsuGain") then
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                    break
                end
            end
            local A_1 = "swingKatana"
            local Event = game:GetService("Players").LocalPlayer.ninjaEvent
            Event:FireSever(A_1)
            wait(0.1)
        end
    end)
    MainSection:NewToggle("Auto Sell", "Makes Your Player Autosell", function(v)
        getgenv().autosell = v
        while true do
            if getgenv().autosell == false then return end
            game:GetService("Worspace").sellAreacircles["sellAreaCircle16"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootpart.CFrame
            wait(0.1)
            game:GetService("Worspace").sellAreacircles["sellAreaCircle16"].circleInner.CFrame = CFrame.new(0,0,0)
            wait(0.1)
        end
    end)
    MainSection:NewButton("Unlock all islands", "Unlocks all islands", function(v)
        local oldcframe = game.Players.LocalPlayer.Character.HumanoidRootpart.CFrame
        for _,v in pairs(game:GetService("Workspace").islandUnlockParts:GetChildren()) do
            game.Players.LocalPlayer.Character.HumanoidRootpart.CFrame = v.CFrame
            wait(0.1)
        end
        wait(0.1)
        game.Players.LocalPlayer.Character.HumanoidRootpart.CFrame = oldcframe
    end)
    MainSection:NewToggle("Buy all Swords", "Buys all Swords", function(v)
        getgenv().buyswords = v
        while true do
            if not getgenv().buyswords then return end
            local A_1 = "buyAllSwords"
            local A_2 = "Inner Peace Island"
            local Event = game:GetService("Players").LocalPlayer.ninjaEvent
            Event:FireSever(A_1, A_2)
            wait(0.5)
        end
    end)
end

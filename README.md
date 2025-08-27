# Renix-Hubb
Renix hub
-- JaydensHub Rayfield (KRNL Mobile Ready)
local Rayfield = loadstring(game:HttpGet("https://sirius.menu/rayfield"))()

local Window = Rayfield:CreateWindow({
    Name = "JaydensHub – Mobile",
    LoadingTitle = "Opening UI…",
    LoadingSubtitle = "Rayfield Base",
    ConfigurationSaving = {Enabled = false},
    KeySystem = false
})

-- Home tab
local HomeTab = Window:CreateTab("Home")

-- Holders for tabs
local LennonTab = nil
local AkunTab = nil
local JaydonsTab = nil
local MirandaTab = nil

-- Lennon Hub button
HomeTab:CreateButton({
    Name = "Lennon Hub – Free Access",
    Callback = function()
        if not LennonTab then
            LennonTab = Window:CreateTab("Lennon Hub")
            loadstring(game:HttpGet("https://pastefy.app/O0LXMwBW/raw", true))()
            LennonTab:CreateParagraph({
                Title = "Lennon Hub",
                Content = "✅ Lennon Hub Loaded Successfully!"
            })
        end
    end
})

-- Akun Disco button
HomeTab:CreateButton({
    Name = "AKUN DISCO FREE",
    Callback = function()
        if not AkunTab then
            AkunTab = Window:CreateTab("Akun Disco")
            loadstring(game:HttpGet("https://raw.githubusercontent.com/AkunDiscoOfficial/Scripts/refs/heads/main/FTG"))()
            AkunTab:CreateParagraph({
                Title = "Akun Disco",
                Content = "✅ Akun Disco Script Loaded Successfully!"
            })
        end
    end
})

-- JaydonsJoiner button
HomeTab:CreateButton({
    Name = "JaydonsJoiner",
    Callback = function()
        if not JaydonsTab then
            JaydonsTab = Window:CreateTab("JaydonsJoiner")
            loadstring(game:HttpGet("https://raw.githubusercontent.com/rexzysab/stealabrainrot/refs/heads/main/main.lua"))()("t.me/rbscriptstt")
            JaydonsTab:CreateParagraph({
                Title = "JaydonsJoiner",
                Content = "✅ JaydonsJoiner Script Loaded Successfully!"
            })
        end
    end
})

-- Miranda HUB button
HomeTab:CreateButton({
    Name = "Miranda HUB – FREE ACCESS",
    Callback = function()
        if not MirandaTab then
            MirandaTab = Window:CreateTab("Miranda HUB")
            loadstring(game:HttpGet("https://pastefy.app/mTbfVy0H/raw", true))()
            MirandaTab:CreateParagraph({
                Title = "Miranda HUB",
                Content = "✅ Miranda HUB Loaded Successfully!"
            })
        end
    end
})

-- Mobile scaling helper
task.spawn(function()
    task.wait(1)
    local gui = game:GetService("CoreGui"):FindFirstChildOfClass("ScreenGui")
    if gui then
        local UIS = Instance.new("UIScale")
        UIS.Parent = gui
        local sz = workspace.CurrentCamera.ViewportSize
        if math.min(sz.X, sz.Y) <= 900 then
            UIS.Scale = 0.9
        else
            UIS.Scale = 1
        end
    end
end)

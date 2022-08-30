local doit = {false, false, false, false, false, false}
local able = true
local uis = game:GetService("UserInputService")
local pos = 0

wait(1)
game.StarterGui:SetCore("SendNotification", {Title = "Thank you for using my script!"; Text = "This is my first script, and any help would be appriciated! (Check F9 for instructions)"; Duration = "10"; Button1 = "Ok shut up";
})
print("This script optimizes ascending\nYou must be in the ascender tab for it to work\nYou must stay in ROBLOX for it to work\nPress S to stop the script\nPress M to toggle Mold\nPress C to toggle Class\nPress E to toggle Enchant\nPress Q to toggle Quality\nPress L to toggle Level\nAnd finally, press R to toggle Rarity.\n\nOnly one can be toggled at once\nIf you want value, go for: Rarity, Mold, Quality\nIf you want damage, go for: Rarity, Class")

uis.TextBoxFocused:Connect(function()
    able = false
end)
uis.TextBoxFocusReleased:Connect(function()
    able = true
end)

uis.InputBegan:Connect(function(input)
    if able then
        if input.KeyCode == Enum.KeyCode.M then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[1] = true
        end
        if input.KeyCode == Enum.KeyCode.C then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[2] = true
        end
        if input.KeyCode == Enum.KeyCode.E then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[3] = true
        end
        if input.KeyCode == Enum.KeyCode.Q then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[4] = true
        end
        if input.KeyCode == Enum.KeyCode.L then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[5] = true
        end
        if input.KeyCode == Enum.KeyCode.R then
            for index = 1, #doit do
                doit[index] = false
            end
            doit[6] = true
        end
        if input.KeyCode == Enum.KeyCode.S then
            for index = 1, #doit do
                doit[index] = false
            end
        end
    end
end)


while wait() do
    wait(0.1)
    for index = 1, #doit do
        pos = index * 100
        local arg = 650
        if pos > 300 then arg = 1250 end
        if doit[index] then
            if pos > 300 then
            mousemoveabs(arg,200 + pos - 300)
            mousemoveabs(arg,199 + pos - 300)
            mouse1click()
            wait(0.3)
            mousemoveabs(arg,500)
            mouse1click()
            end
            if pos <= 300 then
            mousemoveabs(arg,200 + pos)
            mousemoveabs(arg,199 + pos)
            mouse1click()
            wait(0.3)
            mousemoveabs(arg,500)
            mouse1click()
            end
        end
    end
end

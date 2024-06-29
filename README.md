_G.CheckQuest0001 = true

function CheckQuest001()
    while _G.CheckQuest001 do
        wait(1)
        local player = game:GetService("Players").LocalPlayer
        local level = player.PlayerStats.lvl.Value
        if level >= 1500 and level <= 1549 then
            if not VisQuest() then
                local args = {
                    [1] = "take",
                    [2] = "Kill 5 Zombies"
                }
                
                game:GetService("ReplicatedStorage"):WaitForChild("Chest"):WaitForChild("Remotes"):WaitForChild("Functions"):WaitForChild("Quest"):InvokeServer(unpack(args))
            end
        end
    end
end

CheckQuest001()

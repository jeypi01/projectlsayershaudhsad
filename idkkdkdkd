---@diagnostic disable: undefined-global

repeat wait() until game:IsLoaded() 

loadstring(game:HttpGet("https://raw.githubusercontent.com/Novaz5792/X/main/X"))() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/Novaz5792/X/main/Y"))() 

game.ReplicatedStorage:WaitForChild("Remotes"):WaitForChild("getclientping").OnClientInvoke = function(Novaz5792) 
    task.wait(5)
    return true 
end

local mobs = {} 

for i,v in pairs(Workspace.Mobs:GetDescendants()) do 
    if v:FindFirstChild("Npc_Configuration") then
        local modu = require(v.Npc_Configuration) 
        table.insert(mobs, {v, modu.Npc_Spawning.Spawn_Locations[1] or modu.Npc_Spawning.Spawn_Locations, modu.Name})
    end 
    if v.Parent:FindFirstChild("Npc_Configuration") then
        local modu = require(v.Parent.Npc_Configuration) 
        table.insert(mobs, {v.Parent, modu.Npc_Spawning.Spawn_Locations[1] or modu.Npc_Spawning.Spawn_Locations, modu.Name})
    end 
end 

Workspace.Mobs.DescendantAdded:Connect(function(v)
    if v:FindFirstChild("Npc_Configuration") then
        local modu = require(v.Npc_Configuration) 
        table.insert(mobs, {v, modu.Npc_Spawning.Spawn_Locations[1] or modu.Npc_Spawning.Spawn_Locations, modu.Name})
    end 
    if v.Parent:FindFirstChild("Npc_Configuration") then
        local modu = require(v.Parent.Npc_Configuration) 
        table.insert(mobs, {v.Parent, modu.Npc_Spawning.Spawn_Locations[1] or modu.Npc_Spawning.Spawn_Locations, modu.Name})
    end 
end)

Workspace.Mobs.DescendantRemoving:Connect(function(v)
    if v:IsA("Configuration") then 
        for i1,v1 in ipairs(mobs) do 
            if v1[1] == v then 
                table.remove(mobs, i1)
            end 
        end 
    end 
end)

function getclosestmob()
    local ret = {nil, Huge} 
    for i,v in pairs(workspace.Mobs:GetChildren()) do 
        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then 
            local magnitude = (HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude 
            if magnitude < ret[2] then 
                ret[2] = magnitude 
                ret[1] = v 
            end 
        end 
        for i1,v1 in pairs(v:GetChildren()) do 
            if v1:FindFirstChild("HumanoidRootPart") and v1:FindFirstChild("Humanoid") and v1.Humanoid.Health > 0 then 
                local magnitude = (HumanoidRootPart.Position - v1.HumanoidRootPart.Position).Magnitude 
                if magnitude < ret[2] then 
                    ret[2] = magnitude 
                    ret[1] = v1
                end 
            end 
            for i2,v2 in pairs(v1:GetChildren()) do 
                if v2:FindFirstChild("HumanoidRootPart") and v2:FindFirstChild("Humanoid") and v2.Humanoid.Health > 0 then 
                    local magnitude = (HumanoidRootPart.Position - v2.HumanoidRootPart.Position).Magnitude 
                    if magnitude < ret[2] then 
                        ret[2] = magnitude 
                        ret[1] = v2
                    end 
                end 
            end 
        end 
    end 
    return ret[1]
end 


local lib = loadstring(game:GetObjects("rbxassetid://7657867786")[1].Source)()
local subs = lib.subs 
local libclose = subs.Wait

local window = lib:CreateWindow({
    Name = "Zenji Hub",
    Themeable = {
        Info = {"Kalas A Skid"},
        Credit = false, 
        Background = "",
        Visible = true
    }
})

local main1 = window:CreateTab({
    Name = "ฟังชั่น"
})

local section1 = main1:CreateSection({
    Name = "ฟังชั่น"
})

local section2 = main1:CreateSection({
    Name = "Kill Aura",
    Side = "Right"
})

local savedtick = tick()
local curtarget = nil 
section1:AddToggle({
    Name = "ออร่ามอน", 
    Value = false, 
    Flag = "AF", 
    Callback = function(state)
        a = state 
        while a do 
            local target = getclosestmob() 
            if target and target:FindFirstChild("HumanoidRootPart")and (target.Name:match("Civilian") or target.Name:match("Demon")) then 
                HumanoidRootPart.CFrame = CFrame.new(target.HumanoidRootPart.Position + target.HumanoidRootPart.CFrame.LookVector * 7, target.HumanoidRootPart.Position)
            end 
            task.wait()
        end 
    end 
})

local debounce = false 
section2:AddToggle({
    Name = "กดซะถ้านายแน่จริง Kill Aura", 
    Value = false, 
    Flag = "KA", 
    Callback = function(state)
        b = state 
        while b do 
            if (not debounce) and ((not Player:FindFirstChild("combotangasd123")) or Player:FindFirstChild("combotangasd123") and Player:FindFirstChild("combotangasd123").Value < 1) then 
                debounce = true 
                local last = 9999
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 1, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 2, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 3, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 4, nil, nil, 99999)
                last = game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S_:InvokeServer(c, Player, Character, HumanoidRootPart, Humanoid, 919, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 1, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 2, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 3, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 4, nil, nil, 99999)
                last = game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S_:InvokeServer(c, Player, Character, HumanoidRootPart, Humanoid, 919, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 1, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 2, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 3, nil, nil, 99999)
                game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S:FireServer(c, Player, Character, HumanoidRootPart, Humanoid, 4, nil, nil, 99999)
                last = game:GetService("ReplicatedStorage").Remotes.To_Server.Handle_Initiate_S_:InvokeServer(c, Player, Character, HumanoidRootPart, Humanoid, 919, nil, nil, 99999)
                repeat Heartbeat:Wait() until last ~= 9999 
                task.wait()
                debounce = false 
            end 
            task.wait()
        end 
    end 
})


section2:AddDropdown({
    Name = "เลือกอาวุธ", 
    Nothing = "ไม่มีอะไรเลย..", 
    List = {"fist_combat", "Sword_Combat_Slash", "claw_Combat_Slash", "Scythe_Combat_Slash"}, 
    Flag = "SW", 
    Callback = function(selected)
        c = selected 
    end 
})

for i,v in pairs(getconnections(Player.Idled)) do 
    v:Disable()
end

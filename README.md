local CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
local Target = "PLAYER NAME HERE"
for i,x in pairs(game.Players:GetPlayers()) do
if x.Name == Target then
game:GetService("Players").LocalPlayer.Character.Humanoid:UnequipTools()
local Humanoid = game:GetService("Players").LocalPlayer.Character.Humanoid:Clone()
Humanoid.BreakJointsOnDeath = false
game.Players.LocalPlayer.Character.Animate.Disabled = true
game:GetService("Players").LocalPlayer.Character.Humanoid:Destroy()
Humanoid.Parent = game:GetService("Players").LocalPlayer.Character
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
    if v:IsA("Tool") then
        game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool"))
        firetouchinterest(v.Handle,x.Character.HumanoidRootPart,0)
    end
end
end
end
game.Players.LocalPlayer.CharacterAdded:Wait():WaitForChild("Humanoid")
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame

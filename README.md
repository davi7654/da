local player = game.Players.LocalPlayer
local speed = 100 -- Altere este valor para a velocidade desejada (padrão Roblox é 16)

player.CharacterAdded:Connect(function(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.WalkSpeed = speed
end)

-- Caso o personagem já esteja carregado
if player.Character and player.Character:FindFirstChild("Humanoid") then
    player.Character.Humanoid.WalkSpeed = speed
end

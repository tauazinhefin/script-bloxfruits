local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local localPlayer = Players.LocalPlayer

-- Função para voar e matar todos os NPCs
local function enableFlyAndKillNPCs()
    print("Você agora pode voar e todos os NPCs serão eliminados!")
    -- Código para voar e matar NPCs
end

-- Função para fazer chover frutas
local function rainFruits()
    print("Vai começar a chover frutas em você!")
    -- Código para fazer chover frutas
end

-- Função para matar um jogador específico
local function killPlayer(playerName)
    local player = Players:FindFirstChild(playerName)
    if player then
        player.Character:BreakJoints() -- Mata o personagem
        print(playerName .. " foi eliminado!")
    else
        print("Jogador não encontrado")
    end
end

-- Função para exibir o menu
local function displayMenu()
    local screenGui = Instance.new("ScreenGui", localPlayer:WaitForChild("PlayerGui"))
    local frame = Instance.new("Frame", screenGui)
    frame.Size = UDim2.new(0.3, 0, 0.5, 0)
    frame.Position = UDim2.new(0.35, 0, 0.25, 0)
    frame.BackgroundColor3 = Color3.new(0, 0, 0)

    local option1 = Instance.new("TextButton", frame)
    option1.Size = UDim2.new(1, 0, 0.3, 0)
    option1.Position = UDim2.new(0, 0, 0, 0)
    option1.Text = "1. Voar e Matar NPCs"
    option1.MouseButton1Click:Connect(enableFlyAndKillNPCs)

    local option2 = Instance.new("TextButton", frame)
    option2.Size = UDim2.new(1, 0, 0.3, 0)
    option2.Position = UDim2.new(0, 0, 0.35, 0)
    option2.Text = "2. Chuva de Frutas"
    option2.MouseButton1Click:Connect(rainFruits)

    local option3 = Instance.new("TextButton", frame)
    option3.Size = UDim2.new(1, 0, 0.3, 0)
    option3.Position = UDim2.new(0, 0, 0.7, 0)
    option3.Text = "3. Matar Jogador Específico"
    option3.MouseButton1Click:Connect(function()
        local playerName = "NomeDoJogador" -- Substitua pelo nome do jogador que deseja eliminar
        killPlayer(playerName)
    end)
end

-- Detecta inicialização do jogo para exibir o menu
local function onStart()
    displayMenu()
end

onStart()

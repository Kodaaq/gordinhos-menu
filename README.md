local Players = game:GetService("Players")
local player = Players.LocalPlayer
local replicatedStorage = game:GetService("ReplicatedStorage")

function teleportTo(position)
    if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
        player.Character.HumanoidRootPart.CFrame = CFrame.new(position)
    end
end

for level = 1, 2650 do
    print("Subindo para o nível:", level)
    wait(0.1) -- Simula delay de ação

    -- Simula obtenção de estilo de luta
    if level == 150 then
        print("Estilo de Luta: Black Leg desbloqueado.")
    elseif level == 350 then
        print("Estilo de Luta: Electro desbloqueado.")
    elseif level == 800 then
        print("Estilo de Luta: Dragon Claw desbloqueado.")
    end

    -- Simula obtenção de espada
    if level == 200 then
        print("Espada: Katana desbloqueada.")
    elseif level == 600 then
        print("Espada: Saber desbloqueada.")
    end

    -- Simula teleport e ataque em Pre Historic Island
    if level == 1000 then
        print("Indo para Pre Historic Island...")
        teleportTo(Vector3.new(999, 300, -1500)) -- Coordenada fictícia

        print("Atacando todos os NPCs... [Simulado]")
        print("Tampando o vulcão... [Simulado]")
        print("Pegando itens especiais... [Simulado]")
    end

    -- Simula desbloqueio do Haki V2
    if level == 2000 then
        print("Haki V2 desbloqueado.")
    end
end

print("Todos os objetivos concluídos até o nível 2650!")

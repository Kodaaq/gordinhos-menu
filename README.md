-- Painel de Controle (LocalScript dentro de StarterGui)
local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
gui.Name = "PainelGUI"

-- Função para criar botões
local function criarBotao(texto, posY, callback)
	local botao = Instance.new("TextButton")
	botao.Size = UDim2.new(0, 200, 0, 40)
	botao.Position = UDim2.new(0, 10, 0, posY)
	botao.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
	botao.TextColor3 = Color3.fromRGB(255, 255, 255)
	botao.Text = texto
	botao.Parent = gui

	botao.MouseButton1Click:Connect(callback)
end

-- Funções simuladas
local function autoFarm()
	print("AutoFarm Ativado: Atacando NPCs...")
end

local function teleportar()
	if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
		player.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(1000, 100, -1500))
		print("Teleportado para Pre Historic Island!")
	end
end

local function desbloquearHaki()
	print("Haki V2 desbloqueado!")
end

-- Criar botões
criarBotao("Ativar AutoFarm", 50, autoFarm)
criarBotao("Teleportar para Ilha", 100, teleportar)
criarBotao("Desbloquear Haki V2", 150, desbloquearHaki)

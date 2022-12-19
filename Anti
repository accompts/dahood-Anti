-- $$\                $$\                 
-- $$ |               $$ |                
-- $$ |     $$\   $$\ $$ |  $$\  $$$$$$\  
-- $$ |     $$ |  $$ |$$ | $$  |$$  __$$\ 
-- $$ |     $$ |  $$ |$$$$$$  / $$$$$$$$ |
-- $$ |     $$ |  $$ |$$  _$$<  $$   ____|
-- $$$$$$$$\\$$$$$$  |$$ | \$$\ \$$$$$$$\ 
-- \________|\______/ \__|  \__| \_______|
local UserInputService = game:GetService("UserInputService")

local function onInputBegan(input, _gameProcessed)
	if input.KeyCode == Enum.KeyCode.G then
		getgenv().antilock = true
	end
end

local function onInputEnded(input, _gameProcessed)
	if input.KeyCode == Enum.KeyCode.G then
		getgenv().antilock = false
	end
end


UserInputService.InputBegan:Connect(onInputBegan)
UserInputService.InputEnded:Connect(onInputEnded)

game:GetService("RunService").Heartbeat:Connect(function()
    if getgenv().antilock == true then 
    local abc = game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity
    game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = Vector3.new(1,1,1) * (2^16)
    game:GetService("RunService").RenderStepped:Wait()
    game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = abc
    end 
end)
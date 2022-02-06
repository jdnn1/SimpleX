-- By wrqe#9521
-- Version: 1.0

-- Instances:

local screen = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local SimpleNoclip = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local SimpleFly = Instance.new("TextButton")
local SimpleTp = Instance.new("TextButton")
local SimpleRespawn = Instance.new("TextButton")
local DestroyUI = Instance.new("TextButton")

--Properties:

screen.Name = "screen"
screen.Parent = game.CoreGui
screen.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = screen
Main.BackgroundColor3 = Color3.fromRGB(42, 4, 74)
Main.BackgroundTransparency = 0.080
Main.Position = UDim2.new(0.767346919, 0, 0.151291505, 0)
Main.Size = UDim2.new(0, 171, 0, 262)

SimpleNoclip.Name = "SimpleNoclip"
SimpleNoclip.Parent = Main
SimpleNoclip.BackgroundColor3 = Color3.fromRGB(27, 42, 53)
SimpleNoclip.BackgroundTransparency = -0.010
SimpleNoclip.BorderColor3 = Color3.fromRGB(33, 53, 34)
SimpleNoclip.Position = UDim2.new(0, 0, 0.0801526681, 0)
SimpleNoclip.Size = UDim2.new(0, 171, 0, 45)
SimpleNoclip.Font = Enum.Font.Merriweather
SimpleNoclip.Text = "Simple Noclip"
SimpleNoclip.TextColor3 = Color3.fromRGB(0, 0, 0)
SimpleNoclip.TextSize = 14.000
SimpleNoclip.MouseButton1Down:connect(function()
	noclip = false
	game:GetService('RunService').Stepped:Connect(function()
		if noclip then
			game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)

		end
	end)

	local p = game.Players.LocalPlayer
	local mo = p:GetMouse()

	mo.KeyDown:Connect(function(k)
		if k == 'n' then
			noclip = not noclip
			p.Character.Humanoid:ChangeState(11)
		end
	end)
end)

TextLabel.Parent = Main
TextLabel.BackgroundColor3 = Color3.fromRGB(27, 42, 53)
TextLabel.Size = UDim2.new(0, 171, 0, 21)
TextLabel.Font = Enum.Font.Merriweather
TextLabel.Text = "https://discord.gg/XvKtqGFW3x"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 14.000

SimpleFly.Name = "SimpleFly"
SimpleFly.Parent = Main
SimpleFly.BackgroundColor3 = Color3.fromRGB(27, 42, 53)
SimpleFly.Position = UDim2.new(0, 0, 0.251908362, 0)
SimpleFly.Size = UDim2.new(0, 171, 0, 45)
SimpleFly.Font = Enum.Font.Merriweather
SimpleFly.Text = "Simple Fly"
SimpleFly.TextColor3 = Color3.fromRGB(0, 0, 0)
SimpleFly.TextSize = 14.000
SimpleFly.MouseButton1Down:connect(function()
	-- Fly GUI


	-- Instances:

	local fly = Instance.new("ScreenGui")
	local epic = Instance.new("Frame")
	local backgroundtitle = Instance.new("TextLabel")
	local creator = Instance.new("TextLabel")
	local title = Instance.new("TextLabel")
	local close = Instance.new("TextButton")
	local flybutton = Instance.new("TextButton")

	--Properties:

	fly.Name = "fly"
	fly.Parent = game.CoreGui
	fly.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

	epic.Name = "epic"
	epic.Parent = fly
	epic.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	epic.Position = UDim2.new(0.0911376476, 0, 0.466830462, 0)
	epic.Size = UDim2.new(0, 181, 0, 178)
	epic.Active = true
	epic.Draggable = true

	backgroundtitle.Name = "backgroundtitle"
	backgroundtitle.Parent = epic
	backgroundtitle.BackgroundColor3 = Color3.fromRGB(170, 0, 255)
	backgroundtitle.Size = UDim2.new(0, 182, 0, 43)
	backgroundtitle.Font = Enum.Font.SciFi
	backgroundtitle.Text = ""
	backgroundtitle.TextColor3 = Color3.fromRGB(0, 0, 0)
	backgroundtitle.TextScaled = true
	backgroundtitle.TextSize = 14.000
	backgroundtitle.TextWrapped = true

	creator.Name = "creator"
	creator.Parent = epic
	creator.BackgroundColor3 = Color3.fromRGB(170, 0, 255)
	creator.Position = UDim2.new(0.00442049652, 0, 0.762519121, 0)
	creator.Size = UDim2.new(0, 181, 0, 42)
	creator.Font = Enum.Font.SourceSans
	creator.Text = "Made by Arowix"
	creator.TextColor3 = Color3.fromRGB(0, 0, 0)
	creator.TextScaled = true
	creator.TextSize = 14.000
	creator.TextWrapped = true

	title.Name = "title"
	title.Parent = epic
	title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	title.BackgroundTransparency = 1.000
	title.Position = UDim2.new(0.0497237556, 0, 0, 0)
	title.Size = UDim2.new(0, 119, 0, 43)
	title.Font = Enum.Font.SciFi
	title.Text = "Fly"
	title.TextColor3 = Color3.fromRGB(0, 0, 0)
	title.TextScaled = true
	title.TextSize = 14.000
	title.TextWrapped = true

	close.Name = "close"
	close.Parent = epic
	close.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
	close.Position = UDim2.new(0.76795578, 0, 0, 0)
	close.Size = UDim2.new(0, 43, 0, 43)
	close.Font = Enum.Font.GothamBlack
	close.Text = "X"
	close.TextColor3 = Color3.fromRGB(0, 0, 0)
	close.TextScaled = true
	close.TextSize = 14.000
	close.TextWrapped = true
	close.MouseButton1Down:connect(function()
		epic.Visible = false
	end)

	flybutton.Name = "flybutton"
	flybutton.Parent = epic
	flybutton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	flybutton.Position = UDim2.new(0.243093923, 0, 0.344781578, 0)
	flybutton.Size = UDim2.new(0, 84, 0, 42)
	flybutton.Font = Enum.Font.SourceSans
	flybutton.Text = "Click me to Fly"
	flybutton.TextColor3 = Color3.fromRGB(0, 0, 0)
	flybutton.TextSize = 14.000
	flybutton.MouseButton1Down:connect(function()
		loadstring(game:HttpGet("https://pastebin.com/raw/7rXZ9VNc", true))()
		flybutton.Text = "Press E to fly and unfly"
		flybutton.TextSize = 10.000
	end)
end)

SimpleTp.Name = "SimpleTp"
SimpleTp.Parent = Main
SimpleTp.BackgroundColor3 = Color3.fromRGB(27, 42, 53)
SimpleTp.Position = UDim2.new(0, 0, 0.423664093, 0)
SimpleTp.Size = UDim2.new(0, 171, 0, 45)
SimpleTp.Font = Enum.Font.Merriweather
SimpleTp.Text = "Simple Tp Tool"
SimpleTp.TextColor3 = Color3.fromRGB(0, 0, 0)
SimpleTp.TextSize = 14.000
SimpleTp.MouseButton1Down:connect(function()
	mouse = game.Players.LocalPlayer:GetMouse()
	tool = Instance.new("Tool")
	tool.RequiresHandle = false
	tool.Name = "Click Teleport"
	tool.Activated:connect(function()
		local pos = mouse.Hit+Vector3.new(0,2.5,0)
		pos = CFrame.new(pos.X,pos.Y,pos.Z)
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
	end)
end)

SimpleRespawn.Name = "SimpleRespawn"
SimpleRespawn.Parent = Main
SimpleRespawn.BackgroundColor3 = Color3.fromRGB(27, 42, 53)
SimpleRespawn.Position = UDim2.new(0, 0, 0.595419824, 0)
SimpleRespawn.Size = UDim2.new(0, 171, 0, 50)
SimpleRespawn.Font = Enum.Font.Merriweather
SimpleRespawn.Text = "Simple R to Reset (press to work)"
SimpleRespawn.TextColor3 = Color3.fromRGB(0, 0, 0)
SimpleRespawn.TextSize = 14.000
SimpleRespawn.MouseButton1Down:connect(function()
	local player = game.Players.LocalPlayer
	local mouse = player:GetMouse()
	local char = player.Character
	local h = char:WaitForChild("Humanoid")
	mouse.KeyUp:connect(function(key)
		if key == "r" then
			h.Health = 0
		end
	end)
end)

DestroyUI.Name = "DestroyUI"
DestroyUI.Parent = Main
DestroyUI.BackgroundColor3 = Color3.fromRGB(53, 0, 0)
DestroyUI.Position = UDim2.new(0, 0, 0.786259532, 0)
DestroyUI.Size = UDim2.new(0, 171, 0, 56)
DestroyUI.Font = Enum.Font.Merriweather
DestroyUI.Text = "KillSwitch"
DestroyUI.TextColor3 = Color3.fromRGB(0, 0, 0)
DestroyUI.TextSize = 14.000
DestroyUI.TextWrapped = true
DestroyUI.MouseButton1Down:connect(function()
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Visible = false
	end)

end)

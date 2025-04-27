local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Tạo GUI
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "ControlPanelGui"
ScreenGui.Parent = player:WaitForChild("PlayerGui")

local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0.3, 0, 0.3, 0)
Frame.Position = UDim2.new(0.35, 0, 0.35, 0)
Frame.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
Frame.BorderSizePixel = 1
Frame.Active = true
Frame.Draggable = true
Frame.Parent = ScreenGui

-- Tạo chữ toàn màn hình
local FullScreenText = Instance.new("TextLabel")
FullScreenText.Size = UDim2.new(1, 0, 1, 0)
FullScreenText.Position = UDim2.new(0, 0, 0, 0)
FullScreenText.Text = ""
FullScreenText.Font = Enum.Font.SourceSansBold
FullScreenText.TextSize = 50
FullScreenText.TextColor3 = Color3.fromRGB(0, 0, 0)
FullScreenText.BackgroundTransparency = 1
FullScreenText.Visible = false
FullScreenText.Parent = ScreenGui

-- Hàm hiển thị thông báo toàn màn hình
local function showFullScreenMessage(message)
    FullScreenText.Text = message
    FullScreenText.Visible = true
    task.delay(3, function()
        FullScreenText.Visible = false
    end)
end

-- Hàm tạo nút
local function createButton(parent, text, position, color, callback)
    local button = Instance.new("TextButton")
    button.Size = UDim2.new(0.4, 0, 0.2, 0)
    button.Position = position
    button.Text = text
    button.Font = Enum.Font.SourceSansBold
    button.TextSize = 18
    button.BackgroundColor3 = color
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.Parent = parent
    button.MouseButton1Click:Connect(callback)
    return button
end

-- Tạo nút "Super Fly"
createButton(Frame, "Super Fly", UDim2.new(0.3, 0, 0.25, 0), Color3.fromRGB(100, 100, 200), function()
    showFullScreenMessage("Script Fly")
    loadstring(game:HttpGet("https://raw.githubusercontent.com/AmareScripts/DeadRails/refs/heads/main/Bypass%25AntiCheat.lua"))()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/Vehicle%20Fly%20Gui'))()
end)

-- Tạo nút "TWVZ" (đổi tên từ "XuanVp HUD")
createButton(Frame, "TWVZ", UDim2.new(0.3, 0, 0.5, 0), Color3.fromRGB(200, 100, 100), function()
    showFullScreenMessage("Script TWVZ")
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ZhangJunZ84/twvz/refs/heads/main/arisecrossover.lua"))()NVNPRO/XuanVPHUB/refs/heads/main/XuanVPPHUB.lua.txt"))()
end)

-- Tạo nút "GOOMBA" (đổi tên từ "Null Fire")
createButton(Frame, "GOOMBA", UDim2.new(0.3, 0, 0.75, 0), Color3.fromRGB(150, 50, 250), function()
    showFullScreenMessage("Script GOOMBA")
    loadstring(game:HttpGet("https://raw.githubusercontent.com/JustLevel/goombahub/main/AriseCrossover.lua"))()
end)

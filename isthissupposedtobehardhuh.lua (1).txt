-- SKIDDDDSD ECKKKK LOLL

local t1 = {}
local v2 = unpack or table.unpack
if not game:IsLoaded() then
    game.Loaded:Wait()
end
if getgenv().VortexHub then
    print("Previous gui detected!")

    local StarterGui = game:GetService("StarterGui")

    t1.value3 = {
		Title = "Previous gui detected!",
		Text = "Please close the previous gui to create the new one",
		Duration = 5
	}
    StarterGui:SetCore("SendNotification", t1.value3)

    return
end
local v4 = getgenv()
t1.value1 = "VortexHub"
v4[t1.value1] = true
local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")
t1.value3 = game:GetService("TweenService")
local value3 = t1.value3
t1.value2 = game:GetService("RunService")
local value2 = t1.value2
t1.value5 = game:GetService("Lighting")
local value5 = t1.value5
t1.value6 = game:GetService("Workspace")
local value6 = t1.value6
t1.value4 = game:GetService("ReplicatedStorage")
local value4 = t1.value4
t1.value4 = Players.LocalPlayer
local value4_2 = t1.value4
t1.value4 = workspace.CurrentCamera
local value4_3 = t1.value4
t1.value4 = UserInputService.TouchEnabled and not UserInputService.KeyboardEnabled
local value4_4 = t1.value4
t1.value4 = value4_3.ViewportSize
local value4_5 = t1.value4
function t1.value7(p1)
    if setclipboard then
        setclipboard(p1)
    end
end
function t1.value8(p2, p3, p4)
    local StarterGui = game:GetService("StarterGui")
    local SetCore = StarterGui.SetCore
    local v159 = p4 or 3

    SetCore(StarterGui, "SendNotification", {
		Title = p2,
		Text = p3,
		Duration = v159
	})
end
local value7 = t1.value7
local value8 = t1.value8
local t2 = {}
function t1.value8(_)
end
t2.Disable = t1.value8
function t1.value8()
    local ScreenGui = Instance.new("ScreenGui")
    ScreenGui.Name = "VH_Loading"
    ScreenGui.IgnoreGuiInset = true
    ScreenGui.DisplayOrder = 9999
    ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    ScreenGui.Parent = value4_2.PlayerGui
    local Frame = Instance.new("Frame")
    Frame.Size = UDim2.new(1, 0, 1, 0)
    Frame.BackgroundColor3 = Color3.fromRGB(5, 8, 18)
    Frame.BorderSizePixel = 0
    Frame.ZIndex = 1
    Frame.Parent = ScreenGui
    local UIGradient = Instance.new("UIGradient")
    UIGradient.Color = ColorSequence.new({
		ColorSequenceKeypoint.new(0, Color3.fromRGB(0, 80, 160)),
		ColorSequenceKeypoint.new(0.5, Color3.fromRGB(0, 150, 255)),
		ColorSequenceKeypoint.new(1, Color3.fromRGB(0, 60, 140))
	})
    UIGradient.Rotation = 45
    UIGradient.Parent = Frame
    task.spawn(function()
        for _ = 1, 15 do
            local Frame2 = Instance.new("Frame")

            Frame2.Size = UDim2.new(0, math.random(2, 4), 0, math.random(2, 4))
            Frame2.Position = UDim2.new(math.random(), 0, 1.1, 0)
            Frame2.BackgroundColor3 = Color3.fromRGB(100, 200, 255)
            Frame2.BackgroundTransparency = 0.3
            Frame2.BorderSizePixel = 0
            Frame2.ZIndex = 2
            Frame2.Parent = Frame

            local UICorner = Instance.new("UICorner")

            UICorner.CornerRadius = UDim.new(1, 0)
            UICorner.Parent = Frame2

            local v513 = math.random(8, 15)
            local v514 = math.random(-20, 20) / 100

            value3:Create(Frame2, TweenInfo.new(v513, Enum.EasingStyle.Linear), {
				Position = UDim2.new(Frame2.Position.X.Scale + v514, 0, -0.1, 0),
				BackgroundTransparency = 1
			}):Play()
            game:GetService("Debris"):AddItem(Frame2, v513)
        end
    end)
    local v164 = value4_4
    if v164 then
        v164 = value4_5.X - 30
    end
    local v165 = v164 or 420
    local v166 = not value4_4 and 320 or 200
    local Frame3 = Instance.new("Frame")
    Frame3.Size = UDim2.new(0, v165, 0, v166)
    Frame3.Position = UDim2.new(0.5, -v165 / 2, 0.5, -v166 / 2)
    Frame3.BackgroundColor3 = Color3.fromRGB(8, 12, 25)
    Frame3.BackgroundTransparency = 0.1
    Frame3.BorderSizePixel = 0
    Frame3.ZIndex = 5
    Frame3.Parent = Frame
    local UICorner = Instance.new("UICorner")
    UICorner.CornerRadius = UDim.new(0, not value4_4 and 16 or 10)
    UICorner.Parent = Frame3
    local UIStroke = Instance.new("UIStroke")
    UIStroke.Color = Color3.fromRGB(0, 170, 255)
    UIStroke.Thickness = 2
    UIStroke.Transparency = 0.3
    UIStroke.Parent = Frame3
    local v170 = not value4_4 and 80 or 55
    local ImageLabel = Instance.new("ImageLabel")
    ImageLabel.Name = "VHLogo"
    ImageLabel.Size = UDim2.new(0, v170, 0, v170)
    ImageLabel.Position = UDim2.new(0.5, -v170 / 2, 0, not value4_4 and 30 or 12)
    ImageLabel.BackgroundTransparency = 1
    ImageLabel.Image = "rbxassetid://90145481353879"
    ImageLabel.ScaleType = Enum.ScaleType.Fit
    ImageLabel.ZIndex = 6
    ImageLabel.Parent = Frame3
    local UICorner2 = Instance.new("UICorner")
    UICorner2.CornerRadius = UDim.new(0, not value4_4 and 12 or 8)
    UICorner2.Parent = ImageLabel
    local UIStroke2 = Instance.new("UIStroke")
    UIStroke2.Color = Color3.fromRGB(0, 170, 255)
    UIStroke2.Thickness = 2
    UIStroke2.Parent = ImageLabel
    task.spawn(function()
        while true do
            local v515 = ImageLabel

            if v515 then
                v515 = ImageLabel.Parent
            end

            if not v515 then
                break
            end

            local v516 = value3
            local v517 = ImageLabel
            local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
            local uDim2 = UDim2.new(0, v170 + 6, 0, v170 + 6)
            local new = UDim2.new
            local Create = v516.Create
            local v522 = new(0.5, -(v170 + 6) / 2, 0, (not value4_4 and 30 or 12) - 3)

            Create(v516, v517, tweenInfo, {
				Size = uDim2,
				Position = v522
			}):Play()
            task.wait(1)

            local v523 = value3
            local v524 = ImageLabel
            local tweenInfo2 = TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
            local uDim2_2 = UDim2.new(0, v170, 0, v170)
            local Create2 = v523.Create
            local uDim2_3 = UDim2.new(0.5, -v170 / 2, 0, not value4_4 and 30 or 12)

            Create2(v523, v524, tweenInfo2, {
				Size = uDim2_2,
				Position = uDim2_3
			}):Play()
            task.wait(1)
        end
    end)
    local v174 = not value4_4 and 125 or 75
    local TextLabel = Instance.new("TextLabel")
    TextLabel.Size = UDim2.new(1, -20, 0, not value4_4 and 32 or 18)
    TextLabel.Position = UDim2.new(0, 10, 0, v174)
    TextLabel.BackgroundTransparency = 1
    TextLabel.Text = "VORTEX HUB"
    TextLabel.TextColor3 = Color3.fromRGB(0, 200, 255)
    TextLabel.TextSize = not value4_4 and 24 or 14
    TextLabel.Font = Enum.Font.GothamBlack
    TextLabel.ZIndex = 6
    TextLabel.Parent = Frame3
    local v176 = not value4_4 and 160 or 95
    local TextLabel2 = Instance.new("TextLabel")
    TextLabel2.Size = UDim2.new(1, -20, 0, not value4_4 and 18 or 12)
    TextLabel2.Position = UDim2.new(0, 10, 0, v176)
    TextLabel2.BackgroundTransparency = 1
    TextLabel2.Text = "by Proscripter  •  Evidence Tracker v3.0"
    TextLabel2.TextColor3 = Color3.fromRGB(150, 180, 220)
    TextLabel2.TextSize = not value4_4 and 13 or 9
    TextLabel2.Font = Enum.Font.Gotham
    TextLabel2.ZIndex = 6
    TextLabel2.Parent = Frame3
    local _Instance = Instance
    local v179 = not value4_4 and 195 or 115
    local v180 = _Instance.new("TextLabel")
    v180.Size = UDim2.new(1, -20, 0, not value4_4 and 18 or 12)
    v180.Position = UDim2.new(0, 10, 0, v179)
    v180.BackgroundTransparency = 1
    v180.Text = "Loading 0%"
    v180.TextColor3 = Color3.fromRGB(200, 220, 255)
    v180.TextSize = not value4_4 and 12 or 9
    v180.Font = Enum.Font.GothamBold
    v180.TextXAlignment = Enum.TextXAlignment.Left
    v180.ZIndex = 6
    v180.Parent = Frame3
    local v181 = not value4_4 and 220 or 132
    local _Instance2 = Instance
    local v183 = not value4_4 and 10 or 5
    local v184 = _Instance2.new("Frame")
    v184.Size = UDim2.new(1, -20, 0, v183)
    v184.Position = UDim2.new(0, 10, 0, v181)
    v184.BackgroundColor3 = Color3.fromRGB(20, 30, 50)
    v184.BorderSizePixel = 0
    v184.ZIndex = 6
    v184.Parent = Frame3
    local UICorner3 = Instance.new("UICorner")
    UICorner3.CornerRadius = UDim.new(1, 0)
    UICorner3.Parent = v184
    local Frame4 = Instance.new("Frame")
    Frame4.Size = UDim2.new(0, 0, 1, 0)
    Frame4.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
    Frame4.BorderSizePixel = 0
    Frame4.ZIndex = 7
    Frame4.Parent = v184
    local UICorner4 = Instance.new("UICorner")
    UICorner4.CornerRadius = UDim.new(1, 0)
    UICorner4.Parent = Frame4
    local Frame5 = Instance.new("Frame")
    Frame5.Size = UDim2.new(0, 0, 1, 0)
    Frame5.BackgroundColor3 = Color3.fromRGB(150, 220, 255)
    Frame5.BackgroundTransparency = 0.5
    Frame5.BorderSizePixel = 0
    Frame5.ZIndex = 6
    Frame5.Parent = v184
    local UICorner5 = Instance.new("UICorner")
    UICorner5.CornerRadius = UDim.new(1, 0)
    UICorner5.Parent = Frame5
    local v190 = not value4_4 and 240 or 143
    local TextLabel3 = Instance.new("TextLabel")
    TextLabel3.Size = UDim2.new(1, -20, 0, not value4_4 and 16 or 10)
    TextLabel3.Position = UDim2.new(0, 10, 0, v190)
    TextLabel3.BackgroundTransparency = 1
    TextLabel3.Text = "Initializing..."
    TextLabel3.TextColor3 = Color3.fromRGB(120, 150, 200)
    TextLabel3.TextSize = not value4_4 and 11 or 8
    TextLabel3.Font = Enum.Font.Gotham
    TextLabel3.TextXAlignment = Enum.TextXAlignment.Left
    TextLabel3.TextTruncate = Enum.TextTruncate.AtEnd
    TextLabel3.ZIndex = 6
    TextLabel3.Parent = Frame3
    local v192 = not value4_4 and 285 or 170
    local TextLabel4 = Instance.new("TextLabel")
    TextLabel4.Size = UDim2.new(1, -40, 0, not value4_4 and 14 or 10)
    TextLabel4.Position = UDim2.new(0, 10, 0, v192)
    TextLabel4.BackgroundTransparency = 1
    TextLabel4.Text = "© Proscripter  •  Vortex Hub"
    TextLabel4.TextColor3 = Color3.fromRGB(80, 100, 140)
    TextLabel4.TextSize = not value4_4 and 10 or 7
    TextLabel4.Font = Enum.Font.Gotham
    TextLabel4.ZIndex = 6
    TextLabel4.Parent = Frame3
    local v194 = not value4_4 and 24 or 14
    local Frame6 = Instance.new("Frame")
    Frame6.Size = UDim2.new(0, v194, 0, v194)
    Frame6.Position = UDim2.new(1, -v194 - 8, 0, v192 - 2)
    Frame6.BackgroundTransparency = 1
    Frame6.ZIndex = 6
    Frame6.Parent = Frame3
    local UICorner6 = Instance.new("UICorner")
    UICorner6.CornerRadius = UDim.new(1, 0)
    UICorner6.Parent = Frame6
    local UIStroke3 = Instance.new("UIStroke")
    UIStroke3.Color = Color3.fromRGB(0, 170, 255)
    UIStroke3.Thickness = 2
    UIStroke3.Parent = Frame6
    task.spawn(function()
        while true do
            local v529 = Frame6

            if v529 then
                v529 = Frame6.Parent
            end

            if not v529 then
                break
            end

            Frame6.Rotation = Frame6.Rotation + 8
            task.wait(0.02)
        end
    end)
    local t3 = {
		{
			text = "Initializing systems...",
			weight = 5
		},
		{
			text = "Loading anti-detection...",
			weight = 10
		},
		{
			text = "Connecting to game services...",
			weight = 8
		},
		{
			text = "Loading ghost database...",
			weight = 12
		},
		{
			text = "Initializing fingerprint scanner...",
			weight = 10
		},
		{
			text = "Setting up fullbright engine...",
			weight = 8
		},
		{
			text = "Loading antilag optimizer...",
			weight = 10
		},
		{
			text = "Initializing ESP systems...",
			weight = 12
		},
		{
			text = "Loading UI components...",
			weight = 15
		},
		{
			text = "Finalizing setup...",
			weight = 10
		}
	}
    local n1 = 0
    for v202, v203 in ipairs(t3) do

        n1 += v203.weight
    end
    local n2 = 0
    for _, v in ipairs(t3) do
        TextLabel3.Text = v.text

        local v207 = n2 + v.weight / n1
        local v208 = v.weight * 0.04

        value3:Create(Frame4, TweenInfo.new(v208, Enum.EasingStyle.Quart), {
			Size = UDim2.new(v207, 0, 1, 0)
		}):Play()
        value3:Create(Frame5, TweenInfo.new(v208, Enum.EasingStyle.Quart), {
			Size = UDim2.new(v207, 0, 1, 0)
		}):Play()
        task.spawn(function()
            for i = math.floor(n2 * 100), math.floor(v207 * 100) do
                v180.Text = "Loading " .. i .. "%"
                task.wait(v208 / (v207 * 100 - n2 * 100 + 1))
            end
        end)
        n2 = v207
        task.wait(v.weight * 0.04 + 0.15)
    end
    v180.Text = "Loading 100%"
    TextLabel3.Text = "Complete!"
    task.wait(0.5)
    value3:Create(Frame3, TweenInfo.new(0.5, Enum.EasingStyle.Quart), {
		BackgroundTransparency = 1
	}):Play()
    value3:Create(Frame, TweenInfo.new(0.8, Enum.EasingStyle.Quart), {
		BackgroundTransparency = 1
	}):Play()
    task.wait(1)
    ScreenGui:Destroy()
end
local u19 = false
function t1.value10()
    local ScreenGui = Instance.new("ScreenGui")

    ScreenGui.Name = "VH_Warning"
    ScreenGui.IgnoreGuiInset = true
    ScreenGui.DisplayOrder = 9998
    ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    ScreenGui.Parent = value4_2.PlayerGui

    local Frame = Instance.new("Frame")

    Frame.Size = UDim2.new(1, 0, 1, 0)
    Frame.BackgroundColor3 = Color3.fromRGB(5, 8, 18)
    Frame.BorderSizePixel = 0
    Frame.ZIndex = 1
    Frame.Parent = ScreenGui

    local v211 = value4_4 and 45 or 100
    local v212 = not value4_4 and 80 or 25
    local TextLabel = Instance.new("TextLabel")

    TextLabel.Size = UDim2.new(0, v211, 0, v211)
    TextLabel.Position = UDim2.new(0.5, -v211 / 2, 0, v212)
    TextLabel.BackgroundTransparency = 1
    TextLabel.Text = "⚠\239\184\143"
    TextLabel.TextSize = not value4_4 and 80 or 38
    TextLabel.Font = Enum.Font.GothamBlack
    TextLabel.ZIndex = 3
    TextLabel.Parent = Frame
    task.spawn(function()
        while true do
            local v531 = TextLabel

            if v531 then
                v531 = TextLabel.Parent
            end

            if not v531 then
                break
            end

            local v532 = value3
            local v533 = TextLabel
            local tweenInfo = TweenInfo.new(0.6, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
            local uDim2 = UDim2.new(0, v211 + 6, 0, v211 + 6)
            local new = UDim2.new
            local Create = v532.Create
            local v538 = new(0.5, -(v211 + 6) / 2, 0, v212 - 3)

            Create(v532, v533, tweenInfo, {
				Size = uDim2,
				Position = v538
			}):Play()
            task.wait(0.6)

            local v539 = value3
            local v540 = TextLabel
            local tweenInfo3 = TweenInfo.new(0.6, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
            local Create3 = v539.Create
            local uDim2_4 = UDim2.new(0, v211, 0, v211)
            local uDim2_5 = UDim2.new(0.5, -v211 / 2, 0, v212)

            Create3(v539, v540, tweenInfo3, {
				Size = uDim2_4,
				Position = uDim2_5
			}):Play()
            task.wait(0.6)
        end
    end)

    local v214 = not value4_4 and 200 or 78
    local _Instance = Instance
    local v216 = not value4_4 and 22 or 14
    local v217 = _Instance.new("TextLabel")

    v217.Size = UDim2.new(1, 0, 0, v216 + 6)
    v217.Position = UDim2.new(0, 0, 0, v214)
    v217.BackgroundTransparency = 1
    v217.Text = "⚠\239\184\143  WARNING  ⚠\239\184\143"
    v217.TextColor3 = Color3.fromRGB(255, 80, 80)
    v217.TextSize = v216
    v217.Font = Enum.Font.GothamBlack
    v217.ZIndex = 3
    v217.Parent = Frame

    local v218 = value4_4

    if v218 then
        v218 = value4_5.X - 20
    end

    local v219 = v218 or 520
    local v220 = not value4_4 and 280 or 220
    local v221 = not value4_4 and 260 or 105
    local Frame7 = Instance.new("Frame")

    Frame7.Size = UDim2.new(0, v219, 0, v220)
    Frame7.Position = UDim2.new(0.5, -v219 / 2, 0, v221)
    Frame7.BackgroundColor3 = Color3.fromRGB(15, 18, 30)
    Frame7.BorderSizePixel = 0
    Frame7.ZIndex = 3
    Frame7.Parent = Frame

    local UICorner = Instance.new("UICorner")

    UICorner.CornerRadius = UDim.new(0, 12)
    UICorner.Parent = Frame7

    local UIStroke = Instance.new("UIStroke")

    UIStroke.Color = Color3.fromRGB(255, 80, 80)
    UIStroke.Thickness = 1.5
    UIStroke.Transparency = 0.4
    UIStroke.Parent = Frame7

    local v225 = not value4_4 and 12 or 9
    local TextLabel5 = Instance.new("TextLabel")

    TextLabel5.Size = UDim2.new(1, not value4_4 and -30 or -16, 1, -16)
    TextLabel5.Position = UDim2.new(0, not value4_4 and 15 or 8, 0, 8)
    TextLabel5.BackgroundTransparency = 1

    if value4_4 then
        TextLabel5.Text = [[🔒 This script is KEYLESS - do NOT sell it!

⚠️ This script is NOT my fault if you get BANNED.
   Use at your OWN RISK. By using this script, you
   accept full responsibility for consequences.

🛡️ Has STRONG BYPASS but please:
   • Do NOT use brutal features
   • Brutal usage can patch features

💡 Tips: Don't brag, use ESP subtly,
   take breaks, report bugs.

👤 Developer: Proscripter
📅 v3.0  •  Vortex Hub
]]
    else
        TextLabel5.Text = [[🔒 This script is KEYLESS - do NOT sell or resell it!

⚠️ This script is NOT my fault if you get BANNED.
   Use at your OWN RISK. By using this script, you
   accept full responsibility for any consequences.

🛡️ This script includes a STRONG BYPASS but please:
   • Do NOT use brutal/obvious features
   • Brutal usage can patch other features
   • Use features moderately and smartly

💡 Tips for safer use:
   • Don't brag about using scripts
   • Use ESP subtly, not 24/7
   • Take breaks between games
   • Report bugs to developer

👤 Developer: Proscripter
🎨 Vortex Hub UI
📅 Script Version: v3.0
]]
    end

    TextLabel5.TextColor3 = Color3.fromRGB(220, 230, 245)
    TextLabel5.TextSize = v225
    TextLabel5.Font = Enum.Font.Gotham
    TextLabel5.TextXAlignment = Enum.TextXAlignment.Left
    TextLabel5.TextYAlignment = Enum.TextYAlignment.Top
    TextLabel5.TextWrapped = true
    TextLabel5.ZIndex = 4
    TextLabel5.Parent = Frame7

    local v227 = v221 + v220 + 8
    local v228 = not value4_4 and 46 or 38
    local v229 = not value4_4 and 20 or 8
    local v230 = value4_4 and (v219 - v229) / 2 or 190
    local TextButton = Instance.new("TextButton")

    TextButton.Size = UDim2.new(0, v230, 0, v228)
    TextButton.Position = UDim2.new(0.5, -v230 - v229 / 2, 0, v227)
    TextButton.BackgroundColor3 = Color3.fromRGB(0, 180, 100)
    TextButton.BorderSizePixel = 0
    TextButton.Text = "✅ I ACCEPT"
    TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    TextButton.TextSize = not value4_4 and 14 or 11
    TextButton.Font = Enum.Font.GothamBlack
    TextButton.ZIndex = 5
    TextButton.Parent = Frame

    local UICorner7 = Instance.new("UICorner")

    UICorner7.CornerRadius = UDim.new(0, 10)
    UICorner7.Parent = TextButton

    local UIStroke4 = Instance.new("UIStroke")

    UIStroke4.Color = Color3.fromRGB(0, 220, 130)
    UIStroke4.Thickness = 1.5
    UIStroke4.Parent = TextButton

    local TextButton2 = Instance.new("TextButton")

    TextButton2.Size = UDim2.new(0, v230, 0, v228)
    TextButton2.Position = UDim2.new(0.5, v229 / 2, 0, v227)
    TextButton2.BackgroundColor3 = Color3.fromRGB(180, 50, 50)
    TextButton2.BorderSizePixel = 0
    TextButton2.Text = "❌ DECLINE"
    TextButton2.TextColor3 = Color3.fromRGB(255, 255, 255)
    TextButton2.TextSize = not value4_4 and 14 or 11
    TextButton2.Font = Enum.Font.GothamBlack
    TextButton2.ZIndex = 5
    TextButton2.Parent = Frame

    local UICorner8 = Instance.new("UICorner")

    UICorner8.CornerRadius = UDim.new(0, 10)
    UICorner8.Parent = TextButton2

    local UIStroke5 = Instance.new("UIStroke")

    UIStroke5.Color = Color3.fromRGB(255, 80, 80)
    UIStroke5.Thickness = 1.5
    UIStroke5.Parent = TextButton2
    TextButton.MouseEnter:Connect(function()
        value3:Create(TextButton, TweenInfo.new(0.2), {
			Size = UDim2.new(0, v230 + 3, 0, v228 + 2)
		}):Play()
    end)
    TextButton.MouseLeave:Connect(function()
        value3:Create(TextButton, TweenInfo.new(0.2), {
			Size = UDim2.new(0, v230, 0, v228)
		}):Play()
    end)
    TextButton2.MouseEnter:Connect(function()
        value3:Create(TextButton2, TweenInfo.new(0.2), {
			Size = UDim2.new(0, v230 + 3, 0, v228 + 2)
		}):Play()
    end)
    TextButton2.MouseLeave:Connect(function()
        value3:Create(TextButton2, TweenInfo.new(0.2), {
			Size = UDim2.new(0, v230, 0, v228)
		}):Play()
    end)
    TextButton.MouseButton1Click:Connect(function()
        if u19 then
            return
        end

        u19 = true
        value3:Create(Frame, TweenInfo.new(0.2, Enum.EasingStyle.Quart), {
			BackgroundTransparency = 1
		}):Play()
        task.wait(0.2)
        ScreenGui:Destroy()
    end)
    TextButton2.MouseButton1Click:Connect(function()
        value4_2:Kick("You declined the warning. Script closed safely.")
    end)

    while not u19 do
        task.wait(0.1)
    end
end
t1.value8()
task.wait(0.3)
t1.value10()
task.wait(0.3)
t1.value11 = {}
t1.value9 = "Originals"
t1.value11[t1.value9] = {}
function t1.value9(p6, p7, p8, p9)
    local v241 = not p7

    if not v241 then
        v241 = not p7[p8]
    end

    if v241 then
        return
    end

    if not p6.Originals[p7] then
        p6.Originals[p7] = {}
    end

    if not p6.Originals[p7][p8] then
        p6.Originals[p7][p8] = p7[p8]
    end

    p7[p8] = p9
end
t1.value11.HookFunction = t1.value9
function t1.value9(_, _)
    pcall(function()
        local v545 = getrawmetatable(game) or getmetatable(game)

        if v545 and not v545.__namecall_hook then
            local __namecall = v545.__namecall

            v545.__namecall = newcclosure(function(p12, ...)
                local v581 = getnamecallmethod()

                if v581 == "FireServer" or v581 == "InvokeServer" then
                    for _, v in pairs({ ... }) do
                        local v584 = type(v) == "string"

                        if v584 then
                            v584 = string.find(string.lower(v), "anticheat")

                            if not v584 then
                                v584 = string.find(string.lower(v), "detect")

                                if not v584 then
                                    v584 = string.find(string.lower(v), "report")

                                    if not v584 then
                                        v584 = string.find(string.lower(v), "kick")

                                        if not v584 then
                                            v584 = string.find(string.lower(v), "ban")
                                        end
                                    end
                                end
                            end
                        end

                        if v584 then
                            return nil
                        end
                    end
                end

                return __namecall(p12, ...)
            end)
            v545.__namecall_hook = true
        end
    end)
    pcall(function()
        if hookmetamethod then
            local u547
            u547 = hookmetamethod(game, "__index", newcclosure(function(p13, p14)
                local v587 = tostring(p13) == "Player"

                if v587 then
                    v587 = tostring(p14) == "AccountAge"
                end

                if v587 then
                    return math.random(50, 1000)
                end

                if tostring(p14) == "Kick" then
                    return function()
                    end
                end

                return u547(p13, p14)
            end))
        end
    end)
end
t1.value11.Protect = t1.value9
t1.value11:Protect("main")
local t4 = {}
function t1.value9(_)
    for _, descendant in pairs(workspace:GetDescendants()) do
        local v247 = descendant

        pcall(function()
            local v548 = v247:IsA("ParticleEmitter")

            if not v548 then
                v548 = v247:IsA("Trail")

                if not v548 then
                    v548 = v247:IsA("Beam")
                end
            end

            if v548 then
                if not v247:GetAttribute("_KeepAntilag") then
                    v247.Enabled = false

                    return
                end
            else
                if v247:IsA("PostEffect") then
                    v247.Enabled = false

                    return
                end

                if v247:IsA("BasePart") then
                    local v549 = v247.Material == Enum.Material.Plastic

                    if v549 then
                        v549 = v247.Size.Magnitude > 100
                    end

                    if v549 then
                        v247.CastShadow = false
                    end
                end
            end
        end)
    end

    settings().Rendering.QualityLevel = Enum.QualityLevel.Level01

    for _, descendant in pairs(workspace:GetDescendants()) do
        local v250 = descendant

        pcall(function()
            local v550 = v250:IsA("Decal")

            if not v550 then
                v550 = v250:IsA("Texture")
            end

            if v550 then
                local v551 = v250.Name ~= "Handprint1"

                if v551 then
                    v551 = v250.Name ~= "Handprint2"
                end

                if v551 then
                    v250.Transparency = 1
                end
            end
        end)
    end
end
t4.Optimize = t1.value9
local color3 = Color3.fromRGB(255, 50, 50)
t1.value9 = {
	squares = {},
	activeSquare = nil,
	squareLifetime = 6.4,
	showSquare = false,
	squareColor = color3,
	espConnection = nil
}
local value9 = t1.value9
function t1.value9(_)
    if not value9.showSquare then
        return
    end
    for v254, v255 in pairs(value9.squares) do

        local v256 = v255

        pcall(function()
            v256:Destroy()
        end)
    end
    value9.squares = {}
    for _, descendant in pairs(workspace:GetDescendants()) do
        local v259 = descendant:IsA("BasePart")

        if v259 then
            v259 = descendant.Name == "Handprint1"

            if not v259 then
                v259 = descendant.Name == "Handprint2"

                if not v259 then
                    v259 = descendant.Name == "Footprint"

                    if not v259 then
                        v259 = descendant.Name == "Footprint1"
                    end
                end
            end
        end

        if v259 then
            local Part = Instance.new("Part")

            Part.Name = "VortexFingerSquare"
            Part.Anchored = true
            Part.CanCollide = false
            Part.Material = Enum.Material.Neon
            Part.Color = value9.squareColor
            Part.Size = Vector3.new(0.15, descendant.Size.Y + 0.3, descendant.Size.X + 0.3)
            Part.CFrame = descendant.CFrame
            Part.Transparency = 0.4
            Part.Parent = workspace

            local BillboardGui = Instance.new("BillboardGui")

            BillboardGui.Adornee = Part
            BillboardGui.Size = UDim2.new(0, 200, 0, 60)
            BillboardGui.StudsOffset = Vector3.new(0, 2, 0)
            BillboardGui.AlwaysOnTop = true
            BillboardGui.Parent = Part

            local TextLabel = Instance.new("TextLabel")

            TextLabel.Size = UDim2.new(1, 0, 1, 0)
            TextLabel.BackgroundTransparency = 1
            TextLabel.Text = "👆 FINGERPRINT\n" .. string.format("%.1fs", value9.squareLifetime)
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
            TextLabel.TextStrokeTransparency = 0
            TextLabel.TextSize = 14
            TextLabel.Font = Enum.Font.GothamBold
            TextLabel.Parent = BillboardGui

            for _, v in ipairs({
				Vector3.new(-(descendant.Size.X / 2 + 0.1), 0, -(descendant.Size.Z / 2 + 0.1)),
				Vector3.new(descendant.Size.X / 2 + 0.1, 0, -(descendant.Size.Z / 2 + 0.1)),
				Vector3.new(-(descendant.Size.X / 2 + 0.1), 0, descendant.Size.Z / 2 + 0.1),
				Vector3.new(descendant.Size.X / 2 + 0.1, 0, descendant.Size.Z / 2 + 0.1)
			}) do
                local Part2 = Instance.new("Part")

                Part2.Name = "VortexFingerMarker"
                Part2.Anchored = true
                Part2.CanCollide = false
                Part2.Material = Enum.Material.Neon
                Part2.Color = Color3.fromRGB(255, 255, 0)
                Part2.Size = Vector3.new(0.2, 0.2, 0.2)
                Part2.CFrame = descendant.CFrame * CFrame.new(v)
                Part2.Parent = Part
            end

            table.insert(value9.squares, Part)
            task.spawn(function()
                local timestamp = tick()

                while true do
                    local v553 = Part

                    if v553 then
                        v553 = Part.Parent

                        if v553 then
                            v553 = tick() - timestamp < value9.squareLifetime
                        end
                    end

                    if not v553 then
                        break
                    end

                    local timestamp2 = tick()
                    local v555 = value9
                    local v556 = timestamp2 - timestamp
                    local v557 = v555.squareLifetime - v556

                    TextLabel.Text = string.format("👆 FINGERPRINT\n%.1fs", v557)

                    if v557 < 2 then
                        Part.Transparency = math.floor(tick() * 4) % 2 ~= 0 and 0.6 or 0.2
                    end

                    task.wait(0.1)
                end

                local v558 = Part

                if v558 then
                    v558 = Part.Parent
                end

                if v558 then
                    Part:Destroy()
                end
            end)
        end
    end
end
value9.CreateSquare = t1.value9
function t1.value9(_, p18)
    value9.showSquare = p18

    if not p18 then
        for _, v in pairs(value9.squares) do
            local v270 = v

            pcall(function()
                v270:Destroy()
            end)
        end

        value9.squares = {}
    end
end
value9.Toggle = t1.value9
t1.value13 = {
	"EMF Level 5",
	"Ghost Writing",
	"Wither"
}
local t5 = {
	Name = "Aswang",
	Evidence = t1.value13,
	Description = "Feeds on human flesh. Responds aggressively to talking."
}
local t6 = {
	Name = "Banshee",
	Evidence = {
		"Freezing Temps",
		"Ghost Orb",
		"Fingerprints"
	},
	Description = "Targets one player at a time. Screams during hunts."
}
local t7 = {
	Name = "Demon",
	Evidence = {
		"EMF Level 5",
		"Freezing Temps",
		"Fingerprints"
	},
	Description = "Most aggressive ghost. Hunts more frequently."
}
local t8 = {
	Name = "Dullahan",
	Evidence = {
		"Freezing Temps",
		"Laser Projector",
		"Wither"
	},
	Description = "Headless rider. Moves fast in open areas."
}
t1.value13 = {
	Name = "Dybbuk",
	Evidence = {
		"Freezing Temps",
		"Fingerprints",
		"Wither"
	},
	Description = "Possesses victims. Drops sanity quickly."
}
local t9 = {
	Name = "Entity",
	Evidence = {
		"Fingerprints",
		"Laser Projector",
		"Spirit Box"
	},
	Description = "Ancient being. Rarely leaves the ghost room."
}
local t10 = {
	Name = "Ghoul",
	Evidence = {
		"Freezing Temps",
		"Ghost Orb",
		"Spirit Box"
	},
	Description = "Feeds on the dead. Active near corpses."
}
t1.value12 = {
	"Fingerprints",
	"Spirit Box",
	"Wither"
}
local t11 = {
	Name = "Keres",
	Evidence = t1.value12,
	Description = "Bringer of death. Hunts in groups."
}
local t12 = {
	Name = "Leviathan",
	Evidence = {
		"Ghost Writing",
		"Fingerprints",
		"Ghost Orb"
	},
	Description = "Sea monster. Extremely fast when angry."
}
local t13 = {
	Name = "Nightmare",
	Evidence = {
		"EMF Level 5",
		"Ghost Orb",
		"Spirit Box"
	},
	Description = "Haunts dreams. Lowers sanity in sleep."
}
local t14 = {
	Name = "Oni",
	Evidence = {
		"Freezing Temps",
		"Laser Projector",
		"Spirit Box"
	},
	Description = "Active when players are present. Fast mover."
}
t1.value12 = {
	Name = "Phantom",
	Evidence = {
		"EMF Level 5",
		"Fingerprints",
		"Ghost Orb"
	},
	Description = "Looking at it lowers sanity fast."
}
local t15 = {
	Name = "Ravager",
	Evidence = {
		"EMF Level 5",
		"Ghost Writing",
		"Spirit Box"
	},
	Description = "Destroys objects quickly. Very aggressive."
}
local t16 = {
	Name = "Revenant",
	Evidence = {
		"EMF Level 5",
		"Freezing Temps",
		"Ghost Writing"
	},
	Description = "Very slow normally, very fast when it sees you."
}
t1.value14 = {
	"EMF Level 5",
	"Ghost Writing",
	"Laser Projector"
}
local t17 = {
	Name = "Shadow",
	Evidence = t1.value14,
	Description = "Appears as a dark figure. Hard to see."
}
local t18 = {
	Name = "Siren",
	Evidence = {
		"EMF Level 5",
		"Spirit Box",
		"Wither"
	},
	Description = "Lures players with singing. Paralyzes victims."
}
local t19 = {
	Name = "Skinwalker",
	Evidence = {
		"Freezing Temps",
		"Ghost Writing",
		"Spirit Box"
	},
	Description = "Shapeshifter. Appears as other players."
}
local t20 = {
	Name = "Specter",
	Evidence = {
		"EMF Level 5",
		"Freezing Temps",
		"Laser Projector"
	},
	Description = "Floating spirit. Teleports through walls."
}
t1.value14 = {
	Name = "Spirit",
	Evidence = {
		"Ghost Writing",
		"Fingerprints",
		"Spirit Box"
	},
	Description = "Most common ghost. Repelled longer by smudge sticks."
}
local t21 = {
	Name = "The Wisp",
	Evidence = {
		"Laser Projector",
		"Ghost Orb",
		"Wither"
	},
	Description = "Mysterious light. Appears in dark areas."
}
local t22 = {
	Name = "Umbra",
	Evidence = {
		"Fingerprints",
		"Ghost Orb",
		"Laser Projector"
	},
	Description = "Shadow demon. Lurks in darkness."
}
local t23 = {
	Name = "Vesper",
	Evidence = {
		"Ghost Writing",
		"Fingerprints",
		"Wither"
	},
	Description = "Evening spirit. Active at night."
}
local t24 = {
	Name = "Vex",
	Evidence = {
		"Freezing Temps",
		"Ghost Orb",
		"Wither"
	},
	Description = "Annoying spirit. Constantly interacts with objects."
}
local t25 = {
	Name = "Wendigo",
	Evidence = {
		"Ghost Writing",
		"Ghost Orb",
		"Laser Projector"
	},
	Description = "Cannibal spirit. Hunts in forests."
}
local t26 = {
	t5,
	t6,
	t7,
	t8,
	t1.value13,
	t9,
	t10,
	t11,
	t12,
	t13,
	t14,
	t1.value12,
	t15,
	t16,
	t17,
	t18,
	t19,
	t20,
	t1.value14,
	t21,
	t22,
	t23,
	t24,
	t25,
	{
		Name = "Wraith",
		Evidence = {
			"EMF Level 5",
			"Laser Projector",
			"Spirit Box"
		},
		Description = "Reaper spirit. Teleports to players."
	}
}
t1.value9 = {
	Handprints = "Fingerprints",
	GhostOrb = "Ghost Orb",
	SpiritBox = "Spirit Box",
	EMF = "EMF Level 5",
	GhostWriting = "Ghost Writing",
	LaserProjector = "Laser Projector",
	Wither = "Wither",
	Temperature = "Freezing Temps"
}
local value9_2 = t1.value9
t1.value12 = {
	Handprints = false,
	GhostOrb = false,
	SpiritBox = false,
	EMF = false,
	GhostWriting = false,
	LaserProjector = false,
	Wither = false,
	Temperature = false
}
t1.value9 = {
	toggles = {},
	sliders = {},
	dropdowns = {},
	infStamina = false,
	evidence = t1.value12,
	lowestTemp = 100,
	lowestTempRoom = nil,
	highestEMF = 1,
	ghostEspOn = false,
	escapeHunt = false,
	autoSpiritBox = false,
	itemEspOn = false,
	evidenceEspOn = false,
	playersEspOn = false,
	fullbright = false,
	lightToggle = false,
	checkSpeed = 1,
	walkSpeed = 16,
	jumpPower = 100,
	antilagOn = false,
	fingerprintSquareOn = false,
	fingerprintLifetime = 6.4,
	speedHackOn = false,
	speedHackValue = 50,
	antiDetectOn = true,
	itemEspList = {},
	evidenceEspList = {},
	connections = {},
	mainFrame = nil,
	_energyScroll = nil,
	_refreshGhostPanel = nil
}
local value9_3 = t1.value9
local Ghost
local u48
pcall(function()
    Ghost = workspace:WaitForChild("Ghost", 15)

    if Ghost then
        Ghost:FindFirstChildWhichIsA("BasePart")
    end

    local Map = workspace:FindFirstChild("Map")

    if Map then
        Map = workspace.Map:FindFirstChild("Rooms")
    end

    u48 = Map
end)
local value5Ambient = value5.Ambient
local OutdoorAmbient = value5.OutdoorAmbient
local value5Brightness = value5.Brightness
local GlobalShadows = value5.GlobalShadows
local FogEnd = value5.FogEnd
local t27 = {
	Ambient = value5Ambient,
	OutdoorAmbient = OutdoorAmbient,
	Brightness = value5Brightness,
	GlobalShadows = GlobalShadows,
	FogEnd = FogEnd
}
local function v55(p19)
    local num
    local v288 = false
    for _, child in ipairs(value4_2.PlayerGui.Hotbar.Slots:GetChildren()) do
        local v291 = child:IsA("Frame")

        if v291 then
            v291 = string.find(string.lower(child.Name), "invslot")
        end

        if v291 and p19 == child.ItemName.Text then
            v288 = true
            num = tonumber(child.Name:match("%d+"))
        end
    end

    return v288, num
end
local function v56(p20)
    for _, child in pairs(workspace.Items:GetChildren()) do
        local v295 = child:IsA("Model")

        if v295 then
            v295 = p20 == child:GetAttribute("ItemName")
        end

        if v295 then
            return true, child
        end
    end

    return false, nil
end
local function v57(p21)
    value4:WaitForChild("Events"):WaitForChild("RequestItemPickup"):FireServer(p21)
end
local function v58(p22)
    value4:WaitForChild("Events"):WaitForChild("RequestItemDrop"):FireServer("InvSlot" .. tostring(p22))
end
local function v59()
    local Character = value4_2.Character

    if Character then
        local GetChildren = Character.GetChildren

        for _, v in pairs(GetChildren(Character)) do
            local v303 = v:IsA("Model")

            if not v303 then
                v303 = tonumber(v.Name)
            end

            if v303 and v:GetAttribute("Enabled") ~= true and v:FindFirstChild("Handle") then
                value4:WaitForChild("Events"):WaitForChild("ToggleItemState"):FireServer(v)

                return
            end
        end
    end
end
local function v60()
    pcall(function()
        local Union = workspace:WaitForChild("Map"):WaitForChild("Rooms"):WaitForChild("Base Camp"):WaitForChild("Pegboard"):FindFirstChild("Union")
        local Character = value4_2.Character

        if not Character then
            Character = value4_2.CharacterAdded:Wait()
        end

        local v561 = Union

        if Union then
            v561 = Character

            if Character then
                v561 = Character:FindFirstChild("HumanoidRootPart")
            end
        end

        if v561 then
            Character.HumanoidRootPart.CFrame = Union.CFrame + Vector3.new(0, 3, 0)
        end
    end)
end
local function v61()
    local v309
    local n3 = 100
    if not u48 then
        return n3, v309
    end
    for _, child in ipairs(u48:GetChildren()) do
        local Temperature = child:GetAttribute("Temperature")

        if Temperature and Temperature < n3 then
            v309 = child
            n3 = Temperature
        end
    end

    return n3, v309
end
local function v62()
    for _, descendant in ipairs(workspace:GetDescendants()) do
        local v298 = descendant:IsA("BasePart")

        if v298 then
            v298 = descendant.Name == "Handprint1"

            if not v298 then
                v298 = descendant.Name == "Handprint2"

                if not v298 then
                    v298 = descendant.Name == "Footprint"

                    if not v298 then
                        v298 = descendant.Name == "Footprint1"
                    end
                end
            end
        end

        if v298 then
            return true
        end
    end

    return false
end
local function v63()
    for _, descendant in ipairs(workspace:GetDescendants()) do
        local v307 = descendant:IsA("BasePart")

        if v307 then
            v307 = descendant.Name == "GhostOrb"
        end

        if v307 then
            return true
        end
    end

    return false
end
function t1.value14()
    local n4 = 0

    for _, descendant in ipairs(workspace:GetDescendants()) do
        local v326 = descendant:IsA("Folder")

        if v326 then
            v326 = descendant.Name == "Indicators"
        end

        if v326 then
            local GetChildren = descendant.GetChildren

            for _, v in pairs(GetChildren(descendant)) do
                local v330 = v:IsA("BasePart")

                if v330 then
                    v330 = v.Material == Enum.Material.Neon
                end

                if v330 then
                    local num = tonumber(v.Name)

                    if num and n4 < num then
                        n4 = num
                    end
                end
            end
        end
    end

    return n4
end
local value14 = t1.value14
local function v65()
    for _, descendant in ipairs(workspace.Items:GetDescendants()) do
        local v334 = descendant:IsA("BasePart")

        if v334 then
            v334 = descendant.Name == "Petals"

            if v334 then
                v334 = descendant.Color == Color3.new(0, 0, 0)
            end
        end

        if v334 then
            return true
        end
    end

    return false
end
local function v66()
    for _, descendant in ipairs(workspace.Items:GetDescendants()) do
        if not descendant:IsA("Decal") then
            continue
        end

        local Model = descendant:FindFirstAncestorWhichIsA("Model")

        if Model then
            Model = Model:GetAttribute("ItemName") == "Spirit Book"

            if Model then
                Model = descendant.Texture ~= ""
            end
        end

        if Model then
            return true
        end
    end

    return false
end
local function v67()
    local ok, result = pcall(function()
        return #value4_2.PlayerGui.Subtitles.Holder.TextLabel.Text:gsub("%s+", "") >= 3
    end)

    return not not ok and (result or false)
end
local function u68()
    local t28 = {}

    for k, v in pairs(value9_3.evidence) do
        local v322 = k

        if v and value9_2[v322] then
            table.insert(t28, value9_2[v322])
        end
    end

    return t28
end
local function v69()
    local v335 = u68()
    local t29 = {}

    for _, v in ipairs(t26) do
        local n5 = 0
        for v342, v343 in ipairs(v335) do

            for _, v3 in ipairs(v.Evidence) do
                if v3 == v343 then
                    n5 += 1

                    break
                end
            end
        end
        if n5 > 0 then
            local insert = table.insert
            local v347 = #v.Evidence

            insert(t29, {
				ghost = v,
				match = n5,
				total = v347
			})
        end
    end

    table.sort(t29, function(p23, p24)
        local v564 = p23.match == p23.total

        if v564 ~= (p24.match == p24.total) then
            return v564
        end

        return p23.match > p24.match
    end)

    return t29
end
local function v70(p25)
    for _, v in pairs(p25) do
        local v274 = v

        pcall(function()
            v274:Destroy()
        end)
    end

    table.clear(p25)
end
local BillboardGui
local Highlight
local function v73()
    if not Ghost then
        return
    end

    if BillboardGui then
        BillboardGui.Enabled = not BillboardGui.Enabled

        if Highlight then
            Highlight.Enabled = BillboardGui.Enabled
        end

        return
    end

    BillboardGui = Instance.new("BillboardGui")
    BillboardGui.Enabled = true
    BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    BillboardGui.Active = true
    BillboardGui.AlwaysOnTop = true
    BillboardGui.Size = UDim2.new(0, 60, 0, 60)
    BillboardGui.LightInfluence = 0
    BillboardGui.Brightness = 1
    BillboardGui.Adornee = Ghost
    BillboardGui.Parent = game:GetService("CoreGui")

    local TextLabel = Instance.new("TextLabel")

    TextLabel.Size = UDim2.new(1, 0, 1, 0)
    TextLabel.BackgroundTransparency = 1
    TextLabel.Text = "👻 Ghost"
    TextLabel.TextColor3 = Color3.fromRGB(255, 65, 85)
    TextLabel.TextSize = 14
    TextLabel.Font = Enum.Font.GothamBold
    TextLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
    TextLabel.TextStrokeTransparency = 0
    TextLabel.ZIndex = 1
    TextLabel.Parent = BillboardGui
    Highlight = Instance.new("Highlight")
    Highlight.Parent = Ghost
    Highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
    Highlight.OutlineColor = Color3.fromRGB(255, 65, 85)
    Highlight.FillTransparency = 0.8
    Highlight.FillColor = Color3.fromRGB(255, 65, 85)
    Highlight.OutlineTransparency = 0
    Highlight.Adornee = Ghost
    value9_3.ghostEspOn = true
end
local function v74(p26)
    v70(value9_3.itemEspList)

    if not p26 then
        return
    end

    for _, descendant in pairs(workspace:GetDescendants()) do
        if descendant:IsA("Model") and descendant:GetAttribute("ItemName") then
            local BillboardGui2 = Instance.new("BillboardGui")

            BillboardGui2.Name = "VortexItemBil"
            BillboardGui2.Adornee = descendant
            BillboardGui2.Parent = descendant
            BillboardGui2.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            BillboardGui2.Active = true
            BillboardGui2.AlwaysOnTop = true
            BillboardGui2.Size = UDim2.new(0, 100, 0, 36)
            BillboardGui2.LightInfluence = 0
            BillboardGui2.Brightness = 1

            local TextLabel = Instance.new("TextLabel")

            TextLabel.Size = UDim2.new(1, 0, 1, 0)
            TextLabel.BackgroundTransparency = 1
            TextLabel.Text = descendant:GetAttribute("ItemName")
            TextLabel.TextColor3 = Color3.fromRGB(255, 220, 80)
            TextLabel.TextSize = 12
            TextLabel.Font = Enum.Font.GothamBold
            TextLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
            TextLabel.TextStrokeTransparency = 0
            TextLabel.Parent = BillboardGui2

            local Highlight2 = Instance.new("Highlight")

            Highlight2.Parent = descendant
            Highlight2.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            Highlight2.OutlineColor = Color3.fromRGB(255, 170, 0)
            Highlight2.FillTransparency = 1
            Highlight2.OutlineTransparency = 0
            Highlight2.Adornee = descendant
            table.insert(value9_3.itemEspList, BillboardGui2)
            table.insert(value9_3.itemEspList, Highlight2)
        end
    end
end
local function v75(p27)
    v70(value9_3.evidenceEspList)
    if not p27 then
        return
    end
    for v358, v359 in ipairs(workspace.Handprints:GetDescendants()) do

        if v359:IsA("BasePart") then
            local BillboardGui3 = Instance.new("BillboardGui")

            BillboardGui3.Name = "VortexHandBil"
            BillboardGui3.Parent = game:GetService("CoreGui")
            BillboardGui3.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            BillboardGui3.Active = true
            BillboardGui3.AlwaysOnTop = true
            BillboardGui3.Size = UDim2.new(1, 0, 1, 0)
            BillboardGui3.LightInfluence = 0
            BillboardGui3.Brightness = 1
            BillboardGui3.Adornee = v359

            local vector3 = Vector3.new(0, 1, 0)
            local GetDescendants = v359.GetDescendants

            BillboardGui3.StudsOffset = vector3

            for _, v in pairs(GetDescendants(v359)) do
                if v:IsA("ImageLabel") then
                    local clone = v:Clone()

                    clone.Parent = BillboardGui3
                    clone.Size = UDim2.new(1, 0, 1, 0)
                    clone.BackgroundTransparency = 1
                end
            end

            table.insert(value9_3.evidenceEspList, BillboardGui3)
        end
    end
    for _, descendant in ipairs(workspace:GetDescendants()) do
        local v368 = descendant:IsA("BasePart")

        if v368 then
            v368 = descendant.Name == "GhostOrb"
        end

        if v368 then
            descendant.Transparency = 0

            local BillboardGui4 = Instance.new("BillboardGui")

            BillboardGui4.Name = "VortexOrbBil"
            BillboardGui4.Parent = game:GetService("CoreGui")
            BillboardGui4.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            BillboardGui4.Active = true
            BillboardGui4.AlwaysOnTop = true
            BillboardGui4.Size = UDim2.new(3, 0, 3, 0)
            BillboardGui4.LightInfluence = 0
            BillboardGui4.Brightness = 1
            BillboardGui4.Adornee = descendant
            BillboardGui4.StudsOffset = Vector3.new(0, 1, 0)

            local TextLabel = Instance.new("TextLabel")

            TextLabel.Size = UDim2.new(1, 0, 1, 0)
            TextLabel.BackgroundTransparency = 1
            TextLabel.Text = "🔵 Orb"
            TextLabel.TextColor3 = Color3.fromRGB(100, 200, 255)
            TextLabel.TextSize = 12
            TextLabel.Font = Enum.Font.GothamBold
            TextLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
            TextLabel.TextStrokeTransparency = 0
            TextLabel.Parent = BillboardGui4

            local Highlight3 = Instance.new("Highlight")

            Highlight3.Parent = game:GetService("CoreGui")
            Highlight3.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            Highlight3.OutlineColor = Color3.fromRGB(100, 200, 255)
            Highlight3.FillTransparency = 0.7
            Highlight3.FillColor = Color3.fromRGB(100, 200, 255)
            Highlight3.OutlineTransparency = 0
            Highlight3.Adornee = descendant
            table.insert(value9_3.evidenceEspList, BillboardGui4)
            table.insert(value9_3.evidenceEspList, Highlight3)

            return
        end
    end
end
local function v76(p28)
    for _, player in pairs(Players:GetPlayers()) do
        if player ~= value4_2 and player.Character then
            local HumanoidRootPart = player.Character:FindFirstChild("HumanoidRootPart")

            if HumanoidRootPart then
                if p28 then
                    if not HumanoidRootPart:FindFirstChild("VortexPlrBil") then
                        local BillboardGui5 = Instance.new("BillboardGui")

                        BillboardGui5.Name = "VortexPlrBil"
                        BillboardGui5.Parent = HumanoidRootPart
                        BillboardGui5.Adornee = HumanoidRootPart
                        BillboardGui5.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                        BillboardGui5.Active = true
                        BillboardGui5.AlwaysOnTop = true
                        BillboardGui5.Size = UDim2.new(0, 100, 0, 36)
                        BillboardGui5.LightInfluence = 0
                        BillboardGui5.Brightness = 1

                        local TextLabel = Instance.new("TextLabel")

                        TextLabel.Size = UDim2.new(1, 0, 1, 0)
                        TextLabel.BackgroundTransparency = 1
                        TextLabel.Text = player.DisplayName
                        TextLabel.TextColor3 = Color3.fromRGB(0, 170, 255)
                        TextLabel.TextSize = 13
                        TextLabel.Font = Enum.Font.GothamBold
                        TextLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
                        TextLabel.TextStrokeTransparency = 0
                        TextLabel.Parent = BillboardGui5

                        local Highlight4 = Instance.new("Highlight")

                        Highlight4.Name = "VortexPlrHL"
                        Highlight4.Parent = HumanoidRootPart
                        Highlight4.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
                        Highlight4.OutlineColor = Color3.fromRGB(0, 170, 255)
                        Highlight4.FillTransparency = 1
                        Highlight4.OutlineTransparency = 0
                        Highlight4.Adornee = player.Character
                    end
                else
                    local VortexPlrBil = HumanoidRootPart:FindFirstChild("VortexPlrBil")
                    local VortexPlrHL = HumanoidRootPart:FindFirstChild("VortexPlrHL")

                    if VortexPlrBil then
                        VortexPlrBil:Destroy()
                    end

                    if VortexPlrHL then
                        VortexPlrHL:Destroy()
                    end
                end
            end
        end
    end
end
local ok, result = pcall(function()
    return loadstring(game:HttpGet("https://raw.githubusercontent.com/deividcomsono/Obsidian/main/Library.lua"))()
end)
local v79 = not ok
if not v79 then
    v79 = not result
end
if v79 then
    warn("[Vortex Hub] Obsidian failed to load - " .. tostring(result))

    return
end
local u80 = result
function t1.value15()
    return loadstring(game:HttpGet("https://raw.githubusercontent.com/deividcomsono/Obsidian/main/addons/ThemeManager.lua"))()
end
local ok2, result2 = pcall(t1.value15)
t1.value16 = ok2 and result2
function t1.value18()
    return loadstring(game:HttpGet("https://raw.githubusercontent.com/deividcomsono/Obsidian/main/addons/SaveManager.lua"))()
end
local v83 = t1.value16 or nil
local ok3, result3 = pcall(t1.value18)
t1.value16 = ok3
t1.value17 = result3
t1.value17 = t1.value16 and t1.value17 or nil
if v83 then
    v83:SetLibrary(u80)
end
if t1.value17 then
    t1.value19 = u80
    t1.value17:SetLibrary(t1.value19)
end
t1.value18 = u80
t1.value19 = t1.value18.CreateWindow
local RightShift = Enum.KeyCode.RightShift
t1.value19 = t1.value19(t1.value18, {
	Title = "Vortex Hub | Demonology",
	Footer = "by Proscripter v3.0",
	Center = true,
	AutoShow = true,
	ToggleKeybind = RightShift,
	Resizable = true,
	Icon = "rbxassetid://90145481353879"
})
local value19 = t1.value19
local v88 = value19:AddTab("Evidence", "scan")
local v89 = value19:AddTab("Combat", "crosshair")
local v90 = value19:AddTab("Visuals", "eye")
local v91 = value19:AddTab("Player", "user")
local v92 = value19:AddTab("Tools", "wrench")
local v93 = value19:AddTab("Settings", "settings")
local v94 = value19:AddTab("Credits", "star")
t1.value19 = {
	Evidence = v88,
	Combat = v89,
	Visuals = v90,
	Player = v91,
	Tools = v92,
	Settings = v93,
	Credits = v94
}
local v95 = t1.value19.Evidence:AddLeftGroupbox("Evidence Found")
local t30 = {}
t1.value20 = {
	{
		key = "Handprints",
		label = "👋 Handprints / Footprints"
	},
	{
		key = "GhostOrb",
		label = "🔵 Ghost Orb"
	},
	{
		key = "SpiritBox",
		label = "🎙\239\184\143 Spirit Box Response"
	},
	{
		key = "EMF",
		label = "📡 EMF Level 5"
	},
	{
		key = "GhostWriting",
		label = "📖 Inscription (Spirit Book)"
	},
	{
		key = "LaserProjector",
		label = "🔦 Laser Projector Silhouette"
	},
	{
		key = "Wither",
		label = "🌸 Wither (Black Petals)"
	},
	{
		key = "Temperature",
		label = "🌡\239\184\143 Freezing Temperature"
	}
}
for _, v in ipairs(t1.value20) do
    local v99 = v95:AddToggle(v.key, {
		Text = v.label,
		Default = false,
		Callback = function()
    end
	})

    if v99.OnRender then
        v99.OnRender.Active = false
        v99.OnRender.Selectable = false

        for _, descendant in ipairs(v99.OnRender:GetDescendants()) do
            local v102 = descendant:IsA("GuiButton")

            if not v102 then
                v102 = descendant:IsA("ImageButton")

                if not v102 then
                    v102 = descendant:IsA("TextButton")
                end
            end

            if v102 then
                descendant.Active = false
                descendant.Selectable = false
            end
        end
    end

    t30[v.key] = v99
end
task.spawn(function()
    while true do
        task.wait(0.3)

        local _workspace = workspace

        if _workspace then
            _workspace = game.Players.LocalPlayer
        end

        if _workspace then
            local LocalPlayer = game.Players.LocalPlayer
            local Character = LocalPlayer.Character
            local Wither = workspace:FindFirstChild("Wither")
            if not Wither then
                Wither = workspace:FindFirstChild("WitheredFlower")

                if not Wither then
                    Wither = workspace:FindFirstChild("BlackPetals")
                end
            end
            if Wither then
                value9_3.evidence.Wither = true
            end
            for v378, v379 in ipairs(workspace:GetDescendants()) do

                local v380 = v379.Name == "SpiritBook"

                if not v380 then
                    v380 = v379.Name == "GhostBook"
                end

                if v380 then
                    local IsWritten = v379:FindFirstChild("IsWritten")

                    if IsWritten then
                        IsWritten = v379.IsWritten.Value == true
                    end

                    if IsWritten then
                        value9_3.evidence.GhostWriting = true
                    else
                        local Text = v379:FindFirstChild("Text")

                        if Text then
                            Text = #v379.Text.Value > 0
                        end

                        if Text then
                            value9_3.evidence.GhostWriting = true
                        end
                    end
                end
            end
            local v383 = Character
            if Character then
                v383 = Character:FindFirstChild("ColdBreath") or Character:FindFirstChild("FreezingFog")
            end
            if v383 then
                value9_3.evidence.Temperature = true
            end
            if Character then
                local Thermometer = Character:FindFirstChild("Thermometer")

                if not Thermometer then
                    Thermometer = LocalPlayer.Backpack:FindFirstChild("Thermometer")
                end

                if Thermometer then
                    local Value = Thermometer:FindFirstChild("Value")

                    if Value then
                        Value = Thermometer.Value.Value <= 0
                    end

                    Thermometer = Value
                end

                if Thermometer then
                    value9_3.evidence.Temperature = true
                end
            end
            if Character then
                local EMFReader = Character:FindFirstChild("EMFReader")

                if not EMFReader then
                    EMFReader = LocalPlayer.Backpack:FindFirstChild("EMFReader")
                end

                if EMFReader then
                    local Level = EMFReader:FindFirstChild("Level")

                    if Level then
                        Level = EMFReader.Level.Value >= 5
                    end

                    EMFReader = Level
                end

                if EMFReader then
                    value9_3.evidence.EMF = true
                end
            end
            for v390, v391 in ipairs(workspace:GetDescendants()) do

                local v392 = v391.Name == "LaserProjector"

                if v392 then
                    v392 = v391:FindFirstChild("Detected")

                    if v392 then
                        v392 = v391.Detected.Value == true
                    end
                end

                if v392 then
                    value9_3.evidence.LaserProjector = true
                end
            end
            if Character then
                local SpiritBox = Character:FindFirstChild("SpiritBox")

                if not SpiritBox then
                    SpiritBox = LocalPlayer.Backpack:FindFirstChild("SpiritBox")
                end

                if SpiritBox then
                    local Talking = SpiritBox:FindFirstChild("Talking")

                    if Talking then
                        Talking = SpiritBox.Talking.Value == true
                    end

                    SpiritBox = Talking
                end

                if SpiritBox then
                    value9_3.evidence.SpiritBox = true
                end
            end
        end

        for k, v in pairs(t30) do
            local v397 = k
            local v398 = value9_3

            if v398 then
                v398 = value9_3.evidence

                if v398 then
                    v398 = value9_3.evidence[v397] ~= nil
                end
            end

            if v398 then
                v:SetValue(value9_3.evidence[v397])
            end
        end
    end
end)
v95:AddButton({
	Text = "🔄 Reset Evidence Log",
	Func = function()

    for v401, v402 in pairs(value9_3.evidence) do

        value9_3.evidence[v401] = false
    end
    value9_3.lowestTemp = 100
    value9_3.highestEMF = 1
    for _, v in pairs(t30) do
        v:SetValue(false)
    end
end
})
local v103 = t1.value19.Evidence:AddRightGroupbox("Readings & Ghost Info")
local v104 = v103:AddLabel("Temperature: Scanning...", false)
local v105 = v103:AddLabel("EMF Level: 0", false)
local v106 = v103:AddLabel("Ghost Room: ...", false)
local v107 = v103:AddLabel("Difficulty: ...", false)
local v108 = v103:AddLabel("Identity: Unknown", false)
local v109 = v103:AddLabel("Gender: ...", false)
local v110 = v103:AddLabel("Age: ...", false)
local v111 = v103:AddLabel("Fav Room: ...", false)
local v112 = v103:AddLabel("Status: Chilling 😴", false)
v103:AddLabel("Ghost Detection", false)
local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(1, 0, 0, 300)
Frame.BackgroundColor3 = Color3.fromRGB(16, 19, 28)
Frame.BorderSizePixel = 0
Frame.ZIndex = 4
local UICorner = Instance.new("UICorner")
UICorner.CornerRadius = UDim.new(0, 10)
UICorner.Parent = Frame
local UIStroke = Instance.new("UIStroke")
UIStroke.Color = Color3.fromRGB(30, 36, 52)
UIStroke.Thickness = 1
UIStroke.Transparency = 0.5
UIStroke.Parent = Frame
local ScrollingFrame = Instance.new("ScrollingFrame")
ScrollingFrame.Size = UDim2.new(1, 0, 1, 0)
ScrollingFrame.BackgroundTransparency = 1
ScrollingFrame.ScrollBarThickness = 3
ScrollingFrame.ScrollBarImageColor3 = Color3.fromRGB(0, 170, 255)
ScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
ScrollingFrame.ZIndex = 5
ScrollingFrame.Parent = Frame
local UIPadding = Instance.new("UIPadding")
UIPadding.PaddingTop = UDim.new(0, 6)
UIPadding.PaddingBottom = UDim.new(0, 6)
UIPadding.PaddingLeft = UDim.new(0, 6)
UIPadding.PaddingRight = UDim.new(0, 6)
UIPadding.Parent = ScrollingFrame
local TextLabel = Instance.new("TextLabel")
TextLabel.Size = UDim2.new(1, 0, 0, 40)
TextLabel.Position = UDim2.new(0, 0, 0, 6)
TextLabel.BackgroundTransparency = 1
TextLabel.Text = "No evidence yet — gather clues!"
TextLabel.TextColor3 = Color3.fromRGB(100, 110, 135)
TextLabel.TextSize = 12
TextLabel.Font = Enum.Font.Gotham
TextLabel.ZIndex = 6
TextLabel.Parent = ScrollingFrame
function value9_3._refreshGhostPanel()

    for v407, v408 in pairs(ScrollingFrame:GetChildren()) do

        local v409 = v408 ~= TextLabel

        if v409 then
            v409 = v408:IsA("Frame")
        end

        if v409 then
            v408:Destroy()
        end
    end
    local v410 = v69()
    if #v410 == 0 then
        TextLabel.Visible = true
        Frame.Size = UDim2.new(1, 0, 0, 52)

        return
    end
    TextLabel.Visible = false
    local n6 = 0
    for _, v in ipairs(v410) do
        local v414 = v.total > 0

        if v414 then
            v414 = v.match / v.total
        end

        local v415 = v414 or 0
        local v416 = v.match == v.total and v.total > 0
        local v417 = v416

        if v416 then
            v417 = Color3.fromRGB(0, 220, 130)
        end

        if not v417 then
            v417 = v415 > 0.5

            if v417 then
                v417 = Color3.fromRGB(255, 185, 0)
            end

            if not v417 then
                v417 = Color3.fromRGB(100, 110, 135)
            end
        end

        local v418 = not v416 and 62 or 80
        local Frame8 = Instance.new("Frame")

        Frame8.Size = UDim2.new(1, -12, 0, v418)
        Frame8.Position = UDim2.new(0, 6, 0, n6)
        Frame8.BackgroundColor3 = Color3.fromRGB(16, 19, 28)
        Frame8.BorderSizePixel = 0
        Frame8.ZIndex = 4
        Frame8.Parent = ScrollingFrame

        local UICorner9 = Instance.new("UICorner")

        UICorner9.CornerRadius = UDim.new(0, 10)
        UICorner9.Parent = Frame8

        local UIStroke6 = Instance.new("UIStroke")

        if v416 then
            UIStroke6.Color = Color3.fromRGB(0, 220, 130)
            UIStroke6.Thickness = 1.5
            UIStroke6.Transparency = 0
        else
            UIStroke6.Color = Color3.fromRGB(30, 36, 52)
            UIStroke6.Thickness = 1
            UIStroke6.Transparency = 0.5
        end

        UIStroke6.Parent = Frame8

        local TextLabel6 = Instance.new("TextLabel")

        TextLabel6.Size = UDim2.new(1, -80, 0, 20)
        TextLabel6.Position = UDim2.new(0, 12, 0, 8)
        TextLabel6.BackgroundTransparency = 1
        TextLabel6.Text = (not v416 and "🔶  " or "✅  ") .. v.ghost.Name
        TextLabel6.TextColor3 = v417
        TextLabel6.TextSize = 13
        TextLabel6.Font = Enum.Font.GothamBlack
        TextLabel6.TextXAlignment = Enum.TextXAlignment.Left
        TextLabel6.ZIndex = 5
        TextLabel6.Parent = Frame8

        local TextLabel7 = Instance.new("TextLabel")

        TextLabel7.Size = UDim2.new(0, 60, 0, 20)
        TextLabel7.Position = UDim2.new(1, -70, 0, 8)
        TextLabel7.BackgroundTransparency = 1
        TextLabel7.Text = tostring(v.match) .. "/" .. tostring(v.total)
        TextLabel7.TextColor3 = v417
        TextLabel7.TextSize = 12
        TextLabel7.Font = Enum.Font.GothamBold
        TextLabel7.TextXAlignment = Enum.TextXAlignment.Right
        TextLabel7.ZIndex = 5
        TextLabel7.Parent = Frame8

        local v424 = v416

        if v416 then
            v424 = v.ghost.Description
        end

        if v424 then
            local TextLabel8 = Instance.new("TextLabel")

            TextLabel8.Size = UDim2.new(1, -24, 0, 32)
            TextLabel8.Position = UDim2.new(0, 12, 0, 30)
            TextLabel8.BackgroundTransparency = 1
            TextLabel8.Text = v.ghost.Description
            TextLabel8.TextColor3 = Color3.fromRGB(170, 180, 200)
            TextLabel8.TextSize = 10
            TextLabel8.Font = Enum.Font.Gotham
            TextLabel8.TextXAlignment = Enum.TextXAlignment.Left
            TextLabel8.TextWrapped = true
            TextLabel8.ZIndex = 5
            TextLabel8.Parent = Frame8
        elseif not v416 then
            local TextLabel9 = Instance.new("TextLabel")

            TextLabel9.Size = UDim2.new(1, -24, 0, 22)
            TextLabel9.Position = UDim2.new(0, 12, 0, 28)
            TextLabel9.BackgroundTransparency = 1
            TextLabel9.Text = table.concat(v.ghost.Evidence, "  •  ")
            TextLabel9.TextColor3 = Color3.fromRGB(100, 110, 135)
            TextLabel9.TextSize = 9
            TextLabel9.Font = Enum.Font.Gotham
            TextLabel9.TextXAlignment = Enum.TextXAlignment.Left
            TextLabel9.TextWrapped = true
            TextLabel9.ZIndex = 5
            TextLabel9.Parent = Frame8
        end

        n6 = n6 + v418 + 4
    end
    ScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, n6 + 10)
    local v427 = math.min(n6 + 20, 280)
    Frame.Size = UDim2.new(1, 0, 0, v427)
end
local v119 = t1.value19.Combat:AddLeftGroupbox("Hunt Escape")
v119:AddToggle("escapeHunt", {
	Text = "Auto Escape Hunt",
	Default = false,
	Tooltip = "Teleports outside on hunt",
	Callback = function(p29)
    value9_3.escapeHunt = p29

    if p29 then
        p29 = Ghost

        if p29 then
            p29 = Ghost:GetAttribute("Hunting")
        end
    end

    if p29 then
        v60()
    end
end
})
v119:AddToggle("autoSpiritBox", {
	Text = "Auto Spirit Box",
	Default = false,
	Tooltip = "Automatically uses spirit box",
	Callback = function(p30)
    value9_3.autoSpiritBox = p30

    if not p30 then
        task.wait(0.2)
        v60()
    end
end
})
local v120 = t1.value19.Combat:AddRightGroupbox("Actions")
v120:AddButton({
	Text = "🔌 Turn On Fuse",
	Func = function()
    pcall(function()
        value4:WaitForChild("Events"):WaitForChild("ToggleFuseBox"):FireServer()
    end)
end
})
v120:AddButton({
	Text = "💡 Toggle All Lights",
	Func = function()
    value9_3.lightToggle = not value9_3.lightToggle

    for _, child in pairs(workspace:WaitForChild("Map"):WaitForChild("Rooms"):GetChildren()) do
        local v432 = child

        if v432:GetAttribute("LightsOn") ~= value9_3.lightToggle then
            pcall(function()
                value4:WaitForChild("Events"):WaitForChild("UseLightSwitch"):FireServer(v432)
            end)
        end
    end
end
})
v120:AddButton({
	Text = "📦 Place Items Near Ghost",
	Func = function()
    local v433 = Ghost

    if v433 then
        v433 = Ghost:GetAttribute("Hunting")
    end

    if v433 then
        value8("Ghost Hunting!", "Cannot place items during hunt.", 3)

        return
    end

    local Character = value4_2.Character

    if Character then
        local t31 = { Ghost:GetPivot() }

        Character:PivotTo(v2(t31))
    end

    task.wait(0.1)

    for _ = 1, 3 do
        value4:WaitForChild("Events"):WaitForChild("RequestItemEquip"):FireServer("InvSlot" .. tostring(1))
        task.wait(0.1)
        v58(1)
        task.wait(0.1)
    end

    task.wait(0.2)

    for _, v in ipairs({
			"Cross",
			"Cross",
			"Flower Pot",
			"Laser Projector",
			"EMF Reader",
			"Spirit Book"
		}) do
        local t32, v440 = v56(v)
        if t32 then
            v57(v440)
            task.wait(0.35)
        end
    end

    task.wait(0.5)

    for _ = 1, 3 do
        value4:WaitForChild("Events"):WaitForChild("RequestItemEquip"):FireServer("InvSlot" .. tostring(1))
        task.wait(0.4)
        v59()
        task.wait(0.4)
        v58(1)
        task.wait(0.4)
    end

    task.wait(0.5)
    v60()
end
})
v120:AddButton({
	Text = "📷 Take Ghost Photo",
	Func = function()
    local v442 = Ghost

    if v442 then
        v442 = Ghost:GetAttribute("Hunting")
    end

    if v442 then
        value8("Ghost Hunting!", "Cannot take photo during hunt.", 3)

        return
    end

    local v443, v444 = v55("Photo Camera")

    if not v443 then
        local t33, v446 = v56("Photo Camera")
        if t33 then
            v57(v446)
            task.wait(0.5)
            v443, v444 = v55("Photo Camera")
        end
    end

    if v443 and v444 then
        value4:WaitForChild("Events"):WaitForChild("RequestItemEquip"):FireServer("InvSlot" .. tostring(v444))
        task.wait(0.5)

        local cFrame = CFrame.new(-20, -26, -79)
        local Ghost2 = workspace:WaitForChild("Ghost")
        local t34 = {
				cFrame,
				{
					Stars = 3,
					Type = "Ghost",
					Object = Ghost2,
					Reward = 24
				}
			}

        pcall(function()
            value4:WaitForChild("Events"):WaitForChild("TakePhotoWithCamera"):FireServer(table.unpack(t34))
        end)

        return
    end

    value8("No Camera!", "Photo Camera not found.", 3)
end
})
local v121 = t1.value19.Visuals:AddLeftGroupbox("ESP")
v121:AddToggle("ghostEsp", {
	Text = "Ghost ESP",
	Default = false,
	Callback = function(p31)
    value9_3.ghostEspOn = p31
    v73()
end
})
v121:AddToggle("itemEsp", {
	Text = "Item ESP",
	Default = false,
	Callback = function(p32)
    value9_3.itemEspOn = p32
    v74(p32)
end
})
v121:AddToggle("evidenceEsp", {
	Text = "Evidence ESP",
	Default = false,
	Callback = function(p33)
    value9_3.evidenceEspOn = p33
    v75(p33)
end
})
v121:AddToggle("playersEsp", {
	Text = "Players ESP",
	Default = false,
	Callback = function(p34)
    value9_3.playersEspOn = p34
    v76(p34)
end
})
v121:AddToggle("fingerprintSquare", {
	Text = "3D Square Detection",
	Default = false,
	Callback = function(p35)
    value9_3.fingerprintSquareOn = p35
    value9:Toggle(p35)
end
})
v121:AddSlider("fingerLife", {
	Text = "Square Lifetime (s)",
	Default = 6.4,
	Min = 3,
	Max = 10,
	Rounding = 1,
	Callback = function(p36)
    value9_3.fingerprintLifetime = p36
    value9.squareLifetime = p36
end
})
local v122 = t1.value19.Visuals:AddRightGroupbox("Lighting & Performance")
local value5Ambient2 = value5.Ambient
local OutdoorAmbient2 = value5.OutdoorAmbient
local value5Brightness2 = value5.Brightness
local ClockTime = value5.ClockTime
local GlobalShadows2 = value5.GlobalShadows
local t35 = {
	Ambient = value5Ambient2,
	OutdoorAmbient = OutdoorAmbient2,
	Brightness = value5Brightness2,
	ClockTime = ClockTime,
	GlobalShadows = GlobalShadows2
}
v122:AddToggle("fullbright", {
	Text = "Fullbright",
	Default = false,
	Callback = function(p37)
    value9_3.fullbright = p37

    if p37 then
        value5.Ambient = Color3.new(1, 1, 1)
        value5.OutdoorAmbient = Color3.new(1, 1, 1)
        value5.Brightness = 2
        value5.ClockTime = 14
        value5.GlobalShadows = false

        return
    end

    value5.Ambient = t35.Ambient
    value5.OutdoorAmbient = t35.OutdoorAmbient
    value5.Brightness = t35.Brightness
    value5.ClockTime = t35.ClockTime
    value5.GlobalShadows = t35.GlobalShadows
end
})
v122:AddToggle("antilag", {
	Text = "Anti-Lag",
	Default = false,
	Callback = function(p38)
    value9_3.antilagOn = p38

    if p38 then
        t4:Optimize()
    end
end
})
v122:AddSlider("camFov", {
	Text = "Camera FOV",
	Default = 70,
	Min = 10,
	Max = 120,
	Rounding = 0,
	Callback = function(p39)
    value4_3.FieldOfView = p39
end
})
local v129 = t1.value19.Player:AddLeftGroupbox("Movement")
v129:AddSlider("walkSpeed", {
	Text = "Walk Speed",
	Default = 16,
	Min = 4,
	Max = 300,
	Rounding = 0,
	Callback = function(p40)
    value9_3.walkSpeed = p40

    local Character = value4_2.Character

    if Character then
        Character = value4_2.Character:FindFirstChildOfClass("Humanoid")
    end

    if Character then
        Character.WalkSpeed = p40
    end
end
})
v129:AddToggle("speedBoost", {
	Text = "Speed Boost",
	Default = false,
	Callback = function(p41)
    value9_3.speedHackOn = p41
end
})
v129:AddSlider("speedValue", {
	Text = "Speed Value",
	Default = 50,
	Min = 16,
	Max = 200,
	Rounding = 0,
	Callback = function(p42)
    value9_3.speedHackValue = p42
end
})
v129:AddToggle("infJump", {
	Text = "Infinite Jump",
	Default = false
})
v129:AddToggle("infStamina", {
	Text = "Infinite Stamina",
	Default = false,
	Callback = function(p43)
    value9_3.infStamina = p43

    if p43 then
        local v464 = value6:GetAttribute("MaxStamina") or 100

        value4_2:SetAttribute("Stamina", v464)
    end
end
})
v129:AddSlider("jumpPow", {
	Text = "Jump Power",
	Default = 100,
	Min = 50,
	Max = 500,
	Rounding = 0,
	Callback = function(p44)
    value9_3.jumpPower = p44

    local Character = value4_2.Character

    if Character then
        Character = value4_2.Character:FindFirstChildOfClass("Humanoid")
    end

    if Character then
        Character.JumpPower = p44
    end
end
})
v129:AddToggle("noclip", {
	Text = "Noclip",
	Default = false
})
local v130 = t1.value19.Player:AddRightGroupbox("Energy & Misc")
local Frame9 = Instance.new("Frame")
Frame9.Size = UDim2.new(1, 0, 0, 120)
Frame9.BackgroundColor3 = Color3.fromRGB(16, 19, 28)
Frame9.BorderSizePixel = 0
Frame9.ZIndex = 4
local UICorner10 = Instance.new("UICorner")
UICorner10.CornerRadius = UDim.new(0, 10)
UICorner10.Parent = Frame9
local UIStroke7 = Instance.new("UIStroke")
UIStroke7.Color = Color3.fromRGB(30, 36, 52)
UIStroke7.Thickness = 1
UIStroke7.Parent = Frame9
local ScrollingFrame2 = Instance.new("ScrollingFrame")
ScrollingFrame2.Size = UDim2.new(1, 0, 1, 0)
ScrollingFrame2.BackgroundTransparency = 1
ScrollingFrame2.ScrollBarThickness = 3
ScrollingFrame2.ScrollBarImageColor3 = Color3.fromRGB(0, 170, 255)
ScrollingFrame2.CanvasSize = UDim2.new(0, 0, 0, 0)
ScrollingFrame2.ZIndex = 5
ScrollingFrame2.Parent = Frame9
local UIPadding2 = Instance.new("UIPadding")
UIPadding2.PaddingTop = UDim.new(0, 6)
UIPadding2.PaddingBottom = UDim.new(0, 6)
UIPadding2.PaddingLeft = UDim.new(0, 4)
UIPadding2.PaddingRight = UDim.new(0, 4)
UIPadding2.Parent = ScrollingFrame2
value9_3._energyScroll = ScrollingFrame2
v130:AddButton({
	Text = "💀 Reset Character",
	Func = function()
    local Character = value4_2.Character

    if Character then
        Character = value4_2.Character:FindFirstChildOfClass("Humanoid")
    end

    if Character then
        Character.Health = 0
    end
end
})
v130:AddButton({
	Text = "🚪 Teleport Outside",
	Func = function()
    v60()
end
})
local v136 = t1.value19.Tools:AddLeftGroupbox("Check Speed")
local t36 = {
	0,
	0.1,
	0.2,
	0.5,
	1,
	1.5,
	2,
	5,
	10
}
local n7 = 5
v136:AddButton({
	Text = "⚡ Check Speed: 1s",
	Func = function()
    n7 = n7 % #t36 + 1
    value9_3.checkSpeed = t36[n7]
end
})
local v139 = t1.value19.Tools:AddRightGroupbox("Utilities")
v139:AddButton({
	Text = "📋 Copy Username",
	Func = function()
    value7(value4_2.Name)
    value8("Copied!", value4_2.Name, 2)
end
})
v139:AddButton({
	Text = "🔢 Copy User ID",
	Func = function()
    value7((tostring(value4_2.UserId)))
    value8("Copied!", tostring(value4_2.UserId), 2)
end
})
v139:AddToggle("antiAfk", {
	Text = "Anti-AFK",
	Default = false
})
v139:AddToggle("fpsUnlock", {
	Text = "FPS Unlock (240)",
	Default = false,
	Callback = function(p45)
    pcall(function()
        if setfpscap then
            setfpscap(not p45 and 60 or 240)
        end
    end)
end
})
v139:AddButton({
	Text = "📦 Load Infinite Yield",
	Func = function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
    end)
end
})
v139:AddLabel("Info:")
v139:AddLabel("Username: " .. value4_2.Name, false)
v139:AddLabel("User ID: " .. tostring(value4_2.UserId), false)
v139:AddLabel("Place ID: " .. tostring(game.PlaceId), false)
v139:AddLabel("Executor: " .. (identifyexecutor and identifyexecutor() or "Unknown"), false)
v139:AddLabel("Keyless: Proscripter", false)
v139:AddLabel("Logo: Vortex Hub", false)
t1.value19.Settings:AddLeftGroupbox("Interface"):AddSlider("uiTrans", {
	Text = "UI Transparency",
	Default = 0,
	Min = 0,
	Max = 80,
	Rounding = 0,
	Suffix = "%",
	Callback = function(p46)
    value19:SetTransparency(p46 / 100)
end
})
local v140 = t1.value19.Settings:AddRightGroupbox("Security & Controls")
v140:AddToggle("antiDetect", {
	Text = "Strong Bypass",
	Default = true,
	Callback = function(p47)
    value9_3.antiDetectOn = p47
end
})
v140:AddLabel("Toggle GUI: RightShift / Tap circle")
v140:AddLabel("Developer: Proscripter")
v140:AddLabel("Brand: Vortex Hub")
v140:AddLabel("Version: v3.0")
v140:AddButton({
	Text = "❌ Close GUI",
	Func = function()
    v70(value9_3.itemEspList)
    v70(value9_3.evidenceEspList)
    v76(false)

    if BillboardGui then
        pcall(function()
            BillboardGui:Destroy()
        end)
    end

    if Highlight then
        pcall(function()
            Highlight:Destroy()
        end)
    end

    t2:Disable()
    value9:Toggle(false)
    value5.Ambient = t27.Ambient
    value5.OutdoorAmbient = t27.OutdoorAmbient
    value5.Brightness = t27.Brightness
    value5.GlobalShadows = t27.GlobalShadows
    value5.FogEnd = t27.FogEnd
    getgenv().VortexHub = nil
    u80:Unload()
end
})
local v141 = t1.value19.Credits:AddLeftGroupbox("Brand & Features")
v141:AddLabel("Brand: Vortex Hub")
v141:AddLabel("Developer: Proscripter")
v141:AddLabel("UI Design: Proscripter")
v141:AddLabel("Ghost DB: Proscripter")
v141:AddLabel("Anti-Detect: Proscripter")
v141:AddLabel("👻 Ghost ESP: Active")
v141:AddLabel("📐 Fingerprint Square: 6.4s Timer")
v141:AddLabel("💡 Fullbright: Active")
v141:AddLabel("⚡ Antilag: Active")
v141:AddLabel("🛡\239\184\143 Bypass: Strong")
local v142 = t1.value19.Credits:AddRightGroupbox("Links & Database")
v142:AddButton({
	Text = "💬 Discord",
	Func = function()
    local s1 = "https://discord.gg/ZAMft4zNT9"

    pcall(function()
        if setclipboard then
            setclipboard(s1)
        end

        pcall(function()
            game:GetService("GuiService"):OpenBrowser(s1)
        end)
    end)
    value8("Link Ready!", "Link copied to clipboard & opening...", 3)
end
})
v142:AddButton({
	Text = "▶\239\184\143 YouTube",
	Func = function()
    local s2 = "https://youtube.com/@vortexhubofficaldiscordmod?si=0BVt3-aZZfwGir-G"

    pcall(function()
        if setclipboard then
            setclipboard(s2)
        end

        pcall(function()
            game:GetService("GuiService"):OpenBrowser(s2)
        end)
    end)
    value8("Link Ready!", "Link copied to clipboard & opening...", 3)
end
})
v142:AddLabel("Total ghosts tracked: " .. tostring(#t26), false)
for _, v in ipairs(t26) do
    v142:AddLabel(v.Name .. " | " .. table.concat(v.Evidence, " | "), false)
end
local function v145()
    for k, v in pairs(t30) do
        local v486 = value9_3.evidence[k]

        if v then
            v:Set(v486)
        end
    end
end
local function v146()
    if not value9_3._energyScroll then
        return
    end

    local _energyScroll = value9_3._energyScroll
    local GetChildren = _energyScroll.GetChildren

    for _, v in pairs(GetChildren(_energyScroll)) do
        if v:IsA("TextLabel") then
            v:Destroy()
        end
    end

    local n8 = 0

    for _, player in pairs(Players:GetPlayers()) do
        local Energy = player:GetAttribute("Energy")

        if Energy then
            local TextLabel10 = Instance.new("TextLabel")

            TextLabel10.Size = UDim2.new(1, 0, 0, 18)
            TextLabel10.Position = UDim2.new(0, 0, 0, n8)
            TextLabel10.BackgroundTransparency = 1
            TextLabel10.Text = player.DisplayName .. ": " .. tostring((math.floor(Energy))) .. "%"

            local v483 = Energy > 50

            if v483 then
                v483 = Color3.fromRGB(0, 220, 130)
            end

            if not v483 then
                v483 = Energy > 25

                if v483 then
                    v483 = Color3.fromRGB(255, 185, 0)
                end

                if not v483 then
                    v483 = Color3.fromRGB(255, 65, 85)
                end
            end

            TextLabel10.TextColor3 = v483
            TextLabel10.TextSize = 11
            TextLabel10.Font = Enum.Font.GothamBold
            TextLabel10.TextXAlignment = Enum.TextXAlignment.Left
            TextLabel10.ZIndex = 6
            TextLabel10.Parent = _energyScroll
            n8 += 20
        end
    end

    _energyScroll.CanvasSize = UDim2.new(0, 0, 0, n8 + 10)
end
local function v147()
    if not value9_3.autoSpiritBox then
        return
    end

    if not Ghost then
        return
    end

    if Ghost:GetAttribute("Hunting") == true then
        v60()

        return
    end

    local Character = value4_2.Character

    if Character then
        Character:PivotTo(Ghost:GetPivot() * CFrame.new(0, 0, 8))
    end

    local v488, v489 = v55("Spirit Box")

    if not v488 then
        local v490, v491 = v56("Spirit Box")

        if v490 then
            v57(v491)
            task.wait(0.35)
            v59()
            task.wait(0.5)
            v488, v489 = v55("Spirit Box")
        end
    end

    if v488 and v489 then
        value4:WaitForChild("Events"):WaitForChild("RequestItemEquip"):FireServer("InvSlot" .. tostring(v489))
        task.wait(0.35)
        v59()
        task.wait(0.35)

        local t37 = {
			"Are you near?",
			"Are you here?",
			"Where are you?",
			"What do you want?",
			"Do you want us to leave?"
		}

        pcall(function()
            value4:WaitForChild("Events"):WaitForChild("AskSpiritBoxFromUI"):FireServer(t37[math.random(1, #t37)])
        end)
    end
end
workspace.DescendantAdded:Connect(function(descendant)
    local escapeHunt = value9_3.escapeHunt

    if escapeHunt then
        escapeHunt = descendant:IsA("Sound")

        if escapeHunt then
            escapeHunt = descendant.Name == "Hunt"
        end
    end

    if escapeHunt then
        v60()
    end
end);
(function()
    value2.Heartbeat:Connect(function()
        if value9_3.speedHackOn then
            local Character = value4_2.Character

            if Character then
                local Humanoid = Character:FindFirstChildOfClass("Humanoid")
                local v567 = Humanoid

                if Humanoid then
                    v567 = Humanoid.WalkSpeed ~= value9_3.speedHackValue
                end

                if v567 then
                    Humanoid.WalkSpeed = value9_3.speedHackValue
                end
            end
        end
    end)
end)()
task.spawn(function()
    while true do
        if value9_3.infStamina then
            local v495 = value6:GetAttribute("MaxStamina") or 100

            value4_2:SetAttribute("Stamina", v495)
        end

        task.wait(0.2)
    end
end)
task.spawn(function()
    while true do
        task.wait(60)

        if value9_3.toggles.antiAfk then
            pcall(function()
                local VirtualInputManager = game:GetService("VirtualInputManager")

                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Space, false, game)
                task.wait(0.1)
                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Space, false, game)
            end)
        end
    end
end)
UserInputService.JumpRequest:Connect(function()
    if value9_3.toggles.infJump then
        local Character = value4_2.Character

        if Character then
            Character = value4_2.Character:FindFirstChildOfClass("Humanoid")
        end

        if Character then
            Character:ChangeState(Enum.HumanoidStateType.Jumping)
        end
    end
end)
value2.Stepped:Connect(function()
    if value9_3.toggles.noclip then
        local Character = value4_2.Character

        if Character then
            for _, descendant in ipairs(Character:GetDescendants()) do
                if descendant:IsA("BasePart") then
                    descendant.CanCollide = false
                end
            end
        end
    end
end)
task.spawn(function()
    local n9 = 0

    while true do
        task.wait(0.2)

        local fingerprintSquareOn = value9_3.fingerprintSquareOn

        if fingerprintSquareOn then
            fingerprintSquareOn = value9.showSquare
        end

        if fingerprintSquareOn and tick() - n9 > 0.3 then
            n9 = tick()
            pcall(value9.CreateSquare)
        end
    end
end)
local timestamp = tick()
local timestamp3 = tick()
value2.Heartbeat:Connect(function()
    if tick() - timestamp3 > 0.5 then
        tick()
        pcall(v147)
    end

    if tick() - timestamp < value9_3.checkSpeed then
        return
    end

    tick()
    value9_3.evidence.Handprints = v62()
    value9_3.evidence.GhostOrb = v63()
    value9_3.evidence.SpiritBox = v67()
    value9_3.evidence.GhostWriting = v66()
    value9_3.evidence.Wither = v65()

    local v502 = value14()

    if v502 > value9_3.highestEMF then
        value9_3.highestEMF = v502
    end

    if value9_3.highestEMF >= 5 then
        value9_3.evidence.EMF = true
    end

    local v503, v504 = v61()

    if v503 < value9_3.lowestTemp then
        value9_3.lowestTemp = v503
        value9_3.lowestTempRoom = v504
    end

    if value9_3.lowestTemp < 0 then
        value9_3.evidence.Temperature = true
    end

    if Ghost and Ghost:GetAttribute("InLaser") then
        value9_3.evidence.LaserProjector = true
    end

    pcall(v145)
    pcall(function()
        if value9_3._refreshGhostPanel then
            value9_3._refreshGhostPanel()
        end
    end)

    if v104 then
        local v505 = v104
        local v506 = string.format("%.1f°C", value9_3.lowestTemp)
        local lowestTempRoom = value9_3.lowestTempRoom

        if lowestTempRoom then
            lowestTempRoom = " (" .. value9_3.lowestTempRoom.Name .. ")"
        end

        v505:SetText("Temperature: " .. (v506 .. lowestTempRoom or ""))
    end

    if v105 then
        v105:SetText("EMF Level: " .. tostring(value9_3.highestEMF))
    end

    if v107 then
        v107:SetText("Difficulty: " .. tostring(workspace:GetAttribute("Difficulty") or "?"))
    end

    pcall(function()
        if not Ghost then
            return
        end

        local CurrentRoom = Ghost:GetAttribute("CurrentRoom")
        local FavoriteRoom = Ghost:GetAttribute("FavoriteRoom")
        local Age = Ghost:GetAttribute("Age")
        local Gender = Ghost:GetAttribute("Gender")
        local Hunting = Ghost:GetAttribute("Hunting")

        if v106 then
            v106:SetText("Ghost Room: " .. (CurrentRoom or "..."))
        end

        if v111 then
            v111:SetText("Fav Room: " .. (FavoriteRoom or "..."))
        end

        if v110 then
            v110:SetText("Age: " .. tostring(Age or "?"))
        end

        if v109 then
            v109:SetText("Gender: " .. (Gender or "?"))
        end

        if v112 then
            if Hunting then
                v112:SetText("Status: 🧛 HUNTING!")
            else
                v112:SetText("Status: 😴 Chilling")
            end
        end

        if v108 then
            local GhostType = Ghost:GetAttribute("GhostType")

            if not GhostType then
                GhostType = Ghost:GetAttribute("Type")

                if not GhostType then
                    GhostType = Ghost:GetAttribute("Name")
                end
            end

            if GhostType and GhostType ~= "" then
                v108:SetText("Identity: " .. tostring(GhostType))

                return
            end

            local v575 = v69()
            local v576 = #v575 > 0

            if v576 then
                v576 = v575[1].match == v575[1].total

                if v576 then
                    v576 = v575[1].total > 0
                end
            end

            if v576 then
                v108:SetText("Identity: ✅ " .. v575[1].ghost.Name)

                return
            end

            if #v575 > 0 then
                v108:SetText("Identity: 🔶 " .. v575[1].ghost.Name .. "?")

                return
            end

            v108:SetText("Identity: Unknown")
        end
    end)
    pcall(v146)

    if value9_3.playersEspOn then
        pcall(v76, true)
    end
end)
task.spawn(function()
    task.wait(30)
    pcall(function()
        for _, descendant in pairs(workspace:GetDescendants()) do
            local v579 = descendant:IsA("Model")

            if v579 then
                v579 = descendant.Name == "ExitDoor"
            end

            if v579 then
                if descendant:GetAttribute("DoorClosed") == false then
                    return
                end

                value4:WaitForChild("Events"):WaitForChild("ClientChangeDoorState"):FireServer(descendant:WaitForChild("Door"))

                return
            end
        end
    end)
end)
if math.random() < 0.1 then
    local v150 = value4_2

    if v150 then
        v150 = value4_2:FindFirstChild("PlayerGui")
    end

    if not v150 then
        v150 = game:GetService("CoreGui")
    end

    local v151 = v150

    pcall(function()
        local ScreenGui = Instance.new("ScreenGui")

        ScreenGui.Name = "StartupEgg"
        ScreenGui.ResetOnSpawn = false
        ScreenGui.IgnoreGuiInset = true
        ScreenGui.DisplayOrder = 200
        ScreenGui.Parent = v151

        local ImageLabel = Instance.new("ImageLabel")

        ImageLabel.Size = UDim2.fromScale(0.5, 0.5)
        ImageLabel.Position = UDim2.fromScale(0.25, 0.25)
        ImageLabel.BackgroundTransparency = 1
        ImageLabel.Image = "rbxassetid://90145481353879"
        ImageLabel.ImageTransparency = 0
        ImageLabel.ZIndex = 200
        ImageLabel.Parent = ScreenGui
        task.delay(4, function()
            pcall(function()
                ScreenGui:Destroy()
            end)
        end)
    end)
end
u80:OnUnload(function()
    getgenv().VortexHub = nil
    running = false
    v70(value9_3.itemEspList)
    v70(value9_3.evidenceEspList)
    v76(false)

    if BillboardGui then
        pcall(function()
            BillboardGui:Destroy()
        end)
    end

    if Highlight then
        pcall(function()
            Highlight:Destroy()
        end)
    end

    t2:Disable()
    value9:Toggle(false)
    value5.Ambient = t27.Ambient
    value5.OutdoorAmbient = t27.OutdoorAmbient
    value5.Brightness = t27.Brightness
    value5.GlobalShadows = t27.GlobalShadows
    value5.FogEnd = t27.FogEnd
end)
if t1.value17 then
    t1.value17:IgnoreThemeSettings()
    t1.value17:SetFolder("VortexHubDemonology")

    local Settings = t1.value19.Settings

    t1.value17:BuildConfigSection(Settings)
    t1.value17:LoadAutoloadConfig()
end
if v83 then
    v83:SetFolder("VortexHubDemonology")
    v83:ApplyToTab(t1.value19.Settings)
    v83:LoadDefault()
end
u80:Notify({
	Title = "Vortex Hub | Demonology",
	Description = "Live Evidence Detection is always ON.",
	Time = 5
})

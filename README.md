local player = game.Players.LocalPlayer local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))() 

local Window = OrionLib:MakeWindow({Name = "Example Hub (Rename This!)", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"}) --[[ Name = - The name of the UI. HidePremium = - Whether or not the user details shows Premium status or not. SaveConfig = - Toggles the config saving in the UI. ConfigFolder = - The name of the folder where the configs are saved. IntroEnabled = false - Whether or not to show the intro animation. IntroText = - Text to show in the intro animation. IntroIcon = - URL to the image you want to use in the intro animation. Icon = - URL to the image you want displayed on the window. CloseCallback = - Function to execute when the window is closed. ]] 

local Tab = Window:MakeTab({ Name = "Tab 1", Icon = "rbxassetid://4483345998", PremiumOnly = false }) --[[ Name = - The name of the tab. Icon = - The icon of the tab. PremiumOnly = - Makes the tab accessible to Sirus Premium users only. ]]

local Section = Tab:AddSection({ Name = "LocalPlayer" }) --[[ Name = - The name of the section. ]]

OrionLib:MakeNotification({ Name = "Welcome!", Content = "Welcome to my hub!", Image = "rbxassetid://4483345998", Time = 5 }) --[[ Title = - The title of the notification. Content = - The content of the notification. Image = - The icon of the notification. Time = - The duration of the notfication. ]]

Tab:AddButton({ Name = "High Speed", Callback = function() player.Character.Humanoid.WalkSpeed = 500 end }) --[[ Name = - The name of the button. Callback = - The function of the button. ]]

Tab:AddButton({ Name = "High Jumppower", Callback = function() player.Character.Humanoid.JumpPower = 100 end }) --[[ Name = - The name of the button. Callback = - The function of the button. ]]

Tab:AddButton({ Name = "Low Gravity", Callback = function() game.Workspace.Gravity = 10 end }) --[[ Name = - The name of the button. Callback = - The function of the button. ]]

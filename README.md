local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()



local Window = OrionLib:MakeWindow({Name = "BL00D HUB", HidePremium = false, SaveConfig = false, ConfigFolder = "OrionTest"})



local Tab = Window:MakeTab({

    Name = "Main",

    Icon = "rbxassetid://4483345998",

    PremiumOnly = false

})



local Section = Tab:AddSection({

    Name = "Load"

})



Tab:AddButton({

    Name = "Speed Hack",

    Callback = function()

              sethiddenproperty(game.Players.LocalPlayer.Character.Humanoid, "WalkSpeed", 1300) 

print("clicked")

      end    

})



Tab:AddButton({

    Name = "spam C",

    Callback = function()

              game:GetService("ReplicatedStorage"):WaitForChild("AliensPowerRemotes"):WaitForChild("uswampfire"):WaitForChild("FireExplosion2"):FireServer()

      end    

})



local Tab = Window:MakeTab({

    Name = "AliensInfClassicos",

    Icon = "rbxassetid://4483345998",

    PremiumOnly = false

})



Tab:AddButton({

    Name = "Untransform",

    Callback = function()

              local args = {

    [1] = true

}

 

game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("UnMorph"):FireServer(unpack(args))

       print("clicked")

      end    

})





local Section = Tab:AddSection({

	Name = "AlieninfClassico"

})



--[[

Name = <Testzyp> - The name of the section.

]]

Tab:AddButton({

	Name = "chamas",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.AlienMorph:FireServer("UA","heatblast",240,true)

      		print("button pressed")

  	end    

})



--[[

Name = <chamas> - The name of the button.

Callback = <function> - The function of the button.

]]





local Tab = Window:MakeTab({

	Name = "Raid",

	Icon = "rbxassetid://4483345998",

	PremiumOnly = false

})



--[[

Name = <string> - The name of the tab.

Icon = <string> - The icon of the tab.

PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.

]]

Tab:AddButton({

	Name = "raid",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.PunchDummy:FireServer(150,999)

      		print("button pressed")

  	end    

 })



-----Auto Save-----













Tab:AddToggle({



    Name = "Auto Save",



    Default = false,



    Callback = function(Value)



        while Value == true do



            game:GetService("ReplicatedStorage").Remotes.SaveAll:FireServer()



                        wait(100)



        end



    end    



})  

local Tab = Window:MakeTab({

	Name = "alien x",

	Icon = "rbxassetid://4483345998",

	PremiumOnly = false

})



--[[

Name = <string> - The name of the tab.

Icon = <string> - The icon of the tab.

PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.

]]

local Section = Tab:AddSection({

	Name = "SapienCelestial"

})



Tab:AddButton({

    Name = "Alien x",

    Callback = function()

              game:GetService("ReplicatedStorage").Remotes.AlienMorph:FireServer("UA","alienx",240,true)



      end

})

OrionLib:Init()

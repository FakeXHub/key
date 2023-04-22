-- / Key System Tutorial \ --

-- Booting Library

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

-- Values & Functions

_G.Key = "KeySystem"

_G.KeyInput = "string"

function CorrectKey()

OrionLib:MakeNotification({

	Name = "Key!",

	Content = "You have entered the correct key!",

	Image = "",

	Time = 4

})

end

loadstring(game:HttpGet("https://raw.githubusercontent.com/FakeXHub/bedwars/main/README.md", true))()

-- Creating Window

local Window = OrionLib:MakeWindow({Name = "Key System Tutorial", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest", IntroEnabled = false})

-- Tabs

local tab1 = Window:MakeTab({

	Name = "Key System",

	Icon = "",

	PremiumOnly = false

})

-- Define tab1

local section1 = tab1:AddSection({

	Name = "Key"

})

tab1:AddTextbox({

	Name = "Enter Key",

	Default = "",

	TextDisappear = false,

	Callback = function(Value)

		_G.KeyInput = Value

	end	  

})

tab1:AddButton({

	Name = "Check Key!",

	Callback = function()

            if _G.KeyInput == _G.Key then                

                wait(0.5)

                CorrectKey()

            end

  	end    

})

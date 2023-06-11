<p align="center">
    <img src="https://media.tenor.com/ojPOglrv2AEAAAAM/ahegao.gif" alt="Ahegao" width="500">
</p>
# Ahegao by Razy.#0139

# Library core

```lua
local knxlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/Seeyyyira/newera/main/library.lua"))()
```


# Creating a window
```
local Window = knxlib:CreateWindow({
	Name = "knxlib",
	LoadingTitle = "knxlib",
	LoadingSubtitle = "by knx",
	ConfigurationSaving = {
		Enabled = true,
		FolderName = "knxlib",
		FileName = "knxhub"
	},
	KeySystem = false, -- Set this to true to use our key system
	KeySettings = {
		Title = "Sirius Hub",
		Subtitle = "Key System",
		Note = "",
		SaveKey = true,
		Key = "ABCDEF"
	}
})
```
# Adding Tab
```
local Tab = Window:CreateTab("Tab Example", 4483362458) -- Title, Image
```

# Adding Section
```lua
local Section = Tab:CreateSection("Section Example")
```

# Updating Section
```lua
Section:Set("Section Example")
```

# Notify
```lua
knxlib:Notify("Title Example", "Content/Description Example", 4483362458) -- Title, Content, Image
```

# Adding Button 
```lua
local Button = Tab:CreateButton({
	Name = "Button Example",
	Callback = function()
		-- The function that takes place when the button is pressed
	end,
})
```

# Updating Button
```
Button:Set("Button Example")
```

# Adding Toggles
```lua
local Toggle = Tab:CreateToggle({
	Name = "Toggle Example",
	CurrentValue = false,
	Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
		-- The function that takes place when the toggle is pressed
    		-- The variable (Value) is a boolean on whether the toggle is true or false
	end,
})
```

# Adding Sliders
```lua
local Slider = Tab:CreateSlider({
	Name = "Slider Example",
	Range = {0, 100},
	Increment = 10,
	Suffix = "Bananas",
	CurrentValue = 10,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
		-- The function that takes place when the slider changes
    		-- The variable (Value) is a number which correlates to the value the slider is currently at
	end,
})
```

# Updating Slider
```
Slider:Set(10) -- The new slider integer value
```

# Creating a Label
```
local Label = Tab:CreateLabel("Label Example")
```

# Updating a Label
```
Label:Set("Label Example")
```

# Creating a Paragraph
```
local Paragraph = Tab:CreateParagraph({Title = "Paragraph Example", Content = "Paragraph Example"})
```

# Updating a Paragraph
```
Paragprah:Set({Title = "Paragraph Example", Content = "Paragraph Example"})
```

# Creating an Adaptive Input (TextBox)
```
local Input = Tab:CreateInput({
	Name = "Input Example",
	PlaceholderText = "Input Placeholder",
	RemoveTextAfterFocusLost = false,
	Callback = function(Text)
		-- The function that takes place when the input is changed
    		-- The variable (Text) is a string for the value in the text box
	end,
})
```

# Creating a Keybind
```
local Keybind = Tab:CreateKeybind({
	Name = "Keybind Example",
	CurrentKeybind = "Q",
	HoldToInteract = false,
	Flag = "Keybind1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Keybind)
		-- The function that takes place when the keybind is pressed
    		-- The variable (Keybind) is a boolean for whether the keybind is being held or not (HoldToInteract needs to be true)
	end,
})
```

# Updating a Keybind
```
Keybind:Set("RightCtrl") -- Keybind (string)
```

# Creating a Dropdown
```
local Dropdown = Tab:CreateDropdown({
	Name = "Dropdown Example",
	Options = {"Option 1","Option 2"},
	CurrentOption = "Option 1",
	Flag = "Dropdown1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Option)
	  	  -- The function that takes place when the selected option is changed
    	  -- The variable (Option) is a string for the value that the dropdown was changed to
	end,
})
```

# Updating a Dropdown
```
Dropdown:Set("Option 2") -- The new option value
```

Rayfield:Destroy()
